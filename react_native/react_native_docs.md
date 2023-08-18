# Starting React Native project

## Create a new project
```cmd
>> yarn create expo-app <project_name>
>> cd <project_name>
```

## Run project
```cmd
>> yarn expo start
```

## Seting up Tailwind

```cmd
>> yarn add tailwind-rn
>> npx setup-tailwind-rn
```

### Follow instalation steps:
1. Run tailwind-rn in development mode:
```cmd
>> yarn dev:tailwind
```
PS: Let it always running

2. Import TailwindProvider and tailwind.json in the root of your app
```javascript
import {TailwindProvider} from 'tailwind-rn';
import utilities from './tailwind.json';
```

3. Wrap the root of your app into TailwindProvider:
```javascript
<TailwindProvider utilities={utilities}>
 <MyComponent/>
</TailwindProvider>
```

4. Use Tailwind
```javascript
import {useTailwind} from 'tailwind-rn';

const MyComponent = () => {
 const tailwind = useTailwind();

 return <Text style={tailwind('text-blue-600')}>Hello world</Text>;
};
```

In `input.css` add:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```


## After the project is done
Everytime you clone the repository, run `yarn` to install the dependencies
