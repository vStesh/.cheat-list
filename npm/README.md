# How to create NPM module

### create project
```hgignore
npm init 
```

### add to package.json
```hgignore
"main": "dist/index.js",
  "types": "dist/index.d.ts",
  "files": [
    "/dist"
  ],
```

### install TS
```hgignore
npm i typescript
```

### init tsconfig
```hgignore
npx tsc --init
```

### compile
```hgignore
npx tsc
```

### set NodeJS default version using nvm
```hgignore
nvm alias default xx.xx.x
```
