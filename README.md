# Control Horario

Web app para llevar el control horario laboral (molinete de acceso) desde el celular.
Calcula la presencia real (egreso − ingreso − ausencias por gym), el saldo mensual contra 8 h diarias,
el promedio necesario para cerrar el mes en cero, las ausencias por tipo y los cupos de VAC / 14F.

## Publicar en GitHub Pages

1. Subí al repositorio el contenido de esta carpeta: `index.html`, `manifest.webmanifest`, `sw.js` y la carpeta `icons/`.
2. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)` → **Save**.
3. En uno o dos minutos la app queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Instalar en el celular (con el ícono HL)

- **iPhone (Safari):** abrí el link → botón Compartir → **Agregar a inicio**.
- **Android (Chrome):** abrí el link → menú ⋮ → **Instalar app** o **Agregar a pantalla principal**.

## Dónde se guardan los datos

Los datos se guardan **en el navegador de cada dispositivo** (localStorage), no en GitHub.
El celular y la PC no se sincronizan solos: para pasar los datos de uno a otro, descargá un respaldo en uno
(pestaña **Año → Descargar respaldo**) e importalo en el otro (**Importar**).

Importar acepta:
- un respaldo `.json` de esta app, o
- la planilla Excel original `Control Horario - FINAL.xlsx`.

Al importar podés **Combinar** (suma los días; si coinciden, gana el importado) o **Reemplazar** (deja solo lo importado).

> Recomendación: descargá un respaldo cada tanto (la app te avisa si pasaron más de 14 días).

## Privacidad

No subas tus respaldos (`respaldo-*.json`) ni la planilla al repositorio: si el repo es público, cualquiera
podría verlos. El archivo `.gitignore` ya los excluye.

## Actualizar la app

Después de cambiar `index.html`, subí el número de versión en `sw.js` (`control-horario-v1` → `v2`)
para que los celulares descarguen la versión nueva.
