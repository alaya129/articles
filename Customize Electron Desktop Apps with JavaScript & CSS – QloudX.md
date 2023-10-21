# Customize Electron Desktop Apps with JavaScript & CSS – QloudX
[Customize Electron Desktop Apps with JavaScript & CSS – QloudX](https://www.qloudx.com/customize-electron-desktop-apps-with-javascript-css/) 

 ![](https://www.qloudx.com/wp-content/uploads/2023/09/Blog-81-splash-neural-.jpg)

## Table of Contents

-   [Introduction](#introduction)
-   [Electron](#electron)
-   [Source Code](#source-code)
-   [Customizing CSS/JS](#customizing-cssjs)
-   [App Updates](#app-updates)
-   [Conclusion](#conclusion)
-   [About the Author ✍🏻](#about-the-author-%25e2%259c%258d%25f0%259f%258f%25bb)

## Introduction

Browser extensions like [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?utm_source=ext_sidebar&hl=en-US) & [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?utm_source=ext_sidebar&hl=en-US) let you style any webpage with custom CSS & run custom JavaScript code on any website respectively. Unfortunately, such customizability is not available in desktop apps, unless they’re made with Electron. Electron desktops apps are built using HTML, CSS & Javascript, so if you can get to their source code, you can customize them as you like.

## Electron

[Electron](https://www.electronjs.org/) is a free & open-source software framework that allows you to create desktop applications using web technologies like HTML, CSS & JavaScript. It does this by embedding the Chromium web browser & the Node.js runtime environment into a single executable file. This means that you can write your entire application in JavaScript & it will work on Windows, macOS & Linux without any changes.

Electron is a popular choice for building desktop applications because it is:

-   Cross-platform: Electron apps can be built once & deployed to all major platforms.
-   Easy to learn: If you know JavaScript, you can learn Electron quickly.
-   Extensible: Electron apps can be extended with native code using Node.js modules.

Desktop versions of many popular apps like VS Code, GitHub, WhatsApp, Slack, Spotify, WordPress, Skype, Discord, etc are built using Electron.

## Source Code

To find an Electron app’s source code, go to its install location & look for a file called `app.asar`. Consider [Lens](https://k8slens.dev/) for example, a Kubernetes IDE. In macOS, its `app.asar` is located in `/Applications/Lens.app/Contents/Resources`. In Windows, it should be in its install directory under `C:\Program Files`. Since apps in Linux can be installed in various locations, it’s best to search for it using `find / -name app.asar`.

`app.asar` is a compressed archive of the app’s source code & other project assets. When you launch an Electron app, it’ll look for `app.asar` & use the code inside it. If `app.asar` is not found, it’ll look for the equivalent uncompressed `app` directory, expected to contain the same contents as `app.asar`.

To start customizing the app’s CSS/JS, first uncompress `app.asar`:

    npm install -g asar
    asar extract app.asar app
    mv app.asar original-app.asar

Since we renamed `app.asar` above, the app will now use the `app` directory instead.

However, if after customizing files in the `app` directory as described below, you notice your app is misbehaving in certain cases, try repacking the `asar` with your modifications:

    asar pack app app.asar

## Customizing CSS/JS

Steps beyond this point depend on the app that you’re customizing. Look for HTML/CSS/JS files in the `app` directory & change them as needed. In case of Lens for example, it has a main page at `/Applications/Lens.app/Contents/Resources/app/static/build/index.html`, which I customized to include my own CSS & JavaScript code (lines 12 & 13 below):

```


/Applications/Lens.app/Contents/Resources/app/static/build/index.html

`<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <script defer="defer" src="/build/runtime.js"></script>
    <script defer="defer" src="/build/lens.js"></script>
    <link href="/build/lens.css" rel="stylesheet" />
  </head>
  <body>
    <div id="app"></div>
    <div id="terminal-init"></div>
    <link href="custom.css" rel="stylesheet" />
    <script src="custom.js"></script>
  </body>
</html>`
```

`custom.css` & `custom.js` can contain any CSS/JS code you want. In this case for example, I used some CSS to bolden fonts & remove hyperlink underlines & some JavaScript to fit table cells to their content.

## App Updates

You can also modify any of the app’s existing CSS/JS instead of adding your own, like `lens.css` & `lens.js` above. But when the app updates, your changes will be lost. So it’s best to keep your customizations in separate files like `custom.css` & `custom.js` above & keep a copy of these files outside the app. So when the app updates, you only need to add 2 lines to `index.html` & copy over your custom files inside the app again.

## Conclusion

This blog post described how you can change the look & behavior of any Electron-based desktop app by first, getting access to its source code & then customizing it as you see fit. This brings the flexibility of the web to desktop apps & is very useful if your favorite Electron app doesn’t quite work as you want.
