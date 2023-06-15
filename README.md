
```bash
npx create-next-app@latest

cd folder

npx eslint --init
yarn add --dev eslint-plugin-react-hooks
```

Edit eslintrc.json

Add to plugins
```bash
"plugins": ["react", "@typescript-eslint", "react-hooks"],
```

Add to rules
```bash
"rules": {"react-hooks/rules-of-hooks": "error","react-hooks/exhaustive-deps": "warn","react/react-in-jsx-scope": "off"}
```

Add to settings

```bash
"settings":{"react":{"version": "detect"}}
```

```bash
yarn add --dev --exact prettier
```

Create .prettierrc

```bash
{"trailingComma": "none","semi": true,"singleQuote": true}
```

```bash
yarn add --dev eslint-config-prettier eslint-plugin-prettier
```

Open .eslintrc.json
Add to extends

```bash
"extends": ["plugin:prettier/recommended","prettier"],
```

Add to rules
```bash
"rules": {"prettier/prettier": "error"}
```

Create folder .vscode and inside settings.json
```bash
{"editor.formatOnSave": false,"editor.codeActionsOnSave": {"source.fixAll.eslint": true}}
```

```bash
yarn add --dev eslint-plugin-import-helpers
```

Open .eslintrc.json
Add to plugins
```bash
"plugins": ["eslint-plugin-import-helpers"]
```

Add to rules
```bash
"rules": {
  "import-helpers/order-imports": [
    "warn",
    {
      "newlinesBetween": "always",
      "groups": [
        ["/^react/","/@react/","/^next/","/@next/"],
          "/module/",
          "/^@shared/",
          "/absolute/",
          ["parent", "sibling", "index"]
      ],
      "alphabetize": { "order": "asc", "ignoreCase": true }
    }
  ]
}
```

Lets remove @ from import
edit tsconfig.json
Add to compilerOptions

```bash
"baseUrl": "src",
```