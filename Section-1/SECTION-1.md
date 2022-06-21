# Section 1 - Setting Up a Local Development Environment (VSCode)

## Getting Started

First things first welcome to the first ever HubSpot Technical Consulting JavaScript Workshop 👋. Whether you are a JavaScript Newbie or a longtime JavaScript user this workshop has something for everyone. We decided to make this workshop self-paced as with our ever-changing schedules and customer requests it can be hard to find a time that works everyone 🙂. That said if you do find yourself struggling, have questions, or have feedback for improvements feel free to reach out to Sergio or Austin on the NAM Technical Consulting team. With that introductions done let's get into it and start by talking about Visual Studio Code (VSCode) and IDEs!

### What the heck is an IDE your title says VSCode?

That's a good question! An **IDE**, or **Integrated Development Environment**, is an application that enables developers to consolidate the different aspects of writing a computer program. IDE's increase programmer productivity by combining common activities of writing software into a single application just like HubSpot does for Marketers and Sales Reps in the CRM Space with all of our different Hubs 😏. Some of those activities include:

- Editing source code
- Building executables
- Debugging
- Etc.

**Well that's cool and all but we are not developers, so how does this help us?**

That's true! But just like developers we are always looking for ways to increase our productivity and consolidate the apps we use everyday. So let's talk about all the cool things we can get out of an IDE like VSCode (which will be the only IDE we talk about going further in this workshop).

### Syntax Highlighting

Based on the file extension (e.g. .json, .html, .js, etc.) of the file you are editing in VSCode (either natively or through an extension) knows the syntax of the file's language and can provide visual cues. Keywords are words that have special meaning like **class** in JavaScript and get highlighted in different color:

```
// Without syntax highlighting  
class Rectangle {  
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
}
```

```javascript
// With syntax highlighting
class Rectangle {
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
}
```

### Autocomplete

When VSCode knows your programming language, it can anticipate what you're going to type next!  

