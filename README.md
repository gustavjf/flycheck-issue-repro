### Cloning repository and installing dev dependencies:

```
git clone https://github.com/gustavjf/flycheck-issue-repro.git

cd flycheck-issue-repro

yarn
```

### Reproduction:

At this point, you should be able to open `index.js` inside emacs and run `C-c ! v` to inspect the current flycheck status and see the ESLint errors highlighted in the buffer.

Now, try initializing the flowtype config by running `yarn flow init`.

Notice after `.flowconfig` is created that when you return to the buffer and make changes, ESLint errors no longer appear - only flowtype errors.

When you remove `.flowconfig`, the ESlint errors are now visible again, and as expected, flowtype errors are not.
