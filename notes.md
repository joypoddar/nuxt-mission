## Nuxt Dynamic Routes

To create a dynamic page you need to add an underscore before the .vue file name or before the the name of the directory, if you want the directory to be dynamic. You can name the file or directory anything you want but you must prefix it with an underscore.

We can access the router params in our template using $route.params.slug. Let's change the title to be dynamic.

`{{$route.params.slug}}`

Now in our browser anything we type in the URL will be the title of our page. Nice. We can travel to any planet.