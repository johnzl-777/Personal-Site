# Personal-Site

My personal website, built with Less, Slim and plenty of Bootstrap to go. Check out the live version [here](https://www.johnzl.com)

## Dependencies
* `lessc` - installable through `npm` 
* `slim` - Ruby gem

## Structure
The website consists of multiple pages for each section. The code and assets for each page are enclosed in an individual folder.

* `main`: landing page
* `timeline`: experience page
* `resume`: resume page
* `contact`: contact page

Folders usually have a `.less` and a `.slim` file which need to be transpiled into HTML and CSS. The exception is the `main` page as it uses pure CSS insead of Less.

* `index.slim` is supposed to be compiled into `index.html`, a redirect page that brings users to the main landing page

* `slim_compile.rb` takes a CLI argument of the name of the `.slim` file and the output needs to be piped to get a `.html` file like so:

```
ruby slim_compile.rb main.slim > main.html
```

## Local Testing
If you'd like to test the website locally, all files must be removed from their respective directories and put into one flat directory. 

Upon being in the flat directory, you can use `http-server` (installable via `npm`) in the directory and then visit the IP address and port given to you by `http-server`.
