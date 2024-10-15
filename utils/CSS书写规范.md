# CSS书写规范

## CSS属性书写顺序:
1. 布局定位属性：display / position / float / clear / visibility / overflow（建议 display 第一个写，毕竟关系到模式）
2. 自身属性：width / height / margin / padding / border / background
3. 文本属性：color / font / text-decoration / text-align / vertical-align / white- space / break-word
4. 其他属性（CSS3）：content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient …

### 代码实例
```CSS
.jdc
{
    display: block;
    position: relative;
    float: left;
    width: 100px;
    height: 100px;
    margin: 0 10px;
    padding: 20px 0;
    font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
    color: #333;
    background: rgba(0,0,0,.5);
    border-radius: 10px;
 } 
```

<hr>

## CSS常用类名表

|ClassName|含义|
|:-:|:-:|
|about|关于
|account|账户|
|arrow|箭头图标|
|article|文章|
|aside|边栏
|audio|音频
|avatar|头像
|bg,background|背景|
|bar|栏（工具类）|
|branding|品牌化|
|crumb,breadcrumbs|面包屑|
|btn,button|按钮|
|caption|标题，说明|
|category|分类|
|chart|图表
|clearfix|清除浮动|
|close|关闭
|col,column|列|
|comment|评论|
|community|社区|
|container|容器|
|content|内容|
|copyright|版权|
|current|当前态，选中态|
|default|默认|
|description|描述|
|details|细节|
|disabled|不可用|
|entry|文章，博文|
|error|错误
|even|偶数，常用于多行列表或表格中|
|fail|失败（提示）|
|feature|专题|
|fewer|收起
|field|用于表单的输入区域|
|figure|图
|filter|筛选
|first|第一个，常用于列表中|
|footer|页脚
|forum|论坛
|gallery|画廊|
|group|模块，清除浮动|
|header|页头
|help|帮助
|hide|隐藏
|hightlight|高亮|
|home|主页
|icon|图标
|info,information|信息|
|last|最后一个，常用于列表中|
|links|链接
|login|登录
|logout|退出
|logo|标志
|main|主体
|menu|菜单
|meta|作者、更新时间等信息栏，一般位于标|题之下
|module|模块
|more|更多（展开）|
|msg,message|消息|
|nav,navigation|导航|
|next|下一页|
|nub|小块
|odd|奇数，常用于多行列表或表格中|
|off|鼠标离开|
|on|鼠标移过
|output|输出
|pagination|分页|
|pop,popup|弹窗|
|preview|预览|
|previous|上一页|
|primary|主要|
|progress|进度条|
|promotion|促销|
|rcommd,recommendations|推荐|
|reg,register|注册|
|save|保存
|search|搜索
|secondary|次要|
|section|区块|
|selected|已选|
|share|分享
|show|显示
|sidebar|边栏，侧栏|
|slide|幻灯片，图片切换|
|sort|排序
|sub|次级的，子级的|
|submit|提交
|subscribe|订阅|
|subtitle|副标题|
|success|成功（提示）|
|summary|摘要|
|tab|标签页|
|table|表格
|txt,text|文本|
|thumbnail|缩略图|
|time|时间
|tips|提示
|title|标题
|video|视频
|wrap|容器，包，一般用于最外层|
|wrapper|容器，包，一般用于最外层|

<hr>

## CSS初始化代码
```CSS
/* 所有内外边距清零 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* css3 抗锯齿性（文字放大后会有锯齿性），让文字显示的更清晰  */
    -webkit-font-smoothing: antialiased;
    background-color: #fff;
    /* 文字：大小为12px/行高是文字的1.5倍 字体（'\5B8B\4F53'） 就是宋体的意思，因为汉字可能会显示成乱码，所以用 unicode ） */
    font: 12px/1.5 Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, '\5B8B\4F53', sans-serif;
    color: #333;
}

/* em, i 标签会默认让字体切斜，设置成正常显示 */
em,
i {
    font-style: normal;
}

/* 去除 a 标签的默认样式 */
a {
    text-decoration: none;
    color: #333;
}

/* 去除 li 标签的默认样式 */
li {
    list-style: none;
}

img {
    /* 兼容低版本浏览器，如果图片外边包含了链接会有边框的问题 */
    border: 0;
    /* 取消图片底部会有空隙的问题 */
    vertical-align: middle;
}

/* 按钮时的鼠标移上去形状 */
input[type=submit],
input[type=reset],
input[type=button],
button {
    cursor: pointer;
}

/* 去除默认表单元素的轮廓线（默认的太丑了） */
input,
select,
textarea {
    outline: none;
    overflow: hidden;
    border: 0;
}

/* 去除多行文本框默认可拉伸 */
textarea {
    resize: none;
}

/* 清除浮动 */
.clearfix::after {
    content: '\200B';
    display: block;
    clear: both;
    visibility: hidden;
    height: 0;
}

/* 清除浮动（兼容IE） */
.clearfix {
    *zoom: 1;
}
```

## 项目文件夹的命名

|文件夹名称|说明|
|:-|:-|
|project name|项目文件夹|
|images|样式类图片文件夹|
|css|样式文件夹|
|upload|产品类图片文件夹|
|fonts|字体类文件夹|
|js|脚本文件夹|