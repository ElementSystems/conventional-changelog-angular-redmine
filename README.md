> [conventional-changelog](https://github.com/ajoslin/conventional-changelog) [angular](https://github.com/angular/angular) redmine preset

**Issues with the convention itself should be reported on the Angular issue tracker.**

## Angular Convention
Angular's [commit message guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit).

## npm
[NPM Package: conventional-changelog-angular-redmine](https://www.npmjs.com/package/conventional-changelog-angular-redmine)
```
npm install conventional-changelog-angular-redmine --save-dev
```

## Usage/Configuration
To use this conventional changelog you need to active it in the `release.config.js` of [semantic-release](https://github.com/semantic-release/semantic-release).
Make sure to correctly link your redmine installaion by replacing the `finalizeContext` function in `release.config.js` like this:
```
...
"generateNotes": {
        "preset": "angular-redmine",
        "writerOpts": {
            "finalizeContext": function (context, options, commits, keyCommit) {
                context.redmineBaseUrl = 'https://redmine.example.com';
                return context;
            }
        }
    },
    "plugins": [
        ...
        '@semantic-release/release-notes-generator',
        ...
    ]
...
```