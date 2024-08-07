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
        ~ Simple Robot Framework ~
    </h1>
    <small>
        一个bot风格的高效异步事件调度框架
            <br/> 
        A Bot-style event scheduling framework, asynchronous and high-performance
</small>
<br />
    <span>
        <a href="https://github.com/simple-robot/simpler-robot" target="_blank"><b>💡核心库</b></a>
    </span> 
    &nbsp; | &nbsp;
    <span>
        <a href="https://simbot.forte.love/" target="_blank">应用手册</a>
    </span>
    &nbsp; | &nbsp;
    <span>
        <a href="https://github.com/orgs/simple-robot/discussions" target="_blank">🏠社区</a>
    </span>
    <br>
    <small> &gt; 走过路过，不要忘记留下闪亮亮的 <b>⭐</b> 喔~ &lt; </small> 
    <br />
   <a href="https://github.com/ForteScarlet/simpler-robot/releases/latest"><img alt="release" src="https://img.shields.io/github/v/release/ForteScarlet/simpler-robot" /></a>

   <img alt="org-stars" src="https://img.shields.io/github/stars/simple-robot?label=org-stars" />
   <img alt="org-discussions" src="https://img.shields.io/github/discussions/simple-robot/Discussions" />

</div>


## 简介

**`Simple Robot`** v4 是一个基于 **KMP** 的多平台 Bot 风格高性能异步事件调度框架（下文简称simbot），
提供统一的异步API和易用的风格设计，可以协助你更快速高效的编写 Bot 风格的事件调度应用。
目前主要应用于对接各种类型的 Bot 应用平台/框架，并提供部分组件库实现。


