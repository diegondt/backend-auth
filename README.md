# Backend autenticacion usuarios

## Inicializar el repositorio

1. Hemos creado la carpeta
2. Iniciamos y subimos los primeros archivos al repositorio local

```bash
git init
git add .
git commit -m "build"
```
3. Crear el repositorio remoto en Github

```bash
gh repo create
```

## Crear proyecto de npm

1. Para arrancar el proyecto de npm:

```bash
npm init -y
```

2. Descargamos las dependencias

```bash
npm install express
npm i express
```

3. Creamos un .gitignore

## Crear servidor:

1. Creamos un `hola mundo`
2. Añadimos `better-sqlite3`

```bash
npm i better-sqlite3
```

3. Lo integramos en nuestro server

```js
// Conectar a la base de datos
const db = betterSqlite3('database.db');

//obtenemos la ruta absoluta a init.sql
const initSqlPath = path.join(__dirname, 'init.sql');
//leemos el archivo init.sql
const initSql = fs.readFileSync(initSqlPath, 'utf8');
//ejecutamos el contenido de init.sql
db.exec(initSql);
```