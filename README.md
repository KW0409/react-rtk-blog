# Re Blog

這是一個使用 React 框架所建立的部落格平台。<br>
使用者分為訪客和會員，訪客及會員皆可在前台網站享受流暢的文章瀏覽及留言功能，而會員則可以在後台對個人資料及文章進行管理。

> 網站連結：[Re Blog](123)

> 使用者測試帳密：user00/User00
> 後台測試帳密：admin00/Admin00

![部落格網站截圖](https://i.imgur.com/znJvjej.png "部落格網站截圖")

## 目錄

- [功能描述](#功能描述)
- [檔案架構](#檔案架構)
- [使用技術](#使用技術)
- [API 文件](#API文件)

## 功能描述

- 前台功能

  - 註冊頁面：開放使用者註冊（具表單驗證功能）
  - 登入頁面：輸入帳號密碼後可以登入（具表單驗證功能）
  - About 頁面：隨意顯示一些關於這個部落格的話
  - 文章列表頁面：可看到所有文章，一頁只會顯示 5 筆（支援分頁功能，可以換頁）
  - 單篇文章頁面：點進去文章後可以看到文章完整內容
  - 文章分類頁面：可查看不同分類的文章
  - 文章作者頁面：點擊作者可查看該作者發表的所有文章
  - 留言系統：可以用訪客/會員身份新增、編輯、刪除留言
  - 搜尋系統：可搜尋特定文章
    <br>

- 後台功能（僅供註冊會員使用）

  - 會員資料系統：可查看/編輯會員資料
  - 發表文章頁面：可以輸入標題跟內文發表新文章（支援 CKEditor）
  - 文章管理頁面：可編輯、刪除文章

## 檔案架構

```
├── package-lock.json
├── package.json
├── public
│   ├── favicon.ico
│   ├── index.html
│   ├── manifest.json
│   └── robots.txt
├── README.md
├── src
│   ├── API
│   │   ├── fetchAPI.js
│   │   ├── imgurAPI.js
│   │   └── WEBAPI.js
│   ├── components
│   │   ├── App
│   │   │   ├── App.js
│   │   │   └── App.test.js
│   │   ├── common
│   │   │   ├── Counter.js
│   │   │   ├── Dropdown.js
│   │   │   ├── EachErrorMessage.js
│   │   │   ├── Errormessage.js
│   │   │   ├── IconMark.js
│   │   │   ├── index.css
│   │   │   ├── Item.js
│   │   │   ├── Loading.js
│   │   │   ├── PageBtn.js
│   │   │   ├── PopModal.js
│   │   │   └── ProductsSectionTiTleContent.js
│   │   ├── Footer
│   │   │   ├── Footer.js
│   │   │   └── index.js
│   │   ├── Header
│   │   │   ├── Header.js
│   │   │   └── index.js
│   │   ├── img
│   │   │   ├── banner
│   │   │   ├── homePhoto
│   │   │   ├── icon
│   │   │   └── product
│   │   ├── routes
│   │   │   └── ProtectedRoutes.js
│   │   └── Style
│   │       └── style.js
│   ├── context.js
│   ├── hooks
│   │   ├── carts
│   │   │   ├── shipping
│   │   │   ├── useAddCartItems.js
│   │   │   ├── useCartApi.js
│   │   │   ├── useCount.js
│   │   │   ├── useDebounce.js
│   │   │   ├── useGetSingleProduct.js
│   │   │   ├── useRecommendsApi.js
│   │   │   ├── useScroll.js
│   │   │   ├── useShipping.js
│   │   │   └── useShippingApi.js
│   │   ├── common
│   │   │   ├── useHeader.js
│   │   │   └── usePagination.js
│   │   ├── discountHooks
│   │   │   ├── useDiscount.js
│   │   │   └── useEditDiscount.js
│   │   ├── orders
│   │   │   ├── useFIndAllOrder.js
│   │   │   └── useOneOrder.js
│   │   ├── paginationHooks
│   │   │   └── usePagination.js
│   │   ├── productHooks
│   │   │   ├── useAddProduct.js
│   │   │   ├── useAdminProducts.js
│   │   │   ├── useAdminRestoreProducts.js
│   │   │   ├── useCategory.js
│   │   │   ├── useFindHotProducts.js
│   │   │   ├── useFindNewProducts.js
│   │   │   ├── useFindProducts.js
│   │   │   ├── useFindRecommendProducts.js
│   │   │   ├── useHotProducts.js
│   │   │   ├── useSearchProducts.js
│   │   │   └── useUpdateProduct.js
│   │   └── user
│   │       ├── useLogin.js
│   │       ├── useRegister.js
│   │       ├── useSingleTransaction.js
│   │       ├── useTransaction.js
│   │       ├── useUpadtePassword.js
│   │       ├── useUpdateUserInfo.js
│   │       └── useUser.js
│   ├── index.css
│   ├── index.js
│   ├── normalize.css
│   ├── pages
│   │   ├── AddProductPage
│   │   │   ├── AddProductPage.js
│   │   │   └── index.js
│   │   ├── Admin
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── OrderPage.js
│   │   ├── AdminProductsPage
│   │   │   ├── AdminProductsPage.js
│   │   │   ├── components
│   │   │   └── index.js
│   │   ├── AdminProductsRestorePage
│   │   │   ├── AdminProductsRestorePage.js
│   │   │   ├── components
│   │   │   └── index.js
│   │   ├── CartPage
│   │   │   ├── CartPage.js
│   │   │   ├── component
│   │   │   └── index.js
│   │   ├── discountPages
│   │   │   ├── DiscountEditPage.js
│   │   │   ├── DiscountsPage.js
│   │   │   ├── index.js
│   │   │   ├── inputItem.js
│   │   │   └── TdContext.js
│   │   ├── FaqPage
│   │   │   ├── FaqItems.js
│   │   │   ├── FaqPage.js
│   │   │   └── index.js
│   │   ├── HomePage
│   │   │   ├── components
│   │   │   ├── HomePage.js
│   │   │   └── index.js
│   │   ├── HotProductsPage
│   │   │   ├── components
│   │   │   ├── HotProductsPage.js
│   │   │   └── index.js
│   │   ├── LoginPage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── LoginPage.js
│   │   ├── NewProductsPage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── NewProductsPage.js
│   │   ├── OrderWholeListPagePage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── OrderWholeListPage.js
│   │   ├── ProductsPage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── ProductsPage.js
│   │   ├── RegisterPage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── RegisterPage.js
│   │   ├── SearchPage
│   │   │   ├── components
│   │   │   ├── index.js
│   │   │   └── SearchPage.js
│   │   ├── SingleProductPage
│   │   │   ├── index.js
│   │   │   ├── SingleProduct.js
│   │   │   └── SingleProductPage.js
│   │   ├── SingleTransactionPage
│   │   │   ├── index.js
│   │   │   └── SingleTransactionPage.js
│   │   ├── TransactionPage
│   │   │   ├── index.js
│   │   │   └── TransactionPage.js
│   │   ├── UpdateProductPage
│   │   │   ├── index.js
│   │   │   ├── old.js
│   │   │   └── UpdateProductPage.js
│   │   └── UserPage
│   │       ├── components
│   │       ├── index.js
│   │       └── UserPage.js
│   ├── reportWebVitals.js
│   ├── setupTests.js
│   └── utils.js
└── TREE.md
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

## API 文件 {#API 文件}

- [API 文件](./api_docs.md)
