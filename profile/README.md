<!--suppress HtmlDeprecatedAttribute -->
<div align="center">
    <a href="https://simbot.forte.love/"><img src="/logo.png" alt="logo" style="width:230px; height:230px; border-radius:50%; " /></a>
    <h1>
        - 🎉 欢迎！ -
    </h1>
    <small>
        ~ simple robot framework ~      
</small>
<br>
    <span>
        <a href="https://github.com/simple-robot/simpler-robot" target="_blank">核心仓库</a>
    </span> 
    &nbsp; | &nbsp;
    <span>
        <a href="https://simbot.forte.love/" target="_blank">官网</a>
    </span>
    &nbsp; | &nbsp;
    <span>
        <a href="https://github.com/orgs/simple-robot/discussions" target="_blank">🏠社区</a>
    </span> <br />
    <small> &gt; 感谢 <a href="https://github.com/ForteScarlet/CatCode" target="_blank">CatCode</a> 开发团队成员制作的simbot logo &lt; </small>
    <br>
    <small> &gt; 走过路过，不要忘记留下闪亮亮的⭐喔~ &lt; </small> 
    <br>
   <a href="https://github.com/ForteScarlet/simpler-robot/releases/latest"><img alt="release" src="https://img.shields.io/github/v/release/ForteScarlet/simpler-robot" /></a>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/simbot-api/" target="_blank">
  <img alt="release" src="https://img.shields.io/maven-central/v/love.forte.simbot/simbot-api" /></a>
<a href="https://www.yuque.com/simpler-robot/simpler-robot-doc" target="_blank">
  <img alt="doc" src="https://img.shields.io/badge/doc-yuque-brightgreen" /></a>
   <hr>
   <img alt="stars" src="https://img.shields.io/github/stars/ForteScarlet/simpler-robot" />
   <img alt="forks" src="https://img.shields.io/github/forks/ForteScarlet/simpler-robot" />
   <img alt="watchers" src="https://img.shields.io/github/watchers/ForteScarlet/simpler-robot" />
   <img alt="repo-size" src="https://img.shields.io/github/repo-size/ForteScarlet/simpler-robot" />
   
   <img alt="issues" src="https://img.shields.io/github/issues-closed/ForteScarlet/simpler-robot?color=green" />
   <img alt="last-commit" src="https://img.shields.io/github/last-commit/ForteScarlet/simpler-robot" />
   <img alt="search-hit" src="https://img.shields.io/github/search/simple-robot/simpler-robot/simbot" />
   <img alt="top-language" src="https://img.shields.io/github/languages/top/ForteScarlet/simpler-robot" />
<a href="./COPYING"><img alt="copying" src="https://img.shields.io/github/license/ForteScarlet/simpler-robot" /></a>

<br>

</div>

<br />

## 简介

**`Simple Robot`** 是一个JVM平台（和多平台）的bot风格事件调度框架（下文简称simbot），提供统一的异步API和易用的风格设计，可以协助你更快速高效的编写bot风格的事件调度应用。目前主要应用于对接各种类型的bot应用平台/框架，并提供统一的API实现。

