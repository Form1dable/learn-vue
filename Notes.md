# Vue

## Table of Contents

1. About Vue
2. Vue structure
3. Single File Components
4. Features
    1. Data Binding
    2. Text Interpolation
    3. Text Directive
    4. HTML Directive
    5. Binding Directive
    6. Conditional Directive
    7. List rendering

## 1. Vue

The two core features of vue are declarative rendering and reactivity.

## 2. Vue folder structure

**public/**
Contains static assets and the main html file. The content in the main html file is dynamically rendered at runtime.

**src/**

-   main.js - Here the root component is specified and where the dom node will be injected.

-   App.vue - This is the root component

-   components/ - This folder contains all the dynamic components that are used in the application

-   assets/ - contains all the static assets like images, svgs etc.

## 3. Single File Components

Every vue single file component uses a custom file format ending with \*.vue.
Each file contains 3 top-level language blocks.

-   Template
    Template block defines the UI of the component and consists of HTML
-   Script
    Script block controls the logic and functionality of the application
-   Style
    Style block contains css related to the markup

## 4. Features

### 1. Data Binding

**Binding Text**
Vue has a data method that returns an object that contains all the data contained in a single component.

### 2. Text Interpolation

Data can be binded to html using double curly braces to render the selected data property.

### 3. Text Directive: v-text

Vue text directive can be used to inject text data directly into a html tag. This works similar to innerText and replaces the whole text content.

### 4. HTML Directive: v-html

HTML directive works similar to innerHTML and can be used to inject raw html inside the template. This needs to be used cautiously as code can be directly injected to an element opening opportunities for XSS attacks.

### 5. Binding Directive

Binding directive is used to bind attributes to a html element. This can also be used to dynamically bind one or more attributes to an expression. It can also be used to bind an object containing key value pair when used without an argument. When used with class or style, v-bind supports additional values such as arrays or objects.

-   v-bind:id="textInput" - Binds id to an element
-   v-bind:class="primaryButton" - Bind class
-   v-bind:src="'path/folder' + filename" - Binds source attribute with string concatenation
-   v-bind:style={red: isRed} - Binds an object instead of an argument
-   :src - Can also be used with short hand syntax
-   :[key]="value" - Short hand bind of dynamic attribute
-   :prop="someProp" - Binds prop, which must be declared in the child component

### 6. Conditional Directives: v-if="condition", v-else-if="Math.random > 0.5", v-else

Conditional rendering can be done using truthy or falsy value using v-if, v-else-if and v-else directives. This works similar to v-show but, v-show uses css display properties to manipulate the visibility of the element where conditional rendering renders or removes the entire element. For heavy changes it's better to use v-show.

### 7. List rendering: v-for: v-for="item in items :key="item.id"

List rendering can be done using the v-for directive which loops over arrays, objects, numbers, strings and iterables. List order will patch elements in place without moving them but to force re-order of elements a hint using :key attribute should be used.

-   v-for="item in items" - Iteration using alias for the index
-   v-for="(item, index) in items" - Iteration using alias and index
-   v-for="(value, key) in object" - Iterating over object getting values and keys
-   v-for="(value, key, index) in object" - Iterating over objects getting the values, keys and index
