# tmux BOSH release

A [BOSH](https://bosh.io) release for deploying a `tmux` executable.
This release also installs a script to `/etc/profile.d` that makes `tmux` available on the `PATH`.

## Examples

An example manifest for [BOSH-Lite](https://bosh.io/docs/bosh-lite) can be found at [manifests/bosh-lite.yml](manifests/bosh-lite.yml).
This manifest assumes the BOSH-Lite BOSH director has a cloud-config similar to the one in the [cf-deployment repository](https://github.com/cloudfoundry/cf-deployment/blob/master/bosh-lite/cloud-config.yml).
To upload the release and deploy, follow these steps using the [BOSH CLI](https://github.com/cloudfoundry/bosh-cli), assuming the BOSH-Lite director is aliased to `lite`:

```
$ bosh -e lite upload-release releases/tmux/tmux-v0.1.0.yml
$ bosh -e lite -d tmux deploy manifests/bosh-lite.yml
```

## Sources

- tmux: [https://github.com/tmux/tmux](https://github.com/tmux/tmux)
- libevent: [http://libevent.org/](http://libevent.org/)
- ncurses: [http://invisible-island.net/ncurses/](http://invisible-island.net/ncurses/)


## Acknowledgements

Thanks to [https://gist.github.com/ryin/3106801](https://gist.github.com/ryin/3106801) and [https://gist.github.com/haridsv/5040047](https://gist.github.com/haridsv/5040047) for providing most of the  compilation flags required for the BOSH packaging scripts to work.
