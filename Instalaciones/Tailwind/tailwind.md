# Guía de Instalación Tailwind

## Paso 1. Creamos un directorio y accedemos a el

```bash
mkdir proyecto-tailwind
cd proyecto-tailwind
```

## Paso 2. Instalamos node js

* Vamos al sitio oficial de **[Node.js](https://nodejs.org/en/download)**
* Descargamos la versión LTS, que es la más estable.
* Ejecutamos el instalador y seguimos los pasos.

Para confirmar que todo esté en orden, abrimos la terminal de nuestro proyecto y escribimos:

```bash
node -v
npm -v
```

Si aparece su versión significa que Node.js y npm se instalaron correctamente.

## Paso 3. Instalación de Tailwind CSS

En nuestra terminal escribimos:

```bash
npm install tailwindcss @tailwindcss/cli
```

Al terminar la ejecución se crea el directorio **node_modules**, y los archivos **package-lock.json** y **package.json**.

## Paso 4. Editamos el archivo package.json

Abrimos el archivo **package.json** e ingresamos lo siguiente:

```json
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch"
}
```

Nos quedaría algo así:

```json
{
  "scripts": {
    "dev": "npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch"
  },
  "dependencies": {
    "@tailwindcss/cli": "^4.2.4",
    "tailwindcss": "^4.2.4"
  }
}
```

Esto nos permite crear un atajo de npm para no escribir el comando completo cada vez que ejecutemos. En lugar de escribir: `npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch` solo escribimos: `npm run dev`.

## Paso 5. Creamos la estructura del proyecto

Creamos el archivo **index.html** y el directorio **src** dentro del directorio los archivos **input.css** y **output.css**.

```bash
proyecto-tailwind/
│
├── src/
│   ├── input.css
│   └── output.css
│
├── index.html
```

## Paso 6. Editamos index.html

En el **index.html** agregamos la estructura básica de un documento y dentro de la etiqueta `<head>` agregamos: 

```html
<link rel="stylesheet" href="./src/output.css">
```

Nos quedaria algo como:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./src/output.css">
</head>
<body>
    <!-- Ejemplo para ver si funciona tailwind -->
    <h1 class="text-3xl font-bold underline text-amber-500">Hola Mundo</h1>
</body>
</html>
```

## Paso 7. Editamos input.css

Dentro del archivo input.css agregamos:

```css
@import "tailwindcss"; 
```

## Paso 8. Ejecutamos nuestro script

Ingresamos en nuestra terminal:

```bash
npm run dev
```

Esto permite que Tailwind detecte los cambios automáticamente mientras desarrollamos. Para detener la ejecución usamos `ctrl + c`.