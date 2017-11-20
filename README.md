![leasot-to-readme](media/leasot-to-readme.png)

# leasot-to-readme
Parse and output TODOs and FIXMEs directly into your root README.md with each build.

[![NPM Version](http://img.shields.io/npm/v/leasot-to-readme.svg?style=flat)](https://npmjs.org/package/leasot-to-readme)
[![NPM Downloads](http://img.shields.io/npm/dm/leasot-to-readme.svg?style=flat)](https://npmjs.org/package/leasot-to-readme)
[![Build Status](http://img.shields.io/travis/frewinchristopher/leasot-to-readme.svg?style=flat)](https://travis-ci.org/frewinchristopher/leasot-to-readme)

## Usage
First install leasot-to-readme globally:
`npm install -g leasot-to-readme`

To install with default settings for a given project, run at the root of any valid npm project:

`leasot-to-readme default`

This will append the TODOs and FIXMEs to the bottom of README.md. Note that the TODOs and FIXMEs will not be appended to the project's README.md until the `start` command is run.

Alternatively, run leasot-to-readme at anytime with:

`leasot-to-readme run`

## Other Options
`--build-command`, `-b`: Provide one or more build commands to hook into `leasot-to-readme`. Default is `npm start`
`--output-file`, `-o` Provide the output file to append the TODO/FIXME summary to. Default is `README.md`. If a `README.md` does not exist, one will be generated
`--title-file`, `-t` Provide the path name to the title file. Default is '' i.e. no title file.

## Template Files
Template files can be any valid .md file that can be used to create a custom title/header before the TODOs and FIXMEs are listed. Providing a title file will eliminate the `# TODOs and FIXMEs generated by leasot-to-readme` default title, for example a title file my-super-cool-title-file.md could contain:

`# :rocket: Awesome StUfF still on the todo/fix list!!! :rocket:`

To use this as your title instead of the default title, you would issue

`leasot-to-readme -t my-super-cool-title-file.md`