步骤 1：点击「Add file」→「Create new file」
在你截图的页面右上角，找到 Add file 按钮，点一下，选择 Create new file。
步骤 2：输入完整的文件路径
在「Name your file...」这个输入框里，直接完整输入：
plaintext
.github/workflows/hello.yml
注意：
开头是 .github（前面有个点！）
用 / 分隔文件夹，GitHub 会自动帮你创建这两级文件夹
后缀是 .yml，不要写错成 .yaml 或 .txt
步骤 3：粘贴工作流代码
在下面的大编辑框里，把我们之前的模板粘贴进去：
yaml
name: 我的第一个工作流

on:
  push:
    branches: [ main ]  # 推送到 main 分支就自动跑

jobs:
  build:
    runs-on: ubuntu-latest  # 在云端 Ubuntu 上跑

    steps:
    - name: 打印一句话
      run: echo "Hello GitHub Actions！我在云端自动运行啦"

    - name: 查看系统信息
      run: uname -a
步骤 4：提交文件（Commit new file）
拉到页面最底部，填写提交信息（比如 Add first GitHub Actions workflow），然后直接点 Commit new file 按钮。
✅ 完成！
提交成功后，GitHub 会自动触发一次工作流运行
你点仓库上方的 Actions 标签，就能看到正在跑的任务，点进去看日志
