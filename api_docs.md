## API 文件 **_(非正式文件，仍在開發中...)_**

Base URL: https://kwang.tw/reblog

#### 使用者 User

| 說明                 | Method | path             | 權限擁有者 |
| -------------------- | ------ | ---------------- | ---------- |
| 註冊使用者           | POST   | /register        | anyone     |
| 登入使用者           | POST   | /login           | anyone     |
| 取得自己的使用者資料 | GET    | /user            | user       |
| 修改自己的使用者資料 | POST   | /user            | user       |
| 修改自己的密碼       | POST   | /update-password | user       |

#### 文章 Product:

| 說明         | Method | path      | 權限擁有者 |
| ------------ | ------ | --------- | ---------- |
| 取得所有文章 | GET    | /articles | anyone     |
| 修改文章     | POST   | /articles | admin      |
| 新增文章     | POST   | /articles | admin      |
| 刪除文章     | DELETE | /articles | admin      |
| 搜尋文章     | GET    | /articles | anyone     |
