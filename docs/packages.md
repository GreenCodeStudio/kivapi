# Packages

Packages are parts of project that can be reused in other websites. They are contained in `Packages` directory.

Packages are installed by git as git-submodules. It makes development easy (you can make changes in package and then
push it to git repository when working on project that uses this package) and makes you independent from some authority
that manages public repository (see [npm left-pad incident](https://en.wikipedia.org/wiki/Npm_left-pad_incident)).

## How to install existing package

### by cli

```bash
kivapi package install
```

Then enter url to git repository.

You can also list packages available
in [official repository](https://github.com/GreenCodeStudio/kivapi/blob/main/packages.xml)

```bash
kivapi package listAvailable
```

## How to create package

First, create any Kivapi project. Then inside `./Packages` directory (if this directory don't exist, create it) create
new directory with your vendor name, and inside it create directory with package name. Each package name contains vendor
name and package name, separated by slash, for example
CoreLib/Gallery.

Inside package directory make new git repository:

```bash
git init
```

Inside this directory also create `package.xml` file.

Example of `package.xml` file:

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<package>
    <vendor>CoreLib</vendor><!-- need to be equal to directory name -->
    <name>Gallery</name><!-- need to be equal to directory name -->
    <description>
        Simplest photo gallery <!-- description of package will be shown for example in panel -->
    </description>
    <git>https://github.com/GreenCodeStudio/kivapi-CoreLib-Gallery
    </git> <!-- link to repository that this package can be downloaded -->
    <version>0.1.0</version>
</package>
```

Then commit it and push to git. Your empty package is ready to be installed in other projects.

If you think that your package can be useful for others, you can make pull-request or issue
to [official repository](https://github.com/GreenCodeStudio/kivapi/blob/main/packages.xml) which is in fact xml file in
github repo. 
