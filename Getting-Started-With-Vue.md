# `Getting Started with Vue`

The first step to beginning any Vue project is to import the Vue library. For simple projects, we do this by adding the following ``<script>`` tag to the ``<head>`` of the HTML file that will contain the Vue app:

````javascript
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js" defer></script>
````
## `Vue App Instantiation`
Now that we have the Vue library available to use, we need to create our Vue app. All ``Vue`` apps are instances of the ``Vue`` class provided by the imported Vue library. As with all classes, we must use the ``new`` keyword to make an instance of this class, like so: 
````javascript
const app = new Vue({});
````

If you put you ``vue cod``e into ``another file`` you need to import it. Then lets put you file into the same HTML file where we imported the Vue library. In index.html, add the following ``<script>`` tag on the line after importing the Vue library:
````javascript
<script src="./js/app.js" defer></script>
````
## `Attaching Vue Instances`