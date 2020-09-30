# ngNext-hackthon-2020

本项目是 [NG+ Next 2020新生代开发者大赛 -- NG+ Next Hackathon](http://ngplus.world/#hackathon) 中 Conversational AI 主题的学习资料。

## 关于 NG+ Next Hackathon

[NG+ Next 2020新生代开发者大赛 -- NG+ Next Hackathon](http://ngplus.world/#hackathon)在[NG+ 开发者大会 2020](http://ngplus.world/) 期间举办，意在为青年开发者提供展示自己的舞台。参与比赛即有机会! 在比赛中展示你的才华，发现编程的魅力，结交志同道合的伙伴!

大赛通过 [HackHub 网站](https://event.hackhub.cn/event/ng2020) 进行报名，按赛事要求经过海选和专家评比，最终获胜者将得到在 NG+ 开发者大会 2020 上分享的机会，并赢得丰厚的奖励。[HackHub 网站](https://event.hackhub.cn/event/ng2020) 上有详细的大赛主题、参赛对象、大赛安排、评分标准、赛事奖励、活动组织单位的介绍，可点击链接查看详细内容。

本届大赛包括4个主题：
- Angular
- TensorFlow.js
- Conversational AI
- XR

## Conversational AI 学习资料

人工智能的发展带动了对话式交互领域研究的深入，Chatbot 的应用场景越来越丰富。本次大赛希望参赛队伍发挥想象力和创新精神，发掘出多样的 Chatbot 人工智能落地应用，参赛项目将由 [Wechaty](https://wechaty.js.org/) 提供社区支持，[句子互动](https://www.juzibot.com/) 提供云服务的支持。

### Wechaty 

![wechaty-logo](https://camo.githubusercontent.com/d9a57af0493282f9599725857ae7bcd85297a43c/68747470733a2f2f776563686174792e6a732e6f72672f696d672f776563686174792d6c6f676f2e737667)

[Wechaty](https://github.com/wechaty/wechaty) 是一个针对 Chatbot 开发者提供的 Conversational SDK, 开发者通过6行代码即可快速搭建一个聊天机器人，支持[微信个人号](https://github.com/wechaty/wechaty-puppet-padplus)、[微信公众号](https://github.com/wechaty/wechaty-puppet-official-account)、钉钉、抖音、[WhatsApp](https://github.com/wechaty/wechaty-puppet-whatsapp)、Gitter(https://github.com/wechaty/wechaty-puppet-gitter) 等各大主流IM平台。项目支持 [JavaScript](https://github.com/Wechaty/wechaty), [Python](https://github.com/Wechaty/python-wechaty/), [Go](https://github.com/Wechaty/go-wechaty/), [Java](https://github.com/Wechaty/java-wechaty/) 等10种语言，同时可跨平台支持[Linux, Windows, MacOS](https://github.com/wechaty/wechaty/actions?query=workflow%3ANPM) 和 [Docker](https://github.com/wechaty/wechaty/actions?query=workflow%3ADocker).

相关介绍：

:octocat: <https://github.com/Wechaty/wechaty>  
:beetle: <https://github.com/Wechaty/wechaty/issues>  
:book: <https://github.com/Wechaty/wechaty/wiki>  
:whale: <https://hub.docker.com/r/wechaty/wechaty>  

值得注意的是，微信个人号功能非常强大和灵活，是一个非常适合用来做ChatBot的载体。它可以灵活不受限制的发送语音短信、视频、图片和文字，支持多人群聊。但是使用微信个人微信号作为ChatBot，需要通过非官方的第三方库接入微信。因为截至2018年底，微信尚无任何官方的ChatBot API发布。  

在GitHub上可以找到很多支持微信个人号接入的第三方类库，其中大多都是基于Web Wechat的API来实现的，如基于Python的WeixinBot，基于Node.js的Wechaty等。少数支持非Web协议的库，大多是商业私有闭源的，Wechaty是少有的开源项目支持非Web协议的类库。

只需要6行代码，你就可以 通过个人号 搭建一个 微信机器人功能 ，用来自动管理微信消息。

```ts
import { Wechaty } from 'wechaty'

Wechaty.instance()
.on('scan',        qrcode  => console.log('扫码登录：' + qrcode))
.on('login',       user    => console.log('登录成功：' + user))
.on('message',     message => console.log('收到消息：' + message))
.on('friendship',  friendship => console.log('收到好友请求：' + friendship))
.on('room-invite', invitation => console.log('收到入群邀请：' + invitation))
.start()
```

更多功能包括：
- 消息处理：关键词回复
- 群管理：自动入群，拉人，踢人
- 自动处理好友请求
- 智能对话：通过简单配置，即可加入智能对话系统，完成指定任务
- ... 请自行开脑洞

详情请看Wechaty项目，下面列出一些简单的基本功能    

### Conversational AI

人工智能对话作为未来人机交互的入口，必然会成为未来一个非常大的热点，也会成为AI中发展的一个基础设置，通知能够为企业与其客户之间的自动对话提供动力。这些对话可以是基于文本或基于音频的，可以在任何消息传递或基于语音的通信平台上进行。

人工智能技术已经发展到可以非常准确地模仿人类对话的水平。它们使用自然语言处理(NLP)来为这些类似人类的对话加油。它帮助它们理解语音、文本和意图，破译不同的语言，并像人类一样做出反应。比如当它遇到订阅酒店的询问时，它会问：“请问酒店的地点在哪里？”，“请问您准备什么时候入住？”等问题。此外一些对话AI技术非常先进，甚至可以理解上下文并给出个性化对话。

但是，对话式人工智能的目的是什么?

对话型人工智能的主要目的是自动化对话和客户互动，以提供准确的、24小时的支持，比如企业可以将这项技术用于内部各种自动化的流程中，能够减少人工成本，办事效率等。然而，这并不是对话式人工智能技术的唯一用途，还有更多的应用等着在未来得到验证。


### Wechaty + Conversational AI 实战

Wechaty如何与人工智能对话结合起来呢？其实非常简单。同样只需要简单的几行代码就可以完成一个智能对话机器人。

在此次案例当中，我们使用的是微软QnaMaker服务，快速搭建一个QA对话机器人。示例代码如下，详细内容请看[wechaty-qnamaker](https://github.com/wechaty/wechaty-qnamaker)：

```typescript
import { WechatyQnAMaker } from 'wechaty-qnamaker'

const config = {
  mention: true, // default true: require mention the bot in room.
  room: true,
  contact: true, // enable direct message.

  /**
   * Language of Questions & Score of Answers
   */
  language: 'english',
  scoreThreshold: 50,   // minimum score for the answer

  /**
   * QnAMaker Service API
   */
  endpointKey: '705a3468-12bb-4e10-a314-7daa947f18d6',
  knowledgeBaseId: '254e33ad-ca6d-405d-980d-dbd3615e2605',
  resourceName: 'wechaty',
}

const QnAMakerPlugin = WechatyQnAMaker(config)

const wechaty = new Wechaty()
wechaty.use(QnAMakerPlugin)
```

上述代码中，使用的是wechaty社区中的一个插件，外加简单的配置即可完成与微软QnaMaker服务的连接。关于如何使用QnaMaker服务，可在[官网](https://www.qnamaker.ai/)查看详细使用文档。

由此，一个简单的Wechaty + Covnersation AI 实践案例即可完成，是不是非常简单呢 ？ 感兴趣的同学和朋友们可去[wechaty](https://wechaty.js.org/)和[AnaMaker.ai](https://www.qnamaker.ai/)官网查看详细使用文档。
