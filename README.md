# CSS Edge
Intuitive margin and padding classes for quick markup styling

## SMART
Based on the Duodecimal System (aka Base 12) which is a positional system using twelve as its base.

## INSTALL
bower
```shell
$ bower install edge-css
```

## Usage
Include the edge.css in the head of your index.html:

```html
<head>
<link rel="stylesheet" href="bower_components/dist/edge.css">
</head>
```

Add classes to create padding and margins with the following values: 4, 6, 12, 16, 18, 24, 36, 48



```html
<body>
<header class="mt12">This will give this header a margin-top of 12px</header>
</body>
```

These elements have no padding:
```html
<body>
<h1 class="p0">Lorem ipsum</h1>
<h2 class="p0">Dolor sit</h2>
</body>
```

This navigation is centered:
```html
<body>
<!-- Read "margin-vertical-null margin-horizontal-auto" -->
<nav class="mv0 mha">
  <a href="/">Home</a>
</nav>
</body>
```

All properties have `!important` as you should only add those classes, if you definitely want a specific behavior.

Sizes are defined in `px`.

## How it works
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

### 3. Delimiter
```
-         positive value
--        negative value
```
Example:
```css
.mt16  { margin-top: 16px }
.mt-16 { margin-top: 16px }
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

### Possible classes (normal syntax)

The following example just uses one size: s (24px). There is also `xxxs - xxxl` and `0` and `a` (which is auto).

Margin classes (they start with **m**) can have positive and negative values, padding classes (replace the leading **m** with a **p**) just have positive values.

```
mt24      margin-top: 24px
mr24      margin-right: 24px
mb24      margin-bottom: 24px
ml24      margin-left: 24px

mh24      margin-left: 24px; margin-right: 24px
mv24      margin-top: 24px; margin-bottom: 24px

m24       margin: 24px

mt-24      margin-top: -24px
mr-24      margin-right: -24px
mb-24      margin-bottom: -24px
ml-24      margin-left: -24px

mh-24      margin-left: -24px; margin-right: -24px
mv-24      margin-top: -24px; margin-bottom: -24px

m-24       margin: -24px

// there is also 'auto'
mta       margin-top: auto
mra       margin-right: auto
mba       margin-bottom: auto
mla       margin-left: auto

mha       margin-left: auto; margin-right: auto
mva       margin-top: auto; margin-bottom: auto

ma        margin: auto

// padding classes would be like this:
pt24      padding-top: 24px;
pr24       padding-right: 24px;
// etc.
```

## Individualize
1. Install Sass (google it).
2. Run `bower install`
3. Change things in `source/` ()
4. Run `gulp` or `gulp deploy`
