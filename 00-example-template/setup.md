# B"H


### Step 1: Create the `package.json` file:

```sh
cd ~/repos/tailwind-class/00-example-template

npm init -y
```

### Step 2: Install needed packages:

```sh
cd ~/repos/tailwind-class/00-example-template

npm install tailwindcss postcss-cli autoprefixer

```


### Step 3: Create tailwindcss config:

```sh
cd ~/repos/tailwind-class/00-example-template

npx tailwind init

```

### Step 4: Create the `postcss.config.js` file.

### Step 5: Create the `css/tailwind.css` file.

### Step 6: Add the build script to `package.json`:

```json
 "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css"
  },
```

### Step 7: Run the build.

```sh
cd ~/repos/tailwind-class/00-example-template

npm run build

```


### Step 8: Create the `public/index.html` file.


### Step 9: Install `live-server`:

```sh
cd ~/repos/tailwind-class/00-example-template

sudo npm install -g live-server

```



### Step 10: Start `live-server` on the `public` dir:


```sh
cd ~/repos/tailwind-class/00-example-template

live-server public

```
