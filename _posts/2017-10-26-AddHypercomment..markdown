---
layout:     post
comments: true
title:      "[Blog施工記錄] Hypercomments評論欄"
subtitle:   "三人行，必有我師焉"
date:       2017-10-26 12:18:00
author:     "Coco"
header-img: "img/post3-bg.jpg"
published: true
tags:
    - Blog施工記錄
---

首先先感謝一下水八口(?)大大辛苦做的整理

[**<font size="5">「第三方評論系統推薦」</font>**](https://blog.shuiba.co/comment-systems-recommendation )

真的幫了很大的忙，有選擇困難症的朋友肯定可以玩得很歡

說起評論欄的施工也是一路崎嶇顛簸

下面就來廢話一下歷程吧//

## 起源
會想開這個部落格本來是因為看我女神開了新部落格，就著女神給的一點小[資訊](http://candycat1992.github.io/2016/03/02/hello-blog/)，跌跌撞撞勉強的居然也給我磕碰出了一個。

果然人笨別不信邪，女神說一天搞定，我大概搞了２天吧...才把基礎架構架起來。  

剩下的ｍａｒｋｄｏｗｎ、ｊｅｋｙｌｌ、ｒｕｂｙ、ｇｉｔｈｕｂ在我弄出來之前一竅不通喔~小夥伴們有沒有多點信心啊～

## [LiveRe](https://livere.com/)
身為女神腦粉
一開始當然想跟著女神用萌萌的LiveRe
雖然他的中翻實在不怎麼對我胃口
但看著英文也是挺大氣的

但很快的我遭遇到了第一個問題  

我無法登入LiveRe!!  

本來就不是很想用的我找到理由放棄他了阿哈哈(欸

## [RemarkBox](https://www.remarkbox.com/)

基於對開源軟體的好感和對簡潔頁面的追求
我看上了RemarkBox
他的追求是替代 Disqus
支持markdown即時顯示和遊客留言

添加簡單，畫面簡潔
其實是很棒的選擇

不過，雖然一開始用著挺好的
但總不喜歡評論欄最後會跟著一個小紅盒子，和我的網頁風格不搭
最後還是忍痛放棄了他
(哭著跟小紅盒子說掰掰

## [Hypercomments](https://www.hypercomments.com/)

最後我選定了由俄羅斯人開發的Hypercomments，清爽的介面、支援google帳戶與訪客留言，而且還有一個質感的管理後台，簡直再滿意沒有了
開著後台都覺得自己好高大上阿~

免費版支援一個管理者和一個URL，對我來說很夠用了
後台可以管理和查看留言，也可以封鎖刪除等等，除此之外，還有一些個人化設定，有機會再介紹或是可以先試試看

不過有個小缺點是有時會有一些俄文小廣告，我通常是看到就刪掉封鎖了，畢竟略礙眼XD。

那麼，要怎麼在部落格裡加入 Hypercomments呢?

1.  首先，你必須要有一個Google帳號  
因為 Hypercomments是靠Google帳號登入，所以你必須要有一個Google帳號，點擊右上角的Log In登入
![](https://images.plurk.com/7dZ9XaDN3Lchm2qCG4qQ.jpg)

2.  選擇方案  
登入後會自動跳轉到選擇方案的介面，可以選擇第一種(免費版)，點擊下面的install  
![](https://images.plurk.com/30U5oPqEOmEWL2rrG4qQ.jpg)

3.  連結你的網頁  
填入你要使用的網頁URL，像我的是：`https://rapunzel1994.github.io`  
注意這邊他可能會幫你在URL的尾巴多加一個斜線"/"，而我第一次建立時因為這個"/"連結失敗了，小伙伴們可能要注意一下(如果不小心創錯的話是可以刪除的，後面會再介紹)
然後選擇你的部落格類型，在這裡我直接選擇HTML
完成後就前往下一步  
![](https://images.plurk.com/4qQ2SXj6C7VJGuYFG4qQ.jpg)

4.  嵌入代碼  
連結成功後，Hypercomments會給你一串程式碼，直接複製整串代碼到你想放置回應欄的地方，如果你跟我使用同個模版的話，是放在_layout/post裡，位置就看你的排版了。  
程式碼弄丟沒關係，在後台裡的setting/widget/code裡面就有喔~
![](https://images.plurk.com/5q8ZHFsBsUXmYwOHG4qQ.jpg)

另外，最後一行  
`<a href="http://hypercomments.com" rel = "nofollow" class="hc-link" title="comments widget">comments powered by HyperComments</a>`
	
這行會造成在load回應欄的時後出現 Hypercomments的連結，如果不需要的話可以刪掉。

Hypercomments 給的程式碼裡有一行

<pre><code>_hcwp.push({widget:"Stream", widget_id: xxxxx});</code></pre>
這裡的 xxxxx 就是你的ID

使用jekyll的小夥伴，打開你的_config.yml文件
找地方添加這兩行

<pre><code># Hypercomments
hypercomments_id: xxxxx</code></pre>

別真的打xxxxx阿
這個xxxxx就是上面 Hypercomments給的 widget_id

如此一來，你的部落格就添加 Hypercomments完成了！

### 我想刪掉這個URL怎麼辦?
如果不小心給錯連結，或是想要重建，可以找到後台裡的setting/widget/General中最下面的Deletion，就可以刪掉這個URL了，注意，你的一切記錄都會消失喔~

### 最後
終於添加回應欄拉，一個部落格沒有回應欄總覺得不算完整，希望能有機會和大家多多交流囉~