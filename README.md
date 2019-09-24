# Edge CSS

Intuitive margin and padding classes for quick markup styling

```html

<header class="mt12">Header has a margin-top of 12px</header>

<header class="mt12 mb6">Header has a margin-top of 12px and margin-bottom of 6px</header>
```

### Smart

Based on the Duodecimal System (aka Base 12) which is a positional system using twelve as its base. Bootstrap, One%, Skeleton and 960 Grid System are all designed using Base 12 principles. All modern displays are also based on Base 12 and are divisible by 12 or it's four divisors: 2, 3, 4, 6.

### Install

```shell
$ npm i edge-css
```

### Usage

```scss
// Import edge.css into your .scss or .less file
@import 'source/edge.css'
```
or

```html
<!-- Include the edge.css in the head of your index.html -->
<head>
    <link rel="stylesheet" href="assets/style/edge.css" />
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

```shell
m         margin
   -OR-
p         padding
```

### 2. Direction

```shell
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
<div class="mr16"></div> //  .mr16 { margin-right: 16px }
<div class="mr-16"></div> // .mr16 { margin-right: -16px }
```

### 4. Size

```shell

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


```json
{
  "source_data": {
    "items": [
      {
        "resourceType": "Patient",
        "identifier": {
          "value": "patient_abc"
        },
        "name": {
          "given": "Bob",
          "family": "Smith"
        },
        "birthDate": "1981-01-02",
        "ssn": "172-391-2020",
        "address": {
          "text": "111 FIRST ST LAS VEGAS NV 89111"
        },
        "careProvider": [
          {
            "reference": "https://hie.acme.com/practioner/123"
          }
        ]
      }
    ]
  },
  "source_metadata": {
    "items": []
  },
  "ado_data": {
    "@context": "https://ado.utm.webshield.io/json.ld",
    "type": "https://ado.utm.webshield.io/IngestADOData",
    "metadata": {
      "type": "https://ado.utm.webshield.io/IngestMetadata",
      "ado_2_source_mapping": {
        "recordID": "identifier.value"
      }
    },
    "subject": [
      {
        "id": "https://hie.acme.com/patient/abc",
        "type": "https://ado.utm.webshield.io/Person",
        "recordID": "patient_abc",
        "birthDate": "1981-01-02",
        "identifiers": {
          "type": "https://ado.utm.webshield.io/Identifiers",
          "ssn": "172-391-2020"
        },
        "names": [
          {
            "givenName": "Bob",
            "familyName": "Smith",
            "type": "https://ado.utm.webshield.io/PersonName"
          }
        ],
        "addresses": [
          {
            "fullAddress": "111 FIRST ST LAS VEGAS NV 89111",
            "type": [
              "https://ado.utm.webshield.io/PostalAddress"
            ]
          }
        ]
      }
    ],
    "credential": [
      {
        "id": "https://hie.acme.com/credentials/78282-29292",
        "type": [
          "https://ado.utm.webshield.io/Credential",
          "https://ado.utm.webshield.io/RelationshipCredential"
        ],
        "issuer": {
          "id": "https://hie.acme.com/issuer/abc_d",
          "type": "https://ado.utm.webshield.io/Person",
          "description": "person who entered the information into the system"
        },
        "recordID": "patient_abc",
        "credentialSubject": [
          {
            "id": "https://hie.acme.com/person/patient_abc",
            "type": "https://ado.utm.webshield.io/Person",
            "relationship": [
              {
                "type": [
                  "https://ado.utm.webshield.io/PatientRelationship"
                ],
                "knows": "https://hie.acme.com/practioner/practioner_123",
                "startDate": "when person became patient",
                "endDate": "when person stopped being patient"
              }
            ]
          },
          {
            "id": "https://hie.acme.com/practioner/practioner_123",
            "type": "https://ado.utm.webshield.io/Person",
            "relationship": [
              {
                "type": [
                  "https://ado.utm.webshield.io/DoctorRelationship"
                ],
                "knows": "https://ldap.pd.acme.com/person/abc_123",
                "startDate": "when person became doctor",
                "endDate": "when person stopped being doctor"
              }
            ]
          }
        ],
        "basisOfVerification": {},
        "basisOfAccountability": {}
      }
    ],
    "consent": []
  }
}
```
