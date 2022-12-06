    # Start a new session
        $ tmux
    
    # Start a new session with the name mysession
        $ tmux new -s mysession

    # kill/delete session mysession
        $ tmux kill-session -t mysession

    # kill/delete all sessions but the current
        $ tmux kill-session -a
    
    # kill/delete all sessions but mysession
        $ tmux kill-session -a -t mysession

    # Rename session
        Ctrl+b $

    # Detach from session
        Ctrl+b d

    # Detach others on the session (Maximize window by detach other clients)
        : attach -d
    
    # Show all sessions
        $ tmux ls
    
    # Attach to last session
        $ tmux a
        $ tmux attach
        $ tmux attach-session
    
    # Attach to a session with the name mysession
        $ tmux a -t mysession
        $ tmux attach -t mysession
        $ tmux attach-session -t mysession

    # Session and Window Preview
        Ctrl+b w

    # Move to previous session
        Ctrl+b (
    
    # Move to next Session
        Ctrl+b )

    # Create window
        Ctrl+b c

    # Rename current window
        Ctrl+b ,
    
    # Close current window
        Ctrl+b &
    
    # List windows
        Ctrl+b w
    
    # Previous window
        Ctrl+b p
    
    # Next window
        Ctrl+b n
    
    # Switch/select window by number
        Ctrl+b 0..9
    
    # Toggle last active window
        Ctrl+b l
    
    # Reorder window, swap window number 2(src) and 1(dst)
        : swap-window -s 2 -t 1
    
    # Move current window to the left by one position
        : swap-window -t -1
    
    # Toggle last active pane
        Ctrl+b ;
    
    # Split pane with horizontal layout
        Ctrl+b %
    
    # Split pane with vertical layout
        Ctrl+b "
    
    # Move the current pane left
        Ctrl+b {
    
    # Move the current pane right
        Ctrl+b }
    
    # Switch to pane to the direction
        Ctrl+b ↑
        Ctrl+b ←
        Ctrl+b →
        Ctrl+b ↓

