# Contributing to CodeSandbox Client

## Code Organization

The CodeSandbox client is currently divided in to 5 parts.

- `app`: The editor and profile page
- `sandbox`: The preview pane of the editor
- `embed`: The embedded version of CodeSandbox (which you can embed on medium)
- `common`: The common parts between `sandbox`, `embed` and `app`
- `homepage`: Homepage!

This version of CodeSandbox is using the production server as source of truth, this is specified by the environment variable `LOCAL_SERVER`. It's not yet possible to sign in using this version, I haven't figured out how to handle this yet.

## Setting Up the project locally

To install the project you need to have `yarn` and `node`

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your fork:

   ```
   # Clone your fork
   git clone https://github.com/<your-username>/codesandbox-client.git

   # Navigate to the newly cloned directory
   cd codesandbox-client
   ```
2. `yarn` to install dependencies
3. `yarn start` to start the app

> Tip: Keep your `master` branch pointing at the original repository and make
> pull requests from branches on your fork. To do this, run:
>
> ```
> git remote add upstream https://github.com/CompuIves/codesandbox-client.git
> git fetch upstream
> git branch --set-upstream-to=upstream/master master
> ```
>
> This will add the original repository as a "remote" called "upstream,"
> Then fetch the git information from that remote, then set your local `master`
> branch to use the upstream master branch whenever you run `git pull`.
> Then you can make all of your pull request branches based on this `master`
> branch. Whenever you want to update your version of `master`, do a regular
> `git pull`.

## Submitting a Pull Request

Please go through existing issues and pull requests to check if somebody else is already working on it, we use `someone working on it` label to mark such issues.

Also, make sure to run the tests before you commit your changes.

```
yarn test
```

## Add yourself as a contributor

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!

To add yourself to the table of contributors on the `README.md`, please use the
automated script as part of your PR:

```
yarn run add-contributor
```

Follow the prompt and commit `.all-contributorsrc` and `README.md` in the PR.

Thank you for taking the time to contribute! :+1:
