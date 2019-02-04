# Ruige LEE's Page


---------------------------------------

## 个人

* 李锐戈
* E-mail: 295054118@qq.com
* 个人主页：https://github.com/whutddk
* 学校工作主页1：https://gitee.com/whutddk
* 学校工作主页2：https://gitee.com/RGLEE
### 学习经历
* 2010.09-2013.08 广东梅县东山中学（高中）
* 2013.09-2017.06 湖北武汉理工大学-自动化卓越工程师专业（学士）

### 工作经历
* 2014.10-2018.08 武汉理工大学电工电子实验中心-控制组（鉴湖实验室）
* 2017.07-至今 湖北华中科技大学-控制科学与工程 （保研在读-硕士）
* 

### 研究方向
* 本科： 自动控制，工业控制，嵌入式硬件及底层
* 硕士： 软硬件协同设计，IC前端


---------------------------------------

## 项目（倒叙）



### [2016年恩智浦杯全国大学生智能汽车大赛（大三）](git@github.com:whutddk/2016_NXP_ChenFeng.git)

* [仓库链接](git@github.com:whutddk/2016_NXP_ChenFeng.git)
* 有了前一年参赛的经验，更有了资金和赛道，一切就变得特别顺利
* 加入汽车学院参加比赛
* 参与其中的电轨竞速组和电轨节能组，拿下两个全国一等奖
    - 电轨竞速组负责：电路；代码工程搭建、验证、规范化；控制算法搭建、验证；传感器解决方案
    - 电轨节能组负责：电路；取电方案


### 背景
* 2016是比赛的改革年，出现了很多新组别（电轨，信标，双车超车）
* 我们参与的电轨组组别太新，规则摇摆不定
    - 是否取电
    - 传感器方案
* 赛初即做了取电解决方案，后来该方案移动至创意组。鉴于我校从来没有队伍参与创意（不知道保研政策），我们决定第一年试水创意，将创意作为备份组。

### 过程
* 这个组难点在传感器方案，官方给出的传统三点震荡方案很早进行了验证，距离太短。参考TI，LDC系列传感器，把所有手册看了一遍，发现LDC1614和LDC1314的方案最合适，评估版价格相同，选择精度更高的LDC1614。
* 区别于电磁，金属传感器只能看见线圈下面的赛道情况，没有电磁波传播的扩展，所以视角相对较小。前瞻约长，视角越小，越容易发散。
* 双线圈方案与三线圈方案
    - 传感器非线性问题非常严重，这一年探讨了非常多拟合线性化方案
    - 因为双线圈拟合有对称问题，改用三线圈拟合
* 控制
    - 舵机控制
        + 简单三参数PD
        + 因为队友机械能力很强，机械上大量非线性问题都解决了，简单的PID方向控制即可取得非常好的效果
    - 电机调速
        + 增量式PI
* 算法
    - 探讨过模糊控制并进行验证，因为风险较大，后面放弃使用
    - 后面采用简单PID加BNAG-BANG法进行控制
* 总结：如果要我总结智能车赛的三个要点
    - 全程参数线性化
        + 无论是修理机械，调整传感器，PID分段等，全程讨论的是线性控制，将非线性环节用各种手段处理掉，调参就很简单了
    - 保证控制实时性
        + 使用Cortex-M4处理器，核心解算拟合函数，DSP也没开，其实我们组的控制实时裕量还是很足的，当然我自己也是验证过的。
        + 电流环，我反对让学弟搞，主要是实时性难以保证，而学弟意识不到这个问题
    - 构造合适实验验证问题
        + 静电干扰复位原因
        + 起跑线干簧管误触发原因
        + LDC1614复位原因
        + 电机Bang-Bang控制对传感器，电路板的冲击


