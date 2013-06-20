---
layout: post
title: "Octopress - 安裝篇"
date: 2013-06-14 00:58
comments: true
categories: 
---


### 1.安裝RVM & Ruby for Mac
	$ \curl -L https://get.rvm.io | bash -s stable --ruby
	$ rvm install 1.9.3
	$ rvm use 1.9.3 --default
	$ rvm rubygems current

### 2.安裝bundler
	$ gem install bundler
	
### 3.下載Octpress專案
	$ git clone git://github.com/imathis/octopress.git octopress
	$ cd octopress
	$ bundle install
	$ rake install

   若發生此錯誤訊息
	rake aborted!
	You have already activated rake 10.0.4, but your Gemfile requires rake 0.9.2.2. Using bundle exec may solve this.

   解決方式 : 找到Gemfile.lock搜尋rake並把0.9.2.2改成10.0.4, 依照妳目前已經有什麼的rake版本, 就改什麼版本完成之後, 重跑指令。
	$ rake install

### 4.發佈到GitHub(免費)
   
   (1)請至<a target="_blank" href="https://github.com">[GitHub]</a>建立Repository, 並使用 your_username.github.io 命名。
   <br />
   Ex : luckily.github.io

   (2)接著設定Github Pages, 輸入下列指令
	$ rake setup_github_pages

   (3)終端機會提示以下字樣, 要你輸入建立Repository的Github網址
   <br>
	Enter the read/write url for your repository
	(For example, 'git@github.com:your_username/your_username.github.io')
	Repository url:

   (4)像我就輸入
	$ git@github.com:luckily/luckily.github.com.io

   (5)建立及佈署
	$ rake generate
	$ rake deploy

   (6)將source也加入git
	$ git add .
	$ git commit -m 'initial source commit'
	$ git push origin source

   每次寫完部落格上傳到Gihub之後, 最後還要再佈署, 才會看到改變哦!
	$ rake deploy
   等個幾分鐘只要連 http://your_username.github.io 就可以看到自己的網頁拉!!<br />
   就跟我這個網址  http://luckily.github.io 一樣XD


	# TODO
	1.此篇為安裝篇
	2.使用篇指令&語法篇

	```  [程式語言]
	  code

	```

	範例:
  
  程式碼: 
	``` ruby
		def index
			@posts = Post.all
		end
	```

	插入圖片(可把圖片存放在source/images底下):
	{% img center /images/my_car/Audi-R8-GT_1280x1024.jpeg 1280 1024 'image' 'images' %}