# Cuaderno de Facu

App de una sola página (sin backend) para trackear materias, notas, parciales/entregas, asistencia y materiales de estudio, organizada por año.

Todo se guarda en el navegador (`localStorage`), en el dispositivo donde lo abras. No hay servidor ni base de datos: si lo abrís desde el celular y desde la notebook, son dos "cuadernos" separados (para eso está el botón **Exportar copia / Importar copia** de arriba, para pasar los datos de un lado a otro).

## Deployarlo en Vercel

Necesitás tener Node.js instalado en tu compu. No hace falta ningún build: es un solo archivo HTML.

### Opción A — con la CLI de Vercel (la más directa)

1. Abrí una terminal en esta carpeta (`cuaderno-de-facu`).
2. Instalá la CLI si no la tenés: `npm install -g vercel`
3. Corré: `vercel`
   - La primera vez te va a pedir loguearte (abre el navegador) y hacerte un par de preguntas — podés aceptar todos los valores por defecto ("Other" como framework, sin build command).
4. Cuando termine te da una URL de prueba. Para dejarla como definitiva: `vercel --prod`

Cada vez que quieras subir un cambio (por ejemplo si le pido que le agregue algo nuevo), volvés a correr `vercel --prod` desde esta carpeta con el `index.html` actualizado.

### Opción B — con GitHub + el dashboard de Vercel

1. Creá un repo nuevo en GitHub y subí esta carpeta (`git init`, `git add .`, `git commit -m "cuaderno de facu"`, `git push`).
2. Entrá a [vercel.com/new](https://vercel.com/new) y elegí "Import Git Repository".
3. Seleccioná el repo. En "Framework Preset" dejá **Other** (no hace falta build command ni output directory).
4. Deploy. A partir de ahí, cada `git push` a la rama principal actualiza el sitio solo.

## Sobre el año que viene

Arriba de las pestañas hay un selector de **Año**. Cuando arranques el próximo cuatrimestre o año, tocá **+ Nuevo año**: te arma un año nuevo vacío para cargar materias, sin borrar nada de años anteriores — podés volver a mirarlos cuando quieras desde el mismo selector.

## Ideas para más adelante

- Horario semanal de cursada.
- Lista de pendientes generales (no atados a una fecha de parcial).
- Gráfico de evolución de notas a lo largo del año.
- Modo oscuro.
- Sincronización real entre dispositivos (requeriría agregar un backend/base de datos, hoy todo vive en el navegador).
