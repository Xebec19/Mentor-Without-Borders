## Introduction to webdevelopment and overview of HTML and CSS

In this session we covered how webpages are fetched and basic examples of HTML and CSS

### Browsing the web

First we discussed how we perform a search
As we search for www.google.com in our browser. The query is sent to ISP (Internet Service Provider) which looks for
the query in DNS (Domain Name Service). ISP are large organizations which provides internet to users like us.
DNS (Domain Name Service) is a registry which maps domain name to IP Address. IP Address is a unique address given
to each computer over internet.
Back to searching, After ISP finds the required resource in DNS, it sends us back the IP Address of that resource or
server. The resource then sends us the html, css and javascript files which we execute in our browser and a web page
is displayed on our browser.

You can read more about ISP [here](https://www.geeksforgeeks.org/internet-service-provider-isp-hierarchy/)

Once we get the IP Address, we are able to directly connect to that server
How are we able to connect to that server ? Please refer to following diagram.

![internet-backbone drawio](https://user-images.githubusercontent.com/65282610/246672467-fb025138-7249-47d9-941e-838065ad8d87.png)

We connect to ISP, ISP connects Internet Backbone which eventually connects us to the server. The Internet backbone
can be simply defined as the core of the Internet. Here, the largest and fastest networks are linked together with
fiber-optic connections and high-performance routers. Please refer to [link](https://www.submarinecablemap.com/)
which shows us the network of internet backbone.

### Overview of html, css and javascript

Let's have a look to a basic example of html, css and java scipt

To create a html file, we create a file with .html extension. That file should have a

```
<!DOCTYPE html>
```

tag to signify
that document follows html5.
We will need a `<html>` tag which will act as the parent tag of our document.
`<html>` tag has two tags i.e. `<head>` tag and `<body>` tag. `<head>` contains meta information about the web page e.g, title, keywords, description etc of the webpage. `<body>` contains content of the webpage. In the below example we are using

`<h1>` tag to render a heading element.

```
<!doctype html>
<html>
<head>
<title>Web page</title>
</head>
<body>
<h1>Hello world</h1>
</body>
</html>
```

![Screenshot from 2023-06-18 20-37-14](https://user-images.githubusercontent.com/65282610/246673283-7d56be7c-115d-4cdd-9a77-468e7719290c.png)

A simple webpage does not look good. We also need some styling, add some colors and other stuff to make our website
look interactive. We need CSS! CSS helps us to define styling of a webpage. Let's create a basic style for above document.
For now, let's not worry about the syntax because we will cover it in the next sessions. Here, is how we will create
a basic style

```
.root {
    background-color: blue;
}
```

now adding it to our document.

```
<!doctype html>
<html>
<head>
<title>Web page</title>
<style>
.root {
    background-color: blue;
}
</style>
</head>
<body>
<h1 class="root">Hello world</h1>
</body>
</html>
```

As you can notice, we have added class property in h1 tag. We will read about this property while discussing CSS.
Now our document will look as follows

Let's add a basic button here which will show us a message box when we click on it.

```
<button onclick="handleClick()">Click me</button>

<script>
function handleClick() {
    prompt("hello world");
}
</script>
```

Now, we will add the above snippet to our webpage.

```
<!doctype html>
<html>
<head>
<title>Web page</title>
<style>
.root {
    background-color: blue;
}
</style>
</head>
<body>
<h1 class="root">Hello world</h1>
<button onclick="handleClick()">Click me</button>

<script>
function handleClick() {
    prompt("hello world");
}
</script>
</body>
</html>
```
