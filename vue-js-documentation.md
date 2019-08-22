# `Vue.js Documentation by Gabriel Aigner`

## `Importing Vue.js`

You can import Vue by adding a `<script>` tag inside the `<head>` of your project’s HTML file:

```javascript
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js" defer />
```

Use the `defer` attribute on the `<script>` tag to make sure that the page is loaded and ready to hook up to Vue before we actually load Vue. \
\
Even at this preliminary step, the `Vue team` has found ways to shorten your development time. \
Many front-end frameworks, like `React` and `Angular`, have `difficult setup processes` that can make starting a project a hassle. \
The Vue team recognized that many `complex front-end features aren’t useful` until `late in the front-end learning journey` (or sometimes at all). As a result, they `offered` this `simple alternative` that provides most of Vue’s features to developers `quickly` and `easily`. \
\
Now you are ready to use `Vue.js`!

## `Vue Modes`

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

will create a distributable files (production ready) for you in folder dist (default) if you are using `vue-cli`.

## `Creating Vue Apps`

Vue makes it easy to make a new app by exporting a class called `Vue`. Much like any other JavaScript class, we create instances of this class using the `new` keyword. Each of these `Vue` instances is a fully-functioning Vue app. \
\
Let’s look at an example:

```javascript
// app.js
const app = new Vue({});
```

\
The Vue constructor takes in only one object, called the `options object`. \
Each piece of information the Vue app needs to function is added to the options object as a key-value pair. \
This means that developers can easily update or add information in the Vue app by just looking for the correct key in the options object. \
\
![Diagram Create a Vue App](img/diagramCreateVueApp.png)

## `el`

We need to specify to our Vue app which portion of our HTML we want to gain access to our Vue app’s logic. \
We do this by adding a key-value pair to the Vue app’s options object. \
We add a key called `el`, standing for HTML `el`ement, with a value of a CSS selector as a string that will target an element in our HTML and give it access to our Vue app’s functionality.

```javascript
// app.js
const app = new Vue({
  el: "#app"
});
```

In the above example, we wanted an HTML element with an ID of `app` to gain access to our Vue app’s functionality. \
We added an `el key` to the options object and made the value '`#app`', a CSS selector that will target an element with an ID,`#`, of `app`.

```html
<!-- index.html -->
<head>
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js" defer></script>
  <script src="./js/app.js" defer></script>
</head>
<body>
  <div id="app">
    <!-- Vue App HTML Code -->
  </div>
</body>
```

**Note:** We must import our Vue app code after the `<script>` that loads `Vue.js`. \
Otherwise, we would `not` yet have access to the `Vue library in app.js`, \
making it `impossible` to `create` a Vue `app`. This is also why we add `defer` to both elements — to ensure Vue has `fully loaded` when we go to make our Vue app.

## `Data`

An essential feature all front-end frameworks must accomplish is rendering and updating dynamic data. Information like the number of likes on a social media post may change at any second. Front-end frameworks must make it easy to display these types of dynamic data and automatically update them for users as soon as they change. \
\
To display dynamic information we need:

- A place to store the data we will be displaying
- A syntax for displaying that information

Let’s tackle the first point. \
\
As mentioned, everything our Vue app needs should be provided on the options object when the Vue app is created. Therefore, all of our dynamic data will need to be specified in our options object at a property called `data`.

```javascript
const app = new Vue({
  el: "#app",
  data: {
    username: "Gabriel"
  }
});
```

In this example, we added the `data` property to our options object. Apps need to display many pieces of dynamic `data`. To accommodate this, the value of `.data` is an object as well. Every piece of data will be added to the .data object as a key-value pair. In this case, we only added one piece of data called `username` with a value of '`Michael`'.

## `Templates`

As a reminder, we need the following tools to display dynamic information in our Vue app:

- A place to store the data we will be displaying
- A syntax for displaying that information

We now know that we store our dynamic information on the `.data` attribute of our Vue app options object, but how do we display that information if it potentially will keep changing values? \
\
Vue makes use of **templating** meaning that the developer specifies certain content in our HTML isn’t meant to be displayed literally but rather substituted out with the appropriate data from the app. We specify which content inside our HTML should be substituted by surrounding it in two layers of curly brackets, like so:

```javascript
<div id="app">
  <h2>Hello, {{ username }}</h2>
</div>
```

In this example, `{{ username }}` will be filled in with the value of `username` from the Vue app’s `.data` object when the page is rendered to the user. If the value of `username` changes, the value displayed to the user will be changed as well. \
\
This type of HTML code, where dynamic `data` is stubbed out, is called a _template_. Templates contain all of the hard-coded information displayed on the site but specify places where dynamic information needs to be filled in. \
\
Using curly brackets for templating in HTML was popularized by a framework called mustache. As a result, curly braces in templates are often called “mustaches.” Whenever you want to display information from the Vue app’s `data`, you wrap the name of the `.data` property in two sets of mustaches (curly brackets) and the expression will be replaced with the Vue data information for the end user to see. \
\
This is far easier to read and write than trying to write vanilla JavaScript that selects specific HTML elements and updates their content dynamically. Using the `.data` attribute and mustache templates is yet another way Vue makes front-end web development faster to write, easier to read, and less error-prone.

## `Directives`

Directives are custom HTML attributes built into Vue that accomplish incredibly complex, common front-end operations using barely any code. \
\
For example, one very common front-end need is to conditionally display elements. Let’s say we only want to show a login button if a user isn’t already logged in. \
We can add a `v-if` directive as an attribute to HTML elements like so:

