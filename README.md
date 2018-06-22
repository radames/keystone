---
title: KeystoneJS
---

![KeystoneJS](http://keystonejs.com/images/logo.svg)
===================================

[![Build Status](https://travis-ci.org/keystonejs/keystone.svg?branch=master)](https://travis-ci.org/keystonejs/keystone)

[KeystoneJS](http://keystonejs.com) is a powerful Node.js content management system and web app framework built on the [Express](https://expressjs.com/) web framework and [Mongoose ODM](http://mongoosejs.com). Keystone makes it easy to create sophisticated web sites and apps, and comes with a beautiful auto-generated Admin UI.

For Keystone v4 documentation and guides, see [keystonejs.netlify.com](http://keystonejs.netlify.com).

For Keystone v0.3 documentation, see [keystonejs.com](http://keystonejs.com).

You can also deploy a starter project to [Heroku](https://www.heroku.com/) for free to try it out:

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/JedWatson/keystone-starter)

## Keystone 4.0.0 Release Candidate (RC)

We've been working on a major update to KeystoneJS. Keystone 4 is a complete rebuild of Keystone's Admin UI and internal architecture.

Improvements include:

* The Admin UI has been re-written as a single page app using React.js, Redux and Elemental UI
* An updated API for Lists and Fields
* Better support for using Keystone without Express, or with your own express instance
* Core functionality has been refactored and we're breaking Keystone up into separate npm packages
* Startup time has been significantly reduced
* LocalFile, S3File, and AzureFile have been replaced by a new generic `keystone.Storage` engine and File field
* We have much higher unit and end-to-end test coverage

Please try out Keystone 4 and let us know what you think:

```
npm install --save keystone
```

We'll be publishing a summary of the new features, changes and improvements as we get closer to the final release. In the meantime, see the [v0.3 -> v4.0 Upgrade Guide](http://keystonejs.netlify.com/guides/v-0-3-to-v-4-0-upgrade-guide) for information on what's changed.

Also check out our [demo site](http://demo.keystonejs.com), which has been updated to the new version!

## About

Keystone gives you:
 * A simple way to create a dynamic web site or app with well-structured routes, templates, and models
 * A beautiful Admin UI based on the database models you define
 * Enhanced `models` with additional field types and functionality, building on those natively supported by Mongoose
 * Out of the box session management and authentication
 * An updates framework for managing data updates or initialisation
 * Integration with Cloudinary for image uploading, storage and resizing
 * Integration with Mandrill for sending emails easily
 * Integration with Google Places for clever location fields
 * Integration with Embedly for powerful video and rich media embedding tools

... plus a lot of other tools and utilities to make creating complex web apps easier.

Use our [Yeoman Generator](https://github.com/keystonejs/generator-keystone) to get up and running with KeystoneJS quickly, then check out our getting started guide &amp; docs at [keystonejs.com/docs/getting-started](http://keystonejs.netlify.com/getting-started).

We have a demo website at [demo.keystonejs.com](http://demo.keystonejs.com/) where you can play with the Keystone Admin UI, and you can [read the source](https://github.com/keystonejs/keystone-demo) to see how it was built.

### Community

We have a friendly, growing community and welcome everyone to get involved.

Here are some ways:

* Follow [@KeystoneJS](https://twitter.com/KeystoneJS) on twitter for news and announcements.
* Ask technical questions on [Stack Overflow](http://stackoverflow.com/questions/tagged/keystone.js) and tag them `keystonejs.`
* Report bugs and feature suggestions on our GitHub [issue tracker](https://github.com/keystonejs/keystone/issues).
* ... or preferably, submit pull request with patches and / or new features.
* Join the [KeystoneJS Slack](https://launchpass.com/keystonejs) for general discussion with the Keystone community and contributors.

We love to hear feedback about Keystone and the projects you're using it for. Ping us at [@KeystoneJS](https://twitter.com/KeystoneJS) on Twitter.

#### Related Projects
If you are using KeystoneJS in any projects we encourage you to add to our [Related Projects Page](https://github.com/keystonejs/keystone/wiki/Related-Projects). This is also the place to find generators and such that bundle KeystoneJS.

### Contributing

If you can, please contribute by reporting issues, discussing ideas, or submitting pull requests with patches and new features. We do our best to respond to all issues and pull requests, and make patch releases to npm regularly.

If you're going to contribute code, please follow our [coding standards](https://github.com/keystonejs/keystone/wiki/Coding-Standards) and read our [CONTRIBUTING.md](https://github.com/keystonejs/keystone/blob/master/CONTRIBUTING.md).

## Usage

**Check out the [KeystoneJS Getting Started Guide](http://keystonejs.netlify.com/getting-started) to start using KeystoneJS.**

### Installation

The easiest way to get started with Keystone is to use the Yeoman generator:

```bash
$ npm install -g generator-keystone
$ yo keystone
```

Answer the questions, and the generator will create a new project based on the options you select, and install the required packages from **npm**.

Alternatively, to include Keystone in an existing project or start from scratch (without Yeoman), specify `keystone: "4.0.0-rc.0"` in the `dependencies` array of your `package.json` file, and run `npm install` from your terminal.

Then read through the [Documentation](http://keystonejs.netlify.com/documentation) and the [Example Projects](http://keystonejs.com/examples) to understand how to use it.

### Configuration

Config variables can be passed in an object to the `keystone.init` method, or can be set any time before `keystone.start` is called using `keystone.set(key, value)`. This allows for a more flexible order of execution (for example, if you refer to Lists in your routes you can set the routes after configuring your Lists).

See the [KeystoneJS configuration documentation](http://keystonejs.netlify.com/documentation/configuration) for details and examples of the available configuration options.

### Database field types

Keystone builds on the basic data types provided by MongoDB and allows you to easily add rich, functional fields to your application's models.

You get helper methods on your models for dealing with each field type easily (such as formatting a date or number, resizing an image, getting an array of the available options for a select field, or using Google's Places API to improve addresses) as well as a beautiful, responsive admin UI to edit your data with.

See the [KeystoneJS database documentation](http://keystonejs.netlify.com/documentation/database) for details and examples of the various field types, as well as how to set up and use database models in your application.

Keystone's field types include:

 * [Boolean](http://keystonejs.netlify.com/api/field/boolean)
 * [Code](http://keystonejs.netlify.com/api/field/code)
 * [Color](http://keystonejs.netlify.com/api/field/color)
 * [Date](http://keystonejs.netlify.com/api/field/date)
 * [Datetime](http://keystonejs.netlify.com/api/field/datetime)
 * [Email](http://keystonejs.netlify.com/api/field/email)
 * [HTML](http://keystonejs.netlify.com/api/field/html)
 * [Key](http://keystonejs.netlify.com/api/field/key/)
 * [Location](http://keystonejs.netlify.com/api/field/location)
 * [Markdown](http://keystonejs.netlify.com/api/field/money)
 * [Money](http://keystonejs.netlify.com/api/field/money)
 * [Name](http://keystonejs.netlify.com/api/field/name)
 * [Number](http://keystonejs.netlify.com/api/field/number)
 * [Password](http://keystonejs.netlify.com/api/field/password)
 * [Select](http://keystonejs.netlify.com/api/field/select)
 * [Text](http://keystonejs.netlify.com/api/field/text)
 * [Textarea](http://keystonejs.netlify.com/api/field/textarea)
 * [URL](http://keystonejs.netlify.com/api/field/url)
 * [Azure File](http://keystonejs.netlify.com/api/field/azurefile)
 * [CloudinaryImage](http://keystonejs.netlify.com/api/field/cloudinaryimage)
 * [CloudinaryImages](http://keystonejs.netlify.com/api/field/cloudinaryimages)
 * [Embedly](http://keystonejs.netlify.com/api/field/embedly)
 * [LocalFile](http://keystonejs.netlify.com/api/field/embedly)
 * [S3 File](http://keystonejs.netlify.com/api/field/s-3-file)

Keystone also has [Relationship Fields](http://keystonejs.netlify.com/documentation/database/relationships) for managing one-to-many and many-to-many relationships between different models.

### Running KeystoneJS in Production

When you deploy your KeystoneJS app to production, be sure to set your `ENV` environment variable to `production`.
You can do this by setting `NODE_ENV=production` in your `.env` file, which gets handled by [dotenv](https://github.com/motdotla/dotenv).

Setting your environment enables certain features, including template caching, simpler error reporting and html minification, that are important in production but annoying in development.

### Linking Keystone for Development and Testing

If you want to test or develop against the `master` branch of KeystoneJS (or against your own branch), rather than a published version on **npm**, you just need to check it out then use `npm link` to link it to your project. On Mac OS, this is done like this:

 * Clone KeystoneJS locally, e.g. to `~/Development/KeystoneJS`.
 * From the KeystoneJS directory, run `sudo npm link` (you will need to enter your system password).
 * From your project directory, e.g. `~/Development/MySite` (the one with your `package.json` file in it) run `npm link keystone`. This will create a link between `~/Development/MySite/node_modules/keystone` and `~/Development/KeystoneJS`.

Then `require('keystone')` normally in your app - the development copy will be used. Note that running `npm update` will ignore new versions of keystone that have been published.

To go back to using a published version of KeystoneJS from npm, from your project directory, run `npm unlink keystone` then `npm install`.

#### Testing
To run the test suite run `npm test`.

## Thanks

KeystoneJS is a free and open source community-driven project. Thanks to our many  [contributors](https://github.com/keystonejs/keystone/graphs/contributors) and  [users](https://github.com/keystonejs/keystone/stargazers) for making it great.

Keystone's development has been led by key contributors including [Jed Watson](https://github.com/JedWatson), [Joss Mackison](https://github.com/jossmac), and [Max Stoiber](https://github.com/mxstbr) and is proudly supported by [Thinkmill](http://thinkmill.com.au) in Sydney, Australia.


## License

(The MIT License)

Copyright (c) 2016-2018 Jed Watson

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
