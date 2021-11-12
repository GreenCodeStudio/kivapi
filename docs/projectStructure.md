# Project structure
## Files
In main directory of kivapi project there are such files and subdirectories
 * Assets - containing for example images used on your webpage.
 * UploadedFiles - files uploaded by user using admin panel
 * Components - read mode in [Components](components.md)
 * Core - main files of Kivapi. Don't edit files inside this directory
 * Js - your javascript run on webpage
 * Style - scss files for your webpage
 * Packages - installed packages, read more in [Packages](packages.md)
 * Public - directory for webserver (for example Apache or IIS)
 * Tmp - temporary files. You can delete content of this directory, but keep directory itself with permisions to read and write.
 * BuildResults - js and css, that are result of [webpack](https://webpack.js.org/) compilation
 * vendor - [Composer](https://getcomposer.org/) packages
 * .env - environment configuration, such as database connection
 * config.php - project configuration

## Namespaces