### Video
* [省赛（华南赛）预赛](https://v.youku.com/v_show/id_XMTY0ODY4NTUyOA==.html?spm=a2hfx.9903432.collectVideo.5~5~5~1!2~3~A
)
* [省赛（华南赛）决赛](https://v.youku.com/v_show/id_XMTY0OTQxNjM4NA==.html?spm=a2hfx.9903432.collectVideo.5~5!2~5~1!2~3~A)
* [国赛决赛第二次成功](http://v.youku.com/v_show/id_XMzc4NzQyMTY5Ng==.html?spm=a2h3j.8428770.3416059.1)
* [国赛决赛第二视角](https://v.youku.com/v_show/id_XMTY5MTkyMTg3Ng==.html?spm=a2hfx.9903432.collectVideo.5~5!3~5~1!2~3~A)

## Contributors


* 电轨竞速组
  - Yansong Zhang
  - Jiawei Yuan
  - Ruige Lee
  
* 电轨节能组
  - Ruige Lee
  - Yansong Zhang
  - Cong Chen
  - Song Feng（学弟）
  - Rong Huang（学弟）
  - Jiawei Yuan


--------------------------------

### [天际2015（大二飞思卡尔智能车）](https://github.com/whutddk/TJ2015)

* [仓库链接](https://github.com/whutddk/TJ2015)

* 最早介入保研相关比赛是飞思卡尔智能车
* 从大一下期末开始跟着蓝宙的淘宝店，买板子，跑例程
* 觉得自己不适合搞光学组
    - 学长说光学被干扰很严重
    - 实力很强的学长都在摄像头组
    - 那年赛道改革，不用KT板，改用PVC，没有钱买标准赛道，电磁比较容易。。。
* 参加电磁双车组，基于鉴湖实验室的平台
    - 情况有多惨，鉴湖612的地板，贴的胶带痕迹就是当年的调车赛道
    - 大二水平有限，被学长实力碾压，止步校赛

#### 图片

* 当时的调车赛道
    - ![当时的调车赛道](https://github.com/whutddk/TJ2015/blob/master/pic/微信图片_201901312200229.jpg)
* 原型设计
    - ![原型设计](https://github.com/whutddk/TJ2015/blob/master/pic/微信图片_2019013121595710.jpg)
* 赛前版本
    - ![赛前版本](https://github.com/whutddk/TJ2015/blob/master/pic/微信图片_2019013121595728.jpg)

#### Contributors
* Ruige Lee
* Jialong Wang (学弟)
* Fuping Wang 
* Guangpeng Li

--------------------------------

### [自动化学院流水灯大赛（大一下）](https://github.com/whutddk/LED256)
* [仓库链接](https://github.com/whutddk/LED256)
* 大一下学期，学院、科协举办第一届流水灯大赛（搞了两年觉得太简单，就不搞流水灯改搞循迹车了（初级赛））

#### 全彩点阵(第二名)
* 当时比赛时学长指出，这是真彩，不是全彩

* 拼命榨干了51单片机的资源，虽已经历很多全国赛事，至今很为这段代码骄傲。
* 方案
    - 颜色控制
        + 使用三色雾状灯帽LED，共阴引脚。
        + 当时pwm控制颜色的技术不是很成熟，也尝试过了，最终采用I2C控制下的DAC（***TLC5620）***控制颜色的方案：将64个灯的红色阳极接在一起，接到DAC的*chn0*；将64个灯的绿色阳极接在一起，接到DAC的*chn1*；将64个灯的蓝色阳极接在一起，接到DAC的*chn2*
        + 通过控制DAC的输出电压，分别控制每个灯的颜色。
    - 图案控制
        + 扫描技术
        + 使用多个译码器（74hc138，74HC154）组合后逐个扫描64个灯的阴极。
        + 当时申请芯片搞到TI拉黑我校。。。
    - 控制
        + 51单片机，原型验证用的是STC89C52，后面ROM，速度告急，在宏晶官网找了一款引脚完全兼容，，节拍更快的型号换上去，把晶振速度换大。
        + 多个定时器和延时调度
            * 无源蜂鸣器播放音乐
            * 刷新颜色，消隐
            * 保持图片，换图
    - 刷图大致流程
        >
        > for (imageCnt = 0 ;imageCnt < ? ;imageCnt ++):
        > 
        >       for (imageDelayCnt = 0;imageDelayCnt < ? ; imageDelayCnt ++ ):
        >       
        >           for ( lightCnt = 0 ; lightCnt < 64; lightCnt ++ ):   
        >           
        >               decoder select (lightCnt)
        >               
        >               DAC set color (red,green,blue)
        >               
        >               __nop__(3);
        >               
        >               DAC set color (0,0,0)
        >           

#### Contributors
* Xiangjie Wu
* Songhuan Huang
* Wentao Sun
* Ruige Lee


#### 风火轮（第一名）
* 做完摇摇棒，就想到了把摇摇棒安装在自行车的车轮上，网上搜，还真有
* 采用霍尔传感器，需要在车轮上贴一个磁铁标记起始位置
* 每次检测到磁铁后，开始刷图案

* [申请了实用新型专利](http://www.wanfangdata.com.cn/details/detail.do?_type=patent&id=CN201620157427.7)

#### Contributors
* Pu Liu
* Zong Yang
* Ruige Lee

#### 图片
* 风火轮原型
    - ![风火轮原型](https://github.com/whutddk/LED256/blob/master/pic/微信图片_2019013121595610.jpg)
* 风火轮成品
    - ![风火轮成品](https://github.com/whutddk/LED256/blob/master/pic/IMG_20140502_124040.jpg)
* 风火轮效果
    - ![风火轮效果](https://github.com/whutddk/LED256/blob/master/pic/IMG_20140207_230420_SHOT2SHOT20.jpg)
* 真彩点阵原型
    - ![真彩点阵原型](https://github.com/whutddk/LED256/blob/master/pic/微信图片_2019013121595616.jpg)
* 真彩点阵成品
    - ![真彩点阵成品](https://github.com/whutddk/LED256/blob/master/pic/微信图片_2019013121595619.jpg)
* 真彩点阵效果
    - ![真彩点阵效果](https://github.com/whutddk/LED256/blob/master/pic/2014_10_11_22_08_57.jpg)

#### 视频
* 请参考作品视频链接，视频看起来不那么鲜艳
* [风火轮原型版本](https://v.qq.com/x/page/k0127j38gix.html?)
* [风火轮比赛版本](https://v.youku.com/v_show/id_XMzc3ODE3ODQxNg==.html?spm=a2hzp.8244740.0.0)
* [真彩点阵](http://v.youku.com/v_show/id_XMzc3ODE3NDk5Mg==.html?spm=a2h3j.8428770.3416059.1)



-----------------------------------------

### 一些项目的探索（大一上）

* 会了点51，总得要搞点什么
    - 迷你通用版51最小系统
        + ![迷你通用版51最小系统](https://github.com/whutddk/My-WUT/tree/master/一些项目的探索（大一上）/IMG_20131205_172044.jpg)
    - 摇摇棒
        + ![摇摇棒](https://github.com/whutddk/My-WUT/tree/master/一些项目的探索（大一上）/IMG_20131205_172146.jpg)
    - 自动巡线小车
        + ![自动巡线小车](https://github.com/whutddk/My-WUT/tree/master/一些项目的探索（大一上）/微信图片_201901312159566.jpg)


-----------------------------------------
### 我的第一块51单片机（大一上）

* 武汉理工大学真的是一个很适合学习的地方，刚刚军训完，各种科技类社团，实验室宣传。
* 导员支持我们在寝室偷偷焊电路板，然后新建好的寝室还没通网，当时手机流量包一个月50M(QAQ)又溜到图书馆机房写代码，背着电脑去教学楼蹭wifi装环境。现在想想，我们鉴湖这批13级的，真的是艰苦环境出来的。
* 在机器人协会学长们的帮助下，大一的10月底11月初，我完成了自己的第一块51单片机
* 从0到1的突破，虽然焊得很差。

#### 视频
[我的第一块单片机](https://v.youku.com/v_show/id_XMzc3ODM0OTkzMg==.html?spm=a2hzp.8244740.0.0)

#### 图片
![我的第一块单片机](https://github.com/whutddk/My-WUT/blob/master/我的第一块单片机/IMG_20131109_102205.jpg)


-----------------------------------------
### 大学以前

* [基于Visual Basic的一些软件开发](https://github.com/whutddk/myVB)
* 主要涉及
    - 简单的游戏算法
    - 基于winsock的TCP/UDP通信
    - windows一些系统API的调用等



-----------------------------------------

You can use the [editor on GitHub](https://github.com/whutddk/whutddk.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/whutddk/whutddk.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
