# Vue 2 + Vite

This template should help get you started developing with Vue 2 in Vite.

## How to setup Vue2 + vite

1. Create Vue3 Project with vite

```shell
npm create vite@latest
```

2. Install packages

```shell
cd project
pm install
```

3. Install vite-plugin-vue2

```shell
npm install vite-plugin-vue2
```

4. Remove vite-vue plugin from package.json. Remove this line from dependencies

```
"@vitejs/plugin-vue": "^4.0.0"
```

5. Install vue2  [replaces vue3]

```shell
npm install vue@2
```

6. Update `vite.config.js` with following:

```javascript
import { defineConfig } from 'vite'
import { createVuePlugin } from 'vite-plugin-vue2';

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [createVuePlugin()],
})
```

7. Update `App.vue` with following:

```vue
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/vue.svg" />
    <HelloWorld msg="Hello Vue 2 + Vite" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
export default {
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
```
8. update `HelloWorld.vue` with following

```vue
<template>
  <div>
    <h1>{{ msg }}</h1>

    <p>
      <a href="https://vitejs.dev/guide/features.html" target="_blank"
      >Vite Documentation</a
      >
      |
      <a href="https://vuejs.org/v2/guide/" target="_blank"
      >Vue 2 Documentation</a
      >
    </p>

    <button @click="count++">count is: {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test hot module replacement.
    </p>
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
  },
  data() {
    return {
      count: 0,
    };
  },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
```

You are now all set to develop you application. you can run `npm run dev` to start dev server with vite serving your vue 2 app.

