# How to Force Conventional Commits
We will use commitlint to force ourselves to write a conventional commits and if
we try to write a non-conventional commit it will not be accepted.

## How to set-up it
#### Install
Install `@commitlint/config-conventional`
```sh
npm install -D @commitlint/cli @commitlint/config-conventional
```

#### Configuration
Configure commitlint to use conventional config
```sh
echo "export default { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```


#### Local setup
Get high commit message quality and short feedback cycles by linting commit messages right when they are authored.

This guide demonstrates how to achieve this via git hooks.

#### Add hook
```sh
npm install --save-dev husky

# husky@v9
npx husky init

# Add commit message linting to commit-msg hook
echo "npx --no -- commitlint --edit \$1" > .husky/commit-msg
```


### Notes
- Delete the pre-commit file created inside `.husky' folder
- Edit the extension of `commitlint.config.js` file to `commitlint.config.mjs`


You are ready now 😇✌.