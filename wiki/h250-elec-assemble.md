
## 电机的安装

电机，通过螺钉固定在机臂上。**螺钉的紧固需要一把H2.0的六棱螺刀**。

* 第一：四个机臂的顶端都预留有电机固定座，根据自己的布线思路确定电机引线的方向。
* 第二：电机一般附带有长、中、短三种螺钉，根据机臂的厚度及电机底座的厚度选择合适的螺钉。**螺钉的长度在固定时不要超出电机底座的厚度**。以我们提供的H250机架，**绝对不要使用长螺钉**，否则螺钉会顶住电机线圈，将电机报废，笔者第一次装机就因为这个原因报废了4个电机。
* 第三：确定机头的方向，以机头左前方向机臂按照顺时针方向依次标号为1/2/3/4,1、3号机臂位置安装CCW型电机（螺纹为反丝，电机螺帽为黑色），2、4机臂位置安装CW型电机（螺纹为正丝，电机螺帽为红色）。
* 第四：安装技巧。电机孔位设计时可能为了达到牢固、紧固的目的，一组对角孔位间距设计相对较短。我们用之前选择好的螺钉先通过这两个孔位固定电机，若不注意此细节，可能最后你的电机只能安装三个螺钉。


![](/assets/img/ele-8.png)

![](/assets/img/ele-3.png)

## 电调的安装

固定电调之前你要合理的规划H250的整体空间。我们购来的飞控、分电板、电池及后面要搭载的图传设备，都要为它们分配空间，H250的空间相对较小，底边和平面板将空间分三层，笔者的设计为：

* 上层：平面板固定电池，平面板减震平台为图传摄像机预留；
* 中层：平面板与底板夹层放置遥控接收机、摄像头、飞控及图传设备天线装置；
* 底层：底板下方固定电源分电板，机臂固定电调。

设计及布局供参考。

笔者的电调是使用双面胶固定在机臂上，完成电机与电调之间的接线后用尼龙细扎带捆绑在机臂上，空间的分布及布置相对比较合理。

电调一般从两端共引出三组线，电调的引线在这里简单说明。

* 较粗红、黑线输入电源线，和分电板相连。按红正黑负焊接导分电板即可。
* 3根排线为信号线，和CC3D相连。黄色线为信号线，其他两根（中间红色和边上的棕色）输出5V电压给CC3D主控供电，排线插入CC3D主控OUTPUT输出通道，注意信号线对应主控CC3D输出通道‘.’标识端。1号机臂上的的电调接入表示有1的排针上，后面以此类推。
* 3根黑色线为电调输出，于电机相连。烙铁焊接，接头用热缩管包扎隔离。小提示：在[H250飞控CC3D配置](./h250-config.html#section-1)中需要做电机方向校准，**若出现转向相反的情况只需要任意调换两根接线即可**，所以要等到电机方向校准的时候，再固定热缩管。
* 用扎带将电调固定在机臂。若电机与电调的接线有长余部分要处理妥善，多余的扎带剪掉。

![](/assets/img/ele-2.png)

##飞控板的安装及接线

安装CC3D飞控要注意两点：**1、机头的方向与飞控的三角尖端指向保证一致。2、飞控的固定一定要与机体水平**。CC3D是有头模式飞行，机头在装配中必须要有一个参考方向供操控者去识别，建议CC3D的机头与减震平台一侧保持一致。飞控在每次重写配置时都会进入一个陀螺仪校准界面，若飞控校准不在水平面时容易造成校准误差，校准数据出现问题是不可能成功试飞。

下面简单介绍CC3D的各个接口：

* mini USB接口是飞控与上位机地面站通信的接口。用于地面站对CC3D设置配置、上位机读写数据等。
* INTPUT接口：PWM遥控输入，与接收机相连。
* OUTOUT接口：飞控与电调及舵机之间的输出通道接口。
* Flexi Port及Main Port：拓展接口，用户可以通过地面站自行设置。例如通过此端口配置GPS。

![](/assets/img/ele-1.png)

##遥控接收机的安装

CC3D飞控附带有一束一分六的通信线，用于飞控与接收机之间的连接，通信线总端口接飞控的INPUT端，分支接入遥控对应的通道。这里需要注意一点：

* 分支线路有一根3线排线，白色线对应遥控接收机“S”标识，红黑线为CC3D主控向遥控接收机供电，接入接收机的BAT接口。
* 其他分支线路虽然使用3线接口但是只有一根通信线，有线端对应接收机上通道“S”标识插入，顺序为：以电源线为左，将排线从左至右依次插入接收机的CH1至CH5.

![](/assets/img/ele-4.png)

![](/assets/img/ele-6.png)

## 分电板安装及接线方法
分电板可以避免电源一对多包扎接线。H250工作时，锂电池要同时为四个电调同时供电，而电调电源输入线一般较粗，以一对多的接线方法线路显得凌乱且包扎上也不方便处理，既不美观，也不稳定。借助分电板不仅可以解决线路捆绑包扎问题，多余的接口还可以被图传，灯饰等利用。

分电板的丝印层一般都会标识电极符号，合理布局线路，用烙铁焊接处理接头即可。

![](/assets/img/ele-7.png)

**做完这一步，就可以进行[飞控CC3D的配置](./h250-config.html)**，最后再进行下面桨叶的安装。

## 桨叶的安装

H250需要两对正、反桨，在[H250选材列表](./h250-list.html)中笔者对桨叶、电机的型号选择及匹配都有介绍，这里不在赘述。关于正反桨，人们相对的将桨叶分成正、反桨叶，为了简单说明桨叶的安装**笔者在这里定义：塑料桨叶字面朝上，左手按住中心圆孔，右手推桨叶斜面使其圆周运动，若顺时针圆周运动定义为正桨，安装H250的1、3号电机位置；若逆时针圆周运动定义为反桨，安装H250的2、4号电机位置。**对号入座，用螺母紧固。

**桨叶的正确安装建立在选择CCW、CW类型电机和电机旋转方向基础之上，用户在配置电机确认电机的转向时请勿安装桨叶，确定类型及转向正确无误再用螺帽固定对应的桨叶**。