---
title: HTML 属性
date: 2024-05-16 00:16:42
order: 2
---

## 无序列表：`<ul>`

`<ul>` 元素用来将没有数字顺序的一组数据进行分组，并且它们的数字顺序是没有意义的。举个例子，无序列表的列表项通常通过一个字符进行装饰，这些字符的形式可以是点，圆乃至方形。虽然这个字符没有直接在页面上定义，但是可以用与之相关的 CSS 对其进行操作，例如使用 `list-style-type` 属性。

<!-- prettier-ignore-start -->
| `<ul>` 属性 | 说明 |
| --- | --- |
| `type` | 用于设置列表的着重号样式。请使用 CSS 的 `list-style-type` 属性作为代替 <Badge text="已弃用" type="warning" />|\
| | - `circle`：圆-空心 <Badge text="默认值" type="info" />|\
| | - `disc`：圆-实心|\
| | - `square`：方块-实心|
| `compact` | 此布尔属性提示列表是否需要被渲染为更紧凑的样式 <Badge text="已弃用" type="warning" />|\
| | - 用户代理决定如何解释这个属性，且并非所有浏览器都支持它|\
| | - 请使用 CSS 属性 `line-height` 并将它的值设为 80% 来替代该属性 |
<!-- prettier-ignore-end -->

## 有序列表：`<ol>`

<!-- prettier-ignore-start -->
| `<ol>` 属性       | 说明                                                |
| ---------- | --------------------------------------------------- |
| `reversed` |此布尔值属性指定列表中的条目是否是倒序排列的，即编号是否应从高到低反向标注|
| `start`    |一个整数值属性，指定了列表编号的起始值|
| `type`     |设置编号的类型：编号类型适用于整个列表，除非在 `<ol>` 元素的 `<li>` 元素中使用不同的 type 属性|\
| | - `1` 表示数字编号（默认） |\
| | - `a` 表示小写英文字母编号|\
| | - `A` 表示大写英文字母编号|\
| | - `i` 表示小写罗马数字编号|\
| | - `I` 表示大写罗马数字编号|
<!-- prettier-ignore-end -->

## 列表项元素：`<li>`

`<li>` 元素用于表示列表中的项目。它必须包含在一个父元素中：无序列表（`<ul>`）、有序列表（`<ol>`）或菜单（`<menu>`）。在无序列表和菜单中，列表项通常使用项目符号显示。在有序列表中，通常在左侧显示一个升序计数器，如数字或字母。

<!-- prettier-ignore-start -->
| `<li>` 属性       | 说明                                                |
| ---------- | --------------------------------------------------- |
| `value` |这个整数属性指示由 `<ol>` 元素定义的列表项当前序数值|
| `type`     |该字符属性表示编号类型。该类型会覆盖其父元素 `<ol>` 使用的类型（如果有的话） <Badge text="已弃用" type="warning" />|\
| | - `1` 表示数字编号（默认） |\
| | - `a` 表示小写英文字母编号|\
| | - `A` 表示大写英文字母编号|\
| | - `i` 表示小写罗马数字编号|\
| | - `I` 表示大写罗马数字编号|
<!-- prettier-ignore-end -->

## 列表项目

- `<dl>` 元素是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键 - 值对列表)。它可以包括零组或多组 dom 结构，每组 dom 结构中包含一个或多个 `<dt>` 元素，以及 一个或多个 `<dd>` 元素。
- `<dt>` 元素用于在一个定义列表中声明一个术语。该元素仅能作为 `<dl>` 的子元素出现。通常在该元素后面会跟着 `<dd>` 元素，然而，多个连续出现的 `<dt>` 元素都将由出现在它们后面的第一个 `<dd>` 元素定义。
- `<dd>` 元素用来指明一个描述列表 (`<dl>`) 元素中一个术语的描述。这个元素只能作为描述列表元素的子元素出现，并且必须跟着一个 `<dt>` 元素。

```html
<dl>
  <dt>术语1</dt>
  <dd>描述1</dd>
  <dt>术语2</dt>
  <dd>描述2-1</dd>
  <dd>描述2-2</dd>
</dl>
```

## 超链接：`<a>`

`<a>` 元素可以通过它的 href 属性创建通向其他网页、文件、电子邮件地址、同一页面内的位置或任何其他 URL 的超链接。

