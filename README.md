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
To use this conventional changelog you need to active it in the .releaserc of [semantic-release](https://github.com/semantic-release/semantic-release)
```
"plugins": [..., ['@semantic-release/release-notes-generator', {"preset": "angular-redmine"}],...]
```