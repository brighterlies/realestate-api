# GRUPO 9 Ejercicio Guiado: Automatización de Pruebas en una API de Inmobiliaria

## ¿Qué importancia tiene probar en múltiples entornos de Node.js?

Probar en distintas versiones de `Node.js` ayuda a detectar incompatibilidades y asegurar que la aplicación funcione correctamente, permitiendo corregir errores antes del despliegue a producción.

##  ¿Por qué es importante validar la salida de una API desde un workflow?

Las pruebas automatizadas garantizan que la API funcione según lo esperado, detectan errores antes del despliegue y mejoran la confiabilidad del sistema.

## ¿Qué pasos podrías agregar si fueras a hacer despliegue a producción?

Agregaría pasos de construcción y empaquetado para generar artefactos listos para producción, pruebas adicionales de integración y seguridad, despliegue automático mediante `GitHub Actions`, y monitoreo con herramientas de logs y métricas para detectar errores en producción.

## ¿Qué limitaciones tiene GitHub Actions y cómo las enfrentarías?

- `GitHub Actions` tiene limitaciones como el tiempo de ejecución, restricciones en secretos, costos en proyectos grandes y poca paralelización en planes gratuitos. 
- Para enfrentarlas, se pueden usar runners auto-hospedados, optimizar con `caching`, gestionar secretos con control de acceso y aplicar matrices para ejecutar tareas en paralelo.

----------------

## Demo
- En la carpeta `img_workflow` se muestra ambos caso, tanto `sucess` y `failure`. 
- Para provocar el fallo, primero se modifica la ruta en `app.js` cambiando `/api/inmuebles` a `/api/propiedades`. Luego, se suben los cambios al repositorio y se verifica que los tests fallan en `GitHub Actions`. Finalmente, se restaura la configuración original para corregir el error.