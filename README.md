grunt-aws
Grunt tasks for using the Amazon AWS SDK
Getting Started

This plugin requires Grunt 0.4.1

If you haven't used Grunt before, be sure to check out the Getting Started guide, as it explains how to create a Gruntfile as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

npm install {%= name %} --save-dev
Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

grunt.loadNpmTasks('{%= name %}');
The "{%= short_name %}" task

Overview

In your project's Gruntfile, add a section named {%= short_name %} to the data object passed into grunt.initConfig().

grunt.initConfig({
  {%= short_name %}: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
})
Options

options.separator

Type: String Default value: ', '

A string value that is used to do something with whatever.

options.punctuation

Type: String Default value: '.'

A string value that is used to do something else with whatever else.

Usage Examples

Default Options

In this example, the default options are used to do something with whatever. So if the testing file has the content Testing and the 123 file had the content 1 2 3, the generated result would be Testing, 1 2 3.

grunt.initConfig({
  {%= short_name %}: {
    options: {},
    files: {
      'dest/default_options': ['src/testing', 'src/123'],
    },
  },
})
Custom Options

In this example, custom options are used to do something else with whatever else. So if the testing file has the content Testing and the 123 file had the content 1 2 3, the generated result in this case would be Testing: 1 2 3 !!!

grunt.initConfig({
  {%= short_name %}: {
    options: {
      separator: ': ',
      punctuation: ' !!!',
    },
    files: {
      'dest/default_options': ['src/testing', 'src/123'],
    },
  },
})

Release History

(Nothing yet)