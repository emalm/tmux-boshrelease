# tmux BOSH release

A [BOSH](https://bosh.io) release for deploying a `tmux` executable.
This release also installs a script to `/etc/profile.d` that makes `tmux` available on the `PATH`.


## Sources

- tmux: [https://github.com/tmux/tmux](https://github.com/tmux/tmux)
- libevent: [http://libevent.org/](http://libevent.org/)
- ncurses: [http://invisible-island.net/ncurses/](http://invisible-island.net/ncurses/)


## Acknowledgements

Thanks to [https://gist.github.com/ryin/3106801](https://gist.github.com/ryin/3106801) and [https://gist.github.com/haridsv/5040047](https://gist.github.com/haridsv/5040047) for providing most of the  compilation flags required for the BOSH packaging scripts to work.
