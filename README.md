# code-n-sip
Follow ONE of each step 

## Table of contents
1. [Install package manager](#tools)
2. [Serve to localhost (SKIP if you want to use a JS library)](#serve)
3. [Select a language/framework](#lang)
4. [Select a component library (optional)](#comp)
5. [Challenge: consider universal design](#uu)

## Tool for getting Tools <a name="tools"/>
These tools are meant to help download the different packages, frameworks, languages you'll need to code.
*MACOS*
Using [Homebrew (Macos package manager)](https://brew.sh/) to install what is needed via the terminal.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew search package_name // search for packages
brew install package_name
```

*WINDOWS*
Windows Package Manager winget command-line tool is bundled with Windows 11 and modern versions of Windows 10 by default as the App Installer [src](https://learn.microsoft.com/en-us/windows/package-manager/winget/#install-winget)
```
winget search package_name
```
Otherwise links to direct download sources will be given.

## Tool for showing the website on your machine <a name="serve"/>
This workshop is visual, so we need someplace to see the results of our work, our CANVAS if you will. 
These tools build the easel upon which you can put your canvas
The info here has been sourced from [devpractical.com](https://devpractical.com/host-a-html-page-on-localhost/) written by *Avic Ndugu*

### Python
Has a built-in server that can run your html files as needed
(Has an existing carpenter that can build an easel for your canvas)

Install via terminal
```

python --version // check if you have it
```
Or their [website](https://www.python.org/downloads/)
*THEN*
If you have a MAC or LINUX machine
1. open the terminal
2. navigate to this project and make a new folder called src 
```
cd ~/code-n-sip
mkdir src
cd src
```
4. run `python -m SimpleHTTPServer (optional-Port-Number-Here-Without-The-Parantheses)` and you can optionally add a port number on the same line to serve it on a spesific port
5. You will see a `Serving HTTP on 0.0.0.0 port xyz`
6. go to `localhost:xyz`

You are now ready to code

### PHP
```
php --version // check if you have it
```
1. open the terminal
2. navigate to this project and make a new folder called src
```
cd ~/code-n-sip
mkdir src
cd src
```
3. run `php -S 0.0.0.0:8000`  or `php -S localhost:8000` (you can pick which port number you want if you don't like 8000)
4. go to `localhost:8000`

Yer ready to code!

### Node
Make sre you get the [**LTS** version](https://nodejs.org/en/download/)
or via terminal: 
```
node --version // check if you have'm...
npm --version // ...or when you install, check versions

brew search node // search 
winget search node // search

// make sure you get the LTS version by selecting a version that has @

brew install node@10
winget install node@10
```
1. open the terminal
2. navigate to this project and make a new folder called src
```
cd ~/code-n-sip
mkdir src
cd src
```
3. install http-server `npm install http-server -g`
4. run `http-server`
5. visit your localhost

You're ready to code!

## Tools for writing the code <a name="lang"/>
Languages and frameworks for making the website, these tools are what will carry your proverbial paint and make an artwork upon your canvas. 

Whether you slather the paint on with your bare fingers or dare to try a palette knife is up to you.

### ONLY Html and CSS
For just straight up <html> and styling using CSS.
1. Within your `src` folder, make a file called `index.html` 
2. [Here is a simple beginner tutorial for plain html websites](https://devpractical.com/create-a-web-page-using-html/)
3. [Here's an HTML cheat sheet](https://htmlcheatsheet.com/)
4. [And CSS information](https://developer.mozilla.org/en-US/docs/Web/CSS)

### BASIC Javascript with HTML and CSS
For adding scripting to HTML and CSS to make the website more interactive and dynamic
1. Follow steps for ONLY Html and CSS
2. use this [Javascript cheat sheet](https://websitesetup.org/wp-content/uploads/2020/09/Javascript-Cheat-Sheet.pdf) and the internet to figure things out.

## JS libraries
Most if not all of these packages come with a way to run and refresh your web page, along with built in components to make building websites a quicker process.

### React
[create-react-app](https://www.npmjs.com/package/create-react-app) sets up a react project pretty quickly

*Setup*
```
npm --version // if you have over version 5.1 use npx

// if you have version under 5.1:
npm install -g create-react-app
create-react-app codesip

// else:
npx create-react-app my-app
cd my-app
npm start
```

*Run*
```
npm i //first time install, run every time you add a new package
npm run start //starts localhost
```

### Angular
[Check it out](https://www.geeksforgeeks.org/angular-cli-angular-project-setup/)
```
npm install - g @angular/cli
ng new codesip
```
### Vue
[Info here](https://cli.vuejs.org/guide/creating-a-project.html)
Follow the setup in the link, as you can choose between a new and old setup

## Svelte
[setup and tutorial docs!](https://svelte.dev/docs)
```
npm create vite@latest codesip -- --template svelte
cd codesip
npm install
npm run dev
```
## C++
Honestly I have never tried this before so good luck:
* [Article with info for setting up a project](https://learncplusplus.org/how-to-set-up-dev-c-for-your-first-project/)
* [Docs/tutorial from Microsoft](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/ms753736(v=vs.85))

## Elm
[Elm docs!](https://guide.elm-lang.org/)
```

```

### Swift (macos/ios)

### Nice to have
If you are new to this, check out [prettier](https://www.npmjs.com/package/prettier) and [eslint](https://www.npmjs.com/package/eslint) to format and check you code.
In the `package.json` file add (or check that it has) under "scripts":
```
"lint-check": "eslint --cache --ext .js,.ts,.tsx --max-warnings=0 ./src --ignore-path .gitignore",
"format": "prettier --write \"**\""
```
then you can run `npm run format` or `npm run lint` 

## Tool for pretty things <project URL#comp>
Component libraries make pretty things (icons, buttons, dropdowns, headers etc...) with some level of standardization

### AntUi
### MaterialUI
### TailwindUI

## Universal Design <a name="uu"/>
Make the webpage WCAG compliant, considering the requirements given on their website

or a TL;DR short challenge list
1. Components should have enough color and value contrast that makes it easy to distinguish them from each other
   1. if you squint while looking at your screen you should be able to tell if a thing has text on it
2. Components should be visible and make sense even when zooming in 400%
3. Navigating with a keyboard should jump to correct components
   1. tabbing around the page should lead to places that makes sense
4. any image or component that does not have a label or content should be given a label describing its function
5. images need to have a text describing their contents
6. any video you may think to put up better be translated
