# Conexión con el ecosistema de producción

`enviar.html` ya crea pedidos en el backend central de Método NERI y redirige al espacio privado devuelto por la API.

Antes de publicar confirma que `PRODUCCION_API` apunte al despliegue correcto:

```js
var PRODUCCION_API = 'https://intranetmetodonerirealtor.vercel.app/api/produccion';
```

En Vercel, `PRODUCCION_ALLOWED_ORIGINS` debe incluir el dominio donde se publique este repositorio. La descarga final nunca debe volver a ponerse dentro del objeto JavaScript de `entrega.html`; la nueva API la firma únicamente después de validar el estado de pago.
