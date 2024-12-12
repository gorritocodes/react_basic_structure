# How to create a basic react app

## create a folder that will contain the app

currently the folder should have a name that is "URl Safe" (no special characters or spaces)

## install create-react-app

If you want to install react in the root folder, and have the latest version of create-react-app, use the following command:

```bash
npx  create-react-app@latest ./
```

currently there are lost of issues because of software that is deprecated, we'll address that now.

you'll find this issue

```warning
One of your dependencies, babel-preset-react-app, is importing the      
"@babel/plugin-proposal-private-property-in-object" package without     
declaring it in its dependencies. This is currently working because     
"@babel/plugin-proposal-private-property-in-object" is already in your  
node_modules folder for unrelated reasons, but it may break at any time.

babel-preset-react-app is part of the create-react-app project, which   
is not maintianed anymore. It is thus unlikely that this bug will       
ever be fixed. Add "@babel/plugin-proposal-private-property-in-object" to
your devDependencies to work around this error. This will make this message
go away.
```

to solve it you'll need to run:

```bash
npm i @babel/plugin-proposal-private-property-in-object --save-dev
```

if you run the app with:

```bash
npm start
```

you'll get the following error:

```cmd
Module not found: Error: Can't resolve 'web-vitals' in '%FILEPATH%react_basic_structure\src'
```

to solve it:

```bash
npm i web-vitals --save-dev
```

<!-- error if you check the  `npm audit` command:

```cmd

    nth-check  <2.0.1
Severity: high
Inefficient Regular Expression Complexity in nth-check - https://github.com/advisories/GHSA-rp65-9cf3-cjxr
fix available via `npm audit fix --force`
Will install react-scripts@3.0.1, which is a breaking change
node_modules/svgo/node_modules/nth-check
  css-select  <=3.1.0
  Depends on vulnerable versions of nth-check
  node_modules/svgo/node_modules/css-select
    svgo  1.0.0 - 1.3.2
    Depends on vulnerable versions of css-select
    node_modules/svgo
      @svgr/plugin-svgo  <=5.5.0
      Depends on vulnerable versions of svgo
      node_modules/@svgr/plugin-svgo
        @svgr/webpack  4.0.0 - 5.5.0
        Depends on vulnerable versions of @svgr/plugin-svgo
        node_modules/@svgr/webpack
          react-scripts  >=2.1.4
          Depends on vulnerable versions of @svgr/webpack
          Depends on vulnerable versions of resolve-url-loader
          node_modules/react-scripts

postcss  <8.4.31
Severity: moderate
PostCSS line return parsing error - https://github.com/advisories/GHSA-7fh5-64p2-3v2j
fix available via `npm audit fix --force`
Will install react-scripts@3.0.1, which is a breaking change
node_modules/resolve-url-loader/node_modules/postcss
  resolve-url-loader  0.0.1-experiment-postcss || 3.0.0-alpha.1 - 4.0.0
  Depends on vulnerable versions of postcss
  node_modules/resolve-url-loader
```

npm i webpack@latest --save-dev
npm i react-scripts@latest
npm install --save-dev eslint-config-react-app eslint@latest 

npm uninstall webpack@latest
npm uninstall react-scripts@latest
npm uninstall eslint-config-react-app eslint@latest
-->
