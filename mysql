const express = require('express');
const mysql = require('mysql2');
const app = express();
const port = 8080;

// DB 연결 설정 (우리가 만든 서비스 이름 'mysql-service' 사용)
const db = mysql.createConnection({
  host: process.env.DB_HOST || 'mysql-service',
  user: 'root',
  password: 'test123',
  database: 'testdb'
});

app.get('/api', (req, res) => {
  res.json({
    message: "Hello from Backend!",
    db_status: "Trying to connect to DB..."
  });
});

app.listen(port, () => {
  console.log(`Backend app listening at http://localhost:${port}`);
});
