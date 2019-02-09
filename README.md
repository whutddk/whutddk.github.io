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

### 基于python的爬虫（大四~研一）

* 仓库链接（包含隐私数据，私有权限）

### 功能
* 随机爬喜马拉雅音频资源，解析下载其中的音乐
    - 喜马拉雅资源是不加密的
* 爬好友QQ空间
    - 下载全部说说
    - 下载全部可访问相册照片
* 爬取教务处半公开保研数据
    - 这个项目做得略出格，为了给后面的学弟提供当年保研公示的数据
    - 教务处会校内网公开所有保研学生的获奖加分情况，不提供批量下载
    - 脚本化方式批量将全校保研加分情况下载下来分析
* 爬取百度FM的音乐
    - 参考[iRhythm项目](https://github.com/whutddk/iRhythm)


------------------------------
------------------------------
------------------------------

### 基于zynq-7000的伺服控制系统（本科毕业设计）
* 使用zedborad（Cortex-A9(Arm) + Artix-7（FPGA））控制永磁同步电机（PMSM）
* 使用Vivado HLS高层次综合技术完成Park Clark变换
* 手动写状态机，verilog实现I2C协议电流采样芯片的驱动IP
* 效果
    - 可以控制PMSM旋转，粗略调速

* 局限
    - 项目提出的逻辑错误：是为了学习软硬件协同设计而控制PMSM，不符合根据需求选解决方案的项目逻辑
    - 当时对这类设计方法没有经验：HLS的使用仅仅是因为当时不会写变换的ip，没有正确地时序控制，或者说当时就没这个概念
    - 对PMSM控制，对电流环的控制都没有经验，控制周期不对，采样芯片选型失败，控制指标惨不忍睹

* 突破
    - 第一次FPGA设计类的项目尝试
    - 接触了电流环，知道了厉害，成功引导后面学弟比赛不再采坑
    - 尝试了一直没机会碰过的PCB隔离，三相MOS驱动

* 结果
    - 答辩勉强拿到优秀

#### 图片

![系统图](https://github.com/whutddk/My-WUT/blob/master/毕业设计/doc/微信图片_2019013122002213.jpg)

#### 视频
[视频](https://github.com/whutddk/My-WUT/blob/master/毕业设计/doc/trimed_1488445829179.mp4)

---------------

### [资产管理（大四下）](https://github.com/whutddk/wimc)

* [仓库链接](https://github.com/whutddk/wimc)
* 需求
1. 实验室太多：鉴湖，汽院，自动化15楼，寝室，家。
2. 东西太多：开发板n个，显示器n个，教程n堆。。。。。。
3. 自己带的学弟神经大条：
    * 第一学期：拿了我的板子
    * 第二学期："学长，板子不在我这"
    * 第三学期："学长的板子我找到了。。。"
4. 要搬家到华科了

* 所以我急需一套管理系统，来确定我的东西都到哪去了，二维码管理，自动查找最好了。

* 当然，这个项目如果换到现在来做，就不会用这种方法了。

* 基于C++ 的opencv快速建立
* 基于surface平板及其摄像头进行部署
* 通过zbar插件识别二维码
* 尝试安卓部署失败
* 暂时没有采用数据库
* 通过git作为数据同步


-----------------

### [SMATG（大四上）](https://github.com/whutddk/smatg)
* [仓库链接](https://github.com/whutddk/smatg)
* 自己想的AR智能眼镜项目
* 技术关键词
    - opencv:人脸检测，人脸识别
    - respriberry Pi
    - AR

---------------------------

### [2016年恩智浦杯全国大学生智能汽车大赛（大三）](https://github.com/whutddk/2016_nxp_chenfeng)

* [仓库链接](https://github.com/whutddk/2016_nxp_chenfeng)
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

#### 照片
![1](https://github.com/whutddk/2016_NXP_ChenFeng/blob/master/pic/IMG_20160820_100030.jpg)
![2](https://github.com/whutddk/2016_NXP_ChenFeng/blob/master/pic/微信图片_2019013122002214.jpg)
![合照](https://github.com/whutddk/2016_NXP_ChenFeng/blob/master/pic/P60820-124719.jpg)

#### Video
* [省赛（华南赛）预赛](https://v.youku.com/v_show/id_XMTY0ODY4NTUyOA==.html?spm=a2hfx.9903432.collectVideo.5~5~5~1!2~3~A
)
* [省赛（华南赛）决赛](https://v.youku.com/v_show/id_XMTY0OTQxNjM4NA==.html?spm=a2hfx.9903432.collectVideo.5~5!2~5~1!2~3~A)
* [国赛决赛第二次成功](http://v.youku.com/v_show/id_XMzc4NzQyMTY5Ng==.html?spm=a2h3j.8428770.3416059.1)
* [国赛决赛第二视角](https://v.youku.com/v_show/id_XMTY5MTkyMTg3Ng==.html?spm=a2hfx.9903432.collectVideo.5~5!3~5~1!2~3~A)

#### Contributors


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

---------------------------------

### 2016电子设计省赛

* 2016是省赛年，做满也是省特，而且省特限制名额，所以没有那么重视
* 将自己的中心放在智能车赛上
* 省赛的重点为，保稳定，带学弟，保证学弟能保研
* 获得控制组省一


#### 内容
* PSP嵌入式上位机解决方案
    - [仓库链接](https://github.com/whutddk/beacon-PSP)
* 倒立摆
    - 理论指导下的二刷
* TM4C123解决方案
    - [仓库链接](https://github.com/whutddk/2016TiCupTM4/tree/master)
* 直流电机对拖系统
    - 相关内容体现在2016-NXP智能车赛-节能指标组的技术报告中
    - 对电机理论知识的实践
    - 做了第一个论证性实验，后续实验和数据由Jialong学弟代做
* samba 实验室服务器
    - 鉴湖实验室需要传承，学长们毕业了，但留下的资料要共享
    - Linux课也上得差不多了，树莓派已经会一点了
    - 搭个文件服务器呗，把资料放树莓派里，公开局域网，登陆密码
    - 学弟们自己取学长们的资料
    - 意外
        + 在智能车省赛回来的路上，爽姐惊呼，我的资料都传到外面群里去了！！！是不是有人把资料挂论坛换积分
        + 不知道谁干的，项目中止。。。


* 水温控制系统模糊控制（校初赛）
* 平板控制系统（校复赛）
    - 尝试了直流伺服和步进电机两个方案

* 基于LDC1314的金属丝引导电动车（省赛）

#### 图片
![合照](https://github.com/whutddk/My-WUT/blob/master/2016电子设计省赛/doc/mmexport1501921922721.jpg)

#### Contributors
* Ruige Lee
* Rong Huang（学弟）
* Jialong Wang（学弟）


--------------------------------

### 2015 全国大学生电子设计大赛 （大二）

* 比赛题目是[风力摆控制系统](https://github.com/whutddk/My-WUT/blob/master/2015电子设计国赛/doc/风力摆控制系统(B题).pdf)
* 赛前一年进行了大量的赛题练习
    - 旋转倒立摆控制（13年国赛题）
    - 四旋翼控制（14年湖北省赛题）
    - 电动车跷跷板（07年国赛题）
    - 悬挂系统（05年国赛题）
    - 激光打靶（12年省赛题）

#### 总结
* 这是我在鉴湖实验室付出最多，却打得最惨烈的比赛
    - 6月放弃考试复习月，进驻鉴湖考试总攻
    - 得到实验室研究生学长们的大力支持
    - 得到了学院老师的支持
    - 个人投入1W多的比赛经费
    - 最终交付了一个振荡的系统，勉强获得省二
    - 没脸回实验室了
* 原因
    - 团队配合完全失效，只有我个人的输出
    - 自己太过自负，以为真的可以个人单刷电赛
    - 大二水平有限，没有一系列理论指导，瞎调参，却不知道怎么调
* 收获
    - 虽然打得惨烈，但守住了省二这个保研最低限，为大三的发展做好后盾。心中不慌了。
    - 后续比赛开始重视团战
    - 几乎把所有调参方法都实验了，加上大三开始上控制理论，后续比赛的理论指导体系得以建立

#### 图片

![倒立摆](https://github.com/whutddk/My-WUT/blob/master/2015电子设计国赛/doc/倒立摆/mmexport1465474197571.jpg)
![四旋翼](https://github.com/whutddk/My-WUT/blob/master/2015电子设计国赛/doc/四旋翼/7e0edf155bd21f120afb0397ff8248d6e01761bc.jpg)
![激光打靶](https://github.com/whutddk/My-WUT/blob/master/2015电子设计国赛/doc/激光打靶/微信图片_2019013121595724.jpg)
![风力摆原型](https://github.com/whutddk/My-WUT/blob/master/2015电子设计国赛/doc/风力摆/bf55f16d7ba4039cdfdbb038c446ddf1.mp4)

#### Contributors

* Jinpeng Han （学长）
* Fuwen Su （学姐）
* Ruige Lee


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
