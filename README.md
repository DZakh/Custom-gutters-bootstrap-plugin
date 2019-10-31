# Custom gutters bootstrap-plugin

This very simple plugin gives you a possibility to setup your own gutter widths for different screen breakpoints.

## Why?

In Bootstrap 3 we could easily manipulate with this parameter, but now according to [Bootstrap 4 Documentation](https://getbootstrap.com/docs/4.3/layout/grid/#customizing-the-grid) there is no option to choose different `$grid-gutter-width` for different breakpoints. So, this plugin solves the problem!

## Getting started

Install the latest version with NPM.

    npm install custom-gutters-bootstrap-plugin -D
Then import this plugin right after bootstrap.
```scss
@import 'custom';
@import '~bootstrap/scss/bootstrap';
@import 'node_modules/custom-gutters-bootstrap-plugin';
```
Nice! You can also just copy content of index.scss file to your project.

## How to use

Now you can customize width of your gutters. This is done in the same way as change other parameters in bootstrap [(check official documentation)](https://getbootstrap.com/docs/4.3/layout/grid/#grid-tiers). Just create a map variable like this in your `_custom.scss` file or somewhere before bootstrap's import:
```scss
$grid-gutter-widths: (
	xs: 10px,
	md: 20px,
	lg: 30px
);
```
Same as in Bootstrap here we use mobile first approach, so it means that `xs: 10px` also applies for `sm`  devices.

> **Note:** always use pixels and fill in *xs* value.


### Default value...

... is `30px` for each screen size. This's the same as in Bootstrap 4, so nothing will be suddenly broken.

## Thanks for using the plugin -_-