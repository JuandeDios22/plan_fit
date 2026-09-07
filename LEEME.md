# Cómo poner la app en tu iPhone

Son 10 minutos, una sola vez. Después es un icono más en tu pantalla de inicio.

---

## Paso 1 · Crea el repositorio en GitHub (5 min, desde el ordenador)

1. Entra en **github.com** y crea una cuenta gratis (si ya la tienes, salta al punto 2).
2. Arriba a la derecha, pulsa **+** → **New repository**.
3. Rellena:
   - **Repository name:** `mi-plan`
   - **Public** ← tiene que ser público; GitHub Pages gratis no funciona con repos privados.
   - No marques nada más.
4. Pulsa **Create repository**.

> **¿Es un problema que sea público?** No. Lo único que se sube es la app (el plan de
> entrenamiento y la dieta). **Tus datos — pesos, series, notas — se guardan solo en tu
> móvil**, nunca se suben a ningún sitio. Y aunque el repositorio sea público, nadie lo va
> a encontrar si no le das la URL.

## Paso 2 · Sube los archivos

1. En la página que te acaba de salir, pulsa el enlace **uploading an existing file**.
2. Arrastra **los 5 archivos** de esta carpeta de golpe:
   - `index.html`
   - `sw.js`
   - `manifest.webmanifest`
   - `icon-192.png`
   - `icon-512.png`

   *(el `LEEME.md` que estás leyendo no hace falta subirlo, pero tampoco molesta)*
3. Abajo, pulsa el botón verde **Commit changes**.

## Paso 3 · Activa GitHub Pages

1. En tu repositorio, pestaña **Settings** (arriba).
2. En el menú de la izquierda, **Pages**.
3. En **Source**, elige **Deploy from a branch**.
4. En **Branch**, elige **main** y la carpeta **/ (root)**. Pulsa **Save**.
5. Espera 1-2 minutos y recarga la página. Te aparecerá arriba tu dirección:

   ```
   https://TU-USUARIO.github.io/mi-plan/
   ```

## Paso 4 · Instálala en el iPhone

1. Abre esa dirección **en Safari** (importante: tiene que ser Safari, no Chrome — en iOS
   solo Safari puede instalar aplicaciones web).
2. Pulsa el botón de **compartir** (el cuadrado con la flecha hacia arriba, abajo en el centro).
3. Baja y pulsa **Añadir a pantalla de inicio**.
4. Ponle de nombre **Mi Plan** y pulsa **Añadir**.

Listo. Ya tienes el icono. Se abre a pantalla completa, sin barra de navegador, y
**funciona sin cobertura** — puedes entrenar en el garaje o correr por el monte sin datos.

---

## Cosas que conviene saber

**Tus datos viven en el móvil.** No hay cuenta ni servidor: todo se guarda en el
almacenamiento de Safari. Es privado, pero también significa que:

- Si borras el historial y los datos de Safari, **se borran**.
- No se sincroniza con otros dispositivos.

Por eso, cada 3 o 4 semanas entra en **Más → Exportar copia** y guarda el archivo en tus
Archivos o mándatelo por correo. Si algún día pasa algo, **Más → Importar copia** y lo
recuperas todo.

**Los pesos son en crudo.** Carne, pescado, arroz y pasta se pesan crudos, que es como se pesan
al cocinar. Es lo que hace que los números del menú y de la app cuadren entre sí.

**Para actualizar la app** (si quieres cambiar algo del plan más adelante): subes el
`index.html` nuevo al repositorio y la app se actualiza sola la próxima vez que la abras
con conexión. Tus datos no se tocan.

**Si el ciclo se descuadra** (te saltaste días, te fuiste de viaje): en **Más → Ajuste del
ciclo** lo mueves adelante o atrás hasta que cuadre con la sesión que te toca.

---

## Paso 5 (opcional) · Activar la foto de la comida

La app puede reconocer un plato a partir de una foto y estimar calorías y proteína. Usa
Claude, así que necesita una clave de API tuya. **La clave se guarda solo en tu móvil**: no
va al repositorio ni pasa por ningún servidor intermedio.

1. Entra en **console.anthropic.com** y crea una cuenta.
2. En **Billing**, mete **5 $** de saldo.
3. En **API keys** → **Create key**. Cópiala.
4. En la app: **Más → Reconocimiento por foto → Configurar la clave**. Pégala y pulsa
   **Probar la clave** para confirmar que funciona.

