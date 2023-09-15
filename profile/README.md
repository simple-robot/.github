<!--suppress HtmlDeprecatedAttribute -->
<div align="center">
    <a href="https://simbot.forte.love/"><img src="https://raw.githubusercontent.com/simple-robot/.github/main/logo.png" alt="logo" style="width:230px; height:230px; border-radius:50%; " /></a>
    <h1>
        - 🎉 欢迎！ -
    </h1>
    <small>
        ~ simple robot framework ~      
</small>
<br>
    <span>
        <a href="https://github.com/simple-robot/simpler-robot" target="_blank"><b>💡核心仓库</b></a>
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

   <img alt="org-stars" src="https://img.shields.io/github/stars/simple-robot?label=org-stars" />
   <img alt="org-discussions" src="https://img.shields.io/github/discussions/simple-robot/Discussions" />
     

</div>


## 简介

**`Simple Robot`** 是一个JVM平台（和多平台）的bot风格事件调度框架（下文简称simbot），提供统一的异步API和易用的风格设计，可以协助你更快速高效的编写bot风格的事件调度应用。目前主要应用于对接各种类型的bot应用平台/框架，并提供统一的API实现。

**`simbot`** 通过 [Kotlin](https://kotlinlang.org/) 语言开发并兼容Java（jdk8+）等JVM平台语言，且提供Javaer最爱的Spring Boot Starter，协助你快速开发。

## 核心库

核心库是所有组件的前置、标准API的制定者、也是绝大多数统一功能实现的地方。[**👉前往核心库**](https://github.com/simple-robot/simpler-robot)

## 走马观花

**Kotlin core**

```kotlin
suspend fun main() {
   val application = createSimpleApplication {
      installAll() // try to install all components
   }
   
   application.eventListenerManager.listeners {
          // 事件监听
          FriendMessageEvent { event -> // this: EventProcessingContext
             event.reply("Hello, Simbot")
          }
      }
   
   application.join()
}
```

**Java(Spring Boot Starter)**

```java
@SpringBootApplication
@EnableSimbot // 启用simbot
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
    
    /** 事件监听 */
    @Listener
    public void onFriendMessage(FriendMessageEvent event) {
        event.replyBlocking("Hello, ");
        event.getFriendAsync().thenCompose(friend -> friend.sendAsync("Simbot"));
        // 可以选择阻塞或异步的不同风格的Java API
    }
}
```


<br />

## 🤔 猜你感兴趣

### 示例项目/模板项目 

如果你在寻找可以用作示例、或能稍微快速使用的模板项目，那么或许 [simbot-examples](https://github.com/simple-robot/simbot-examples) 和 [simbot-archetypes](https://github.com/simple-robot/simbot-archetypes) 可以帮到你。

### 文档/API文档

是一个不仔细看的坏孩子呢。文档的话，在最上面的 [**官网**](https://simbot.forte.love/) 就是喔。核心库的API文档（KDoc）也可以在那里面找到。

当然，我们也提供了一个 [**文档引导站点**](https://docs.simbot.forte.love) 供你选择。

### 教学视频

你也许可以去 [这个B站视频](https://www.bilibili.com/video/BV1vA411o7A3/) 的所属合集中看看。


## 🙋 你在吗？

你有在使用simbot吗? 通过为你的仓库[添加 `simbot` 主题](https://docs.github.com/zh/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)来告诉我们吧!

## 🐾体验如何？

体验如何？到 [👉这个**投票帖**](https://github.com/orgs/simple-robot/discussions/2) 来分享一下你的使用体验吧 ( •̀ ω •́ )✧


## 组件引导

### 组件库

<hr />

<table>
<thead>
  <tr>
    <th rowspan="2">组件</th>
    <th rowspan="2">仓库</th>
    <th rowspan="2">手册</th>
    <th rowspan="2">API文档</th>
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
<td>QQ频道组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-qq-guild/" target="_blank">👉前往仓库</a></td>
<td><a href="https://simple-robot.github.io/simbot-component-qq-guild/" target="_blank">📕前往手册</a></td>
<td>
<a href="https://docs.simbot.forte.love/components/qq-guild">API文档</a>
</td>
<td>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-qq-guild-core/">
<img alt="QQ频道 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-qq-guild-core?label=releases">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-qq-guild-core/">
<img alt="QQ频道 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-qq-guild-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>mirai组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-mirai" target="_blank">👉前往仓库</a></td>
<td><a href="https://component-mirai.simbot.forte.love/" target="_blank">📕前往手册</a></td>
<td>
<a href=https://docs.simbot.forte.love/components/mirai">API文档</a>
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
<td>KOOK(开黑啦)组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-kook" target="_blank">👉前往仓库</a></td>
<td><a href="https://component-kook.simbot.forte.love/" target="_blank">📕前往手册</a></td>
<td>
<a href="https://docs.simbot.forte.love/components/kook">API文档</a>
</td>
<td>
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="KOOK(开黑啦)组件 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-kook-core?label=releases">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="KOOK(开黑啦)组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-kook-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>米游社组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-miyoushe" target="_blank">👉前往仓库</a></td>
<td>📕前往手册(TODO)</td>
<td>
API文档(TODO)
</td>
<td>
TODO
<!--
<a href="https://repo1.maven.org/maven2/love/forte/simbot/component/simbot-component-miyoushe-core/">
<img alt="米游社组件 Releases" src="https://img.shields.io/maven-central/v/love.forte.simbot.component/simbot-component-miyoushe-core?label=releases">
</a>
-->
</td>
<td>
TODO
<!--
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="米游社组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-kook-core%2Fmaven-metadata.xml&label=snapshot">
-->
</a>
</td>
</tr>


</tbody>

</table>


## 📚 图书馆

如果你想要找核心库或者各个组件的 **API Doc** 或者文档地址的话，也许你可以去 [**📚 图书馆**](https://github.com/simple-robot-library) 看看~

## 🕶 交流与反馈

✨一同建设 [**社区**](https://github.com/orgs/simple-robot/discussions) 是我们最推荐的相互交流的方式。如果你发现了一些问题，可以通过 [**Issues**](https://github.com/simple-robot/simpler-robot/issues) 进行反馈。

✨如果想要讨论与simbot相关的内容，可以添加QQ交流群 [`185375305`](https://jq.qq.com/?_wv=1027&k=0HVo8aFV) 或者加入 [QQ频道](https://pd.qq.com/s/anzubgojn)。但是要注意，群里不应该也不接受反馈问题，主要以互相交流为主。

> **Note**
> 
> 我们仍在考虑是否真的**有必要**提供交流群。

## 🤝 协助我们

⭐为你青睐的仓库贡献一枚star或参与到[社区](https://github.com/orgs/simple-robot/discussions)的活跃建设中就是对我们最大的鼓励与帮助！

⭐如果你希望参与项目的建设，欢迎通过PR对某一仓库进行贡献！

⭐我们的开发团队生产力非常低，因为人手总是不足。如果你也想要参与到我们的团队中来，欢迎通过[邮箱](mailto:ForteScarlet@163.com)、[社区](https://github.com/orgs/simple-robot/discussions)、[QQ频道](https://pd.qq.com/s/anzubgojn) 或 [QQ群聊](https://jq.qq.com/?_wv=1027&k=NqEoJTK2) 联系我们~


## ✨ 贡献星星！

如果你喜欢 Simple Robot, 那么不妨前往[核心库][simbot-core-home]以及你所青睐的组件为它点个可爱的🌟~

你的支持就是最优质的更新动力，非常感谢❤️


[![Star History Chart](https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date)](https://star-history.com/#simple-robot/simpler-robot&Date)


[![Star History Chart](https://api.star-history.com/svg?repos=simple-robot/simbot-component-qq-guild,simple-robot/simbot-component-mirai,simple-robot/simbot-component-kook,simple-robot/simbot-component-miyoushe&type=Date)](https://star-history.com/#simple-robot/simbot-component-qq-guild&simple-robot/simbot-component-mirai&simple-robot/simbot-component-kook&simple-robot/simbot-component-miyoushe&Date)


> _powered by [Star History](https://star-history.com/)_

[simbot-core-home]: https://github.com/simple-robot/simpler-robot

