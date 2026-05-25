```
import mysql from "mysql2/promise";
import express from "express"
import cors from "cors"

export const app = express()
app.use(express.json());
app.use(cors())
let con = await mysql.createConnection({
    host: "localhost",
    port: 3306,
    database: "viragbolt",
    user: "root",
    password: ""
});

app.listen(88, err => console.log(err ? err : "server on 88"))
```

```
{
  "name": "backend",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "type": "module",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "nodemon index.js"
    
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "packageManager": "pnpm@10.30.3",
  "dependencies": {
    "cors": "^2.8.6",
    "express": "^5.2.1",
    "mysql2": "^3.22.3"
  }
}

```
