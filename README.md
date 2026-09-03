# Sonrisa Pep — landing page

Página de una sola pantalla para agendar horas dentales. HTML, CSS y JavaScript planos:
sin framework, sin build, sin dependencias que instalar.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | El sitio. Es lo único que Vercel necesita servir. |
| `clinica.jpg` | La foto de la sección superior. Para cambiarla, reemplaza este archivo por otro con el mismo nombre. |
| `sonrisa-pep.html` | La misma página con la foto incrustada, usada para la vista previa en Claude. No hace falta para el despliegue. |

## Publicar en Vercel

1. Crea un repositorio en GitHub y sube esta carpeta:

   ```
   git remote add origin https://github.com/USUARIO/sonrisa-pep.git
   git push -u origin main
   ```

2. Entra a [vercel.com/new](https://vercel.com/new), elige **Import Git Repository** y selecciona el repo.
3. Vercel detecta que es un sitio estático. Deja *Framework Preset* en **Other** y no toques
   los comandos de build: no hay build.
4. **Deploy**. En menos de un minuto queda online con HTTPS.

Cada `git push` a `main` vuelve a desplegar automáticamente.

## Dónde tocar cada dato

| Dato | Dónde |
|---|---|
| Teléfono y WhatsApp | busca `56982998674` (aparece en los enlaces y en la variable `WHATSAPP` del script del final) |
| Correo | busca `mscabrer@gmail.com` |
| Dirección | busca `Luis Pasteur 2450` |
| Precios | busca `class="price"` |
| Horarios | busca `class="hours"` |
| Datos para Google | bloque `application/ld+json` al final del archivo |

El formulario no envía nada a un servidor: arma el mensaje y abre WhatsApp con los datos del
paciente ya escritos. Para recibir las solicitudes por correo o guardarlas en una base de datos
hay que conectar un backend.

## Créditos

Foto de portada: Benyamin Bohlouli vía [Unsplash](https://unsplash.com/photos/e7MJLM5VGjY),
Unsplash License (uso comercial libre, sin atribución obligatoria).
