# B"H




### Global prerequisite step 
- only need to run once on machine:

```sh
sudo npm install -g live-server
```


### **`01-from-scratch`** prerequisite cleanup step:
- Only needed if run if you already ran through this walkthrough already.

```sh
# Step 0: Cleanup. 
cd ~/repos/tailwind-class/

rm -r 01-from-scratch
```


### **`01-from-scratch`** steps 1 thru 7:

```sh
# Step 1:
cd ~/repos/tailwind-class
mkdir 01-from-scratch
cd ~/repos/tailwind-class/01-from-scratch


# Step 2: Create the `package.json` file:
npm init -y


# Step 3: Install needed packages:
npm install tailwindcss postcss-cli autoprefixer


# Step 4: Create tailwindcss config:
npx tailwind init


# Step 5: Create the postcss.config.js file:
touch postcss.config.js


# Step 6: Create the css/tailwind.css file:
mkdir css && touch css/tailwind.css


# Step 7: Create the public/index.html file:
mkdir public && touch public/index.html
```


### Step 8: Add the following contents to the `postcss.config.js` file.
```js
module.exports = {
  plugins: [
    require('tailwindcss'),
    require('autoprefixer'),
  ]
}
```

### Step 9: Add the following contents to the `css/tailwind.css` file.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```


### Step 10: Add the build script *within* the `package.json` file:

```json
 "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css"
  },
```

### Step 11: Add the following contents to the `public/index.html` file.
```html
<html lang="en">

    <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <meta http-equiv="X-UA-Compatible" content="ie=edge">
          <title>Vos Machsts</title>
          <link rel="stylesheet" href="/build/tailwind.css">
    </head>

    <body>
        <h1 class="text-4xl font-bold text-center text-blue-500">Hello world!</h1>
    </body>

</html>
```


### Steps 12 and 13:

```sh
# Step 12: Run the build.
npm run build

# Step 13: Start `live-server` on the `public` dir:
live-server public
```







