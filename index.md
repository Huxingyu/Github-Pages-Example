---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>Huxingyu_2017</h1>
        
        <a href="https://www.douban.com/people/83097413/" target="_blank"><img src="https://www.douban.com/favicon.ico" alt="" width="22"/></a>
        <a href="https://www.zhihu.com/people/hu-xing-yu-94" target="_blank"><img src="https://www.zhihu.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://steamcommunity.com/id/huxingyu/" target="_blank"><img src="http://store.steampowered.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://codeforces.com/profile/huxingyu1996" target="_blank"><img src="http://codeforces.com/favicon.ico" alt="" width="22"/></a>
        <a href="https://github.com/Huxingyu" target="_blank"><img src="https://github.com/favicon.ico" alt="" width="22"/></a>
        <a href="https://arxiv.org/find/astro-ph/1/au:+Xingyu_Hu/0/1/0/all/0/1" target="_blank"><img src="https://arxiv.org/favicon.ico" alt="" width="22"/></a>
        <a href="https://twitter.com/XingyuHu" target="_blank"><img src="https://twitter.com/favicon.ico" alt="" width="22"/></a>
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