```html
<button v-if="userIsLoggedIn">Log Out</button>
<button v-if="!userIsLoggedIn">Log In</button>
```

`v-if` acts an awful lot like `JavaScript if`. It will only display the HTML element it is on if the `v-if statement` returns `true`. In this case, it will check our `.data` for a value of `userIsLoggedIn`. Then it will only display our `“Log Out”` button if `userIsLoggedIn` is `true` and will only display our “Log In” button if it is `false`. \
\
Another complex, common front-end need is to render an array of items identically. We can use `v-for` as an attribute, like so:

```html
<ul>
  <li v-for="todo in todoList">{{ todo }}</li>
</ul>
```

Bam, just like that `v-for` will iterate through every item in our `.data‘s` todoList array, create a variable called `todo` containing each succesive array element, and create an `li` displaying each element in the list. `Even if a new item is added to the list, the list will be re-rendered instantly to display that new item.` \
\
One more super cool directive is `v-model`. v-model can be added to any form field and hooked up to our Vue app’s `data`. Modifying the form field will then automatically modify the specified Vue app data!

```html
<input v-model="username" />
```

The above `input` field will display the current value of `username` on the Vue app’s `data` object and will change the value of `username` if the user modifies the value in the field. That’s some complicated JavaScript implemented perfectly with very little code. \
\
As you may have noticed, every built-in Vue directive starts with **`v-`**. There are too many for me to cover, however you can view a list of them all [here](https://vuejs.org/v2/api/#Directives). \
Just know that if there isn’t a directive that does what you need — you can even make your own! \
[See all Java Directives here](https://vuejs.org/v2/api/#Directives) \
\
Directives make complex front-end code easy to write, easy to read, and optimized for great site performance.

### Handling events

If we make a button and want to open a function we can use `v-on` like this:

```javascript
<button v-on:click="doSomething()">Click me</button>
```

This method can be written into the methods section in the `Vue object`:

```javascript
new Vue({
  el: "#app",
  data: {
    counter: 0
  },
  methods: {
    doSomething: function(event) {
      this.counter++;
    }
  }
});
```

If we want more than one parameter we have to write it like this:

```javascript
<button v-on:click="doSomething(2, $event)">Click me</button>
```

This method can be written into the methods section in the `Vue object`:

```javascript
new Vue({
  el: "#app",
  data: {
    counter: 0
  },
  methods: {
    doSomething: function(i, event) {
      this.counter += i;
    }
  }
});
```

### Modifying an Event - with Event Modifiers

Handling events isnot all, we can also `modify` them.
As example we make a `input field`, and want to read the input data when someone is `pressing enter` and `pressing space`, because we can chain this modifiers.

`````javascript
<input type="text" v-on:keyup.enter.space="readInput" />
````
and the Vue object

````javascript
new Vue({
        el: "#app",
        data: {
          inputData: ""
        },
        methods: {
          readInput: function(event) {
            this.inputData = event.target.value;
          }
        }
      });
````

We can also use .tab , .esc and some more.
But that is only the top of the iceberg, because this are only the modifiers for keyup :D

## `Components`

It is incredibly common to re-use complex elements throughout a front-end web app. For example, every post on Instagram or Facebook needs to look the same but contain different information. Additionally, they need to look the same on many different pages within the site and on many different devices. To make this easier, Vue has added the ability to create custom, reusable HTML elements called **components**. \
\
When creating a component, you provide a template that should be rendered whenever the component is used in HTML. You then specify which pieces of dynamic information, called **props**, the component can receive to fill in this template. When used in your HTML code, props look like normal HTML attributes, you add them to the opening tag of the component HTML element with a name and a value. \
\
Once you’ve created your component, you can then use it throughout your site just like any other HTML element. This means no copy/pasting of HTML code, no need to make the same change in multiple places across your site, and no potentially broken or misstyled elements. \
\
Knowing how and when to make components is a slightly more advanced topic, so we won’t cover it in depth. However, that doesn’t mean we can’t play around with them right now. Let’s check one out! \
\
Component example:

```javascript
const Tweet = Vue.component('tweet', {
 props: ['message', 'author'],
 template: '<div class="tweet"><h3>{{ author }}</h3>
            <p>{{ message }}</p></div>'
});
```

And where you use the components, you have to bind the props of the component like this:

```javascript
<div class="tweets">
  <tweet
    v-for="tweet in tweets"
    v-bind:author="username"
    v-bind:message="tweet"
  />
</div>
```

This is the vue for it:

```javascript
const app = new Vue({
  el: "#app",
  data: {
    username: "CoderInTraining",
    newTweet: "",
    tweets: [
      "Started learning to code today. Wish me luck!",
      "Today I start learning Vue. I got this."
    ],
    bio: "Excited future front-end  engineer."
  }
});
```

## `Virtual DOM`

Everything You have read about Vue thus far has been primarily about syntax. \
Syntactical features like mustache templates, directives, and components greatly \
improve speed of code-writing and readability of code. However, these features don’t \
necessarily improve page speed, an essential issue all front-end frameworks need to address. \
\
Behind the scenes, Vue uses a really cool data structure called a **virtual DOM** to vastly improve speed and responsiveness of Vue apps. The best way to introduce this topic is to see it in action, so watch a short video to understand what a virtual DOM is and how it speeds up app performance. Check it out to learn how Vue apps render and respond to user actions so quickly. \
\
[Click here to watch the video](https://www.youtube.com/watch?v=jwRAdGLUarw)
`````
