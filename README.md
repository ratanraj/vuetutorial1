Vue Js Tutorial

Day 1:

Installation
Required packages:
nodes
npm
web-pack
vue-pack
vue-cli

Installation instructions for MacOS:

Installation instructions for Ubuntu:
install node
'apt install node'
With nodejs you will have npm installed.

Install vue-pack and vue-cli after installing npm.
Vue-cli provides command line interface to the vue-pack.
Type $ vue-init <template> <project_name> to create a project.

install dependencies
Change the directory to the newly created project as follows:
$ cd <project_name>
This newly created project has a file called package.json which has a list of dependencies for this project. To install all the dependencies,  just do $ npm install.

Run project
To run this project: '$ npm run <script>'
The scripts are defined in package.json. We have dev & build.

serve with hot reload at localhost:8080
$ npm run dev

build for production with minification
$ npm run build

build for production and view the bundle analyzer report
$ npm run build --report


Tada!
You got your project up and running. 

Reference: For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


> Vue.js project

Structure of the project:
App.vue is the main vue component. 

In vuejs the project is divided into different components. 
Eg: The top navigation bar is a component. The health-check is a component, each health-check is a component. Button can be a component, a progress bar can be a component. 
The components can interact with each other through events and message.

components
The component has 3 parts: template, script, style. 
<template></template>
<script></script>
<style></style>

The template:
In the template we can provide structure for the component using HTML. We can render data to the DOM using 	mustache binding {{variable}} or v-text attribute <div v-text=”variable”></div>

Script:
In the script tag, we can define the data and behaviour of the component. If we want to use other components in our component, we can import those components here.

Style:
The style part of the component has css rules to render the component. Usually the css rules apply to the whole project, but we can limit the css rules to this component by specifying the scoped attribute in the style tag.
<script scoped></style>

Eg: Following the tutorial demo,
The input box data can be dynamically bound to a data. 
Changing input box data, variable value changes in real-time.
v-model is for form elements.
v-bind is for binding attribute.
V-bind makes the property dynamic. 

Note: Style scoped- Style applies to only this component. 