<!-- prettier-ignore-start -->
| `<a>` 属性 | 说明                                                       |
| -------- | ----------------------------------------------------------- |
| `href`   | 超链接所指向的 URL     |
| `hreflang`   | 该属性用于指定所链接到的文档的人类语言     |
| `ping`   | 包含一个以空格分隔的 URL 列表，当跟随超链接时，浏览器会发送带有正文 PING 的 POST 请求。通常用于跟踪。   |
| `name`   | 规定锚的名称                                                |
| `target` | 规定在何处打开链接文档                                      |\
|          | - `_self`：默认；在相同的框架中打开被链接文档               |\
|          | - `_blank`：在新窗口中打开被链接文档                        |\
|          | - `_parent`：在父框架集中打开被链接文档（配合 iframe 使用） |\
|          | - `_top`：在整个窗口中打开被链接文档（配合 iframe 使用）    |
| `download`   | 导致浏览器将链接的 URL 视为下载资源。可以使用或不使用 filename 值： |\
| | - `filename`：决定文件名的值。/ 和 \ 被转化为下划线（_）。文件系统可能会阻止文件名中其他的字符，因此浏览器会在必要时适当调整文件名。 |\
| | - 如果没有指定值，浏览器会从多个来源决定文件名和扩展名： |\
| |   - `Content-Disposition` HTTP 标头|\
| |   - URL 路径的最后一段|\
| |   - 媒体类型。来自 `Content-Type` 标头，`data: URL` 的开头，或 `blob: URL` 的 `Blob.type`|
<!-- prettier-ignore-end -->

```html
<a href="https://sbgong.github.io">sbgong</a>

<a href="#C1">第一章</a>
<a name="C1">第一章</a>
```

## 图像标签：`<img>`

注意：从技术上讲 img 标签并不会在网页中插入图像，而是从网页上链接图像；img 标签创建的是被引用图像的占位空间。

| 属性     | 说明                                                  |
| -------- | ----------------------------------------------------- |
| `src`    | 规定显示图像的 URL <Badge text="必需" type="error" /> |
| `alt`    | 规定图像的替代文本 <Badge text="必需" type="error" /> |
| `title`  | 鼠标悬停时显示的内容                                  |
| `width`  | 设置图像的宽度；单位：px 或百分比                     |
| `height` | 定义图像的高度；单位：px 或百分比                     |

```html
<img src="/1.jpg" alt="sbgong" /><br />
<img src="/2.jpg" height="200" width="200" />
```

## 地图标签：`<map>` & `<area>`

### map 标签

map 标签定义一个客户端图像映射。图像映射（image-map）指带有可点击区域的一幅图像。

- area 元素永远嵌套在 map 元素内部。area 元素可定义图像映射中的区域。
- img 中的 usemap 属性可引用 map 中的 id 或 name 属性。

| 属性   | 说明                      |
| ------ | ------------------------- |
| `id`   | 为 map 标签定义唯一的名称 |
| `name` | 为 image-map 规定的名称   |

### area 标签

area 标签定义图像映射中的区域

| 属性     | 说明                                                    |
| -------- | ------------------------------------------------------- |
| `alt`    | 定义此区域的替换文本 <Badge text="必需" type="error" /> |
| `coords` | 定义可点击区域（对鼠标敏感的区域）的坐标                |
| `shape`  | 定义区域的形状                                          |
| `href`   | 定义此区域的目标 URL                                    |
| `target` | 规定在何处打开 href 属性指定的目标 URL                  |

### 代码案例

```html
<!-- 带有可点击区域的图像映射 -->
<img src="planets.jpg" border="0" usemap="#planetmap" alt="Planets" />

<map name="planetmap" id="planetmap">
  <area shape="circle" coords="180,139,14" href="venus.html" alt="Venus" />
  <area shape="circle" coords="129,161,10" href="mercur.html" alt="Mercury" />
  <area shape="rect" coords="0,0,110,260" href="sun.html" alt="Sun" />
</map>
```

## meter 标签

meter 标签定义已知范围或分数值内的标量测量。也被称为 gauge（尺度）；例子：磁盘用量、查询结果的相关性等等。

注意：meter 标签不应用于指示进度（在进度条中）。如果标记进度条，请使用 progress 标签。

| 属性      | 说明                                                |
| --------- | --------------------------------------------------- |
| `value`   | 规定度量的当前值 <Badge text="必需" type="error" /> |
| `max`     | 规定范围的最大值                                    |
| `min`     | 规定范围的最小值                                    |
| `high`    | 规定被视作高的值的范围                              |
| `low`     | 规定被视作低的值的范围                              |
| `optimum` | 规定度量的优化值                                    |

```html
<meter value="3" min="0" max="10">3/10</meter><br />
<meter value="0.6">60%</meter>
<meter min="0" low="40" high="90" max="100" value="95"></meter>
<meter value="0.3" high="0.9" low="0.1" optimum="0.5"></meter>
```

## progress 标签

| 属性    | 说明                     |
| ------- | ------------------------ |
| `max`   | 规定任务一共需要多少工作 |
| `value` | 规定已经完成多少任务     |

```html
<progress value="22" max="100"></progress><br />
<progress></progress>
```

## audio 标签

由于版权等原因，不同的浏览器可支持播放的格式是不一样的；注意：谷歌浏览器把音频和视频自动播放禁止了。

