# NancyWiki-Py27

## English Version

[NancyWiki](https://code.google.com/p/nancywiki/) is a simple wiki engine running on Google App Engine using Python 2.5 runtime. NancyWiki-Py27 is its migrated version on Python 2.7 runtime.

### Original Introduction of NancyWiki
NancyWiki is developed based on Google App Engine using Python. The meta language in wiki is Markdown since it is simple and easy to use.

NancyWiki aims to build an easy to use personal wiki system for reading, studying, and taking notes.

NancyWiki's principle is to be as simple and useful as possible. It keeps the simplicity of code. There are only 3 Python files: main.py, models.py, views.py. Meanwhile, it is completely built using theme templates so users can create their own theme for the wiki system. Currently there are 2 themes provided in theme directory and can be switched in the settings page.

For details, please refer to [http://wiki.coderzh.com](http://wiki.coderzh.com) (Chinese only)

### Demo
NancyWiki provides a [Demo Page](http://wiki.coderzh.com/demo). Anyone can edit this page.

### Installation
After downloading the source, change `application` in `app.yaml` to your app id in Google App Engine.

    application: yourappname

Since NancyWiki itself does not provide comments system, it uses Disqus in templates. If you want to use comments, you would need to register for a Disqus account and modify `comments` block in `wiki.html` to your code.

    <div id="comments">
        <div id="disqus_thread"></div>
        <script type="text/javascript">
            disqus_developer = 1;
            (function() {
                var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
                dsq.src = 'http://nancywiki.disqus.com/embed.js';
                (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
            })();
        </script>
        <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript=nancywiki">comments powered by Disqus.</a></noscript>
    </div>

After configuration, update your app using

    python appcfg.py update yourappname

Great. Now it is working, you may visit it at: http://yourappname.appspot.com

## Chinese Version

[NancyWiki](https://code.google.com/p/nancywiki/) 是一个基于 GAE 开发的 Wiki 引擎，使用了 Python 2.5 运行时。 NancyWiki-Py27 是它的 Python 2.7 移植版。

### NancyWiki 原始说明

NancyWiki 是基于 Google App Engine 开发的，使用的语言是 Python。Wiki 标记语言采用的是Markdown，因为它简单，易用。

NancyWiki 致力于打造用户真正想要的个人 Wiki 系统。多看书，多学习，多记笔记，就用 NancyWiki！

NancyWiki 尊崇的原则：尽量保持简单，实用。NancyWiki 保持了代码的精简，一共 3 个 Python 文件：main.py, models.py, views.py。同时，提供了完善的换肤功能，让用户更加简单的 DIY 自己的 Wiki 皮肤，现 themes 目录提供了 simple 和 plain 两套皮肤，可以在设置页面随时进行切换。

详细请见：http://wiki.coderzh.com

如果访问不了，请访问：http://coderzh.appspot.com

### 试用
NancyWiki提供了一个[Demo](http://wiki.coderzh.com/demo)页面，任何人都可以对这个页面进行编辑。心动不如行动，赶紧体验一下吧。

### 安装
下载了源码后，打开`app.yaml`文件，修改`application`字段为你的GAE应用的名称：

    application: yourappname

然后，由于NancyWiki本身不提供评论系统（简单原则），而是在模板里挂接Disqus的评论系统。因此，如果想使用Disqus评论系统，请先注册一个Disqus账号，然后学习一下用法。待你了解差不多之后，回过头来，修改一下wiki.html模板中的评论部分的代码为你自己的Disqus代码。

    <div id="comments">
        <div id="disqus_thread"></div>
        <script type="text/javascript">
            disqus_developer = 1;
            (function() {
                var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
                dsq.src = 'http://nancywiki.disqus.com/embed.js';
                (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
            })();
        </script>
        <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript=nancywiki">comments powered by Disqus.</a></noscript>
    </div>

配置完了，上传：

    python appcfg.py update yourappname

太棒了，赶紧体验一下吧，访问：http://yourappname.appspot.com

## License
Copyright 2013 SSHZ.ORG.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This software is a derivative work of NancyWiki by CoderZh.com licensed under Apache License, Version 2.0.
