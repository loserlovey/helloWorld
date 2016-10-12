# Install Scrapy on Python 2.7 on Windows


### Install pywin32

Install [pywin32](https://sourceforge.net/projects/pywin32/) is required on windows system.

### Install lxml

需要单独安装相应版本 [lxml](http://www.lfd.uci.edu/~gohlke/pythonlibs/#lxml)

	检查python已安装模块
		>>> help('modules')
		
	安装相应版本 lxml 
		>>> pip install lxml-3.6.4-cp27-cp27m-win32.whl
		or
		>>> pip install lxml-3.6.4-cp27-cp27m-win_amd64.whl
		or
		>>> pip install lxml-3.6.4-cp35-cp35m-win_amd64.whl
		
	
	测试是否安装成功
		# scrapy version

### 安装scrapy框架 

	# pip install scrapy

# Create project

	# scrapy startproject tutorial

	
生成目录：
	
	tutorial/
		scrapy.cfg
		tutorial/
			__init__.py
			items.py
			pipelines.py
			settings.py
			__pycache__/
			spiders/
				__init__.py
				__pycache__

		

- scrapy.cfg: 项目的配置文件
- tutorial/: 该项目的python模块。之后您将在此加入代码。
- tutorial/items.py: 项目中的item文件.
- tutorial/pipelines.py: 项目中的pipelines文件.
- tutorial/settings.py: 项目的设置文件.
- tutorial/spiders/: 放置spider代码的目录.


# Define Item

    import scrapy


	class TutorialItem(scrapy.Item):
	    # define the fields for your item here like:
	    # name = scrapy.Field()
	    title = scrapy.Field()
		link = scrapy.Field()
		desc = scrapy.Field()

# First Spider

    import scrapy


	class DmozSpider(scrapy.spiders.Spider):
	    name = "dmoz"
	    allowed_domains = ["dmoz.org"]
	    start_urls = [
	        "http://www.dmoz.org/Computers/Programming/Languages/Python/Books/",
	        "http://www.dmoz.org/Computers/Programming/Languages/Python/Resources/"
	    ]
	
	    def parse(self, response):
	        filename = response.url.split("/")[-2]
	        with open(filename, 'wb') as f:
	            f.write(response.body)

Save it as dmoz_spider.py under tutorial/spiders/

# Crawling

Enter the root folder of the project.

	# scrapy crawl dmoz