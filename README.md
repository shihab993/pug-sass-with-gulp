# Pug-sass with Gulp

Use this as a simple structure for a simple start to a simple site.



## Requeriments
This project have some requeriments you need to meet in order to compile it. First of all, you need NodeJS in order to run javascript on the console, you can go to the [NodeJS](http://nodejs.rg) site and follow trough the installation process. After you get the `node` command on the console, you need to install Gulp and Bower globally with the following command.

```
node install -g gulp bower
```

Gulp is the one that will run all the compilation, watchers and others tasks. Bower will get the dependencies for the client side like jQuery. Those are the only requeriments to run this project.

## Install
In order to start using the project you need to clone it to your pc.
```
git clone https://github.com/shihab993/pug-sass-with-gulp.git project-name

```
After you have it on you pc, you need to go in the console to the project folder and execute the following command to gather all the dependencies.
```
npm install && bower install
```
After the proccess finish you will have all you need to start coding.

## How to use
To start using it, the only thing you need to do is open the project on you code editor of choice and code. To compile and live preview all your changes you have some command that will help you. Here are the list of commands you should know.

Every command have to be executed on the root directory of the project using the gulp command like `gulp clean` or `gulp build`

* **default**: Compile and watch for changes (For development)
* **clean**: Removes all the compiled files on ./build
* **js**: Compile the JavaScript files
* **pug**: Compile the Pug templates
* **sass**: Compile the Sass styles
* **images**: Copy the newer to the build folder
* **favicon**: Copy the favicon to the build folder
* **vendor-js**: compack vendor js files
* **vendor-csss**: compack vendor js files
* **build**: Build the project
* **watch**: Watch for any changes on the each section
* **help**: Print this message
* **browsersync**: Start the browsersync server

If you are in development, the `gulp` command is the best choice for you. Go to the project folder in the console and execute `gulp default`, it will compile the project and start a server that will refresh every time you change something in the code. Gulp will be watching for changes and will tell you how to access the project from local and public url. Every browser that point to that url will be auto refreshed. As an extra feature for testing purpose any interaction on one browser will be reflected on any others. Try it on a phone, tablet and pc at the same time.

## Structure
The project have a very simple and flexible structure. If the default place for any file or directory needs to be moved, be sure to update to the new position on the config file.

```
├───build -> All the compiled files will be placed here (Distribuction)
│   ├───assets -> Compiled Assets
│   ├───index.html -> Compiled Pug files
├───source -> Source files for the project
│   ├───assets -> Assets for the project
│   │   ├───img -> Images
│   │   └───js -> Scripts
│   ├───sass  -> Sass styles
│   │   └───main.sass -> Main file in where all other sass files should be included.
│   ├───vendors -> Vendors folder for all the dependencies (Managed by Bower)
│   └───views -> Templates directory for Pug files
│   │   └───index.pug
├───.bowerrc -> Define where the dependencies will be installed
├───bower.json -> Bower configuration file for manage project dependencies
├───package.json -> NodeJS configuration file for manage node dependencies
├───gulpfile.js -> Gulp Tasks
├───config.js -> Project configuration
```
All the files in the build folder will be auto-generated by the different tasks when the project compiles. Be sure to not modify any file manually in the build folder because changes will be replaced on the compile process.
