# git-blast

A custom git command that works just like `git blame` but shows the committer's Twitter username instead of their name.

This project was inspired by [these](https://twitter.com/sigfig/status/1494548394982854663) [tweets](https://twitter.com/jaredforsyth/status/1494773495674380289)

## Warning

This is for novelty purposes only. I don't suggest blasting people on Twitter over some code they wrote. If you do please be nice.

This project is meant to be a fun experiment and has many limitations:

1. The code does not have good error handling
1. You should probably not write Node.js/JavaScript code like this. I was avoiding using any external libraries.
1. Using this a lot is probably a good way to get rate limited by the GitHub API
1. This script is written in Node.js which is maybe weird for a custom git command but I suck at bash
1. This script finds the committer's Twitter username by looking up their GitHub profile and then reading the `twitter_username` field. If they user hasn't set their Twitter username on their GitHub profile this won't work and will just show their email address.

## Installation

You must have Node.js installed to use this

1. Download the `git-blast` file from this repo and save it somewhere in your `PATH`
1. Make the file is executable by running `chmod 755 git-blast`

## Usage

In any git project run `git blast [git-blame-options] <filename>`

This command takes all the same arguments as `git blame`

## License

This code is made available under the MIT license

## Credits

Made with 🥃 by [Ian Sutherland](https://iansutherland.ca) ([@iansu](https://twitter.com/iansu))
