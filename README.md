# next-9-app-bug
Repo for bug repros

## Summary

We have several apps who's `_app.js` exports a common structure from a
shared module that is a dependency of each app. This has worked well for use
with previous versions of next, but is failing under v9.

This repo reproduces the problem in it's simplest form.

## To Reproduce

```bash
git clone https://github.com/kinetifex/next-9-app-bug.git
cd ./next-9-app-bug
npm i
npm run build
```

This will fail with:

```bash
# TypeError: Class constructor App cannot be invoked without 'new'
```

## Expected behavior

The app builds fine.
To see this working correctly with `next@8.1.0`

```bash
git checkout works-with-8
npm i
npm run build
```
