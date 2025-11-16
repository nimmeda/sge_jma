# Pasos:
## Paso 1:
Vamos a definir cuatro servicios: postgres_dev, odoo_dev, postgres_prod, y odoo_prod.

Para ello, primero crearemos la siguiente estructura de carpetas para el desarollo:

OdooDev  
-- dataPG_devv  
-- odoo_dev  
---- addons  
---- filestore  
---- sessions  
---- config 
## Paso 2:
Vamos ahora a crear la estructura de carpetas para la produccion:

OdooProd  
-- dataPG_prod  
-- addons
## Paso 3:
Abriremos ahora Docker desktop y en una terminal dentro de la carpeta de lainstalación ejecutaremos el siguiente comando: `docker network createshared_network`
## Paso 4:
Ejecutaremos el comando: `docker compose up -d` y esperaremos a que termine de ejecutarse e instalarse

## Compose.yml final:
```yml
services:
  postgres_dev:
    image: postgres:14
    container_name: postgres_dev
    environment:
      - POSTGRES_DB=postgres
      - POSTGRES_USER=odoo
      - POSTGRES_PASSWORD=paso
    volumes:
      - ~/OdooDev/dataPG:/var/lib/postgresql/data
    networks:
      - shared_network

  odoo_dev:
    image: odoo:16
    container_name: odoo_dev
    environment:
      - HOST=postgres_dev
      - USER=odoo
      - PASSWORD=paso
    ports:
      - '8069:8069'
    volumes:
      - ~/OdooDev/volumesOdoo/addons:/mnt/extra-addons
      - ~/OdooDev/volumesOdoo/filestore:/var/lib/odoo/filestore
    depends_on:
      - postgres_dev
    command: --dev=all
    networks:
      - shared_network

  postgres_prod:
      image: postgres:14
      container_name: postgres_prod
      environment:
        - POSTGRES_DB=postgres
        - POSTGRES_USER=odoo
        - POSTGRES_PASSWORD=paso
      volumes:
        - ~/OdooProd/dataPG_prod:/var/lib/postgresql/data
      networks:
        - shared_network

  odoo_prod:
      image: odoo:16
      container_name: odoo_prod
      environment:
        - HOST=postgres_prod
        - USER=odoo
        - PASSWORD=paso
      ports:
        - "8070:8069"
      volumes:
        - ~/OdooProd/addons:/mnt/extra-addons
      depends_on:
        - postgres_prod
      networks:
        - shared_network

networks:
  shared_network:
    external: true
```
