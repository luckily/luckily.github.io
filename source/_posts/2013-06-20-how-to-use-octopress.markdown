---
layout: post
title: "Octopress - 使用篇"
date: 2013-06-20 16:43
comments: true
categories: 
---

## Octopress常用的語法

1.建立文章
   正常的情況下執行此行:
	$ rake rake new_post['how-to-use-octopress']

   但如果你使用的是zsh shell的話, 就必須這樣打:
	$ rake rake "new_post[how-to-use-octopress]"


<br />

2.建立/更新
	$ rake generate
   每一次只要有執行過<code>rake rake new_post</code>來產生文章之後, 都必須使用下列指令, 之後在網頁重整才能看到剛剛建立的文章。


<br />

3.本機預覽
	$ rake preview
   可以在<code>http://localhost:4000</code>上預覽Blog, 順便一提, **如果只是修改文章內容, 其實只要重整就可以看到修改後的變化**, 換言之...只有執行<code>rake new_post</code>之後, 才需要再執行<code>rake generate</code>。


<br />

4.寫完文章之後要上傳至Github
	$ git add .
	$ git commit -m 'OK, push.'
	$ git push origin source


<br />

5.佈署部落格
	$ rake deploy
   記得佈署前都應該要先做第4點的動作, 佈署完成就可以到<code>http://user_name.github.io</code>看看部落格最新的狀況囉。



## 在別台電腦也要使用Octopress

   很多人常常也會有兩三台電腦(筆電/桌機), 所以也會有不同電腦使用Octopress的需求, 要注意的是一般文章原始檔或圖片都放在soruce的分支。
   首先一樣安裝完Octopress並進入該目錄。
	$ git clone git://github.com/imathis/octopress.git octopress 
	$ cd octopress
	$ bundle install
	$ rake install

   然後, 按照步驟先綁GitHub
	$ rake setup_github_pages

   依照指示輸入<code>https://github.com/your_username/your_username.github.io)</code>, 完成之後接著輸入, 把原始檔下載下來
	$ git pull origin source

   下載下來之後, 當然還是要輸入下面這行, 才能用<code>rake preview</code>來本機觀看囉!
	$ rake generate