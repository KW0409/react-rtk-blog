# RE Blog

這是一個使用 React 框架所建立的部落格平台。<br>
使用者分為訪客和會員，訪客及會員皆可在前台網站享受流暢的文章瀏覽及留言功能，而會員則可以在後台對個人資料及文章進行管理。

> 網站連結：[RE Blog](https://kw0409.github.io/react-rtk-blog/#/)

> 使用者測試帳密：user00/user00

![部落格網站截圖](https://user-images.githubusercontent.com/80152099/190562029-bbd3c9c1-eca6-4773-ba26-50a78a7af354.png "部落格網站截圖")

## 目錄

- [功能描述](#功能描述)
- [檔案架構](#檔案架構)
- [使用技術](#使用技術)
- [API 文件](#API-文件)

## 功能描述

- 前台功能

  - 註冊頁面：開放使用者註冊（具表單驗證功能）
  - 登入頁面：輸入帳號密碼後可以登入（具表單驗證功能）
  - About 頁面：隨意顯示一些關於這個部落格的話
  - 文章列表頁面：可看到所有文章，一頁只會顯示 5 筆（支援分頁功能，可以換頁）
  - 單篇文章頁面：點進去文章後可以看到文章完整內容
  - 文章分類頁面：可查看不同分類的文章 _(開發中...)_
  - 文章作者頁面：點擊作者可查看該作者發表的所有文章
  - 留言系統：可以用訪客/會員身份新增、編輯、刪除留言
  - 搜尋系統：可搜尋特定文章 _(開發中...)_
    <br>

- 後台功能（僅供註冊會員使用）

  - 會員資料系統：可查看/編輯會員資料 _(開發中...)_
  - 發表文章頁面：可以輸入標題跟內文發表新文章 _(支援 CKEditor 功能開發中...)_
  - 文章管理頁面：可編輯、刪除文章

## 檔案架構

```
├── api_docs.md
├── build
├── node_modules
├── package-lock.json
├── package.json
├── public
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
├── README.md
└── src
    ├── components
    │   ├── App
    │   │   ├── App.js
    │   │   └── index.js
    │   ├── Header
    │   │   ├── Header.js
    │   │   └── index.js
    │   ├── Loader
    │   │   ├── index.js
    │   │   └── Loader.js
    │   └── Pagination
    │       ├── index.js
    │       └── Pagination.js
    ├── context.js
    ├── customHooks
    │   ├── usePagination.js
    │   └── useSubmit.js
    ├── index.css
    ├── index.js
    ├── pages
    │   ├── AboutPage
    │   │   ├── AboutPage.js
    │   │   └── index.js
    │   ├── ArticlePage
    │   │   ├── ArticlePage.js
    │   │   └── index.js
    │   ├── HomePage
    │   │   ├── HomePage.js
    │   │   ├── index.js
    │   │   └── PostList.js
    │   ├── index.js
    │   ├── LoginPage
    │   │   ├── index.js
    │   │   └── LoginPage.js
    │   ├── NewPostPage
    │   │   ├── index.js
    │   │   └── NewPostPage.js
    │   ├── RegisterPage
    │   │   ├── index.js
    │   │   └── RegisterPage.js
    │   └── UpdatePostPage
    │       ├── index.js
    │       └── UpdatePostPage.js
    ├── redux
    │   ├── features
    │   │   ├── postSlice.js
    │   │   └── userSlice.js
    │   ├── selector.js
    │   └── store.js
    ├── utils.js
    └── WebAPI.js
```

## 使用技術

- React Hooks
- styled-components
- Redux Toolkit
- Redux thunk
- Bootstrap
- AWS EC2
- FileZilla
- Nginx
- PM2

## API 文件

- [API 文件](./api_docs.md) _(開發中...)_
