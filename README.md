## Git 状态切换 ★★★

```sequence
工作区 ->  暂存区: git add xxx
暂存区 ->  版本区: git commit -m "提交信息"
版本区 ->  服务器: git push -u origin master
服务器 --> 工作区: git pull
版本区 --> 暂存区: git reset HEAD
暂存区 --> 工作区: git checkout -- a.txt
版本区 --> 暂存区: git checkout HEAD a.txt
版本区 --> 工作区: git checkout HEAD a.txt

Note right of 服务器: Gitlab、Github等
Note right of 版本区: 已经被Git版本控制
Note right of 暂存区: 暂时保存，即将交给Git进行版本管理
Note right of 工作区: 项目文件夹，进行“增删改”的区域
```
