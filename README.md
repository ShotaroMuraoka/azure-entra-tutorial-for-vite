# Activity Log

```sh
npm create vite@latest vitespalocal -- --template react
cd vitespalocal
npm install
npm run dev
#npm install @azure/msal-browser @azure/msal-react
# https://github.com/AzureAD/microsoft-authentication-library-for-js/issues/7577
npm install @azure/msal-browser@3.27.0 @arjenbloemsma/msal-react
npm install react-bootstrap bootstrap
```

Replace '@azure/msal-react' to '@arjenbloemsma/msal-react'.  
Rewrite App.css and index.css.  
index.js should be placed in main.jsx.  