**Cuánto cuesta:** con el modelo Haiku, cada foto sale por unos **0,003 $**. Aunque hagas
4 fotos al día desde hoy hasta la boda, el total es **menos de 3 $**. Con 5 $ te sobra.

**Si algún día falla con "ese modelo no existe":** los modelos se renuevan cada cierto
tiempo. Entra en **Más → Reconocimiento por foto** y cambia el nombre del modelo por el
que esté vigente (por ejemplo `claude-sonnet-5`). No hay que tocar nada más.

> **Sobre la precisión:** la estimación por foto se equivoca típicamente entre un 20 y un
> 40 %, y falla más con guisos, salsas y aceite — justo donde más se esconden las calorías.
> Por eso la app te enseña lo que ha visto y **te deja corregir el número antes de guardar**.
> Úsala para llevar el registro sin esfuerzo, no como una báscula. Si un plato lo conoces
> bien, tu ojo será mejor que la foto.

**Mejor todavía que la foto: describir el plato.** En **Dieta → Comidas → Describirlo** escribes
"150 g de pollo, 2 huevos y una cucharada de aceite" y sale el desglose ingrediente a ingrediente.
Es más preciso que la foto porque los gramos los pones tú, y cuesta la décima parte. Además,
la app le pasa a Claude su propia tabla de 137 alimentos y las 33 recetas del plan, así que los
números salen de ahí y no de lo que el modelo se invente.

Con foto o con texto, **el resultado sale desglosado por ingredientes con sus gramos**: tocas el
gramaje que no cuadre y el total se recalcula solo. Si algo se le ha ido, hay una casilla para
darle una aclaración ("el pollo eran 250 g, sin aceite") y que lo repase.

Y si no tienes clave o estás sin cobertura, el botón **Calcular sin la API** reconoce lo que has
escrito contra la tabla de alimentos y hace las cuentas en el propio móvil.

---

## Cómo se usa, en 20 segundos

- **Hoy** — la sesión que toca, calculada automáticamente por la fecha. Toca el cuadrado
  de cada ejercicio para marcarlo hecho. En los días de fuerza escribe el peso y las
  repeticiones de cada serie; al marcar el ✓ de una serie arranca solo el descanso de 90 s
  y te vibra el móvil cuando toca la siguiente. El botón **i** de cada ejercicio abre su
  ficha: patrón, nivel y material, posición de partida, ejecución, errores típicos, qué debes
  notar, un vídeo, y el mismo movimiento **un escalón más fácil o más exigente**.
  El botón **⇄** cambia el ejercicio: te propone alternativas del mismo patrón que puedas hacer
  con mancuernas, comba, esterilla y una silla. El cambio **se guarda para ese día y esa
  variante** (la próxima vez ya sale cambiado) y se deshace cuando quieras. Si un ejercicio no
  te va, *No quiero volver a hacerlo* y no vuelve a aparecer entre las alternativas.
  Los cambios y los descartes se gestionan en **Más → Ejercicios**.
- **Ciclo** — los 10 días de un vistazo, con lo ya completado en verde. Toca cualquier día
  para verlo.
- **Peso** — te pesas, y la app calcula la media de 7 días y la compara con la curva
  objetivo. También cintura.
- **Dieta** — pestaña **Comidas**: lo que llevas comido hoy en calorías y proteína (foto,
  descripción por texto, a mano o directo desde el menú), y la media de los últimos días, que es
  el número que de verdad decide si bajas de peso.
  **Menú**: los 7 días de la semana con las cinco comidas, sus calorías y su proteína. Las
  cantidades de arroz, patata, pan, fruta y aceite **se ajustan solas** a tu objetivo del día;
  la proteína y la verdura no se tocan. Botón de **lista de la compra** de la semana entera y
  de registrar el día completo de un toque.
  **Recetas**: 33 recetas, todas de 20 minutos o menos, con los ingredientes en gramos, las
  calorías y la proteína de cada uno, y los pasos. Las de *batch cooking* están pensadas para
  multiplicarlas por tres el domingo.
  El resto de pestañas: tus calorías y macros (se ajustan solos al cruzar 98, 92 y 86 kg), qué
  comer, qué no, y cómo salir a comer fuera.
- **Más** — tus récords por ejercicio, los cambios y descartes de ejercicios, las 6 reglas y la
  copia de seguridad.

El catálogo tiene **64 fichas de ejercicio**: los del plan y los que se ofrecen como alternativa.
Cada serie que registras guarda el nombre del ejercicio que hiciste, así que **cambiar un ejercicio
no descoloca tus récords antiguos**.
