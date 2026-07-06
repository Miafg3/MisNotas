# Guía de Instalación Sass

## Paso 1. Creamos un directorio y accedemos a él

```bash
mkdir proyecto-sass
cd proyecto-sass
```

## Paso 2. Instalamos Node.js

- Vamos al sitio oficial de **[Node.js](https://nodejs.org/en/download)**
- Descargamos la versión LTS.
- Ejecutamos el instalador y seguimos los pasos.

Para confirmar que todo esté en orden, abrimos la terminal de nuestro proyecto y escribimos:

```bash
node -v
npm -v
```

Si aparece su versión significa que Node.js y npm se instalaron correctamente.

## Paso 3. Instalación de Sass

En nuestra terminal escribimos:

```bash
npm install sass
```

Al terminar la ejecución se crea el directorio **node_modules**, y los archivos **package-lock.json** y **package.json**.

## Paso 4. Editamos el archivo package.json

Abrimos el archivo **package.json** e ingresamos lo siguiente:

```json
"scripts": {
  "dev": "npx sass --watch scss/style.scss css/style.css"
}
```

Nos quedaría algo así:

```json
{
  "scripts": {
    "dev": "npx sass --watch scss/style.scss css/style.css"
  },
  "dependencies": {
    "sass": "^1.89.0"
  }
}
```

Esto crea un **script de npm**, permitiéndonos ejecutar Sass mediante:

```bash
npm run dev
```

## Paso 5. Creamos la estructura del proyecto

Creamos el archivo **index.html** y los directorios **scss** y **css** dentro de ellos los archivos **style.scss** y **style.css**.

```bash
proyecto-sass/
│
├── scss/
│   └── style.scss
│
├── css/
│   └── style.css
│
├── index.html
```

## Paso 6. Editamos index.html

En el **index.html** agregamos la estructura básica de un documento y dentro de la etiqueta `<head>` agregamos: 

```html
<link rel="stylesheet" href="./css/style.css">
```

Nos quedaria algo como:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sass</title>
    <link rel="stylesheet" href="./css/style.css">
</head>
<body>
    <h1>Hola Mundo</h1>
</body>
</html>
```

## Paso 7. Escribimos código Sass

Dentro de style.scss podemos escribir codigo para ver que todo funcione.

Ejemplo:

```scss
$primary-color: crimson;

h1 {
  color: $primary-color;
}
```

## Paso 8. Ejecutamos Sass

En la terminal escribimos:

```bash
npm run dev
```

Esto permite que Sass detecte cambios automáticamente y compile de .scss a .css

Para detener la ejecución usamos:

```bash
ctrl + c
```