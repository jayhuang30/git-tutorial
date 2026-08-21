# 初始化
```Bash
git init -b main 
```

# 建立分支(名為main)
```Bash
git branch -M main
```

# 修正或建立附註tag (搭配訊息，針對該commit id)
針對

```Bash
git tag -a 1.0.0 21317e4 -m "fix the tag"
```

# 推送至(remote repo的)main分支
```Bash
git push origin main
```

# 強制推送(remote repo的)main分支
```Bash
git push origin main --force-with-lease  
```

# 推送新標籤
推送名為1.0.1和1.0.2這兩個新標籤

```Bash
git push origin 1.0.1 1.0.2
```

# 修正(當前)commit訊息
```Bash
git commit --amend -m <commit-message>
```

# 針對某commit，顯示 Commit 訊息，並列出異動檔案及行數增減統計
```Bash
git show --stat <commit-hash>
```

# 顯示 Commit 訊息、檔案名稱以及異動狀態（A: 新增, M: 修改, D: 刪除）
```Bash
git show --name-status <commit-hash>
```

# 針對某commit，只顯示 Commit 訊息與受影響的檔案名稱
```Bash
git show --name-only <commit-hash>
```

# 針對某commit，只列出受影響的檔案名稱
```Bash
git diff-tree --no-commit-id --name-only -r e7b7d38
```

# 重置前一次的推送，但未重置Commit 
```Bash
git reset --soft HEAD~1
```

# 重置前N次的推送，但未重置Commit 
重置前3次的推送，但未重置Commit 

```Bash
git rebase -i HEAD~3
```

# 取消暫存多加入的檔案
```Bash
git reset HEAD path/to/unwanted_file.cs
```

# 查詢「恰好指向」該 Commit 的 Tag（若該 Commit 正好是打 Tag 的點）
```Bash
git tag --points-at <commit-id>
```
# 查詢「包含」該 Commit 的所有 Tag（該 Commit 之後所有包含此變更的 Tag）
```Bash
git tag --contains <commit-id>
```

# 刪除遠端誤植的標籤

```Bash
git push origin :refs/tags/"1,0.1"
git push origin :refs/tags/"1,0.2"
```

or

```Bash
git push origin --delete "1,0.1" "1,0.2"
```

# 查看本機repo的commit log
若要列出完整的話

```Bash
git log
```

若只要簡單列出(每個commit只占一行)

```Bash
git log --oneline
```

