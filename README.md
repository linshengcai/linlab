这是我的个人主页所用的模板，该主题是[Sébastien Saunier](https://raw.github.com/ssaunier/ssaunier.github.io/)在[marcgg](http://marcgg.com/)的基础上改写的。我fork过来后，也稍微做了些修改，如果你觉得不错，可以直接从我这里fork过去，fork过去后还请你把涉及到我的一些信息、文章、图片删掉，[主题预览](http://yongyuan.name/)。

### 已完成功能

1. 调用豆瓣api显示书单列表
2. 在线简历
3. 添加latex公式支持([效果见博文](http://yongyuan.name/blog/decision-tree.html))
4. test

### 安装步骤

1. 把模板下载过去，如果你没有用单独的域名的话，把`CNAME`文件删掉，然后顺便把`_posts`里的文章删掉； 
2. 配置`_config.yml`，比如把title修改成你自己； 
3. 修改英文页面[default.html](https://github.com/willard-yuan/willard-yuan.github.io/blob/master/_layouts/default.html)，把里面出现的固定的url更改成你的url； 
4. 修改中文页面[index.html](https://github.com/willard-yuan/willard-yuan.github.io/blob/master/cn/index.html)，主要是中文页面的一些内容； 
5. **resume**目录是在线简历，[演示效果](http://yongyuan.name/resume/)，这个你在用时，把前面那个[default.html](https://github.com/willard-yuan/willard-yuan.github.io/blob/master/_layouts/default.html)中把latex的简历url换成这个目录的url；  
6. **book**模板，这个你需要有一个豆瓣账号，现在[books/index.html](https://github.com/willard-yuan/willard-yuan.github.io/blob/master/books/index.html)页面把title等修改一下，然后到[douban.api.js](https://github.com/willard-yuan/willard-yuan.github.io/blob/master/js/douban.api.js)把账号user和api改一下。
