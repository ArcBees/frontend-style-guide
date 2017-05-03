# SCSS Boilerplate

This file structure is a fork of the [7-1 architecture pattern](https://github.com/HugoGiraudel/sass-boilerplate) from [Sass Guidelines](https://sass-guidelin.es/#architecture).

## Main file

The main file should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@import` and comments.

## 01. Abstracts

The `01-abstracts/` folder gathers all Sass tools and config files used across the project. Every global variable, function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. (The grid might be the exception to this rule)

## 02. Vendors

The `02-vendors/` folder contain all the CSS files from external libraries and frameworks – Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to say “Hey, this is not from me, not my code, not my responsibility”.

You can modify the vendor file, but by doing so, you won't be able to update them later on without losing your changes. It would be wise to add your changes in another file called `_overwrites.scss`.

## 03. Base

The `03-base/` folder holds what we might call the boilerplate code for the project. In there, you might find the typographic rules, and probably a stylesheet defining some standard styles for commonly used HTML elements, like `a` or `p` tags.

There should be no classes in this folder, only styling default elements.

## 04. Layout

The `04-layout/` folder contains everything that takes part in laying out the site or application. This folder will have stylesheets for the main parts of the site: header, footer, navigation, sidebar…

## 05. Components

For elements that will be reused through the site, there is the `05-components/` folder. While `04-layout/` is macro (defining the global wireframe), `05-components/` is more focused on widgets. It contains all kind of specific modules like a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in this folder since the whole site/application should be mostly composed of tiny modules.

## 06. Pages

If you have page-specific styles, it is better to put them in the `06-pages/` folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a _home.scss file.

Every page-specific class will start with `p-`. So, if you see `p-home__box` inside the Contact page, it's a good sign that you should move this style into `05-components/_box.scss` so it can be reused.

## 07. Helpers

The `07-helpers/` folder contain files with tiny snippets of CSS that are used widely through the app without being a component. For exemple: `.is-centered` inside `_helpers.scss` will center the text. You can carefully use some `!important` here and there as these classes should win the specificity war when they are used.

## Shame file

Finally, the `_shame.scss` file should contain all the code that you know is not 100% perfect but that you don't have the time to fix. This way, you keep a clean code through your site and stack all of your fixes and hacks in only on place.

You should fix everything that's inside of this file before shipping in production.
