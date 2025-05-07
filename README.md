# azure-entra-tutorial-for-vite

## Overview
SPA で Microsoft Entra テナントにログインするチュートリアルを Vite に書き換えたアプリです。  
https://learn.microsoft.com/en-us/entra/identity-platform/tutorial-single-page-app-react-register-app

## Usage

`.env` ファイルを作成します。

```sh
$ cp .env.example .env
$ npm run dev
```

`.env` に必要な値を入力します。

```
VITE_ENTRA_CLIENT_ID={クライアントID}
VITE_ENTRA_REDIRECT_URI=http://localhost:5173
VITE_ENTRA_TENANT_ID={テナントID}
```

起動します。

```sh
$ npm run dev
```

`http://localhost:5173` にアクセスします。

## Notes
~~現在 (2025-02-21) は、@azure/msal-react が React v19 に対応していません。~~  
~~https://github.com/AzureAD/microsoft-authentication-library-for-js/issues/7577~~  
~~そのため、本家のチュートリアルで利用しているライブラリを差し替えています。~~  

2025-05-06 に React v19 対応版がリリースされました。
https://github.com/AzureAD/microsoft-authentication-library-for-js/pull/7735

構築手順は以下。

```sh
npm create vite@latest vitespalocal -- --template react
cd vitespalocal
npm install
npm run dev
npm install @azure/msal-browser@3.27.0 @azure/msal-react
npm install react-bootstrap bootstrap
```

create-react-app で構築したファイルとの差分は主に以下。
* App.css
* index.css
* index.js を main.jsx に変更
