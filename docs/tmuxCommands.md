# Tmux Commands

## Start tmux
    $ tmux 
## Create a pane to the side <br>
<span style="color:green">**Ctrl+b+%** </span> (% for horizontal panes)<br>
<span style="color:green"> **Ctrl+b+"**  </span> ( " for vertical panes)


## Navigate between panes <br>

<span style="color:green"> **Ctrl+b+arrows** </span>


## Exit a pane
    $ exit

## Kill all sessions 
    $ tmux kill-server

## New tmux window <br>
<span style="color:green"> **Ctrl+b+c** </span> (bottom bar displays new window number, * indicates active window)<br>

## Switch between windows <br>
**Ctrl+b+window_number ⇒ Ctrl+b+1 or Ctrl+b+0** <br>

## Rename a window <br>
**Ctrl+b+, ⇒ type name and hit Enter**

## Detach a session <br>
**Ctrl+d**

## View sessions running in background 
    $ tmux ls

## Attach a session to tmux
    $ tmux attach -t <name_of_window> 
    example: tmux attach -t 0

## Rename a session
    $ tmux rename-session -t <old_name> <new_name>
    example: tmux rename-session -t 0 git

## Create a new session with name
    $ tmux new -s docker

## Kill a particular session
    $ tmux kill-session -t <name_of_session>
    example: `tmux kill-session -t docker

## Resize active pane border <br>
**Hold Ctrl+b+arrow**