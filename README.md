Welcome to your very first React app! In the following content, we'll start with the basics by setting up React and building your first "Hello World" web app. We'll take it step by step.

First, let's get React installed. We'll go with the pure, simplest method that doesn't require any special tools only for learning purposes. You'll create a folder for the code:

```
$ mkdir ~/projects
```

Now, within the newly created folder, let's create a separate folder to keep the React library code:

```
$ mkdir ~/projects/react
```

Next, we need to add two files: one for React itself and the other for ReactDOM, which is an add-on. You can grab the latest version of both from the unpkg.com host. Here's how you can do it:

```sh
  curl -L https://unpkg.com/react@latest/umd/react.development.js > ~/projects/react/react.js
  curl -L https://unpkg.com/react-dom@latest/umd/react-dom.development.js > ~/projects/react/react-dom.js
```

You now have React and ReactDOM locally, which means you can learn anywhere, even without an internet connection.

Now, let's create a simple web page that will serve as our React app. Save the following code in a file named `hello-react.html`:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Hello React</title>
  <meta charset="utf-8">
</head>
<body>
  <div id="app"> <!-- Your app will render here --> </div>
  <script src="react/react.js"></script>
  <script src="react/react-dom.js"></script>
  <script>
    // Your app's code will go here
  </script>
</body>
</html>
```

Congratulations, you've just built your first React application! To see it in action, open the `hello-react.html` file in your browser, and you'll see the magic of "Hello World" come to life.

Now, let's understand what happened in the code. First, you included the React library and its ReactDOM add-on using `<script>` tags. Then, you defined the location where your React app should render, using the `<div id="app">` placeholder.

The actual app code that rendered "Hello World" looks like this:

```javascript
ReactDOM.render(
  React.createElement('h1', null, 'Hello world!'),
  document.getElementById('app')
);
```

This code uses the `React.createElement()` method, which creates a React component. In this case, it creates an `<h1>` element with the text "Hello world!" and renders it within the `<div id="app">`.

React is designed with simplicity in mind. You have the React object and the ReactDOM object, and you use them to create components and render them in the browser. React's power lies in its component-based approach, where you can combine and reuse components to build complex user interfaces.

To make things even easier, you can use JSX, a syntax that looks like HTML but is not natively understood by browsers. JSX makes the code more readable and allows you to write components in a more intuitive way. To use JSX, you need to transpile it with Babel. For learning purposes, we'll do the transpilation in the browser, but for production, you'd typically set up a build process.

Thanks to [Stoyan Stefanov (2022). _React: Up & Running: Building Web Applications_.](https://www.oreilly.com/library/view/react-up/9781492051459/) O’Reilly Media, Inc. for the inspiration and a great explanation
