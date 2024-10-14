# 实验数据

## 概览

本研究的数据集包含71个应用，总共有121个崩溃错误。这些应用来源于两个主要的数据集：来自Themis基准测试的20个应用，包含34个错误，以及从F-Droid收集的额外51个应用，包含87个错误。

你可以在[Google Drive](https://drive.google.com/drive/folders/1vjCY1Tr6Tp_QctP_KpbeCb7-erTJn_-N?usp=sharing) 下载额外添加的数据集。

## 数据详情

### `Bugtobetest`

它包括被测试应用的APK安装包，以及与错误相关的相应信息。

### `readme`

所有应用的README文件。文件名是哈希化的GitHub链接。

### `selected_data`

包含所有问题，包括以下信息：

`app_name,category,github_link,issue_title,issue_description,issue_link,level,comments,bug_steps`

### `app_activities.csv`

该文件包含以下应用级信息：

`app_name,github_link,github_xml_link,activities,ATG`

### `app2package.csv`

记录了启动各种应用的起始活动。

### `manual_bugs.csv`

用作测试数据的与错误相关的信息。

## 哈希计算

为了防止同名但不同类别的软件出现命名冲突，我们使用GitHub链接的哈希值作为应用级信息的文件名。例如，README文件就是使用哈希方法命名的。算法如下：

```python
import hashlib

def hash_github_link(github_link: str):
    """
    github_link 示例：https://github.com/izivkov/CasioGShockPhoneSync 
    """
    repo_name = github_link.split('github.com/')[-1].rstrip('/')
    hash_name = hashlib.md5(repo_name.encode()).hexdigest()[:32]
    return hash_name
```

请注意，由于网络原因，我无法成功解析提供的Google Drive链接。这可能是由于链接本身的问题，或者是网络连接的问题。请检查链接的合法性，并在适当的时候重试。如果您需要进一步的帮助，请告知我。
