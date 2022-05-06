# Consult Git Commit

## Installation with straight.el and use-package

```el
(use-package consult-git-commit
  :straight (consult-git-commit :host github :repo "aaronjensen/consult-git-commit")
  :after git-commit
  :bind (:map
         git-commit-mode-map
         ("M-s" . #'consult-git-commit-message)))
```

## Commands

- `consult-git-commit-message`: Select and insert a commit message from recent
  history. Uses `git-commit` and `log-edit-comment-ring`.

## Tips

Use `save-hist` to persist your commit messages across sessions.

```el
(use-package savehist
  :config
  (add-to-list 'savehist-additional-variables 'log-edit-comment-ring)
  (savehist-mode))
```

