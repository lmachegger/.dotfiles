# .dotfiles

These are my personal dotfiles, synced with GNU stow.

## How to add a new config file to gnu stow:

1. Navigate to dotfiles folder (`~/.dotfiles/`) in my case.
2. Create a folder with the application-name as name. This way, we can later install the dotfile of a specific package / application.
3. In this package folder, recreate the exact layout (in regard to your homedirectory) where the dotfile(s) is stored.
   e.g. for alacritty, after these 3 steps the structure should look like this:
   `~/.dotfiles/alacritty/.config/alacritty/alacritty.yml`
   We acted as if `~/.dotfiles/alacritty/` was our homedirectory, and recreated our actual layout from the config.
4. To add our config to stow, run: `stow --adopt -nvt ~ <package-folder>`
   e.g. for our alacritty example: `stow --adopt -nvt ~ alacritty`

    Some things to note:

-   we specified our home directory with the `-t` flag
-   we only simulated our actions up to this point, with the `-n` flag

5. After checking, that the simulation does exactly what we expected, we can remove the `-n` flag and run the command again: `stow --adopt -vt ~ <package-folder>`.

## Where to check for a detailed tutorial:

[DevInsideYou](https://www.youtube.com/channel/UCSBUwLT9zXhUalKfJrc2q2A) made a really good and detailed [video tutorial](https://www.youtube.com/watch?v=CFzEuBGPPPg&t=1396s) about gnu stow!
