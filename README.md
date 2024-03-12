# pwa-text-editor

The purpose of this project was to build a text editor that runs in the browser. The app is a single-page application that meets PWA criteria. Additionally, it features a number of data persistence techniques that serve as redundancy in case one of the options is not supported by the browser - including IndexedDb and Service Worker functionality. The application also works offline. 

The acceptance criteria were as follows:
```md
GIVEN a text editor web application
WHEN I open my application in my editor
THEN I should see a client server folder structure
WHEN I run `npm run start` from the root directory
THEN I find that my application should start up the backend and serve the client
WHEN I run the text editor application from my terminal
THEN I find that my JavaScript files have been bundled using webpack
WHEN I run my webpack plugins
THEN I find that I have a generated HTML file, service worker, and a manifest file
WHEN I use next-gen JavaScript in my application
THEN I find that the text editor still functions in the browser without errors
WHEN I open the text editor
THEN I find that IndexedDB has immediately created a database storage
WHEN I enter content and subsequently click off of the DOM window
THEN I find that the content in the text editor has been saved with IndexedDB
WHEN I reopen the text editor after closing it
THEN I find that the content in the text editor has been retrieved from our IndexedDB
WHEN I click on the Install button
THEN I download my web application as an icon on my desktop
WHEN I load my web application
THEN I should have a registered service worker using workbox
WHEN I register a service worker
THEN I should have my static assets pre cached upon loading along with subsequent pages and static assets
WHEN I deploy to Render
THEN I should have proper build scripts for a webpack application
```
This challenge utilized the node environment to create a program using dynamic Javascript. and relevant libraries to create a PWA application with persistent data. I first encountered issues when trying to add various database logic. The second issue was setting up the webpack to include everything needed to render the app. Even though I included a path to the service worker file, I continued to receive messages that it could not connect. There were also issues pointing to the right image files. I was still unable to display the header file in the html file (see index file for detail - commented text) as expected or the favicon - the other features appear to work. There were some messages in the terminal that I had trouble interpreting; for instance there was a persistent message about calling InjectManifest multiple times. I am unsure how this is the case, as it is only listed once but more work with the webpack documentation would likely prove beneficial here. I found Insomnia tremendously helpful in testing the endpoints after each code edit. Naming convention continues to be an important particular to consider when building the logic. 

Reformatting code, implementing clear naming convention, and notating often are skills that I work on continously - I hope to make them a natural part of the build process. 

## Usage

The server.js file can be used to understand the dynamic code that supports the application. Here is a link to the deployed application, for your reference: https://pwa-text-editor-f34v.onrender.com

## Credits
The project was completed with help from the course materials and tutor, Erik Hirsch.

## License

MIT License
Copyright (c) [2023] [Amber Watson]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
The application should have a db.json file on the back end that will be used to store and retrieve notes using the fs module.