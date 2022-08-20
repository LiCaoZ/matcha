# FAQ（或者可能会被问到的问题）

Q：为什么启用主题过后，首页的文章列表会直接显示全文内容？
A：如果不想显示全文，可以在文章编辑器里，把想要显示在首页的内容和希望读者进入文章页面阅读的内容用 `<!--more-->` 隔开，这样首页就只会显示 `<!--more-->` 前面的内容；如果觉得麻烦，可以把主题的设置「文章摘要显示模式」改为「阶段前200字符」或「不显示摘要」。

Q：演示站里有下拉框和 NOTICE 这样的组件，怎样才能用到我的博客文章里？
A：这些功能是用 [BracketDown](https://github.com/BigCoke233/typecho-plugin-BracketDown) 插件实现的，主题只是对插件做了适配

Q：为什么启用主题后，我的网站跟演示站看起来不一样？
A：主题内置有两种样式，分别是 Ringo 和 Journal，演示站使用的是 Journal，而默认是 Ringo 哦，需要在后台设置1里修改

Q：前面提到的两种样式，它们之间有什么区别？
A：这两种样式的设计分别取自 Ringo 主题和 Journal 主题，他们都是 Matcha 主题的前身。
启用任何一个都不会影响主题的功能，只是看起来不太一样而已。Ringo 看起来更加简洁，Journal 看起来更大气，按照自己的品味选择一个就好啦。

Q：为什么我启用某些插件后，前台的一些功能失效了？（例如 pjax 失效，返回顶部按钮失效）
A：一些插件为了在前台实现某些功能，引入了 `jQuery`，主题也引入了这个库，重复引用会导致问题。
一般来说，插件作者会在插件设置里留一个可以关闭 `jQuery` 引入的选项，把可疑的插件都排查一下。

Q：为什么启用主题后，些插件和我自己添加的 js 代码不能正常运行？
A：这可能是因为主题使用了 pjax 的原因，一些新出现在页面中的内容不会被 js 重新加载，你需要在主题的设置「Pjax 回调函数」里写入代码重载相应的功能；一般来说，需要重载的插件会提供对应的回调函数，或者直接在搜索引擎搜索也能找到，但也会遇到没有现成代码的情况，就需要自己写或者寻求他人帮助了。

Q：为什么我启用主题之后，页面变得很奇怪，背景是纯白色，页面的内容也乱了？
A：这是 css 和 js 没能正确引入导致的。检查 Typecho 的站点地址设置，看看里面填写的是不是自己博客现在的地址，注意 http 和 https 有没有写对；如果没能解决的话，查看网页源代码，看看引入的 css 和 js 地址到底是什么。

Q：我的博客不是一个人维护的，能不能加入显示文章作者的功能？
A：大概率不能，Matcha 主题的定位一直是个人独立博客主题。

Q：我好像遇到了 bug，我该怎么办？
A：不是任何问题都是 bug，你需要在将这个 bug 提交给作者之前做一些简单的确认：
1. 如果你修改或者添加了一些代码，还原他们，看看问题会不会复现；
2. 关闭所有的插件，看看问题会不会复现；
3. 切换成其他主题，看看问题会不会复现。
在确定这个问题的确是主题自身造成的之后，再通过发布 Issues 或者其他联系方式反馈给作者