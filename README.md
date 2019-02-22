# Edge CSS

Intuitive margin and padding classes for quick markup styling

```html
<div class="mt12">Header has a margin-top of 12px</div>
<div class="mt12 mb6">Header has a margin-top of 12px and margin-bottom of 6px</div>
```

### Smart

Based on the Duodecimal System (aka Base 12) which is a positional system using twelve as its base. Bootstrap, One%, Skeleton and 960 Grid System are all designed using Base 12 principles. All modern displays are also based on Base 12 and are divisible by 12 or it's four divisors: 2, 3, 4, 6.

### Install

```shell
$ npm i edge-css
```

### Usage

Include the edge.css in the head of your index.html

```html
<head>
    <link rel="stylesheet" href="bower_components/source/edge.css" />
</head>
```

Add classes to create padding and margins with the following `(px) values`: 2, 3, 4, 6, 12, 16, 18, 24, 36, 48

```html
<body>
    <header class="mt12">Header has a margin-top of 12px</header>
</body>
```

These elements have no padding

```html
<body>
    <h1 class="p0">Lorem ipsum</h1>
    <h2 class="p0">Dolor sit</h2>
</body>
```

This navigation is centered

```html
<body>
    <!-- Read "{ margin: auto 0 }" -->
    <nav class="ma0">
        <a href="/">Home</a>
    </nav>
</body>
```

All CSS properties have `!important` so they will override any class that is specified before them.

```html
<style>
    .btn-default {
        margin: 12px;
    }
</style>

<!-- This button will have margin-top, margin-left and margin-bottom of 12px and a margin-right of 0px; -->
<button class="btn-defulat mr0">Submit</button>
```

### How it works

All classes are composed of some simple parts.

### 1. Property shortcut

```
m         margin
   -OR-
p         padding
```

### 2. Direction

```
t         top
b         bottom
r         right
l         left

v         vertical
h         horizontal

(none)    No direction specified means *all* directions (m8 = `margin: 8px;`)

```

### 3. Positive or negative values (margins only)

```html
<div class="mr16"></div>
positive value { margin-right: 16px }
<div class="mr-16"></div>
negative value { margin-right: -16px }
```

### 4. Size

```
a  auto
0  0px
4  4px
6  6px
8  8px
12  12px
16  16px
18  18px
24  24px
32  32px
48  48px
```

### Example of classes with 24px margins

```html
<!--Margins-->

<div class="m24">margin: 24px</div>
<div class="mt24">margin-top: 24px</div>
<div class="mr24">margin-right: 24px</div>
<div class="mb24">margin-bottom: 24px</div>
<div class="ml24">margin-left: 24px</div>
<div class="mh24">margin-left: 24px; margin-right: 24px</div>
<div class="mv24">margin-top: 24px; margin-bottom: 24px</div>

<!--Negative margins-->

<div class="m-24">margin: -24px</div>
<div class="mt-24">margin-top: -24px</div>
<div class="mr-24">margin-right: -24px</div>
<div class="mb-24">margin-bottom: -24px</div>
<div class="ml-24">margin-left: -24px</div>
<div class="mh-24">margin-left: -24px; margin-right: -24px</div>
<div class="mv-24">margin-top: -24px; margin-bottom: -24px</div>
```

### Example of classes with auto margins

```html
<!--Auto margins-->

<div class="ma">margin: auto</div>
<div class="mta">margin-top: auto</div>
<div class="mra">margin-right: auto</div>
<div class="mba">margin-bottom: auto</div>
<div class="mla">margin-left: auto</div>
<div class="mha">margin-left: auto; margin-right: auto</div>
<div class="mva">margin-top: auto; margin-bottom: auto</div>

<!--Margin auto 0 for centering any element within it's parent-->

<div class="ma0">margin: auto 0</div>
```

### Customize

Dev dependencies

-   [SASS] - Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.
-   [Gulp] - The automated task/build runner for development.

cd into your local directory and run the following commands

```shell
$ npm install
```

```shell
$ gulp
```

Modify the .scss files in the source folder and gulp will automatically update your edge.css file in the dist folder

[sass]: http://sass-lang.com/install
[gulp]: https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md
