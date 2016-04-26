# ETENG-WIKI构建说明
## 发布方式
* 极课学院wiki
* 利用MKDocs 在github 发布
该模板包含了两种发布方式的配置

## 极课wiki 配置

* 可以通过根目录下的 __config.json__ 文件配置自定义参数，具体如下：

	{
	    "name": "项目名称，必填",
	    "introduction": "Wiki 首页的项目介绍，必填",
	    "title": "页面的 title 标签的内容，非必填",
	    "keywords": "页面的 keywords 标签的内容，非必填",
	    "description": "页面的 description 标签的内容，非必填",
	    "path": {
	        "content": "正文的文件夹路径，相对路径绝对路径皆可，默认根目录，非必填",
	        "images": "引用图片的文件夹路径，相对路径绝对路径皆可，默认为根目录下的 images 文件夹，非必填",
	        "readme": "关于页面的路径，相对路径绝对路径皆可，默认根目录下的 README.md，非必填",
	        "toc": "目录的路径，相对路径绝对路径皆可，默认根目录下的 TOC.md，非必填"
	        }
	}
* 通过 __TOC.md__配置文章目录
one 

	- 关于我们
	    - [关于极客学院] \(about-us.md)
	    - [关于极客学院 Wiki]\(about-wiki.md)
	- [联系我们]\(contact.md)  
or like
	
	- [前言]\(eBook/preface.md)
	- 第一部分：学习 Go 语言
	    - 第1章：Go 语言的起源，发展与普及
	        - 1.1 [起源与发展]\(eBook/01.1.md)
		    - 1.2 [语言的主要特性与发展的环境和影响因素]\(eBook/01.2.md)
	    - 第2章：安装与运行环境
		    - 2.1 [平台与架构]\(eBook/02.1.md)


## 示例
GitHub 仓库地址：https://github.com/Unknwon/the-way-to-go_ZH_CN  
Wiki 项目地址：http://wiki.jikexueyuan.com/project/the-way-to-go/  

	{
	    "name": "Go 入门指南",
	    "introduction": "Go 经典书籍《The Way To Go》的中文译本。",
	    "path": {
	        "content": "eBook",
	        "readme": "README_gc.md"
	    }
	
	}
	
我们最基本配置为:

	{
	    "name": "WIKI-NAME",
	    "introduction": "WIKI INTRODUCTION ",
	    "path": {
	        "content": "docs"
	    }
	
	}

## MKDocs 配置

### Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
       
 通过__mkdocs.yml__配置标题,主题和目录结构
 
	site_name: 易腾WIKI列表
	pages:
	- Home: index.md
	- About: about-wiki.md
	- Start: start.md
	- Contact: contact.md
	theme: readthedocs
   

# 极课学院 wiki
配置说明 ： http://wiki.jikexueyuan.com/project/help/config-json.html

# MkDocs doc 
For full documentation visit [mkdocs.org](http://mkdocs.org).

# 快速开始,贡献一个wiki

##Installation
In order to install MkDocs you'll need Python installed on your system, as well as the Python package manager, pip. You can check if you have these already installed like so:

	$ python --version
	Python 2.7.2
	$ pip --version
	pip 1.5.2
MkDocs supports Python 2.6, 2.7, 3.3, 3.4 and 3.5.

On Windows we recommend that you install Python and pip with [Chocolatey](https://chocolatey.org/) .

Install the mkdocs package using pip:

	pip install mkdocs
You should now have the mkdocs command installed on your system. Run mkdocs --version to check that everything worked okay.

	$ mkdocs --version
	mkdocs, version 0.15.2
	
------------------------------------
## 贡献给一个wiki 
 首先加入 __易腾知识库__ 这个组织 ,[联系我们](contact.md)  
 例如我贡献ETENG-WIKI这个项目
 
	 git clone https://github.com/ETENG-WIKI/ETENG-WIKI.git
	 cd	ETENG-WIKI
	 mkdocs serve
	 
在浏览器中 Running at: http://127.0.0.1:8000/ 就可看到现在的效果 

增加一页   在docs 中新建***.md  
__TOC.md__增加配置指向  
__mkdocs.yml__ 增加配置指向

在***.md 中编写即可 
## 发布 

* 极课wiki发布
* 通过github发布
待续.......... 累了

