# Solution for exercice 2

1. tmux  
    It stands for terminal multiplexer that splits the terminal into `windows` and `panes`
    Commands in tmux consists of `prefix key` + `command key`
    ```
    $tmux
    ```
    This will open a new session named numerically 
    To give it name:
    ```
    $tmux new -s session_name   
    ```
    To rename it:
    
    tmux rename-session -t <old name> <new>
    
    The default prefix key is `ctrl+b`
     - `C-b %` to split panes into a left and a right pane.
     - `C-b "` to split a pane into top and bottom panes.
     - `C-b <arrow kek>` to navigate through panes.
     - `C-d` or `exit` to close a pane.
     - `C-b c` to creat a new window. 
        - `C-b p` to switch to the previous window & `C-b n` to the next.
        - `C-b <win number>` to move to any win you need.
     - Re-attaching to Tmux Session 
     ```
     $ tmux ls
     ```
     choose your session to be attached then 
     ```
     $ tmux attach-session -t <the selected one>
     ```
     - To detach the current session `c-b d` or `c-b D` to choose which one to be detached. 
     
   2. fzf   
     It a tool used for searching for files 
     
   3. When type
    ```
     $ apt install vim
     ```
     it shows errors, and ask me if I am root?
     Installation needs root's permissions to be excuted, we can do it with `sudo`
     ```
     $ sudo apt install vim 
     ```
    - `!15` it installs snapd which is an installer for snaps [packages] or required to run snaps.
     
   4. `history` is used to view the previous commands 
      `cat ~/.bash_history` also views the previous commads, 
        then pressing `ctrl+r` to look for any command you want.  
        You can also try `fzf` 
        ```
        $ cat ~/.bash_history | fzf
        ```
    5. - Symbolic link: it's a file that points to another file like a shortcut in Windows, Symbolic links contain the path to the original file.
        To creat a symbolic link:
        ```
        $ln -s "file name" "symbolic link"
        ```
        - Hard links: They are copies of the original file they point to. The same way Hard links are also created with `ln`  
       
        If the original file is removed the soft link  will point to no file, which means if you delete or move the source file the symbolic link will loss access           to the information, while with the hard link the information remains despite the source file removal because it is a full and exact copy of that file.
        Symbolic links can be used to link directories while with hard links that’s not possible.
        
        After running `ls -l` we notice that `the symbolic link -> the original file` 
        
    6. The command `diff` compares files line by line 
       That difference between the files is called a `patch` we use it to apply the differences.

        
