# Scrroll In <img src = "https://github.com/devfolioco/scrroll-in/blob/master/images/icon-32.png?raw=true">
<p align = "center">
<img src = "https://forthebadge.com/images/badges/uses-html.svg"> <img src = "https://forthebadge.com/images/badges/uses-css.svg"> <img src = "https://forthebadge.com/images/badges/made-with-javascript.svg"> <br> <img src = "https://forthebadge.com/images/badges/built-with-love.svg">


[![All Contributors](https://img.shields.io/badge/all_contributors-11-orange.svg?style=flat-square)](#contributors)

Never forget where you left a page.

<p float="left">

<a href="https://chrome.google.com/webstore/detail/scrroll-in/cjgjbjogfodppempgdlppgefojbcmjom?hl=en&gl=IN" target="_blank">
<img src="https://developer.chrome.com/webstore/images/ChromeWebStore_Badge_v2_496x150.png" alt="Scrroll In - An extension to save scroll position of any webpage | Product Hunt Embed" style="height:64px;margin-right:20px;" height="64px" /></a>
<a href="https://www.producthunt.com/posts/scrroll-in?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-scrroll-in" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=169127&theme=light" alt="Scrroll In - An extension to save scroll position of any webpage | Product Hunt Embed" style="width: 250px; height: 54px;" width="250px" height="54px" /></a>

</p>

> Contribute to this project during hacktoberfest and get exclusive limited edition Devfolio schwag if your pull requests gets merged. [Read more](https://devfolio.co/blog/hacktoberfest-2019-devfolio/)

## Motivation 💡

You must have been in a situation wherein you are reading a long article, but you don't have enough time to finish it, so you close the tab, and the next time you open the article again, you have no idea where you left it.

So this extension lets you save the scroll position of the webpage, so you can continue from exactly where you left.

I know there are a few extensions that already serve this purpose, but most of them either didn't work correctly or lacked the features that I needed, so I ended up creating my own.

## How it works? 🤔

Under the hood, this extension uses the [chrome localStorage API](https://developer.mozilla.org/en/DOM/Storage#localStorage) to store the scroll positions for different webpages. I avoided using sync storage due to its storage limitations ([read more](https://developer.chrome.com/apps/storage)). This extension creates an object which stores the URL as keys and the scroll position as values.

The functions for adding or updating, reading and deleting are in the files `save.js`, `get.js` and `delete.js` respectively, which are executed as content scripts from `popup.js` whenever the respective button is clicked.

The `background.js` handles switching icon color whenever a tab is changed, or the URL is updated.

The popup sheet is also handled by `popup.js` by dynamically changing the UI following the availability of the URL in the localStorage object.

## Features 🚀

- You can **save** the scroll position of the page and then revisit the page at any time to continue where you left. 
- Also, extension allows you to save **multiple scrolls** from the page. 
- You can **fetch** the last saved scroll.
- If you dont want a scroll you can **delete** it.
- Extension allows you to see all the saved scrolls arranged in the newly first order where you can **delete** any specific scroll or **clear all** the scrolls at once.
- You can use **update** the scroll which will update the last saved scroll with the current one.
- You can add customizable keyboard shortcuts to **save**, **fetch** or **delete** scrolls without having to open the extension popup.
- The extension **auto fetches** the last saved scroll position on page load, if page has any saved scroll.

## Development 💻

To run the extension locally follow these steps:

- Visit `chrome://extensions` and turn on developer mode.
- Click on `Load unpacked` at the top left and select the extension root folder.
- Now you can go ahead and modify `popup.js` or `popup.html`. Changes would directly be visible in the extension.
- If you change something in `background.js` or `manifest.json` then you will need to reload the extension.

## Contributing 🌏

All you need to know for contributing to this project is basic **JavaScript**, **HTML**, and **CSS**.

You can visit the issues page to find some relevant issues to contribute to or feel free to open a new issue for something that you think can be improved.

Also, if you have any doubts regarding any of the concepts or how to get started, feel free to drop me a message on [Twitter](https://twitter.com/psuranas) or the [Devfolio community Telegram group](https://t.me/devfolio).

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://prateeksurana.me"><img src="https://avatars3.githubusercontent.com/u/21277179?v=4" width="100px;" alt="Prateek Surana"/><br /><sub><b>Prateek Surana</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=prateek3255" title="Code">💻</a> <a href="#design-prateek3255" title="Design">🎨</a> <a href="#content-prateek3255" title="Content">🖋</a> <a href="https://github.com/devfolioco/scrroll-in/commits?author=prateek3255" title="Documentation">📖</a></td>
    <td align="center"><a href="http://laylawrote.com"><img src="https://avatars3.githubusercontent.com/u/19983454?v=4" width="100px;" alt="Layla Hedges"/><br /><sub><b>Layla Hedges</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=N7Layla" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/shikharsaxena98"><img src="https://avatars1.githubusercontent.com/u/21315618?v=4" width="100px;" alt="shikharsaxena98"/><br /><sub><b>shikharsaxena98</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=shikharsaxena98" title="Code">💻</a></td>
    <td align="center"><a href="http://adityaketkar.me"><img src="https://avatars0.githubusercontent.com/u/22611315?v=4" width="100px;" alt="Aditya Ketkar"/><br /><sub><b>Aditya Ketkar</b></sub></a><br /><a href="#design-adityaketkar" title="Design">🎨</a></td>
    <td align="center"><a href="https://github.com/DEBSUBHRO"><img src="https://avatars0.githubusercontent.com/u/42496309?v=4" width="100px;" alt="DEBSUBHRA ROY"/><br /><sub><b>DEBSUBHRA ROY</b></sub></a><br /><a href="#design-DEBSUBHRO" title="Design">🎨</a></td>
    <td align="center"><a href="http://aashisresume.firebaseapp.com"><img src="https://avatars2.githubusercontent.com/u/29084675?v=4" width="100px;" alt="Aashis kumar"/><br /><sub><b>Aashis kumar</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=aesher9o1" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/RohitKaushal7"><img src="https://avatars2.githubusercontent.com/u/43717403?v=4" width="100px;" alt="Rohit Kaushal"/><br /><sub><b>Rohit Kaushal</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=RohitKaushal7" title="Code">💻</a> <a href="#design-RohitKaushal7" title="Design">🎨</a></td>
  </tr>
  <tr>
    <td align="center"><a href="http://adi.surge.sh"><img src="https://avatars1.githubusercontent.com/u/15871340?v=4" width="100px;" alt="Aditya Agarwal"/><br /><sub><b>Aditya Agarwal</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=itaditya" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/MitchMo"><img src="https://avatars2.githubusercontent.com/u/11459569?v=4" width="100px;" alt="Mitch Moore"/><br /><sub><b>Mitch Moore</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=MitchMo" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/underscoreanuj"><img src="https://avatars1.githubusercontent.com/u/30765911?v=4" width="100px;" alt="Anuj Singh"/><br /><sub><b>Anuj Singh</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=underscoreanuj" title="Code">💻</a></td>
    <td align="center"><a href="http://www.gaberosedesign.com"><img src="https://avatars3.githubusercontent.com/u/7225212?v=4" width="100px;" alt="Gabe"/><br /><sub><b>Gabe</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=roseg43" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/Alucard17"><img src="https://avatars1.githubusercontent.com/u/26205172?v=4" width="100px;" alt="alucard17"/><br /><sub><b>alucard17</b></sub></a><br /><a href="https://github.com/devfolioco/scrroll-in/commits?author=alucard17" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind are welcome!
