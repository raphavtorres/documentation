# React Native

### Currently the tailwind is not working properly

# Starting React Native project

### Prepare dev environment

```bash
>> npm install --global expo-cli
```


### Create a new project

```bash
>> npx create-expo-app <app_name>
```


### Run project

```bash
>> npx expo start
```


### Handling installations

```bash
>> npx expo instal
```

### Seting up Tailwind

```bash
>> yarn add nativewind
>> yarn add --dev tailwindcss
```

### Create a tailwind.config.js file

```bash
>> npx tailwindcss init
```

### Paste the next comands in the tailwind.config.js file
```javascript
/** @type {import('tailwindcss').Config} \*/
module.exports = {
    content: ["./App.{js,jsx,ts,tsx}", "./src/**/\*.{js,jsx,ts,tsx}"],
    theme: {
        extend: {},
    },
    plugins: [],
}
```

### Add the Babel plugin, modify your babel.config.js
```javascript
// babel.config.js
module.exports = function (api) {
    api.cache(true);

    return {
        presets: ['babel-preset-expo'],
        plugins: ["nativewind/babel"],
    };
};
```


### After the project is done
Everytime you clone the repository, run `yarn` to install the dependencies
