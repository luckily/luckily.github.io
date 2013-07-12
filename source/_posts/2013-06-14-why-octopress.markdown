---
layout: post
title: "Octopress - 第一篇文章"
date: 2013-06-14 14:42
comments: true
categories: Octopress
---

## 寫Code的人想有個筆記兼具分享的部落格

其實很久以前就有想要搞一個技術部落格, 在這之前有用過無名、痞客邦，但貼code的時候總不能就直接control+c然後control+v吧 ? 因為直接貼code上去既醜又沒人看的懂...<!--more-->

如果要像有像下面這樣的背景效果, 還要自己掛css上去, 真的太麻煩了
{% img center /images/2013-06-14/blog_view_code.png 512 100 'image' 'images' %}
<br />


## 輕鬆簡單

要的不多, 只要能**貼code**、**貼圖**、**簡單佈署**, 然後最重要的是除了能免費掛上網、還能有免費的**網域**!!

除了上述優點外, 還可以練習佈署、版本控制(git)..等等優點, 可謂『摸蛤仔兼洗褲』XD

<a href="http://octopress.org/" title="Ooctopress">Ooctopress</a>是一套部落格產生器, 內容編輯採用<a href="http://markdown.tw/" title="markdown">Markdown</a>語法。

其實有跟我相同需求的人, 這套Octopress在下就非常推薦了, 但如果只是純粹想寫寫心情, 非需要貼code性質的需求, 那還是建議用痞客邦、無名吧...不然你會想自殺的。
<br />


### 例如使用如下markdown語法
```
	``` ruby posts_controller.rb
		def show
			@posts = Post.where(:enabled => ture)
		end
	```
```

即可得到這樣的效果
``` ruby posts_controller.rb
	def show
		@posts = Post.where(:enabled => ture)
	end
```

如果要插入圖片, 就先把圖片存放在source/images底下:
然後放以下markdown語法:
``` ruby
  {% img center /images/my_car/Audi-R8-GT_1280x1024.jpeg 1280 1024 'image' 'images' %}
```
或者直接用html語法也行 
``` ruby
  <img class="center" src="/images/my_car/Audi-R8-GT_1280x1024.jpeg" width="1280" height="1024" title="image" alt="images">
```

效果
{% img center /images/my_car/Audi-R8-GT_1280x1024.jpeg 1280 1024 'image' 'images' %}


<br />


## 參考

其實網路上隨便搜尋個Octopress關鍵字, 都有一拖拉酷的資源可以查, 下面是覺得很不錯的資源, 他們也對Octopress是什麼東西介紹的很詳細, 可以去看看，他們也都是用Octopress。

待小弟有空在來多講講關於這東西是怎麼一回事，小弟還是個新手XD

<a href="http://blog.xdite.net/posts/2011/10/07/what-is-octopress/" title="xidte" target="_blank">Why Octopress? By XDite</a>

<a href="http://wwssllabcd.github.io/blog/2012/08/01/how-to-install-octopress-on-window/" target="_blank">Octopress 安裝教學、心得筆記 (Windows)</a>

<a href="http://garylai1990.github.io/blog/2012/12/18/di-ci-yong-octopressjiu-shang-shou/" target="_blank">第一次用Octopress就上手</a>

<a href="http://wwssllabcd.github.io/blog/2012/08/01/how-to-install-octopress-on-window/" target="_blank" title="printf(" I'm EricWang ")">printf(" I'm EricWang ")</a>