**`simbot`** 通过 [Kotlin](https://kotlinlang.org/) 语言开发并兼容Java（jdk8+）等JVM平台语言，且提供Javaer最爱的Spring Boot Starter，协助你快速开发。

## 走马观花

```kotlin
suspend fun main() {
   createSimpleApplication {
      listeners {
          // 事件监听
          FriendMessageEvent { event -> // this: EventProcessingContext
             event.reply("Hello, Simbot")
          }
      }
   }.join()
}
```

**Java(Spring Boot Starter)**

```java
@SpringBootApplication
@EnableSimbot // 启用
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
    
    /** 事件监听 */
    @Listener
    public void onFriendMessage(FriendMessageEvent event) {
        event.replyBlocking("Hello, ");
        event.getFriend().sendAsync("Simbot");
        // 阻塞或异步的不同风格的Java API
    }
}
```


<br />

## 组件引导

### 组件库

<hr />

<table>
<thead>
  <tr>
    <th rowspan="2">组件</th>
    <th rowspan="2">仓库</th>
    <th rowspan="2">使用手册</th>
    <th rowspan="2">api文档</th>
    <th colspan="2">
版本参考

</th>
  </tr>
  <tr>
    <th>RELEASES</th>
    <th>SNAPSHOT</th>
  </tr>
</thead>
<tbody>
<tr>
<td>腾讯频道组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-tencent-guild" target="_blank">👉前往仓库</a></td>
<td><a href="https://www.yuque.com/simpler-robot/simpler-robot-doc/mudleb" target="_blank">语雀文档</a></td>
<td>
<a href="https://simple-robot-library.github.io/simbot3-component-tencent-guild-apiDoc">API文档</a>
</td>
<td>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-tencent-guild-core/">
<img alt="腾讯频道 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-tencent-guild-core?label=releases">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-tencent-guild-core/">
<img alt="腾讯频道 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-tencent-guild-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>mirai组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-mirai" target="_blank">👉前往仓库</a></td>
<td><a href="https://www.yuque.com/simpler-robot/simpler-robot-doc/mudleb" target="_blank">语雀文档</a></td>
<td>
<a href="https://simple-robot-library.github.io/simbot3-component-mirai-apiDoc">API文档</a>
</td>
<td>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-mirai-core/">
<img alt="Mirai组件 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-mirai-core?label=releases">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-mirai-core/">
<img alt="Mirai组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-mirai-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>Kook(开黑啦)组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-kook" target="_blank">👉前往仓库</a></td>
<td><a href="https://www.yuque.com/simpler-robot/simpler-robot-doc/mudleb" target="_blank">语雀文档</a></td>
<td>
<a href="https://simple-robot-library.github.io/simbot3-component-kaiheila-apiDoc">API文档</a>
</td>
<td>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="Kook(开黑啦)组件 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-kook-core?label=releases">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="Kook(开黑啦)组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-kook-core%2Fmaven-metadata.xml&label=snapshot">
</a>

</td>
</tr>
</tbody>

</table>


## 📚 图书馆

如果你想要找核心库或者各个组件的 **API Doc** 或者文档地址的话，也许你可以去 [**📚 图书馆**](https://github.com/simple-robot-library) 看看~

## 🕶 交流与反馈

一同建设 [**社区**](https://github.com/orgs/simple-robot/discussions) 是我们最推荐的相互交流的方式。如果你发现了一些问题，可以通过 [**Issues**](https://github.com/simple-robot/simpler-robot/issues) 进行反馈。

如果想要讨论与simbot相关的内容，可以添加交流群 [`185375305`](https://jq.qq.com/?_wv=1027&k=NqEoJTK2) ，但是要注意，群里不应该也不接受反馈问题，主要内容以互相交流为主。

## 🤝 协助我们

⭐为你青睐的仓库贡献一枚star或参与到[社区](https://github.com/orgs/simple-robot/discussions)的活跃建设中就是对我们最大的鼓励与帮助！

⭐如果你希望参与项目的建设，欢迎通过PR对某一仓库进行贡献！

⭐我们的开发团队生产力非常低，因为人手总是不足。如果你也想要参与到我们的团队中来，欢迎通过[邮箱](mailto:ForteScarlet@163.com)、[社区](https://github.com/orgs/simple-robot/discussions)、[群聊](https://jq.qq.com/?_wv=1027&k=NqEoJTK2) 联系我们~


## ✨ 贡献星星！

如果你喜欢 Simple Robot, 那么不妨前往[核心库][simbot-core-home]以及你所青睐的组件为它点个可爱的🌟~

你的支持就是最优质的更新动力，非常感谢❤️

[![Star History Chart](https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date)](https://star-history.com/#simple-robot/simpler-robot&Date)

[![Star History Chart](https://api.star-history.com/svg?repos=simple-robot/simbot-component-tencent-guild,simple-robot/simbot-component-mirai,simple-robot/simbot-component-kook&type=Date)](https://star-history.com/#simple-robot/simbot-component-tencent-guild&simple-robot/simbot-component-mirai&simple-robot/simbot-component-kook&Date)

> _powered by [Star History](https://star-history.com/)_

[simbot-core-home]: https://github.com/simple-robot/simpler-robot

