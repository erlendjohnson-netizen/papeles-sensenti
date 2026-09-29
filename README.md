# Papeles de Sensentí

Edición y transcripción paleográfica de 348 láminas del **Archivo Municipal de Sensentí**
(Ocotepeque, Honduras), 1787–1857. Treinta y un expedientes: causas criminales, pleitos de
tierras y de ganado, mortuales, cuentas municipales y peticiones.

Proyecto Arqueológico Río Cucuyagua y Sensentí (PARCS) — Erlend M. Johnson.

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub, por ejemplo `papeles-sensenti`.
2. Subir el contenido de esta carpeta a la raíz del repositorio.
3. En **Settings → Pages**, elegir *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
4. El sitio queda en `https://<usuario>.github.io/papeles-sensenti/` al cabo de un minuto.

Desde la línea de órdenes:

```
git init
git add .
git commit -m "Papeles de Sensentí"
git branch -M main
git remote add origin https://github.com/<usuario>/papeles-sensenti.git
git push -u origin main
```

## Estructura

```
index.html        portada: el archivo (introducción) y la lista de los 31 expedientes
metodo.html       convenciones de transcripción y correcciones al catálogo
doc/*.html        una página por expediente (estudio + relevancia y contexto)
img/<doc>/*.jpg   las láminas
.nojekyll         evita que GitHub procese el sitio con Jekyll
```

Las páginas son HTML estático, sin dependencias ni build. Se pueden abrir localmente
haciendo doble clic en `index.html`.

## Añadir un expediente

Cada página de `doc/` es autónoma: lleva su propio CSS dentro. Para añadir una,
basta copiarla en `doc/`, poner sus láminas en `img/<nombre>/` y añadir una tarjeta
en la rejilla de `index.html`.

## Secciones de cada página de documento

Las tres primeras son pestañas; las dos últimas van debajo, siempre visibles.

1. **El caso** (pestaña) — qué dice el papel, unidad por unidad.
2. **Relevancia** (pestaña) — qué institución o práctica deja ver el expediente, y qué
   puede sacar de él quien no estudie este valle. Es interpretación, y va marcada como tal.
3. **Las láminas** (pestaña) — fotografía, transcripción paleográfica y lectura en
   español de hoy, con el selector de versión y el índice de planas.
4. **Quién es quién** — las personas del expediente.
5. **Nota final** — lo que no se lee, y las correcciones al catálogo.

Las pestañas funcionan con JavaScript sencillo y teclado (flechas izquierda y derecha).
Un enlace del tipo `doc/x.html#fIMG_1648` abre directamente la pestaña de láminas
en esa plana.
