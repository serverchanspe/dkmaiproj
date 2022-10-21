# 自制省钱高性价比maimaiDX控制器$全!$解

## 第零部分 协议

### 对于请勿侵犯SEGA以及WAHLAP权益的声明
本作仅适用于个人制作游玩，原则上不提倡也不反对制作后发售。若发售或由读者自己的行为造成不当影响和任何纠纷，本教程作者和本教程不负任何责任。请勿侵犯SEGA以及WAHLAP权益。若作者行为或是本教程产生了不良影响，我对我的行为表示抱歉并可修补甚至撤下本教程，希望大家的理解。  
当大家在展示自己手台效果的时候，不要发布不该发布的东西，让我们一起遵守。

### 对于协力者，贡献者的感谢

我的触摸代码部分几乎完全是mai2touch的项目搬来的，然后更改修复了一些mpr121配置上的问题，配置部分借鉴了Arduino-Chunithm-Controller的代码。读卡器使用的也是同作者的Arduino-Aime-Reader。在此对mai2touch，Arduino-Chunithm-Controller,Arduino-Aime-Reader和它们的作者表示衷心的感谢，如果没有mai2touch和Arduino-Chunithm-Controller以及对它们下了很多心血的作者，我的控制器将失去它最重要的灵魂。  
在此感谢[Sucareto](https://github.com/Sucareto)以及他的项目[Arduino-Aime-Reader](https://github.com/Sucareto/Arduino-Aime-Reader)，[Arduino-Chunithm-Controller](https://github.com/Sucareto/Arduino-Chunithm-Controller)和[mai2Touch](https://github.com/Sucareto/Mai2Touch)!

传承开源精神，我将自用的程序开源，但是仅仅用于我手里的硬件测试成功，不同的走线，制作方法，使用的mpr配置等也不一样，不建议照搬。

### 对于本教程版权的声明

本教程是由Helloworld_Dk纯手打写出的，思路也是几乎完全自己想的。  
如果我能给大家的想法产生帮助，我感到非常荣幸，如果您觉得我的方案对您有帮助，希望可以在您的项目发布时，跟上一句"本方案的部分灵感来自Dk"或类似的话，我将不甚感激

## 第一部分 总览

![总览](Pictures/zonglan001.png)

本方案是使用导电膜裁切，漆包线引出的触摸部分为核心的低价maimai控制器制作方案。由于被~~逼到无奈~~很多也像制作maimai手台的玩家支持，而写了这样的一个教程。

本作品旨在弄个便宜好用的方案，让大多数人都可以轻松把这个东西做出来，同时不要效果差到没法玩。

为想要做一个maimai手台，而又对高昂的价格和空缺的思路望而却步的观众们提供一个全新的高性价比的思路。

只要你不嫌麻烦，有耐心，有学习的精神，就可以以非常低的价格做出视频中的样子。甚至，可以使用这个思路做一个超低价的街机尺寸台

所以没有想过类似定制玻璃什么的，当然，使用定制的材料一定会让效果更好，甚至还原出街机的水准。

### [方案效果展示](https://www.bilibili.com/video/BV1pe4y1m7pr/)
### [使用32u4的延迟更新后的展示](https://www.bilibili.com/video/BV1PW4y1E7io/)

todo: 按键的相关制作教程  
stat: 延迟的问题已经被消除

## 第二部分 目录
- 第零部分 协议
    - 对于请勿侵犯SEGA以及WAHLAP权益的声明
    - 对于协力者，贡献者的感谢
    - 对于本教程版权的声明
- 第一部分 总览
    - 介绍
    - 方案效果展示
    - todo和stat
- 第二部分 目录
    - 目录
- 第三部分 触屏制作指导
- 第四部分 读卡器个人思路分享
- 第五部分 已删除
- 第六部分 按键和灯光（未完成）
## 第三部分 触屏制作指导
**这位更是重量级**

![触屏ALL](Pictures/chuping001.png)

整个制作是非常的省钱，非常的好用，像是铝箔贴的chuni控制器，纯手作省钱能用就行精神是这样的。

本教程与之前发布的[专栏](https://www.bilibili.com/read/cv19157015)相互照应，相互补充，建议一起阅读

```圣经
做 手 台 不 试 试 瞎 搞 手 作 便 宜 省 钱 ， 就 像 四 大 名 著 不 看 红 楼 梦 ， 说 明 这 个 人 文 学 造 诣 和 自 我 修 养 不 足 ， 他 理 解 不 了 这 种 内 在 的 阳 春 白 雪 的 高 雅 艺 术 ， 他 只 能 看 到 外 表 的 辞 藻 堆 砌 ， 参 不 透 其 中 深 奥 的 精 神 内 核 ， 他 整 个 人 的 层 次 就 卡 在 这 里 了 ， 只 能 度 过 一 个 相 对 失 败 的 人 生。
```

**你需要的材料：**  
- 触摸部分
  - 尺寸合适的ito导电膜，一定要买带胶，除非你真的想好了胶怎么办。下面会有为什么要这么做的说明。
  - 一张较薄的亚克力板或者玻璃板，尺寸至少覆盖圆形屏幕区域。此处感觉玻璃容易碎，亚克力容易划花，大家自行斟酌。本人使用的一张比亚克力优秀的塑料板。
  -  较细的漆包线
  -  你超棒的手工能力
  -  透明胶带
- 屏幕部分
  -  一块跟你触摸板相对应的合适大小的屏幕，本教程应该不适用于小于十寸的屏幕。
- 程序和mcu
  -  本人使用的mai2touch项目，并对其进行修改，相关链接在教程开头协议部分。
  - Arduino或类似的开发板，我建议使用pro micro，不建议使用使用了ch340串口ic的板子。但是我使用pro micro被喷过和嘲讽过.....别人说它性能太差，可是我真的喜欢。

**制作过程详解**  
这部分在专栏讲的很详细，特别是图片详细。  
统共有以下步骤：  
### 1\. 打印对照纸
说的玄乎，其实就是用一张A4纸或类似的纸，将触摸区块图片打印下来。尺寸要与你目标屏幕显示的大小完全对应。建议打印至少两张。

![打印对照纸](Pictures/dydzz001.png)

### 2\. 裁切
把a4纸跟买到的触摸膜贴在一起固定好，然后根据a4纸，裁下每一片触摸区块  
注意一定要固定好哦，不然剪着剪着位移了剪除奇形怪状的区块可就难办了！
![裁切](Pictures/caiqie001.png)
![裁切](Pictures/caiqie002.png)
![裁切](Pictures/caiqie003.png)
## 3\.粘贴

首先你不是打印了两张A4纸吗，一张被剪了，另一张好好的，请规划好位置之后，把A4纸打印面朝向亚克力板或玻璃板粘贴，在另一面应该可以透过亚克力板或者玻璃板，看到另一面清晰的打印的区块。用于之后粘贴位置的对应。
![粘贴对应](Pictures/zhantieduiying001.png)

导电膜是这样的结构：  
不导电面朝上，导电面朝下，依次是： 

0. 一层保护膜
1. （如果是带胶的才有）一层透明胶
2. 聚酯离型膜，自此间隔，上面称为不导电面，下面称为导电面，不导电面有胶，导电面无胶
3. ito导电涂层
4. 一层保护膜

在**粘贴**这一步，我们需要完成的是

0. 亚克力或玻璃板
1. （如果是带胶的自带，没带胶的会让你痛苦到怀疑人生）一层透明胶
2. 聚酯离型膜
3. ito导电涂层
4. 一层保护膜

假设没有买带胶的膜，就自行点胶（透明的，支持粘贴塑料的，不会腐蚀塑料的，固化不回缩的，粘贴可以调整的）固定每片触摸块到屏幕上。  
在写这篇教程的时候，我自己搞的胶腐蚀了我的塑料板，导致A5区域透明性下降...**距今已过去十分钟，警钟敲烂**，所以千万别贪便宜买不带胶的！  
需要撕下不导电面的保护膜。不导电面朝向塑料板粘贴，**请勿将导电面贴到塑料板上**。  
如果是买的带胶的导电膜，不导电面恰好是带胶面，裁好了可以轻松粘在塑料板上。完全不用经历大力对抗胶水的那一步。  
~~唉，这个地方别省钱，要不让你感受人间痛苦，宛如晚清十大酷刑。~~

~~自己搞胶的痛苦，详见专栏图片。~~
![痛苦](Pictures/tongku001.png)
![坏处](Pictures/huaichu001.png)
## 4\.引线

在**引线**这一步，我们需要完成的是

0. 亚克力或玻璃板
1. 一层透明胶
2. 聚酯离型膜
3. ito导电涂层
4. 漆包线
5. 单面带胶的透明胶带

![引线](Pictures/yinxian001.png)

之前我说的是  
```
要去漆包线的绝缘漆，  
撕掉导电面保护膜，  
用透明胶带初固定，  
尽力沿着区间缝隙走线， 

评价是先走中心的c区，然后慢慢向外区块做，这个是中心思想，  
其次是按照从下到上 顺序操作的，先是最底下的区，56那些处理好，慢慢往上处理。  
这样在处理完一些之后，可以横着贴一张长长的透明胶带把已经完成的区固定好避免之后散掉。
```
依然可以参照，在此补充操作绝对步骤，引用我教别人的聊天记录
```
这样
先把漆包线准备好,头上刮漆打圈
把带胶不导电面贴好
然后准备一段透明胶带
然后把导电面保护膜解开
放漆包线
粘胶带
一气呵成
```
这里有关ito的一个特性，是ito遇水，二氧化碳容易变质，影响导电性能和透明性。  
所以在放上漆包线后，应当尽快用一些方法将导电面全部覆盖隔绝空气。我使用的是透明胶带，虽然不是特别好看但是能用。

关于导线具体从区块到触摸板边缘的引出方法，详见b站专栏，非常详细！

```
总的说就是先从底下的中间考虑，也就是看下图先处理底下中间红圈再处理绿圈再处理橙圈再贴一张透明胶带上去。再往上一步一步地处理整个触摸面板。

运用了贪心的思想，中间的区肯定是最需要往外走的，所以需要先考虑，从哪条缝走过去。而边上的很简单就可以引出去，可以在把难搞的安顿好之后再处理。从下往上一是因为可以做一块贴一整块透明胶带，其次是下面不会像上面一样被屏幕挡住无法从边上轻松走线。先把东西往下安顿可以减少后续上面的工作量。

要点：处理顺序、不要吝啬在圆外面的初固定胶带，周围挡起来游玩看不见，减少线乱飞
```

![走线](Pictures/zouxian001.png)

## 4\.接线
详见b站专栏，讲的足够详细，基本没有要补充的。
```
1.先把arduino跟mpr121的I2C连好。

2.根据程序确定哪个区接在哪个mpr121的哪个io，如果你的程序不知道是哪个io，把程序写到板子里面，用一根螺丝刀按在每个io上，看游戏测试汇报哪个区被按下。通常是连续的，比如A1到A8是一个mpr的0到7之类的，很好确定，这个是一种办法。另一种是根据你从触摸面板上接出的漆包线的位置，在程序里面规划好哪个接哪个合适不用绕，可以走线不像我一样乱糟糟。

3.走漆包线。面对从塑料板边缘引出的34根漆包线无从下手是吗？我感觉这样比较好：以横向中轴为开始的地方，从这里向上下处理。

因为两边的线很容易可以从边上引到中间的mpr121上，而偏上偏下的难搞要绕。所以从中间处理会方便很多。走线原则：从空闲地方走，尽量隔出空隙，不要横跨一张mpr121板子，上面不能直接 绕，绕最好从左右，下面也可以勉强绕一下。
![接线](Pictures/jiexian001.png)
之前留的漆包线建议足一些，不然这步容易踩坑：要绕一些地方焊接，就需要足够长的线。有时候线发现不够长，这时候如果你发现在透明胶带下走的路径对现在要走的地方不合适，觉得拽回来就可以了，不绕路了，够长了。但是小心！！你一拉那个漆包线，很可能把上面在触摸区域走的打好圈的线拽移位，到其他区或者圈没了。这会让你极其难办。你不得不拆下粘的很牢的透明胶带，把线重新拽回原位打圈放在该在的位置上。透明胶带这种东西撕下来粘第二次透明效果就会很差，所以千万不要乱拽漆包线，返工让你怀疑人生

但是遇到真的不够长怎么办呢，可以尝试用圆滑的焊接接上一段，做好绝缘应该没什么问题。

到这里，你的线接好了。

要点：确定好io对应区，写在之前打印过的A4纸上，对照着纸上面的区块位置接会方便很多。不要拽漆包线。
```

## 5\.程序部分

我使用的是github上的开源项目mai2Touch。曾遇到过问题如下

QA1：对于328p编译失败，不支持的开发板：改改上面的宏定义即可。（不建议使用带ch340的328p板子... ~~感觉是延迟的来源，新买的板子还没到...不确定。~~ 就是延迟的来源，不用洗，我promicro已经到了，非常低延迟，爱来自32u4。这条QA仅限于你要用UNO/NANO/MICRO才可能会用到，但是本人非常不建议使用，因为延迟极大

QA2：Serial.write 歧义 编译失败：在write传入的参数前面强制类型转换为(byte)。如Serial.write('A');改为Serial.write((byte)'A');

QA3:触摸出现问题，莫名触发，串音，灵敏度错：~~我自己重写了mpr121配置部分代码然后就解决了，某论坛有配置详细教程，这就不发了。~~实际上是从Arduino-Chunithm-Controller搬来的寄存器设定代码并加以改动，我摊牌了。

## 6\.游戏连接部分

你好，不可能发游戏的，这里只提一下连接的一些问题

QA1:怎么连的：串口直连，按照github上的readme走。

QA2:怎么按下在闪，不是长按：github（截止到写这个专栏）里面教的写错了。**DummyTouchPanel=1应该是0**，1的话是开启了的mai程序自带的调试触摸，然后导致自己的设备和自带的调试对着干，一个说按了一个说没按，就开始闪。设置为0避免程序调试触摸影响。

QA3: 怎么感觉我的触摸没问题，但是程序里面好像跟无响应一样：~~神奇问题，你插上电脑之后先用ide传一遍程序进去就会好。用rts|dts小工具试过也不行，就是ide传程序可以，非常神奇。仅发生在我手上的ch340的arduino nano上，其他板子也许没问题。传过程序之后，只要不断电，reset arduino 不会影响。断电需要重传程序解决。~~ 听国际友人说好像是ch340在arduino上锁i2c什么的？我英语很差，初中水平，看不懂.....反正避免使用328p+ch340即可解决问题。非要用的话，每次重新上电需要重刷一遍程序。

~~ 其实我当时这么乱的接线我觉得我必定失败，一定串音，结果上测试程序告诉我静默跟没接一样的一点干扰都没有\(7\-11\)，按下能上最高100多的数值\(40\-120\)，我超，太美丽了，这必成功，我都不敢相信，但是真的可以！！乱搞万岁  ~~ 删除线挂了，给其它符号转义了也没用，不知道为什么。

~~至此，已成艺术品~~  
**至此，触摸部分硬件软件完成，撒花  *★,°*:.☆(￣▽￣)/$:*.°★**

## 第四部分 读卡器个人思路分享

![读卡器正](Pictures/dukaqizheng001.png)
![读卡器反](Pictures/dukaqifan001.png)

在最新一次发布的b站展示视频中，可以看见我的读卡器。他最亮眼的部分是均匀的光。其原理是使用了一块拆机的 **屏幕背光板** 进行光的一个导，视频中并非完成品，要做的更完善，需要使用大一点的背光板，配合侧照的灯，而不是我这粗制滥造的测试机的操作，不过对于全尺寸的灯加上手动侧照已经能达到如此不错的效果，等到完善之后效果应该不言而喻的非常不错。  

目前我看到其他大佬们制作的读卡器，没有使用了本方案的，我觉得这个思路对于光的均匀度方面效果不错，于是就发出来供大家参考。

关于读卡器的程序
使用的是Arduino-Aime-Reader项目。但是注意，这个项目并不原生支持328p。由于~~我家328p奇多~~读卡器并不需要极低的延迟，所以我考虑了使用~~我家奇多~~ 的arduino nano(328p+ch340)制作，因为成本低。在过程中遇到了一些问题并解决了,如下：  
QA1：程序无法通过编：需要改改宏，这个上面说过了。  
QA2：程序编译正常，readertest正常，手动发包疑似正常，就是游戏不可以：发现游戏发送初始化命令，发送dts/rts或相关内容的时候会让arduino重启（reset触发），显然不对劲，因为在重启过程中，游戏发包arduino不会给出回应。尝试短接rst与3v3强制禁止其重启，问题解决。
```
但是usb转串口可以重启arduino不是bug而是一个不错的功能，arduino在下载程序的时候需要重启才可以开始。电脑可以让arduino重启本身是为了方便下载程序而做出的美好设计，但是在此处影响了功能。  
如果直接短接会造成无法正常下载程序。我的解决方法是在rst跟3v3直接加一个开关，下载程序就断开，当读卡器的时候就闭合。  
这样也许会？对复位电路产生略微的短路，但是目前使用效果极佳，就先这样用了。
```

## 第五部分 已删除

## 第六部分 按键和灯光

![不存在的按键，和简单的灯光](Pictures/anjiandeng001.png)

直接promicro做成键盘就完事，这个人人都会不用教网上一抓一大把。  
据说可以把灯光塞进跟按键同一个promicro，但是我没试过（
在todo列表中
待完成



<br>

------
END SEL &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DOCUMENT BY HELLOWORLD_DK