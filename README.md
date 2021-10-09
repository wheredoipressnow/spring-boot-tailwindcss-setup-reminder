## Setup tailwindcss in Spring Boot project
Install tailwind and dependencies
```bash
npm init -y
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest
```

Create configuration
```bash
npx tailwindcss init
```

Configure purge
```js
  purge: [
    './src/main/resources/**/*.html',
  ]
```

Start jit in watch mode
```bash
npx tailwindcss -o ./src/main/resources/static/css/tailwind.css --watch --jit --purge="./src/main/resources/**/*.html"
```

Create app.css and inject tailwind's styles
```scss
@tailwind base;
@tailwind components;
@tailwind utilities;
```
