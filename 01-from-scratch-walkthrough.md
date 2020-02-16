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


### **`01-from-scratch`** actual steps:

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


# Step 8: Create the public/index.html file:
mkdir public && touch public/index.html
```


### Step ????: Create the `postcss.config.js` file.
```js
module.exports = {
  plugins: [
    require('tailwindcss'),
    require('autoprefixer'),
  ]
}
```

### Step ???: Create the `css/tailwind.css` file.

### Step 6: Add the build script to `package.json`:

```json
 "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css"
  },
```



```sh

# Step 7: Run the build.
npm run build

# Step 10: Start `live-server` on the `public` dir:
live-server public
```







