<!--suppress HtmlDeprecatedAttribute -->
<div align="center">
    <a href="https://simbot.forte.love/">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/simple-robot/.github/main/logo-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/simple-robot/.github/main/logo.svg" />
  <img alt="simbot logo" src="https://raw.githubusercontent.com/simple-robot/.github/main/logo.svg" width="260" />
</picture>
    </a>
    <h1>
        - 🎉 欢迎！ -
    </h1>
    <small>
        ~ Simple Robot Framework ~      
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
   
   <h1></h1><!-- 更细的 'hr' -->
   <p><i><small>一个bot风格的高效异步事件调度框架 / A Bot-style event scheduling framework, asynchronous and high-performance</small></i></p>

</div>


## 简介

**`Simple Robot`** v4 是一个基于 **KMP** 的多平台 Bot 风格高性能异步事件调度框架（下文简称simbot），
提供统一的异步API和易用的风格设计，可以协助你更快速高效的编写 Bot 风格的事件调度应用。
目前主要应用于对接各种类型的 Bot 应用平台/框架，并提供部分组件库实现。


**`simbot`** 通过 [Kotlin](https://kotlinlang.org/) 语言开发、
基于 [KMP](https://kotlinlang.org/docs/multiplatform.html) 支持多平台，
并兼容Java（**jdk11+**）等JVM平台语言，
且提供大量 Java 友好 API 和 Spring Boot starter，协助你快速开发。


## 核心库

核心库是所有组件的前置、标准API的制定者、也是绝大多数统一功能实现的地方。[**👉前往核心库**](https://github.com/simple-robot/simpler-robot)

## 走马观花

**Kotlin core**

```kotlin
suspend fun main() {
   val application = launchSimpleApplication {
        findAndInstallAllPlugins(true)
        findAndInstallAllComponents(true)
   }
   
   application.listeners {
          // 事件监听
          process<FriendMessageEvent> { event -> // this: EventProcessingContext
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
    public Mono<?> onFriendMessage(ChatChannelMessageEvent event) {
        event.replyBlocking("Hello, ");
        event.getContentAsync().thenCompose(chatChannel -> chatChannel.sendAsync("Simbot"));
        return event.replyReserve("爱你").transform(SuspendReserve.mono());
        // 可以选择阻塞、异步或响应式等多种不同风格的 Java API
        // 前排提醒：这里仅供示例，不建议混用多种风格，尤其是阻塞和异步混用。
    }
}
```


<br />

## 社群 / Communities

<details><summary>👉 展开查看<b> QQ群</b></summary>

群号：[点击加入 185375305](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=qXs-qowPJFHVfTeAklMWrQXjmuIuCWRv&authKey=U0CnmHB5YTLkYNgkqEp22qYofX%2Fgo%2BzoYI5QM%2FlVdLWuJ5%2BU0ge0KviRdZ%2FQuwEz&noverify=0&group_code=185375305)

![S9YOY3DF{5CGIZIKNVIM~70_tmb](https://github.com/simple-robot/.github/assets/40045247/8b463829-515b-4498-babc-ce226e2c567a)

</details>

<details><summary>👉 展开查看<b> QQ频道</b></summary>

QQ频道：[点击加入QQ频道](https://pd.qq.com/s/ge096m1xq)

![DEK66C_%WLD__C0KJR180%4](https://github.com/simple-robot/.github/assets/40045247/c69eb850-c754-4a14-92bf-6de1fbee8a86)

</details>

<details><summary>👉 展开查看<b> Discord</b></summary>

Discord: [点击加入Discord](https://discord.gg/eFB3HeBp9B)


</details>


✨一同建设 [**社区**](https://github.com/orgs/simple-robot/discussions) 是我们最推荐的相互交流的方式。如果你发现了一些问题，可以通过 [**Issues**](https://github.com/simple-robot/simpler-robot/issues) 进行反馈。
与他人交流，并留下你的足迹吧！



## 🤔 猜你感兴趣

### 文档/API文档

是一个不仔细看的坏孩子呢。文档的话，在最上面的 [**官网**](https://simbot.forte.love/) 就是喔。核心库的API文档（KDoc）也可以在那里面找到。

当然，我们也提供了一个 [**文档引导站点**](https://docs.simbot.forte.love) 供你选择。

### 教学视频

你也许可以去 [这个B站视频](https://www.bilibili.com/video/BV1vA411o7A3/) 的所属合集中看看。

## 🙋 你在吗？

你有在使用simbot吗? 通过为你的仓库 [添加 `simbot` 主题](https://docs.github.com/zh/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics) 来告诉我们吧!

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
<a href="https://github.com/simple-robot/simbot-component-kook/releases">
<img alt="QQ频道 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-qq-guild">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-qq-guild-core/">
<img alt="QQ频道 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-qq-guild-core%2Fmaven-metadata.xml&label=snapshot">
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
<a href="https://github.com/simple-robot/simbot-component-kook/releases">
<img alt="KOOK(开黑啦)组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-kook">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-kook-core/">
<img alt="KOOK(开黑啦)组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-kook-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>🚧 Discord组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-discord" target="_blank">👉前往仓库</a></td>
<td><a href="https://simple-robot.github.io/simbot-component-discord">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/discord">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-discord/releases">
<img alt="Discord组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-discord">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-discord-core/">
<img alt="Discord组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-discord-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<tr>
<td>🚧 Telegram组件</td>
<td><a href="https://github.com/simple-robot/simbot-component-telegram" target="_blank">👉前往仓库</a></td>
<td><a href="https://simple-robot.github.io/simbot-component-telegram">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/telegram">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-telegram/releases">
<img alt="Telegram组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-telegram">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-telegram-core/">
<img alt="Telegram组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-telegram-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<!-- 濒危 -->
<tr>
<td>⚠ mirai组件 <i>濒危</i></td>
<td><a href="https://github.com/simple-robot/simbot-component-mirai" target="_blank">👉前往仓库</a></td>
<td><a href="https://component-mirai.simbot.forte.love/" target="_blank">📕前往手册</a></td>
<td>
<a href=https://docs.simbot.forte.love/components/mirai">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-mirai/releases">
<img alt="Mirai组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-mirai">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-mirai-core/">
<img alt="Mirai组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-mirai-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>

<!-- 已逝 -->
<tr>
<td>💀 <del>米游社组件</del> <b>已逝</b></td>
<td><a href="https://github.com/simple-robot/simbot-component-miyoushe-villa" target="_blank">👉前往仓库</a></td>
<td><a href="https://simple-robot.github.io/simbot-component-miyoushe-villa">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/miyoushe-villa">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-miyoushe-villa/releases">
<img alt="米游社组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-miyoushe-villa">
</a>
</td>
<td>
<a href="https://oss.sonatype.org/content/repositories/snapshots/love/forte/simbot/component/simbot-component-miyoushe-villa-core/">
<img alt="米游社组件 Snapshot" src="https://img.shields.io/maven-metadata/v?metadataUrl=https%3A%2F%2Foss.sonatype.org%2Fcontent%2Frepositories%2Fsnapshots%2Flove%2Fforte%2Fsimbot%2Fcomponent%2Fsimbot-component-miyoushe-villa-core%2Fmaven-metadata.xml&label=snapshot">
</a>
</td>
</tr>


</tbody>

</table>

## 组件库开发模板

> [!note]
> 首先前排提示一下，这是指的**组件开发**，并非普通应用开发。

我们从 simbot4 开始会持续提供一些用于开发**组件库/插件库**的模板项目，如果你感兴趣，
在阅读**组件开发**相关文档之余也可以试试它们喔

> [!warning]
> 模板项目不一定会更新的很及时，如果你有发现任何描述错误、落后的版本、错误的逻辑，也都欢迎为其提交 issue 或 pr，感谢您的协助！

- [基于KMP的组件库模板](https://github.com/simple-robot/simbot4-multiplatform-component-template)

## 📚 图书馆

如果你想要找核心库或者各个组件的 **API Doc** 或者文档地址的话，也许你可以去 [**📚 图书馆**](https://github.com/simple-robot-library) 看看~

## 🤝 协助我们

⭐ 为你青睐的仓库贡献一枚star或参与到[社区](https://github.com/orgs/simple-robot/discussions)的活跃建设中就是对我们最大的鼓励与帮助！

⭐ 如果你希望参与项目的建设，欢迎通过PR对某一仓库进行贡献！

⭐ 我们的开发团队生产力非常低，因为人手总是不足。如果你也想要参与到我们的团队中来，欢迎通过[**邮箱**](mailto:ForteScarlet@163.com)、[**社区**](https://github.com/orgs/simple-robot/discussions)、**QQ频道** 或 **QQ群** 联系我们~

## ✨ 贡献星星！

如果你喜欢 Simple Robot, 那么不妨前往[核心库][simbot-core-home]以及你所青睐的组件为它点个可爱的🌟~

你的支持就是最优质的更新动力，非常感谢❤️

<!-- Star History -->

<a href="https://star-history.com/#simple-robot/simpler-robot&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date" />
  </picture>
</a>

<br />

<a href="https://star-history.com/#simple-robot/simbot-component-kook&simple-robot/simbot-component-qq-guild&simple-robot/simbot-component-mirai&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=simple-robot/simbot-component-kook%2Csimple-robot/simbot-component-qq-guild%2Csimple-robot/simbot-component-mirai&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=simple-robot/simbot-component-kook%2Csimple-robot/simbot-component-qq-guild%2Csimple-robot/simbot-component-mirai&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=simple-robot/simbot-component-kook%2Csimple-robot/simbot-component-qq-guild%2Csimple-robot/simbot-component-mirai&type=Date" />
  </picture>
</a>



> _powered by [Star History](https://star-history.com/)_

[simbot-core-home]: https://github.com/simple-robot/simpler-robot

