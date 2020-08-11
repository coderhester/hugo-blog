# hugo-blog
脚本自动化创建博客和发布博客，让大家更加的愿意写博客和分享知识，当突然有了些灵感或者想写博客的想法的时候，需要立马行动起来，不能有太多的阻碍。此Python脚本就是帮助大家更加的容易些博客，感觉不到自己在写静态博客。

## 配置文件

```xml
[blog]
# hugo的根目录
hugo_path=/Users/kid/tangf/SevenBook/site

# 博客的文章根目录
path=/Users/kid/tangf/SevenBook/site/content/post

# 新建博客是否打开,使用系统默认此文件的打开方式
open_auto=false

# 远程服务器地址
host=root@sbk
# 远程服务器的博客目录
host_path=/data/SevenBook/site

# sonic的索引创建
# 内容介绍： https://www.7benshu.com/post/2020/08/05-1/
# 开源地址： https://github.com/tangfei-china/hugo-search-fast
# 详细的介绍和使用请看上两个链接
# 是否开启sonic搜索,默认关闭
sonic_enabled=false
# 索引创建执行文件
sonic=/Users/kid/tangf/SevenBook/site/sonicIndex/search_index
# 索引创建配置文件
sonic_conf=/Users/kid/tangf/SevenBook/site/sonicIndex/conf.yaml
```

## 使用

```shell
# 创建博客，如果open_auto=true，创建完会自动打开，默认是关闭的
python3 hugo.py -n

# 查看帮助
python3 hugo.py -h

# 发布博客内容到服务器
python3 hugo.py -p 新增了博客内容
```

