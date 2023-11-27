# Chocolatey Docs


This site is built using [Statiq](https://statiq.dev/).


## Building the site

### Setup

There are a number or pre-requisites that are needed before you will be able to build the website locally.  These include:

* .NET Core SDK
* NodeJS

There is a `.\setup.ps1` file in the root of this repository that can be used to install all necessary packages, and which will be kept up to date as these change.

### Building the site

To build the site locally on your machine, either run the `.\build.ps1` or the `build.sh` file (depending on your system).  This will compile the site, and all generated output file be placed into the `output` folder.

### Previewing the site

To preview the site locally on your machine, either run the `.\preview.ps1` or the `preview.sh` file (depending on your system).  Once completed, you should be able to open a browser on your machine to `http://localhost:5080` and the site will be loaded.  Once running, any changes made to the files within the `input` folder will cause the site to be rebuilt with the new content.

### Troubleshooting the build

If you are having build errors with `'copyTheme' errored after`, try removing the `node_modules` directory and clearing your yarn cache with `yarn cache clean`.

## Adding a New Highlight

To add a new Highlight, follow the steps below:

1. Check to see if the Highlight you are writing already has a folder associated with it. This will match the current year and month that you are posting the Highlight in. If there is already a folder, copy the file from `/en-us/highlights/template/template.md` into the folder your new Highlight will go in, then skip to step #4.
1. Copy the folder `/en-us/highlights/template` and rename it to the format of "YYYY-MM". For example: "2023-04".
1. In your new folder, update the `index.md` file:
    1. Change the `PostedDateTime` to the first day of the current month. This should match the folder name. This will be the heading title that appears on the [Highlights page](xref:highlights).
    1. Remove the `IsActive: false` line completely. This is set to `true` by default, and a section will now appear for the given month on the Highlights page.
1. In your new folder, change the file name of `template.md` to match the title of the Highlight you are writing. This should be something that can easily be identified if changes will need to be made by another person later.
1. Update your new (previously `template.md`) file as needed:
    1. Remove the `IsActive: false` line completely. This is set to `true` by default, and will now be shown on the Highlights page.
    1. To make the Highlight appear on the Home page, remove the `ShowOnHome: false` line completely. This is set to `true` by default, and will now be shown on the Home page.


# docs