**`simbot`** 通过 [Kotlin](https://kotlinlang.org/) 语言开发、
基于 [KMP](https://kotlinlang.org/docs/multiplatform.html) 支持多平台，
并兼容Java（**jdk11+**）等JVM平台语言，
且提供大量 Java 友好 API 和 Spring Boot starter，协助你快速开发！

## Why simbot?

- 基于 Kotlin Multiplatform，支持**多平台**！
- 得益于Kotlin与挂起特性，使用**更简洁、更简单**的代码编写更加高效的逻辑！
- **Java友好！** 不会Kotlin？没关系，我们为Java开发者提供了阻塞、异步、响应式等多种风格的API！
- **支持SpringBoot**，助力你快速整合simbot、高效开发！
- **组件化**，不仅易于支持组件间的协同与应用，也使得任意组件库的开发成为可能！
- 不仅仅是API调库侠！simbot提供**更完备的实现与更多高级功能**。<br /><small>屏蔽掉你不想知道的细节，让你更加专注于你的逻辑本身！<i>发送消息？`send` 就完事儿了！</i></small>

## 核心库

核心库是所有组件的前置、标准API的制定者、也是绝大多数统一功能实现的地方。

[**👉前往核心库**](https://github.com/simple-robot/simpler-robot)

## 组件库

<hr />

<table>
<thead>
  <tr>
    <th>组件</th>
    <th>描述</th>
    <th>手册</th>
    <th>API文档</th>
    <th>版本参考</th>
  </tr>
</thead>
<tbody>
<!-- QQ -->
<tr>
<td><a href="https://github.com/simple-robot/simbot-component-qq-guild/" target="_blank">QQ机器人组件</a></td>
<td>对接QQ官方API的QQ机器人多平台组件库，支持QQ群聊、单聊与QQ频道</td>
<td><a href="https://simbot.forte.love/component-qq-guild.html" target="_blank">📕前往手册</a></td>
<td>
<a href="https://docs.simbot.forte.love/components/qq-guild/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-kook/releases">
<img alt="QQ机器人 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-qq-guild">
</a>
</td>
</tr>

<!-- OB -->
<tr>
<td><a href="https://github.com/simple-robot/simbot-component-onebot" target="_blank">OneBot组件</a></td>
<td>对接OneBot客户端协议的多平台组件库</td>
<td><a href="https://simbot.forte.love/component-onebot.html">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/onebot/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-onebot/releases">
<img alt="OneBot组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-onebot">
</a>
</td>
</tr>

<!-- KOOK -->
<tr>
<td><a href="https://github.com/simple-robot/simbot-component-kook" target="_blank">KOOK(开黑啦)组件</a></td>
<td>对接KOOK官方API的多平台组件库</td>
<td><a href="https://simbot.forte.love/component-kook.html" target="_blank">📕前往手册</a></td>
<td>
<a href="https://docs.simbot.forte.love/components/kook/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-kook/releases">
<img alt="KOOK(开黑啦)组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-kook">
</a>
</td>
</tr>

<!-- Telegram -->
<tr>
<td>🚧 <a href="https://github.com/simple-robot/simbot-component-telegram" target="_blank">Telegram组件</a></td>
<td>对接Telegram官方API的多平台组件库</td>
<td><a href="https://simbot.forte.love/component-telegram.html">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/telegram/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-telegram/releases">
<img alt="Telegram组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-telegram">
</a>
</td>
</tr>

<!-- Discord -->
<tr>
<td>🚧 <a href="https://github.com/simple-robot/simbot-component-discord" target="_blank">Discord组件</a></td>
<td>对接Discord官方API的多平台组件库</td>
<td><a href="https://simbot.forte.love/component-discord.html">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/discord/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-discord/releases">
<img alt="Discord组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-discord">
</a>
</td>
</tr>

<!-- kritor -->
<!--
<tr>
<td>🚧 <a href="https://github.com/simple-robot/simbot-component-kritor" target="_blank">Kritor组件</a></td>
<td>-</td>
<td><a href="https://simple-robot.github.io/simbot-component-kritor">📕前往手册</a> (暂无，待建设)</td>
<td><a href="https://docs.simbot.forte.love/components/kritor/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-kritor/releases">
<img alt="Kritor组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-kritor">
</a>
</td>
</tr>
-->

<!-- 濒危 -->
<!--
<tr>
<td>⚠ <a href="https://github.com/simple-robot/simbot-component-mirai" target="_blank">mirai组件</a> <i>濒危</i></td>
<td>对接第三方开源框架Mirai的JVM平台组件库 <br /><i>（组件仅支持simbot3, 且此框架已经不再活跃甚至不再维护，因此组件库不再做跟进更新）</i></td>
<td><a href="https://component-mirai.simbot.forte.love/" target="_blank">📕前往手册</a></td>
<td>
<a href="https://docs.simbot.forte.love/components/mirai/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-mirai/releases">
<img alt="Mirai组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-mirai">
</a>
</td>
</tr>
-->

<!-- 已逝 -->
<!--
<tr>
<td>💀 <a href="https://github.com/simple-robot/simbot-component-miyoushe-villa" target="_blank"><del>米游社组件</del></a> <b>已逝</b></td>
<td>对接米游社大别野官方API的多平台组件库 <br /><i>米游社大别野已成为历史</i></td>
<td><a href="https://simple-robot.github.io/simbot-component-miyoushe-villa">📕前往手册</a></td>
<td><a href="https://docs.simbot.forte.love/components/miyoushe-villa/">API文档</a>
</td>
<td>
<a href="https://github.com/simple-robot/simbot-component-miyoushe-villa/releases">
<img alt="米游社组件 Releases" src="https://img.shields.io/github/v/release/simple-robot/simbot-component-miyoushe-villa">
</a>
</td>
</tr>
-->

</tbody>

</table>

## 走马观花

**Kotlin & simbot-core**

```kotlin
suspend fun main() {
   val application = launchSimpleApplication {
        findAndInstallAllPlugins(true)
        findAndInstallAllComponents(true)
   }
   
   application.listeners {
          // 事件监听
          process<ContactMessageEvent> { event -> // this: EventProcessingContext
             event.reply("Hello, Simbot")
          }
      }
   
   application.join()
}
```

**Java & Spring Boot**

```java
@SpringBootApplication
@EnableSimbot // 启用simbot
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }

    // 可以选择阻塞、异步或响应式等多种不同风格的 Java API
    // 前排提醒：这里仅供示例，不建议混用多种风格，尤其是阻塞和异步混用。

    /** 事件监听，监听一个通用的标准事件类型 */
    @Listener
    public void onFriendMessage(ChatChannelMessageEvent event) {
        event.replyBlocking("Hello, Simbot!");
    }

    /**
     * 假设：你在使用Telegram组件，那么此处为监听 Telegram 的普通群消息事件
     * 并且这里以 reactor API 为例
     */
    @Listener
    public Mono<Void> onTelegramChatGroupMessage(TelegramChatGroupMessageEvent event) {
        return event.replyReserve("Hello, Simbot!").transform(SuspendReserve.mono()).then();
    }

     /**
     * 假设：你在使用KOOK组件，那么此处为监听KOOK的聊天子频道消息事件
     * 并且这里以 Java async API 为例
     */
    @Listener
    public CompletableFuture<?> onKookChannelMessage(KookChannelMessageEvent event) {
        return event.replyAsync("Hello, Simbot!");
    }
}
```

**Kotlin 构建消息**

```Kotlin
// 单个消息元素
val text = "你好".toText()
val at = At(123456.ID)
// 组装消息链
val messages = text + at
// 构建消息链
val built = buildMessages {
    +"你好"
    +at
    +Face(666.ID)
}
```

**Java 构建消息**

```Java
// 单个消息元素
var text = Text.of("你好");
var at = new At(Identifies.of(123456));
// 组装消息链
var messages = Messages.of(text, at);
// 构建消息链
var built = MessagesBuilder.create()
    .add("你好")
    .add(at)
    .add(new Face(Identifies.of(666)))
    .build();
```

> [!note]
> 针对不同的平台，各组件还可能会提供更多组件专属的消息元素类型，比如QQ频道中的 Ark 或 markdown 等。

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


✨除了前往社群，一同建设 [**社区**](https://github.com/orgs/simple-robot/discussions) 是我们最推荐的相互交流的方式。如果你发现了一些问题，也可以通过 [**Issues**](https://github.com/simple-robot/simpler-robot/issues) 进行反馈。
与他人交流，并留下你的足迹吧！


## 🤔 猜你感兴趣

### 文档/API文档

是一个不仔细看的坏孩子呢。文档的话，在最上面的 [**官网**](https://simbot.forte.love/) 就是喔。核心库的API文档（KDoc）也可以在那里面找到。

当然，我们也提供了一个 [**文档引导站点**](https://docs.simbot.forte.love) 供你选择。

### 教学视频

你也许可以去 [这个B站视频](https://www.bilibili.com/video/BV1vA411o7A3/) 的所属合集中看看。

## 🙋 你在吗？

你有在使用simbot吗? 通过为你的仓库 [添加 `simbot` 主题](https://docs.github.com/zh/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics) 来告诉我们吧!

## 组件库开发

除了直接使用组件开发应用，simbot也支持使用 Kotlin 开发任意的自定义组件。

我们从 simbot4 开始会持续提供一些用于开发**组件库/插件库**的模板项目，如果你感兴趣，
在阅读**组件开发**相关文档之余也可以试试它们喔！

**开发模板**

> [!warning]
> **组件开发**与应用开发不同，不要搞混喔。
> 
> 模板项目不一定会更新的很及时，如果你有发现任何描述错误、落后的版本、错误的逻辑，也都欢迎为其提交 issue 或 pr，感谢您的协助！

- 🍓 [**基于KMP的组件库模板**](https://github.com/simple-robot/simbot4-multiplatform-component-template)

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

<a href="https://github.com/simple-robot/simpler-robot">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=simple-robot/simpler-robot&type=Date" />
  </picture>
</a>

<br />

> _powered by [Star History](https://star-history.com/)_

[simbot-core-home]: https://github.com/simple-robot/simpler-robot