![Gif of VSCode Autocomplete](https://code.visualstudio.com/assets/docs/editor/intellisense/intellisense.gif)

### Debugging

Everyone makes mistakes 🤷  but how do know when we do And how do we fix them? Well VSCode has lots of debugging and even parses your code for error before it even runs.

![Gif of VSCode Error Parsing](https://code.visualstudio.com/assets/docs/nodejs/extensions/eslint.gif)

### Okay you sold me! Now how do I set this up?

## Setting Up VSCode Efficiently

Well the first step is to download VSCode onto your machine (don't worry it works on both Macs 🍎 and Windows 🪟, and Linux if you somehow have that on your work computer 🤷). You can download VSCode for your corresponding OS from this link [here](https://code.visualstudio.com/download).

Once your done with that you are pretty much ready to go for most of your daily use cases. But since we are Technical Consultants and always looking for the fastest and easiest way of doing things lets now customize some of the settings in VSCode to really increase our productivity.

### 'settings.json'

In VSCode all of your settings both native and extension specific (don't worry we will talk about extensions soon) live in the settings.js file. This file is located in the root of your VSCode installation folder. You can also access it by using the **Command Palette** which you can access on Mac by using `Shift` + `⌘` + `p` and on Windows by using `Ctrl` + `Shift` + `p` and then typing in 'open settings' + `Enter`.

![Image of VSCode settings.json](https://code.visualstudio.com/assets/docs/getstarted/settings/lang-based-settings.png)

If you are not familiar with JSON, this can look pretty intimidating. But the good news is that you can also use the settings GUI to set the settings for both native and extension specific settings. You can access the settings GUI by clicking on the gear icon on the bottom right of the VSCode window.

### Recommended Settings

Now that we know how to get to the VSCode settings we can start adding some settings to help with our productivity and make it even easier to use VSCode.

#### Files

Files: Auto Save: onFocusChange - In my VSCode environment I have my setting Auto Save set to onFocusChange. This means that every time I switch tabs or move focus to another window VSCode will save my files. This is super helpful when working on multiple files at once (or if you are easily distracted by client emails and forget to save your work...repeatedly 😬)

#### Editor

Editor: Bracket Pair Colorizer: Enabled - This is a great feature that used to need an extension to work but is now supported natively in VSCode. It will highlight matching brackets when you are typing. This can be super helpful when you are trying to troubleshoot deeply nested JSON objects and ensure they are all closed properly.

Editor: Format On Paste: Enabled - One of my biggest gripes with the CMS Hub Editor is the lack of formatting tools and is such a pain to manually format big files. With VSCode we have access to extension like Prettier that we can set as out default formatter for our files. Then with this setting every time I paste something in my editor Prettier will automatically format it for me.

Editor: Format On Save: Enabled - This pretty similar to that first recommended setting where on saving of a file it will format my files. This is just nice because it saves you from having to go back and fix any messy code you created while writing your code.

Editor: Inline Suggest: Enabled - I actually thought this was enabled by default but according to my VSCode environment I modified it but I would recommend enabling it to ensure you get inline suggestions on your code.

Editor: Auto Close Bracket

#### JavaScript

JavaScript: Update Import On File Move: Enabled - Personally I hate having to go back and update file import paths when I move files around in a project. This setting automatically sets the paths for you when you move a file instead of you having to have to go redo all of your imports.

### Extensions/Themes

We all like a little customization from time to time. So let's dive into extensions and themes and see how they can make our time with VSCode even more enjoyable and productive.

#### Themes

Lets start with themes in VSCode since they are not a necessity for maximizing VSCode but can help make things more visually appealing and sometimes easier to read. To install a theme you can open up the extensions page by clicking the extensions icon in the left sidebar (or by using `Shift` + `⌘` + `x` on Mac and `Ctrl` + `Shift` + `x` on Windows) and then searching themes in search box.
My personal goto theme is [SynthWave '84 by Robb Owen](https://marketplace.visualstudio.com/items?itemName=RobbOwen.synthwave-vscode) because I like the colors it uses plus the fact that you can make the background of text glow. But feel free to find a theme that works for you. In addition to the changing VSCode color scheme you can also change the icons that are used in the VSCode window. My go to icon theme is the [Material Icons pack by Philipp Kief](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme) but if this doesn't work for you just like the SynthWave theme you can find a icon pack/theme that works for you or even better [make your own](https://docs.microsoft.com/en-us/shows/vs-code-livestreams/build-your-own-vs-code-theme)! 😎

#### Extensions

Okay so we now have our VSCode environment looking good but what about productivity? Well lets start by talking about how do we add an extension to VSCode. To install an extension it is the exact same as installing a theme or an icon pack. You find an extension by searching in the extensions page, click into the extension and then click the install button. Super easy right? Once you have installed the extension it will immediately start working but if you want uninstall it you can do so by going back to the extension's page in VSCode and clicking the uninstall button and if the extension supports extra settings you can find them in your VSCode settings.

###### Recommended Extensions

Here is a list of some of my goto extensions in VSCode and brief descriptions of what they do:

[:emojisense:](https://marketplace.visualstudio.com/items?itemName=bierner.emojisense) by Matt Bierner - I found adding emojis to documents such as this can be a pain with Apple's emoji keyboard but with this extension all I have to do is either add a : and then start typing the name of the emoji to add one or hit `⌘` + `i` and then select the emoji I want from the picker 🚀

![Gif of Emojisense](https://raw.githubusercontent.com/mattbierner/vscode-emojisense/master/media/example.gif)

[Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag) by Jun Han - This extension will automatically close tags when you type a closing tag.

![Gif of Auto Close Tag](https://github.com/formulahendry/vscode-auto-close-tag/raw/HEAD/images/usage.gif)

[Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) by Jun Han - This extension will automatically renames paired HTML/XML tag.

![Gif of Auto Rename Tag](https://github.com/formulahendry/vscode-auto-rename-tag/raw/HEAD/images/usage.gif)

[Babel JavaScript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel) by Michael McDermott - This extension will allow you to get syntax highlighting for JavaScript, TypeScript, Flow, and GraphQL.

![Image of Babel JavaScript Extension Highlighting](https://raw.githubusercontent.com/mgmcdermott/vscode-language-babel/master/images/screenshot.png)

[change-case](https://marketplace.visualstudio.com/items?itemName=wmaurer.chang) by wmaurer - This extension will allow you to change the case of selected text. You can change the case of the selected text to camel, constant, dot, kebab, lower, lowerFirst, no (lower case, space separated), param (lower case, dash separated), pascal (same as camel but first letter also capitalized), path (lower case, slash separated), sentence (lower case, space separated), snake (lower case, underscore separated), swap (convert to string and reverse each letter to opposite), title, upper, upperFirst. To use open the command palette (`Shift` + `⌘` + `p`) type Change Case and then the name of the case you want to use.

![Gif of Change Case](https://cloud.githubusercontent.com/assets/2899448/10712456/3c5e29b6-7a9c-11e5-9ce4-7eb944889696.gif)

[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) by StreetSide Software - If you are terrible speller (like myself 😬) this extension helps by spell checking your code as you type.

![Gif of Code Spell Checker](https://raw.githubusercontent.com/streetsidesoftware/vscode-spell-checker/main/images/example.gif)

[CSS Peek](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek) by Pranay Prakash - This extension will allow you to see the CSS properties of the selected element in the editor.

![Gif of CSS Peek](https://github.com/pranaygp/vscode-css-peek/raw/master/readme/working.gif)

Additionally it supports Symbol Provider so you can quickly jump to the right CSS/SCSS/LESS code if you already know the class or id name.

![Gif of CSS Peek jumping to code](https://github.com/pranaygp/vscode-css-peek/raw/master/readme/symbolProvider.gif)

[GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) by GitHub - This extension is one of the most impressive things I have ever seen in my years of software development. It is a personal AI pair programmer which suggests line completions and entire function bodies as you type. You can even type a comment of a function or line of code you want to write and Copilot will suggest the rest. IT IS WILD.. and terrifying... and very sky netty 😱. You can get access by first joining the waitlist [here](https://github.com/features/copilot/signup) (you'll also need a GitHub account). Once approved you can then install the extension sign in to your GitHub account on VSCode and start using it and be amazed.

![Gif of GitHub Copilot](https://miro.medium.com/max/1400/1*XyCPuRbbpfWnqI6I4GTVZQ.gif)

[HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css) by ecmel - This extension gives you HTML id and class attribute completion in VSCode.

[HubSpot VS Code Extension](https://marketplace.visualstudio.com/items?itemName=hubspot.hubl) by HubSpot - This extension introduces new file languages: `HTML` + `HUBL` and `HTML` + `CSS`. In order to use these new features, you'll want to make sure you've told VSCode to use these languages. For one-off files, you can simply change the language in the lower right hand corner of your screen. However, we recommend adjusting your file associations under your User or Workspace preferences so HubL syntax highlighting will automatically be applied to all of your projects:

- In VSCode, press `⌘` + `Shift` + `p` to open the command prompt
- Search for and select the command Preferences: Open Settings (UI)
- Choose either the "User" or "Workspace" tab
- In "Search settings" look up **files.associations**
- Select "Add Item" and add these file associations: `*.html: html-hubl` and `*.css: css-hubl`

[IntelliCode API Usage Examples](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.intellicode-api-usage-examples) by Microsoft - Ever wish you could easily access code examples for APIs you work with? IntelliCode API Usage Examples makes that a reality. Now with just one click you can access examples for over 100K different APIs!

![Gif of IntelliCode API Usage Examples](https://aka.ms/IntelliCodeUsageExamplesv2)

[IntelliSense for CSS class names in HTML](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion) by Zignd -  This extension provides CSS class name completion for HTML class attributes based on the definitions found in your workspace or external files referenced through the link element.

![Gif of IntelliSense for CSS class names in HTML](https://i.imgur.com/5crMfTj.gif)

[JavaScript (ES6) code snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets) by charalampos karypidis - This extension contains code snippets for JavaScript in ES6 syntax (also support TypeScript).

Import and Export Snippets

|Trigger|Content|
|--- |--- |
|imp→|imports entire module `import fs from 'fs';`|
|imn→|imports entire module without module name `import 'animate.css'`|
|imd→|imports only a portion of the module using destructing `import {rename} from 'fs'`;|
|ime→|imports everything as alias from the module `import * as localAlias from 'fs';`|
|ima→|imports only a portion of the module as alias `import { rename as localRename } from 'fs';`|
|rqr→|require package `require('');`|
|req→|require package to const `const packageName = require('packageName');`|
|mde→|default module.exports `module.exports = {};`|
|env→|exports name variable `export const nameVariable = localVariable;`|
|enf→|exports name function `export const log = (parameter) => { console.log(parameter);};`|
|edf→|exports default function `export default function fileName (parameter){ console.log(parameter);};`|
|ecl→|exports default class `export default class Calculator { };`|
|ece→|exports default class by extending a base one `export default class Calculator extends BaseClass { };`|

Class Helpers

|Trigger|Content|
|--- |--- |
|con→|adds default constructor in the class `constructor() { }`|
|met→|creates a method inside a class `add() { }`|
|pge→|creates a getter property `get propertyName() {return value;}`|
|pse→|creates a setter property `set propertyName(value) { }`|

Various Methods

|Trigger|Content|
|--- |--- |
|fre→|forEach loop in ES6 syntax `array.forEach(currentItem => { })`|
|fof→|for ... of loop `for(const item of object) { }`|
|fin→|for ... in loop `for(const item in object) { }`|
|anfn→|creates an anonymous function `(params) => { }`|
|nfn→|creates a named function `const add = (params) => { }`|
|dob→|destructing object syntax `const { rename } = fs`|
|dar→|destructing array syntax `const [first, second] = [1, 2]`|
|sti→|set interval helper method `setInterval(() => { });`|
|sto→|set timeout helper method `setTimeout(() => { });`|
|prom→|creates a new Promise `return new Promise((resolve, reject) => { });`|
|thenc→|adds then and catch declaration to a promise `.then((res) => { }).catch((err) => { });`|

Console Methods

|Trigger|Content|
|--- |--- |
|cas→|console alert method `console.assert(expression, object)`|
|ccl→|console clear `console.clear()`|
|cco→|console count `console.count(label)`|
|cdb→|console debug `console.debug(object)`|
|cdi→|console dir `console.dir`|
|cer→|console error `console.error(object)`|
|cgr→|console group `console.group(label)`|
|cge→|console groupEnd `console.groupEnd()`|
|clg→|console log `console.log(object)`|
|clo→|console log object with name `console.log('object :>> ', object);`|
|ctr→|console trace `console.trace(object)`|
|cwa→|console warn `console.warn`|
|cin→|console info `console.info`|
|clt→|console table `console.table`|
|cti→|console time `console.time`|
|cte→|console timeEnd `console.timeEnd`|

[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) by Ritwick Dey - This extension allows you to be able launch a local development server with live reload feature for static & dynamic pages.

![Gif of Live Server](https://github.com/ritwickdey/vscode-live-server/raw/HEAD/images/Screenshot/vscode-live-server-animated-demo.gif)

[npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script) by Microsoft - This extension supports running npm scripts defined in the package.json file and validating the installed modules against the dependencies defined in the package.json.

Notice The validation is done by running npm and it is not run when the modules are managed by yarn.

The package.json validation reports warnings for modules:

- that are defined in the package.json, but that are not installed
- that are installed but not defined in the package.json
- that are installed but do not satisfy the version defined in the package json.

![Image of npm extension](https://github.com/Microsoft/vscode-npm-scripts/raw/HEAD/images/validation.png)

[npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense) by Christian Kohler - This extension auto-completes npm modules in import statements.

![Gif of npm Intellisense](https://github.com/ChristianKohler/NpmIntellisense/raw/HEAD/images/auto_complete.gif)

[Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) by Christian Kohler - This extension auto-completes paths/filenames.

![Gif of Path Intellisense](https://i.giphy.com/iaHeUiDeTUZuo.gif)

[Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) by Prettier - This extension is an opinionated code formatter. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.

[Rewrap](https://marketplace.visualstudio.com/items?itemName=stkb.rewrap) by stkb - This extension re-wraps comment blocks in many languages, with per-language settings.

![Img of Rewrap](https://stkb.github.io/Rewrap/images/example1.png)

[Turbo Console Log](https://marketplace.visualstudio.com/items?itemName=ChakrounAnas.turbo-console-log) by ChakrounAnas - This extension make debugging much easier by automating the operation of writing meaningful log message.

![Gif of Turbo Console log](https://image.ibb.co/dysw7p/insert_log_message.gif)

### VSCode Shortcuts

#### Open the command palette to quickly search for a & access a file

Mac: `Shift` + `⌘` + `P` or `⌘` + `P`

Windows/Linux: `CTRL` + `P`

Navigating through files is one of the most common options and this command can come in pretty handy. You can type the name of the file in the search box and select the file by clicking or by pressing enter on the search result to open the file

![Gif of Command Palette being open](https://miro.medium.com/max/700/1*0iRL1nLPdak_CH1Vplk1OQ.gif)

#### Add cursors to all matching selections

Mac: `⌘`  + `SHIFT` + `L`
Windows/Linux: `CTRL` + `SHIFT` + `L`

One of my favorite features of VS Code is multi cursors. They allow you to replace text or append more text without copy-pasting or requiring you to change it one at a time.

Using this command, you can add cursors to all matching selections in the document.

![Gif of all selection shortcut](https://miro.medium.com/max/700/1*EMEAQBiLin4rtwlGmFdqaw.gif)

#### Add cursor to next matching selection

Mac: `⌘` + `D`
Windows/Linux: `CTRL` + `D`

Like the above command, this is also used to add cursors but with this, you can add the cursor to the next matching selection. This is especially helpful when you don’t want to select all occurrences together

![Gif of next matching selection](https://miro.medium.com/max/700/1*mPKmQihPEPditYIjM9HODA.gif)

#### Undo last cursor operation

Mac: `⌘` + `U`

Windows/Linux: `CTRL` + `U`

If you need to undo cursor selection in a case where you selected more cursors than required or reset the cursor to a previous position, you can use this command to undo the last cursor action

![Gif of undo cursor operation](https://miro.medium.com/max/700/1*LHhKt1cE8Ogou2cGp1rKMA.gif)

#### Select current line

Mac: `⌘` + `L`
Windows/Linux: `CTRL` + `L`

Often we use mouse drag to select the text, but if we want to select entire lines, we can use this command

![Gif of select current line](https://miro.medium.com/max/700/1*of0o1lDWN4VZ63qVMOy_KA.gif)

#### Go to a specific line

Mac: `CTRL` + `G`

Windows/Linux: `CTRL` + `G`

We can navigate to a specific line of the document by using this simple command and typing the line number.

This is especially helpful in situations when error stack traces provide us the line number of the file and our file is large.

#### Close all open editor tabs

Mac: `⌘` + `K` + `W`

Windows/Linux: `CTRL` + `K` + `W`

This command is useful when we want to clear all tabs.

Often while debugging or developing, I have opened many tabs and when I want to change the context or start fresh, this command comes in very handy

![Gif of closing all open editors](https://miro.medium.com/max/700/1*cJrwBOvbU7WtBy5bcIy_Xw.gif)

#### Toggle block comment

Mac: `SHIFT` + `OPTION` + `A`

Windows: `SHIFT` + `ALT` + `A`, Linux: `CTRL` + `SHIFT` + `A`

This shortcut also allows us to add a new block comment or toggle existing ones.

We enclose a piece of Javascript code with /**/ to add a block comment. However, with this shortcut, we can add or remove a block comment for the selected code block or add new ones.

Line comments can be toggled with `⌘` + `/` (Windows/Linux: `CTRL` + `/`)

![Gif of toggle block comment](https://miro.medium.com/max/700/1*J_gxNfNsQBtfNMpXBVyJbA.gif)

#### Fold code block

Mac: `⌘` + `OPTION` + `[`

Windows/Linux: `CTRL` + `SHIFT` + `[`

This command is especially useful when we want to focus on a specific area of the code and hence ignore some code blocks. This folds the block closest to the cursor.

You can unfold the code block with `⌘` + `OPTION` + `]` (or Windows/Linux: `CTRL` + `SHIFT` + `]`)

![Gif of code folding block](https://miro.medium.com/max/700/1*CgrDhbxLKSjMityu17W5bQ.gif)

#### Move line up or down

Mac: `OPTION` + `UP/DOWN`

Windows/Linux: `ALT` + `UP/DOWN`

When you want to move a piece of code, for example, a variable declaration either up or down, you cut and paste it to the appropriate place but if the readjustment is for a few lines you can use this command to move the current line/selection up or down

![Gif of moving line up or down](https://miro.medium.com/max/700/1*STSU_D-qFPJtcgpAzZFL8w.gif)

#### Open integrated terminal

Mac: `CTRL` + `

Windows/Linux: `CTRL` + `

One of the most amazing features of VS Code is that it supports an integrated terminal which you can use just like a normal terminal and to run code or perform other operations. This command helps you open the terminal when you need it

![Gif of integrated terminal](https://miro.medium.com/max/700/1*H9Bx-xLT1uY0yEqp368WJw.gif)

#### Split editor view

Mac: `⌘` + `\`

Windows/Linux: `CTRL` + `\`

You can split your editor view to open multiple files together.

This is especially helpful when you want to refer to content from a file while coding in another.

![Gif of split editor view](https://miro.medium.com/max/700/1*ZFCPT3YqPY8Bzs5jyDuPIA.gif)

#### Format document

Mac: `SHIFT` + `OPTION` + `F`

Windows: `SHIFT` + `ALT` + `F`, Linux: `CTRL` + `SHIFT` + `I`

Often we have extensions enabled or settings configured to format documents on save but sometimes we like to control when we want to format the document. This is where this command comes in.

It allows us to format the current document according to the configured settings.

![Gif of formatting document](https://miro.medium.com/max/700/1*DOsTljYKIn9taSjsYwyDlQ.gif)

#### Duplicate selection up or down

Mac: `OPTION` + `SHIFT` + `UP / DOWN`

Windows/Linux: `SHIFT` + `ALT` + `UP/DOWN`

Using this command you can duplicate the selected code either above or below the current code.

I love to use this when some functions are almost identical except for some small changes which I make after duplicating the previous implementation

![Gif of duplicating selection](https://miro.medium.com/max/700/1*domXxhy17wJSOvoxGhvWBg.gif)

#### Toggle Sidebar

Mac: `⌘` + `B`

Windows/Linux: `CTRL` + `B`

You can use this command to toggle the sidebar to make more space for your file view as and when needed.

![Gif of toggling sidebar](https://miro.medium.com/max/700/1*jA102Uf8gfgpfqF_VQfR-A.gif)
