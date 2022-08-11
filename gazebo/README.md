Things to make colcon more enjoyable with Gazebo

Uses `direnv` to automatically load environment when in workspace folder or children

Install with `apt install direnv` and add to your shell as needed:
Typically you put something in your shell rc file like: `eval $(direnv hook zsh)`
On Ubuntu RTD: /usr/share/doc/direnv/hook.md


```
cp envrc ~/workspaces/gz_garden/.envrc
cp default.yaml ~/workspaces/gz_garden/default.yaml
cd ~/workspaces/gz_garden/
direnv allow
```


Also uses `ccache`:

```
sudo apt install ccache
# Big ol cache
ccache --set-config=max_size=30G
# Trade some slop for speed
ccache --set-config=sloppiness=locale,time_macros

```
