
# fzf.vim


```
ctl-t  新規タブで開く


Command         List
Files [PATH]    Files (similar to :FZF)
GFiles [OPTS]   Git files (git ls-files)
GFiles?         Git files (git status)
Buffers         Open buffers
Colors          Color schemes
Ag [PATTERN]    ag search result (ALT-A to select all, ALT-D to deselect all)
Lines [QUERY]   Lines in loaded buffers
BLines [QUERY]  Lines in the current buffer
Tags [QUERY]    Tags in the project (ctags -R)
BTags [QUERY]   Tags in the current buffer
Marks           Marks
Windows         Windows
Locate PATTERN  locate command output
History         v:oldfiles and open buffers
History:        Command history
History/        Search history
Snippets        Snippets (UltiSnips)
Commits         Git commits (requires fugitive.vim)
BCommits        Git commits for the current buffer
Commands        Commands
Maps            Normal mode mappings
Helptags        Help tags
Filetypes       File types


key bind default

ctrl-f:forward-char          mv char forward
ctrl-b:backward-char         mv char back
 alt-f:forward-word          mv word forward
 alt-b:backward-word         mv word back
ctrl-a:beginning-of-line     mv cursor - 行頭
ctrl-e:end-of-line           mv cursor - 行末

ctrl-d:delete-char           del char forward
ctrl-h:backward-delete-char  del char back
 alt-d:kill-word             del word forward
ctrl-w:unix-word-rubout      del word back
ctrl-u:unix-line-discard     del cursor - 行頭

set -x FZF_DEFAULT_OPTS '--bind=ctrl-o:accept'

ctrl-l:forward-char,ctrl-f:forward-word
```






