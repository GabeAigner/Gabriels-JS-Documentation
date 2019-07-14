# `Vue.js Documentation by Gabriel Aigner`

## How to start?

Just add this script to your head:

```
<script src="https://cdn.jsdelivr.net/npm/vue@2.5.16/dist/vue.js"></script>
```

Now you are ready to use `Vue.js`!

## Vue Modes

This section is only relevant if you are using a custom build setup. \
The Vue Modes can be sometimes nessesary for you if you use `VUE-CLI`. \

### Development Mode

If you are running Vue in an development environment

```
npm run dev
```

then you might see this warning:

```
You are running Vue in development mode.
Make sure to turn on production mode when deploying for production.
```

`Don’t be alarmed` it’s just to tell you, to use `minified version of vue.js` code when you have finished your development and ready to deploy the files on a web sever. Then it will be the `Production Mode`.

#### Find here more about [turning on Production Mode](https://vuejs.org/v2/guide/deployment.html)!

### Production Mode

```
npm run build
```

will create a distributable files (production ready) for you in folder dist (default) if you are using vue-cli
