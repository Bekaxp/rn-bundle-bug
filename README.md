# Repro for the Metro bundle bug

This is a reproduction of a bug reported here:

## Steps to reproduce

1. Clone this repo
2. Run `yarn` to install dependencies
3. If you are using iOS, install gems with `cd ios && bundle install` and run `bundle exec pod install` to install the pods as well.
4. Run `yarn ios` to start the app.
5. The app should open and explode :).

## To make it work

1. Open `metro.config.js`.
2. Disable `unstable_enablePackageExports` flag.
3. Run `yarn start --reset-cache`.
4. The app should work now.
