# videojs-record

# Kira specific information -- PLEASE keep up to date

### Changes made

This is a fork of the `videojs-record` library where we needed to make a couple of changes

- Allow the library to take in and pass along the video bitrate to record in
  - Allows us to use whatever bitrate we want to better control video sizes generated
  - Uses the Kira version of [RecordRTC](https://github.com/kira/RecordRTC) (see `package.json`)
  - See
    - [CORE-1839](https://kiratalent.atlassian.net/browse/CORE-1839)
    - [Diff](https://github.com/kira/videojs-record/pull/2)
- Allow us to pass in custom file locations for the ffmpeg-wasm library files
  - Allows us to more easily serve the files from the same domain
  - See
    - [CORE-1836](https://kiratalent.atlassian.net/browse/CORE-1836)
    - [Diff](https://github.com/kira/videojs-record/pull/3)

### Making Changes

- Clone the repository
- Node 20 is required to run the project
  - `nvm install 20 && nvm use 20`
- Install the dependencies
  - `npm ci`

### Testing the changes in Nectar
- Make your changes
- Run the build
  - `npm run build`
- Copy and overwrite all the files from the `dist` folder to `<nectar_home>/node_modules/@kira/videojs-record/dist/`
- Restart the React dev server

### Cutting a new release

- Merge your pull request
- From your local machine, run the following on a new branch created from `main`
```shell
$ npm version patch
$ git push 
$ git push --tags
```
- Create a new PR with the changes
- Merge your PR
- Run the `Build and Publish Package` Github action
- Update the releases page on Github
- You can now reference the release number created in other projects with `@kira/videojs-record` and the version number
  - ex: `yarn add \@kira/videojs-record@4.8.2`


# Original README

A [video.js](https://www.videojs.com/) plugin for recording audio/video/image files.

![Screenshot](https://raw.githubusercontent.com/collab-project/videojs-record/master/docs/img/screenshot.png?raw=true "Screenshot")

## Documentation

The documentation and examples can be found on: https://collab-project.github.io/videojs-record

[![npm version](https://img.shields.io/npm/v/videojs-record.svg?style=flat)](https://www.npmjs.com/package/videojs-record)
[![npm](https://img.shields.io/npm/dm/videojs-record.svg)](https://github.com/collab-project/videojs-record/releases)
[![License](https://img.shields.io/npm/l/videojs-record.svg)](LICENSE)
[![Build Status](https://github.com/collab-project/videojs-record/workflows/videojs-record/badge.svg?branch=master)](https://github.com/collab-project/videojs-record/actions?workflow=videojs-record)
[![Coverage Status](https://coveralls.io/repos/github/collab-project/videojs-record/badge.svg?branch=master)](https://coveralls.io/github/collab-project/videojs-record?branch=master)
![Size](https://img.shields.io/bundlephobia/minzip/videojs-record.svg?style=flat)
[![Financial Contributors on Open Collective](https://opencollective.com/collab/all/badge.svg?label=financial+contributors)](https://opencollective.com/collab)
![Stars](https://img.shields.io/github/stars/collab-project/videojs-record.svg?style=social)

Donate
------

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/collab/contribute)]

#### Individuals

<a href="https://opencollective.com/collab"><img src="https://opencollective.com/collab/individuals.svg?width=890"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website. [[Contribute](https://opencollective.com/collab/contribute)]

<a href="https://opencollective.com/collab/organization/0/website"><img src="https://opencollective.com/collab/organization/0/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/1/website"><img src="https://opencollective.com/collab/organization/1/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/2/website"><img src="https://opencollective.com/collab/organization/2/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/3/website"><img src="https://opencollective.com/collab/organization/3/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/4/website"><img src="https://opencollective.com/collab/organization/4/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/5/website"><img src="https://opencollective.com/collab/organization/5/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/6/website"><img src="https://opencollective.com/collab/organization/6/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/7/website"><img src="https://opencollective.com/collab/organization/7/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/8/website"><img src="https://opencollective.com/collab/organization/8/avatar.svg"></a>
<a href="https://opencollective.com/collab/organization/9/website"><img src="https://opencollective.com/collab/organization/9/avatar.svg"></a>
