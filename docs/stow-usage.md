# Stow usage

Brief tutorial about how to use `stow`.

## Add one existing config to

Select the config file you want to create a symlink. For example, `zsh` and run the following command:

```bash
stow --adopt -vt ~ zsh
```

It is going to create a symlink from your existing `.zshrc` in home directory into this repository. This way, it can be versioned in your configs and further managed by `stow` while re-applying it to a new machine.

Some notes about command options:

- `v`: verbose
- `t`: target directory
- `adopt`: creates the symlink from the real config into this project. In stow dialect, it means packaging the config into a `stow` config.

## Apply your configs into a new machine

1. clone this repo somewhere
2. get into this project directory
3. run listing the app configs you want to apply. If you don't specify, it will apply all your configs.

```bash
stow -vSt ~ zsh bash
```

## More info about stow

- [Sync your .dotfiles with git and GNU like a pro - by DevInsideYou](https://www.youtube.com/watch?v=CFzEuBGPPPg)