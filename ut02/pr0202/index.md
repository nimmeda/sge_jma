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

## YML final:
```yml

```
