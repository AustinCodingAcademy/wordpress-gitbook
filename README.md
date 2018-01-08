[![CircleCI](https://circleci.com/gh/AustinCodingAcademy/wordpress-gitbook.svg?style=svg&circle-token=8d9042bc60224af55dc502288b22c03f547951cc)](https://circleci.com/gh/AustinCodingAcademy/wordpress-gitbook)

![](http://en.gravatar.com/userimage/107370100/a08594145564536138dfaaf072c7b241.png)
# Austin Coding Academy

## Wordpress GitBook

### Setup
1. `git clone` repository
1. `cd` into project directory and run `npm install` to install dependencies
1. Run `npm run gitbook install` to install GitBook plugins
1. Run `npm run gitbook serve` to serve locally at `http://localhost:4000`

### Development
1. Any change to any of the pages should trigger a rebuild
1. To add a new page, be sure to link it in the `SUMMARY.md`

### Contributing
1. Make sure to stop and re-serve the book to make sure it builds
1. Make all changes in a branch and push up
1. Make a PR against `master` and assign it to @kevincolten and/or @CLofton
