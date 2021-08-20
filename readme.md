# How to reproduce this bug:

## Expected behavior using default configuration:

1. Run `yarn run serve`
2. Edit `arbitrary-watch-file.txt`
3. Watch Browsersync reload in the terminal

## Unexpected behavior using custom configuration

1. Note that `.eleventy.js` and `config.js` have the same contents
2. Delete `.eleventy.js` so Eleventy doesn't load it by default
3. Run `yarn run brokenserve`, which tells Eleventy to use the custom config location `config.js`
4. Edit `arbitrary-watch-file.txt`
5. Watch Browsersync fail to reload, even though the config specified `arbitrary-watch-file` as a file that should cause Browsersync to reload