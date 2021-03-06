#### MVC是什么
- M是Model，数据类型，负责数据相关的事物，问题的本质就是Model，解决问题就是给问题建立Model
- V是View，视图，负责用户界面
- C是Controller控制器，负责监听用户事件，然后调用M和V更新数据和视图

在知乎上看到一个题主用场景解释了三者的关系：
- 在一个阳光明媚的午后, 你跟千千万万的小白领一样来到了银河SOHO附近的星巴克. 你径直走到一位棕围裙的咖啡师面前:
  "您好, 给我来一个中杯的拿铁"
  "您要的是这个么?" 咖啡师指着Tall的杯子微笑地问道
  "嗯, 这个中杯" 你指着Grande的杯子说道
  "对不起先生, 那个是大杯, 这个才是中杯" 咖啡师继续保持尴尬而不失礼貌的微笑, 指着Tall的杯子说道
  "你这不是大中小三个杯子吗? 我要这个中杯" 你觉得自己理直气壮
  "对不起先生, 那个是大杯. 这才是中杯...中杯, 大杯, 特大杯" 咖啡师指着Tall, Grande, Venti解释道
  好了...你不是罗永浩, 你也不用扇自己几个嘴巴子.
  
- 重点是在刚才这个情景里, 你是User, 你点的中杯拿铁就是你的User Request.
  对咖啡师来说, 一杯拿铁真是low爆了, 根本无法展现其棕围裙的功力. 不过是这么几步:
  1. 用浓缩咖啡机把咖啡豆磨成粉
  2. 加热牛奶打奶泡
  3. 把磨碎的咖啡粉放入过滤斗里, 锁在冲煮头上
  4. 按下double选项, 制作一杯浓缩咖啡
  5. 把牛奶倒入浓缩咖啡中并按心情决定是否拉一个花
  6. 把咖啡递给你
  
  咖啡师的大脑里存储着这些步骤, 她的脑瓜子就是Controller.
  只要你点的饮品(User Request)是她能理解和制作的, 她就可以立即开始工作.
  如果你非捣乱, 来星巴克点豆汁, 咖啡师(Controller)无法理解你这个User Request, 就会报错(比如返回503/404)
  
  咖啡师没法给你做豆汁的原因除了味儿太大以外, 更重要的是他的工具和材料有限.
  咖啡师有限的工具和材料就是Model, 包括下面几种东西:
  * 贼老贵的浓缩咖啡机
  * 非洲哥伦比亚高萃取精猫屎咖啡豆
  * 分不清大中小还是特大大中的咖啡杯
  * 咖啡师一会如萝卜一般一会如青葱一般的双手
  在一家星巴克里, 所有的材料都是共享的。你换一个咖啡师还是可以给你做同样的拿铁.
  类似的，即使来一个黑围裙咖啡师, 他也做不了豆汁, 因为没有那些原材料.
  
  最后, 你拿到手里的, 看得见摸得着可以喝的这杯拿铁就是View.
  这杯咖啡(View)是从有限的材料(Model)里来的, 并由咖啡师的大脑(Controller)精心组织和安排并制作的.
  同样的原料也可以作出不同的咖啡比如美式比如摩卡比如卡布基诺: 同样的Model通过Controller可以组织成不同的View.
  
  奇思妙想:
  * 想再来一杯? 你看着你空空如也的咖啡杯(View)是没有任何作用的. 你只能再跟咖啡师要一杯(another User Request)
  * 咖啡师接到你的order之后到给你端上咖啡的时间肯定是越短越好. 这就告诉我们Controller应该maintain很少的logic. 一个NB的咖啡师可能在每天开门之前就把原材料都准备好.
  * 咖啡师能不能直接把咖啡粉和牛奶倒到你嘴里然后搅一搅让你喝下去? 行是可行但是可能会造成星巴克流血事件. 咖啡师还是应该在吧台后面把咖啡做好后再端给你. 这就告诉我们View不应该contain太多的logic
  
  回到Web Development:
  1. 用户发送了一个Request, 比如"/home"
  2.Controller接到这个Request, 会发出一系列的指令: 比如让Model执行一些操作或者更新某个View
  3.Model接到Controller的指令, 去数据库里拿出一些数据返回给Controller
  4.Controller接到数据, 更新了"/home"的页面
  5. 用户看到了这个页面

#### 怎么用js引入css   jquery
- 用import   ' 路径'   
**- 引入jquery 用 $ from '路径'
- console.log ($) 就会显示   引入是否成功

前提是yarn   add jquery        或者  npm install   jquery

#### 所有操作系统滚动条大概在14-19px

#### 模块化的背景
- 早期，js程序很小，大多用来执行独立的脚本任务，在web页面的地方提供一定交互，所以一般不需要多大的脚本。
- 现在罪行的浏览器开始原生支持模块化功能。

#### 导出模块的功能
- 我们用export语句来执行，语句使用花括号起来用逗号分割。
- export { name, draw, reportArea, reportPerimeter };

#### 导出模块
- export需要关键字from，然后是模块路径。


