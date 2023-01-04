# Vue

## Table of Contents

1. About Vue
2. Vue structure
3. Single File Components

### 1. Vue Specialities

---

The two core features of vue are declarative rendering and reactivity.

### 2. Vue folder structure

---

**public/**
Contains static assets and the main html file. The content in the main html file is dynamically rendered at runtime.

**src/**

-   main.js - Here the root component is specified and where the dom node will be injected.

-   App.vue - This is the root component

-   components/ - This folder contains all the dynamic components that are used in the application

-   assets/ - contains all the static assets like images, svgs etc.

### 3. Single File Components

---

Every vue single file component uses a custom file format ending with \*.vue.
Each file contains 3 top-level language blocks.

-   Template
    Template block defines the UI of the component and consists of HTML
-   Script
    Script block controls the logic and functionality of the application
-   Style
    Style block contains css related to the markup
