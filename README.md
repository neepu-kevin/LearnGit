# Git 常用命令速查
## 一、版本提交与回退
| 命令 | 作用 | 关键说明 |
|------|------|----------|
| `git add .` | 所有修改加入暂存区 | `.` 代表当前目录，可替换为具体文件 |
| `git commit -m "说明文档"` | 提交暂存区到本地仓库 | `-m` 后必须写提交备注 |
| `git reset --hard HEAD^` | 回退到上一个版本 | `HEAD^`=上一版本，`--hard` 清空未提交修改 |
| `git status` | 查看工作区/暂存区状态 | 显示修改、未提交、未跟踪文件 |
| `git checkout -- test.txt` | 还原工作区文件 | 撤销 test.txt 所有未提交修改 |
| `git diff HEAD -- readme.txt` | 对比文件差异 | `-`=删除行，`+`=新增行 |
| `git log` | 查看提交历史 | `--oneline` 精简显示 |
| `git reflog` | 查看所有操作记录 | 含被删除/回退的提交，用于恢复 |
| `git reset --hard 版本ID` | 回退到指定版本 | 版本ID从 log/reflog 获取（前6位即可） |

## 二、文件操作
| 命令 | 作用 | 关键说明 |
|------|------|----------|
| `git rm test.txt` | 删除文件并加入暂存区 | 需 commit 完成仓库删除 |

## 三、远程仓库（GitHub）
| 命令 | 作用 | 关键说明 |
|------|------|----------|
| `git remote add origin 你的SSH地址` | 绑定远程仓库 | origin 是远程仓库默认别名 |
| `git push -u origin master` | 推送本地master到远程 | GitHub新版用 `git push -u origin main` |
| `git branch -M main` | 本地master重命名为main | 适配GitHub默认分支名 |
| `git remote -v` | 查看远程仓库地址 | 验证绑定是否正确 |

## 核心注意事项
1. 命令需逐行执行，切换英文输入法
2. `--hard` 会清空未提交修改，谨慎使用
3. 推送前需配置SSH密钥，首次推送输 `yes` 验证主机