| 属性                  | 说明                                                                                                                                                                                          |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `autoplay="autoplay"` | 如果出现该属性，则音频在就绪后马上播放                                                                                                                                                        |
| `controls="controls"` | 如果出现该属性，则向用户显示控件，比如播放按钮、暂停、音量等                                                                                                                                  |
| `loop="loop"`         | 如果出现该属性，则每当音频结束时重新开始播放                                                                                                                                                  |
| `muted="muted"`       | 规定视频输出应该被静音                                                                                                                                                                        |
| `preload`             | 规定是否在页面加载后载入音频；如果设置了 autoplay 属性，则忽略该属性<br>（1）`auto`：当页面加载后载入整个音频<br>（2）`meta`：当页面加载后只载入元数据<br>（3）`none`：当页面加载后不载入音频 |
| `src="URL"`           | 要播放的音频的 URL                                                                                                                                                                            |

```html
<!-- 多浏览器支持的方案 -->
<audio controls="controls" autoplay="autoplay" loop="loop" muted preload="auto">
  <source src="/i/song.ogg" type="audio/ogg" />
  <source src="/i/song.mp3" type="audio/mpeg" />
  Your browser does not support the audio element.
</audio>
```

## video 标签

| 属性       | 说明                                                                                                                                                                                          |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `src`      | 要播放的视频的 URL                                                                                                                                                                            |
| `width`    | 设置视频播放器的宽度                                                                                                                                                                          |
| `height`   | 设置视频播放器的高度                                                                                                                                                                          |
| `controls` | 如果出现该属性，则向用户显示控件，比如播放按钮、音量等                                                                                                                                        |
| `autoplay` | 如果出现该属性，则视频在就绪后马上播放                                                                                                                                                        |
| `loop`     | 如果出现该属性，则当媒介文件完成播放后再次开始播放                                                                                                                                            |
| `muted`    | 规定视频的音频输出应该被静音                                                                                                                                                                  |
| `poster`   | 规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像                                                                                                                                  |
| `preload`  | 规定是否在页面加载后载入音频；如果设置了 autoplay 属性，则忽略该属性<br>（1）`auto`：当页面加载后载入整个音频<br>（2）`meta`：当页面加载后只载入元数据<br>（3）`none`：当页面加载后不载入音频 |

```html
<!-- 多浏览器支持的方案 -->
<video
  controls="controls"
  autoplay="autoplay"
  width="320"
  height="240"
  loop="loop"
  muted
  poster="/img/w3school.gif"
  preload="auto"
>
  <source src="movie.ogg" type="video/ogg" />
  <source src="movie.mp4" type="video/mp4" />
  <track kind="subtitles" src="subs_chi.srt" srclang="zh" label="Chinese" />
  <track kind="subtitles" src="subs_eng.srt" srclang="en" label="English" />
  Your browser does not support the video tag.
</video>
```

## track 标签

| 属性      | 说明                                                                                                                                                                                                                                                                                                                                       |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `default` | 规定该轨道是默认的，假如没有选择任何轨道                                                                                                                                                                                                                                                                                                   |
| `src`     | 轨道的 URL                                                                                                                                                                                                                                                                                                                                 |
| `label`   | 轨道的标签或标题                                                                                                                                                                                                                                                                                                                           |
| `srclang` | 轨道的语言，若 kind 属性值是 "subtitles"，则该属性必需的                                                                                                                                                                                                                                                                                   |
| `kind`    | 表示轨道属于什么文本类型<br>（1）`captions`：该轨道定义将在播放器中显示的简短说明<br>（2）`chapters`：该轨道定义章节，用于导航媒介资源<br>（3）`descriptions`：该轨道定义描述，用于通过音频描述媒介的内容，假如内容不可播放或不可见<br>（4）`metadata`：该轨道定义脚本使用的内容<br>（5）`subtitles`：该轨道定义字幕，用于在视频中显示字幕 |

```html
<track kind="subtitles" default src="chisubs.srt" srclang="zh" />
<track kind="subtitles" src="subschi.srt" srclang="zh" label="Chinese" />
<track kind="subtitles" src="subseng.srt" srclang="en" label="English" />
```

## embed 标签

embed 可以用来插入各种多媒体，格式可以是 Midi、Wav、AIFF、AU、MP3 等等。url 为音频或视频文件及其路径，可以是相对路径或绝对路径

| 属性     | 说明               |
| -------- | ------------------ |
| `src`    | 嵌入内容的 URL     |
| `type`   | 定义嵌入内容的类型 |
| `width`  | 设置嵌入内容的宽度 |
| `height` | 设置嵌入内容的高度 |

