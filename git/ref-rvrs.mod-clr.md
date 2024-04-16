
# 修正を元に戻す


https://www.atlassian.com/ja/git/tutorials/undoing-changes


## 概要

- git checkout : commit から worktree に file を戻す

- git commit   : --amend で 直前の commit を破棄して, 再 commit

- git reset    : 指定した commit の状態へ, head, worktree, index を戻す

- git restore  : worktree, index の file を head の内容に戻す


使用度 低

- git rebase   : commit 履歴を変更する

- git revert   : commit を削除する新しい commit を作成する


## 基本

基本的には, commit をやり直したいことが多いと思われる






## push 後

push までしてしまった場合, さらなる修正で直すほうが無難です
( どうしてもの場合を除けば )




