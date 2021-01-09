## Nuxt Dynamic Routes

To create a dynamic page you need to add an underscore before the .vue file name or before the the name of the directory, if you want the directory to be dynamic. You can name the file or directory anything you want but you must prefix it with an underscore.

We can access the router params in our template using $route.params.slug. Let's change the title to be dynamic.

`{{$route.params.slug}}`

Now in our browser anything we type in the URL will be the title of our page. Nice. We can travel to any planet.

## Nuxt Data Fetching

In Nuxt there are two ways to get data. Let's take a look at the differences between fetching data using the async data hook and using the fetch Hook. They're pretty much very similar. The main difference is that async data is called before the page is loaded so we don't have access to this and we don't need to define the data property as it gets merged with our data.

Whereas when using the fetch hook, it gets called after the page is loaded.

Let's add a list of our planets to the index page using the fetch hook.

As Fetch is called after the page is created we need to define our data and then assign that data to the result of our fetch. Let's add an empty array for our planets and then we can use this to merge the results form our api to our data.