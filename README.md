# try-storybook
 
## Get Started

A starter project created on 20210304, following [Storybook Get Started](https://storybook.js.org/docs/react/get-started/install).

```bash
npx sb init

npm run storybook
```

Fails due to `ERR! Error: Cannot find module 'react/package.json'`. Fixes with 

```bash
npm install --save-dev react react-dom
```