```html
<embed src="helloworld.swf" />
<embed src="tulip.jpg" width="300" height="300" />
<embed src="helloworld.swf" type="application/x-shockwave-flash" />
<embed src="http://player.youku.com/player.php/sid/XMTI4MzM2MDIwOA==/v.swf" allowFullScreen="true" quality="high" width="480" height="400" align="middle" allowScriptAccess="always" type="application/x-shockwave-flash"></embed>
```

## object-param 标签

```html
<object classid="clsid:F08DF954-8592-11D1-B16A-00C0F0283628" id="Slider1" width="100" height="50">
  <param name="BorderStyle" value="1" />
  <param name="MousePointer" value="0" />
  <param name="Enabled" value="1" />
  <param name="Min" value="0" />
  <param name="Max" value="10" />
</object>
```

## frameset 标签

frameset 元素可定义一个框架集。它被用来组织多个窗口（框架）。每个框架存有独立的文档。在其最简单的应用中，frameset 元素仅仅会规定在框架集中存在多少列或多少行。您必须使用 cols 或 rows 属性。

注意：

- 不能将 frameset 标签和 body 标签一起使用
- 如果需要为不支持框架的浏览器添加一个 noframes 标签，请务必将此标签放置在 body 标签中

| 属性   | 说明                                            |
| ------ | ----------------------------------------------- |
| `cols` | 定义框架集中列的数目和尺寸；单位：pixels、%、\* |
| `rows` | 定义框架集中行的数目和尺寸；单位：pixels、%、\* |

```html
<html>
<frameset cols="25%,50%,25%">
  <frame src="/example/html/frame_a.html">
  <frame src="/example/html/frame_b.html">
  <frame src="/example/html/frame_c.html">

<noframes>
<body>您的浏览器无法处理框架！</body>
</noframes>

</frameset>
</html>
```

## frame 标签

> frame 标签定义 frameset 中的一个特定的窗口（框架）

| 属性           | 说明                                                                                                                                                   |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `frameborder`  | 规定是否显示框架周围的边框<br>（1）1：有边框；默认值<br>（2）0：无边框                                                                                 |
| `longdesc`     | 规定一个包含有关框架内容的长描述的页面                                                                                                                 |
| `marginheight` | 定义框架的上方和下方的边距                                                                                                                             |
| `marginwidth`  | 定义框架的左侧和右侧的边距                                                                                                                             |
| `name`         | 规定框架的名称                                                                                                                                         |
| `noresize`     | 规定用户无法调整框架的大小                                                                                                                             |
| `scrolling`    | 规定是否在框架中显示滚动条<br>（1）`auto`：在需要的时候显示滚动条<br>（2）`yes`：始终显示滚动条（即使不需要）<br>（3）`no`：从不显示滚动条（即使需要） |
| `src`          | 规定在框架中显示的文档的 URL                                                                                                                           |

```html
<!-- 不带边框的双框架页面 -->
<frame src="frame_a.htm" frameborder="0" />

<!-- 第一个框架的上边距和下边距是 50 像素，第二个框架的上边距和下边距是 0 -->
<frame src="/example/html/frame_a.html" marginheight="50" />
<frame src="/example/html/frame_b.html" marginheight="0" />

<!-- 第一个框架的左边距和右边距是 50 像素，第二个框架的左边距和右边距是0  -->
<frame src="frame_a.htm" marginwidth="50" />
<frame src="frame_b.htm" marginwidth="0" />
<!-- 被命名的框架 -->
<frame src="frame_a.htm" name="frame_a" />
<!-- 无法调整大小的框架 -->
<frame src="frame_a.htm" noresize="noresize" />
<!-- 总是显示滚动条的框架 -->
<frame src="frame_a.htm" scrolling="yes" />
```

## iframe 标签

> iframe 元素会创建包含另外一个文档的内联框架（即行内框架）

| 属性           | 说明                                                                                                                                                       |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `frameborder`  | 规定是否显示框架周围的边框<br>（1）1：有边框；默认值<br>（2）0：无边框                                                                                     |
| `longdesc`     | 规定一个页面，该页面包含了有关 iframe 的较长描述                                                                                                           |
| `marginheight` | 定义 iframe 的顶部和底部的边距                                                                                                                             |
| `marginwidth`  | 定义 iframe 的左侧和右侧的边距                                                                                                                             |
| `name`         | 规定 iframe 的名称                                                                                                                                         |
| `scrolling`    | 规定是否在 iframe 中显示滚动条<br>（1）`auto`：在需要的时候显示滚动条<br>（2）`yes`：始终显示滚动条（即使不需要）<br>（3）`no`：从不显示滚动条（即使需要） |
| `src`          | 规定在 iframe 中显示的文档的 URL                                                                                                                           |
| `width`        | 定义 iframe 的宽度                                                                                                                                         |

```html
<iframe src="/index.html" width="400px" height="300px">
  <p>Your browser does not support iframes.</p>
</iframe>
```
