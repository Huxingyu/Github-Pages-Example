---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>Huxingyu胡行宇</h1>
        
        <a href="https://www.douban.com/people/83097413/" target="_blank"><img src="https://www.douban.com/favicon.ico" alt="" width="22"/></a>
        <a href="https://www.zhihu.com/people/hu-xing-yu-94" target="_blank"><img src="https://www.zhihu.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://steamcommunity.com/id/huxingyu/" target="_blank"><img src="http://store.steampowered.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://codeforces.com/profile/huxingyu1996" target="_blank"><img src="http://codeforces.com/favicon.ico" alt="" width="22"/></a>
        <a href="https://github.com/Huxingyu" target="_blank"><img src="https://github.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://dblp.uni-trier.de/" target="_blank"><img src="http://dblp.uni-trier.de/img/favicon.ico" alt="" width="22"/></a>
        <embed src="http://www.xiami.com/widget/35780868_H_L_album/wallPlayer.swf" type="application/x-shockwave-flash" width="675" height="235" wmode="transparent"></embed>
      </div>
      <div id="particles-js"></div>
    </div>

    <div class="index-content">
      <ul class="artical-list">
        {% for post in site.categories.blog %}
        <li>
          <a href="{{ post.url }}" class="title">{{ post.title }}</a>
          <div class="title-desc">{{ post.description }}</div>
        </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</body>
