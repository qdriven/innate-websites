# 工作流相关的任务

## Task 1: 没有自动fetch issues的脚本

1. 请帮我实现自动fetch issues的脚本
2. 另外github action中的任务，是否可以调整到2个小时跑一次


## Task 2: 实现一个daemon进程，用于自动fetch issues

1. 请在这个mono repo中创建一个daemon进程，用于自动fetch issues
2. 这个daemon进程需要自己手动出发，同时如果触发了会在本地类似执行github action的工作，
   例如fetch issues，更新本地数据库，提交数据。
3. 这个实现在packages/ 这个目录中实现，可以采用cli模式，实现文档需要写入到docs/目录中，创建一个新目录中完成比如 task-watcher类似的名字


## Task 3: 实现一个补充提交github issue的工具

1. 读取task文件，按照markdown 内容提交到github issue
2. 按照内容解析，task 1内容就是一个issue，task2就是另外一个issue
3. 过程中是否可以调用AI让AI告诉他之前处理这个ISSUE做的事然后做一些补充呢？是否可以实现这个过程？
4. 需要给出一份整个功能的分析报告，是否可行？有个实现计划，然后在继续实现，先不写代码

实际场景可能是这样：
1. 先写了Task 让AI 执行代码，但是这个Task 内容是自己写的，AI执行时候补充的内容没有被更新
2. 并且这个Task 没有提交作为Github的Issue进行保存
3. 那么无如果需要补充提交这个Task 到Github的Issue中，但是有需要把一些当时AI产生的内容补充回来，这个过程可以实现吗？我问的问题主要是这个，不是从github issue拉下来在做补充