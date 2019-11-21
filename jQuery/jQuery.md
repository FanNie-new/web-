# `jQuery

## jQuery 教程

**`jQuery`是一个`JavaScript`库**

**`jQuery`极大地简化了`JavaScript`编程**

**`jQuery`很容易学习**

---

### 每一章中用到的实例

```html
<html>

<head>
    <script type="text/javascript" src="jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("p").click(function() {
            $(this).hide();
        });
    });
    </script>
</head>

<body>
    <p>If you click on me, I will disappear.</p>
</body>

</html>
```

### 你将学到什么

----



学到如何通过使用`jQuery`应用`JavaScript`效果。

`jQuery`是一个"写的更少，但做的更多"的轻量级`JavaScript`库。

基本上，将学习到如何选取`HTML`元素，以及如何对它们执行类似隐藏、移动记忆操作其内容等任务。

---

### 需要具备的基础知识

在开始学习`jQuery`之前，你应该对以下知识有基本的了解：

- `HTML`
- `CSS`
- `JavaScript`

---

## jQuery 简介

**`jQuery`库可以通过一行简单的标记被添加到网页中**

---

### `jQuery`库 - 特性

`jQuery`是一个`JavaScript`函数库

`jQuery`库包含以下特性：

- `HTML`元素选取
- `HTML`元素操作
- `CSS`操作
- `HTML`事件函数
- `JavaScript` 特效和动画
- `HTML DOM` 遍历和修改
- `AJAX`
- `Utilities`

---

### 向你的页面添加`jQuery`库

`jQuery`库位于一个`JavaScript`文件中，其中包含了所有的`jQuery`函数。

可以通过下面的标记把`jQuery`添加到网页中：

```html
<head>
<script type="text/javascript" src="jquery.js"></script>
</head>
```

注意：`<script>`标签应该位于页面的`<head>`部分。

---

### 基础`jQuery`实例

下面的例子演示了`jQuery` 的`hide()`函数，隐藏了`HTML`文档中所用的`<p>`元素。

**实例**

```html
<html>

<head>
    <script type="text/javascript" src="jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide();
        });
    });
    </script>
</head>

<body>
    <h2>This is a heading</h2>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
    <button type="button">Click me</button>
</body>

</html>
```

---

### 下载`jQuery`

共有两个版本的`jQuery`可供下载：一份时精简过的，另一份是未压缩的(供调试或阅读)。

这连个版本都可以从 [jQuery.com]() 下载。

---

### 库的替代

`Google`和`Microsoft`对`jQuery`的支持都很好。

如果你不愿意在自己的计算机上存放`jQuery`库，那么可以从`Google`或`Microsoft`加载`CDN jQuery`核心文件。

**使用`Google`的`CDN`**

```html
<head>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs
/jquery/1.4.0/jquery.min.js"></script>
</head>
```

**使用`Microsoft`的`CDN`**

```html
<head>
<script type="text/javascript" src="http://ajax.microsoft.com/ajax/jquery
/jquery-1.4.min.js"></script>
</head>
```

---

## jQuery 安装

---

### 把`jQuery`添加到你的网页

如需使用`jQuery`，你需要下载`jQuery`库，然后把它包含在希望使用的网页中。

`jQuery`库是一个`JavaScript`文件，你可以使用`HTML`的`<script>`标签引用它：

```html
<head>
<script src="jquery.js"></script>
</head>
```

**注意**：`<script>`标签应该位于页面的`<head>`部分。

**提示**：你是否很疑惑为什么没有在`<script>`标签中使用`type="text/javascript"`？

在`HTML5`中，不必那样做了。`JavaScript`是`HTML5`以及所有现代浏览器的默认脚本语言!

---

### 下载`jQuery`

有两个版本的`jQuery`可供下载：

- `Production version` - 用于实际的网站中，已被精简和压缩。
- `Development version` - 用于测试和开发(未压缩，是可读的代码)

这两个版本都可以从 [jQuery.com]() 下载。

提示：你可以把下载文件放到与页面相同的目录中，这样更方便使用。

---

### 替代方案

如果你不希望下载并存放`jQuery`，那么也可以通过`CDN`(内容分发网络)引用它。

谷歌和微软的服务器都存有`jQuery`。

如需从谷歌或微软引用`jQuery`，请使用以下代码之一：

**`Google CDN`**：

```html
<head>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.0/jquery.min.js">
</script>
</head>
```

提示：通过`Google CDN`来获得最新可用的版本：

如果你观察上什么的`Google URL` - 在`URL`中规定了`jQuery`版本(1.8.0)。如果你希望使用最新版本的`jQuery`，也可以从版本字符串的末尾(比如本例1.8)删除一个数字，谷歌会返回1.8系列中最新的可用版本(1.8.0、1.8.1等等)，或者也可以只剩第一个数字，那么谷歌会返回1系列中最新的可用版本(从1.1.0到1.9.9).

**`Microsoft CDN`**：

```html
<head>
<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js">
</script>
</head>
```

提示：使用谷歌或微软的`jQuery`，有一个很大的优势：

许多用户在访问其他站点时，已经从谷歌或微软加载过`jQuery`。所以结果是，当他们访问你的站点时，会从缓存中加载`jQuery`，这样可以减少加载时间。同时，大多数`CDN`都可以确保当用户向其请求文件时，会从离用户最近的服务器上返回响应，这样也可以以提高加载速度。

---

## jQuery 语法

---

通过`jQuery`，你可以选取(查询，`query`)`HTML`元素，并对它们执行"操作"(`actions`)。

---

### jQuery语法实例

演示`jQuery hide()`函数，隐藏当前的`HTML`元素。

```html
$(this).hide()

<html>

<head>
    <script type="text/javascript" src="/jquery/jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $(this).hide();
        });
    });
    </script>
</head>

<body>
    <button type="button">Click me</button>
</body>

</html>
```

演示`jQuery hide()`函数，隐藏`id="test"`的元素。

```html
$("#test").hide()

<html>

<head>
    <script type="text/javascript" src="/jquery/jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#test").hide();
        });
    });
    </script>
</head>

<body>
    <h2>This is a heading</h2>
    <p>This is a paragraph.</p>
    <p id="test">This is another paragraph.</p>
    <button type="button">Click me</button>
</body>

</html>
```

演示`jQuery hide()`函数，隐藏所有`<p>`元素。

```html
$("p").hide()

<html>

<head>
    <script type="text/javascript" src="/jquery/jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide();
        });
    });
    </script>
</head>

<body>
    <h2>This is a heading</h2>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
    <button type="button">Click me</button>
</body>

</html>
```

演示`jQuery hide()`函数，隐藏所有`class="test"`的元素。

```html
$(".test").hide()

<html>

<head>
    <script type="text/javascript" src="/jquery/jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $(".test").hide();
        });
    });
    </script>
</head>

<body>
    <h2 class="test">This is a heading</h2>
    <p class="test">This is a paragraph.</p>
    <p>This is another paragraph.</p>
    <button type="button">Click me</button>
</body>

</html>
```

---

### jQuery语法

`jQuery`语法是为`HTML`元素的选取编制的，可以通过对元素执行某些操作。

基础语法是：**`$(selector).action()`**

- 美元符号定义`jQuery`
- 选择符`(selector)`"查询"和"查找"`HTML`元素
- `jQuery`的`action()`执行对元素的操作

**示例**

`$(this).hide()`- 隐藏当前元素

`$("p").hide()`- 隐藏所有段落

`$(".test").hide()`- 隐藏所有`class="test"`的所有元素

`$("#test").hide()`- 隐藏所有`id="test"`的元素

提示：`jQuery`使用的语法是`XPath`与`CSS`选择器语法的组合。

---

### 文档就绪函

我们可以注意到在实例中的所有`jQuery`函数位于一个`document ready`函数中：

```js
$(document).ready(function(){

--- jQuery functions go here ----

});
```

这是为了防止文档在完全加载(就绪)之前运行`jQuery`代码。

如果在文档没有完全加载之前就运行函数，操作可能失败。下面是两个具体的例子：

- 试图隐藏一个不存在的元素
- 获得未完全加载的图像的大小

## jQuery 选择器

---

**选择器允许你对元素组或单个元素进行操作**。

---

### `jQuery`选择器

在前面的章节中，我们展示了一些有关如何选取`HTML`元素的实例。

关键点是学习`jQuery`选择器是如何准确地选取你希望应用效果的元素。

`jQuery`元素选择器和属性选择器允许你通过标签名、属性名或内容对`HTML`元素进行选择。

选择器允许你对`HTML`元素组或单个元素进行操作。

在`HTML DOM`述语中：

选择器允许你对`DOM`元素组或单个`DOM`节点进行操作。

---

### `jQuery`元素选择器

`jQuery`使用`CSS`选择器来选取`HTML`元素。

`$("p")`选取`<p>`元素

`$("p.intro")`选取所有`class="intro"`的`<p>`元素

`$("p#demo")`选取所有`id="demo"`的`<p>`元素。

---

### `jQuery`属性选择器

`jQuery`使用`XPath`表达式来选择带有给定属性的元素。

 `$("[href]")`选取所有带有`href`属性的元素。

`$("[href='#']")`选取所有带有`href`值等于`"#"`的元素。

`$("[href!='#']")`选取所有带有`href`值不等于`"#"`的元素。

`$("[href$='.jpg']")`选取所有`href`值以`".jpg"`结尾的元素。

---

### `jQuery CSS`选择器

`jQuery CSS`选择器可用于改变`HTML`元素的`CSS`属性。

下面的例子把所有`p`元素的背景颜色更改为红色：

**实例**

```js
$("p").css("background-color","red");
```

---

### 更多的选择器实例

| 语法                   | 描述                                                       |
| :--------------------- | :--------------------------------------------------------- |
| `$(this)`              | 当前 `HTML `元素                                           |
| `$("p")`               | 所有 `<p> `元素                                            |
| `$("p.intro")`         | 所有` class="intro" `的` <p>` 元素                         |
| `$(".intro")`          | 所有 `class="intro" `的元素                                |
| `$("#intro")`          | `id="intro" `的元素                                        |
| `$("ul li:first")`     | 每个 `<ul>` 的第一个 `<li> `元素                           |
| `$("[href$='.jpg']")`  | 所有带有以 `".jpg"` 结尾的属性值的 `href `属性             |
| `$("div#intro .head")` | `id="intro" `的 `<div> `元素中的所有` class="head" `的元素 |

 如需完整的参考手册，请访问 [jQuery 选择器参考手册](https://www.w3school.com.cn/jquery/jquery_ref_selectors.asp)。 

---

## jQuery 事件

---

 **`jQuery` 是为事件处理特别设计的。** 

---

### `jQuery `事件函数

`jQuery` 事件处理方法是 `jQuery `中的核心函数。

事件处理程序指的是当` HTML` 中发生某些事件时所调用的方法。术语由事件“触发”（或“激发”）经常会被使用。

通常会把 `jQuery `代码放到 `<head>`部分的事件处理方法中：

**实例**

```html
<html>

<head>
    <script type="text/javascript" src="jquery.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide();
        });
    });
    </script>
</head>

<body>
    <h2>This is a heading</h2>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
    <button>Click me</button>
</body>

</html>
```

 在上面的例子中，当按钮的点击事件被触发时会调用一个函数： 

```js
$("button").click(function() {..some code... } )
```

 该方法隐藏所有` <p> `元素： 

```js
$("p").hide();
```

---

### 单独文件中的函数

如果您的网站包含许多页面，并且您希望您的` jQuery` 函数易于维护，那么请把您的` jQuery `函数放到独立的 `.js `文件中。

当我们在教程中演示` jQuery `时，会将函数直接添加到 `<head> `部分中。不过，把它们放到一个单独的文件中会更好，就像这样（通过 `src` 属性来引用文件）：

**实例**

```html
<head>
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript" src="my_jquery_functions.js"></script>
</head>
```

---

### `jQuery `名称冲突

`jQuery` 使用 `$` 符号作为 `jQuery` 的简介方式。

某些其他 `JavaScript `库中的函数（比如` Prototype`）同样使用 `$` 符号。

`jQuery` 使用名为 `noConflict()` 的方法来解决该问题。

***`var jq=jQuery.noConflict()`***，帮助您使用自己的名称（比如 `jq`）来代替` $ `符号。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $.noConflict();
    jQuery(document).ready(function() {
        jQuery("button").click(function() {
            jQuery("p").text("jQuery 仍在运行！");
        });
    });
    </script>
</head>

<body>
    <p>这是一个段落。</p>
    <button>测试 jQuery</button>
</body>

</html>
```

---

### 结论

由于 `jQuery `是为处理 `HTML `事件而特别设计的，那么当您遵循以下原则时，您的代码会更恰当且更易维护：

- 把所有 `jQuery` 代码置于事件处理函数中
- 把所有事件处理函数置于文档就绪事件处理器中
- 把 `jQuery `代码置于单独的` .js` 文件中
- 如果存在名称冲突，则重命名` jQuery` 库

---

### `jQuery` 事件

 下面是` jQuery `中事件方法的一些例子： 

| `Event` 函数                      | 绑定函数至                                     |
| :-------------------------------- | :--------------------------------------------- |
| `$(document).ready(function)`     | 将函数绑定到文档的就绪事件（当文档完成加载时） |
| `$(selector).click(function)`     | 触发或将函数绑定到被选元素的点击事件           |
| `$(selector).dblclick(function)`  | 触发或将函数绑定到被选元素的双击事件           |
| `$(selector).focus(function)`     | 触发或将函数绑定到被选元素的获得焦点事件       |
| `$(selector).mouseover(function)` | 触发或将函数绑定到被选元素的鼠标悬停事件       |

 如需完整的参考手册，请访问 [jQuery 事件参考手册](https://www.w3school.com.cn/jquery/jquery_ref_events.asp)。 

---

## jQuery 效果 - 隐藏和显示

---

 **隐藏、显示、切换，滑动，淡入淡出，以及动画，哇哦！** 

---

### 实例

`jQuery hide()`

演示一个简单的`jQuery hide()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js">
    </script>
    <script>
    $(document).ready(function() {
        $("p").click(function() {
            $(this).hide();
        });
    });
    </script>
</head>

<body>
    <p>如果您点击我，我会消失。</p>
    <p>点击我，我会消失。</p>
    <p>也要点击我哦。</p>
</body>

</html>
```

`jQuery hide()`

另一个`hide()`演示。如何隐藏部分文本。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".ex .hide").click(function() {
            $(this).parents(".ex").hide("slow");
        });
    });
    </script>
    <style type="text/css">
    div.ex {
        background-color: #e5eecc;
        padding: 7px;
        border: solid 1px #c3c3c3;
    }
    </style>
</head>

<body>
    <h3>中国办事处</h3>
    <div class="ex">
        <button class="hide" type="button">隐藏</button>
        <p>联系人：张先生<br />
            北三环中路 100 号<br />
            北京</p>
    </div>
    <h3>美国办事处</h3>
    <div class="ex">
        <button class="hide" type="button">隐藏</button>
        <p>联系人：David<br />
            第五大街 200 号<br />
            纽约</p>
    </div>
</body>

</html>
```

---

### `jQuery hide()` 和 `show()`

 通过 `jQuery`，您可以使用 `hide() `和 `show() `方法来隐藏和显示`HTML `元素： 

```js
$("#hide").click(function(){
  $("p").hide();
});

$("#show").click(function(){
  $("p").show();
});
```

**实例**

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("#hide").click(function() {
            $("p").hide();
        });
        $("#show").click(function() {
            $("p").show();
        });
    });
    </script>
</head>

<body>
    <p id="p1">如果点击“隐藏”按钮，我就会消失。</p>
    <button id="hide" type="button">隐藏</button>
    <button id="show" type="button">显示</button>
</body>

</html>
```

**语法**：

```js
$(selector).hide(speed,callback);

$(selector).show(speed,callback);
```

 可选的 `speed` 参数规定隐藏/显示的速度，可以取以下值："`slow`"、"`fast`" 或毫秒。 

 可选的 `callback` 参数是隐藏或显示完成后所执行的函数名称。 

 下面的例子演示了带有 `speed` 参数的 `hide() `方法： 

**实例**：

```js
$("button").click(function(){
  $("p").hide(1000);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide(1000);
        });
    });
    </script>
</head>

<body>
    <button type="button">隐藏</button>
    <p>这是一个段落。</p>
    <p>这是另一个段落。</p>
</body>

</html>
```

---

### `jQuery toggle()`

通过` jQuery`，您可以使用 `toggle() `方法来切换 `hide() `和 `show()` 方法。

显示被隐藏的元素，并隐藏已显示的元素：

**实例**：

```js
$("button").click(function(){
  $("p").toggle();
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").toggle();
        });
    });
    </script>
</head>

<body>
    <button type="button">切换</button>
    <p>这是一个段落。</p>
    <p>这是另一个段落。</p>
</body>

</html>
```

**语法**：

```js
$(selector).toggle(speed,callback);
```

可选的 `speed` 参数规定隐藏/显示的速度，可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是 `toggle() `方法完成后所执行的函数名称。

---

### ·jQuery ·效果参考手册

 如需全面查阅 `jQuery` 效果，请访问 [jQuery 效果参考手册](https://www.w3school.com.cn/jquery/jquery_ref_effects.asp)。 

---

## jQuery 效果 - 淡入淡出

---

 **通过` jQuery`，您可以实现元素的淡入淡出效果。** 

---

### 实例

`jQuery fadeIn()`

演示`jQuery fadeIn()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeIn();
            $("#div2").fadeIn("slow");
            $("#div3").fadeIn(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeIn() 方法。</p>
    <button>点击这里，使三个矩形淡入</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;display:none;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;display:none;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;display:none;background-color:blue;"></div>
</body>

</html>
```

`jQuery fadeOut()`

演示`jQuery fadeOut()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeOut();
            $("#div2").fadeOut("slow");
            $("#div3").fadeOut(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeOut() 方法。</p>
    <button>点击这里，使三个矩形淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>

</html>
```

`jQuery fadeToggle()`

演示`jQuery fadeToggle()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeToggle();
            $("#div2").fadeToggle("slow");
            $("#div3").fadeToggle(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeToggle() 方法。</p>
    <button>点击这里，使三个矩形淡入淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>
</body>

</html>
```

`jQuery fadeTo()`

演示`jQuery fadeTo()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeTo("slow", 0.15);
            $("#div2").fadeTo("slow", 0.4);
            $("#div3").fadeTo("slow", 0.7);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeTo() 方法。</p>
    <button>点击这里，使三个矩形淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>

</html>
```

---

### `jQuery Fading` 方法

通过` jQuery`，您可以实现元素的淡入淡出效果。

`jQuery` 拥有下面四种 `fade `方法：

- `fadeIn()`
- `fadeOut()`
- `fadeToggle()`
- `fadeTo()`

---

### `jQuery fadeIn() `方法

` jQuery fadeIn()` 用于淡入已隐藏的元素。 

**语法**：

```js
$(selector).fadeIn(speed,callback);
```

可选的` speed `参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback`参数是 `fading `完成后所执行的函数名称。

下面的例子演示了带有不同参数的 `fadeIn()` 方法：

**实例**：

```js
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeIn();
            $("#div2").fadeIn("slow");
            $("#div3").fadeIn(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeIn() 方法。</p>
    <button>点击这里，使三个矩形淡入</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;display:none;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;display:none;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;display:none;background-color:blue;"></div>
</body>

</html>
```

### `jQuery fadeOut() `方法

` jQuery fadeOut()` 方法用于淡出可见元素。 

**语法**：

```js
$(selector).fadeOut(speed,callback);
```

可选的` speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是 `fading` 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 `fadeOut()` 方法：

**实例**

```js
$("button").click(function(){
  $("#div1").fadeOut();
  $("#div2").fadeOut("slow");
  $("#div3").fadeOut(3000);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeOut();
            $("#div2").fadeOut("slow");
            $("#div3").fadeOut(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeOut() 方法。</p>
    <button>点击这里，使三个矩形淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>

</html>
```

---

### `jQuery fadeToggle()` 方法

`jQuery fadeToggle()` 方法可以在 `fadeIn()` 与 `fadeOut()` 方法之间进行切换。

如果元素已淡出，则 `fadeToggle()` 会向元素添加淡入效果。

如果元素已淡入，则 `fadeToggle()` 会向元素添加淡出效果。

**语法**：

```js
$(selector).fadeToggle(speed,callback);
```

可选的 `speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是 `fading` 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 `fadeToggle()` 方法：

**实例**

```js
$("button").click(function(){
  $("#div1").fadeToggle();
  $("#div2").fadeToggle("slow");
  $("#div3").fadeToggle(3000);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeToggle();
            $("#div2").fadeToggle("slow");
            $("#div3").fadeToggle(3000);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeToggle() 方法。</p>
    <button>点击这里，使三个矩形淡入淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>
</body>

</html>
```

---

### `jQuery fadeTo()` 方法

 `jQuery fadeTo()` 方法允许渐变为给定的不透明度（值介于 `0` 与 `1` 之间）。 

**语法**：

```js
$(selector).fadeTo(speed,opacity,callback);
```

必需的 `speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

`fadeTo()` 方法中必需的 `opacity` 参数将淡入淡出效果设置为给定的不透明度（值介于 `0` 与 `1` 之间）。

可选的 `callback` 参数是该函数完成后所执行的函数名称。

下面的例子演示了带有不同参数的 `fadeTo()` 方法：

**实例**

```js
$("button").click(function(){
  $("#div1").fadeTo("slow",0.15);
  $("#div2").fadeTo("slow",0.4);
  $("#div3").fadeTo("slow",0.7);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("#div1").fadeTo("slow", 0.15);
            $("#div2").fadeTo("slow", 0.4);
            $("#div3").fadeTo("slow", 0.7);
        });
    });
    </script>
</head>

<body>
    <p>演示带有不同参数的 fadeTo() 方法。</p>
    <button>点击这里，使三个矩形淡出</button>
    <br><br>
    <div id="div1" style="width:80px;height:80px;background-color:red;"></div>
    <br>
    <div id="div2" style="width:80px;height:80px;background-color:green;"></div>
    <br>
    <div id="div3" style="width:80px;height:80px;background-color:blue;"></div>
</body>

</html>
```

---

### `jQuery `效果参考手册

 如需全面查阅 `jQuery` 效果，请访问 [jQuery 效果参考手册](https://www.w3school.com.cn/jquery/jquery_ref_effects.asp)。 

---

## jQuery 效果 - 滑动

---

 **`jQuery` 滑动方法可使元素上下滑动。** 

---

### 实例

`jQuery slideDown()`

演示`jQuery slideDown()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideDown("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
        display: none;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```

`jQuery slideUp()`

演示`jQuery slideUp()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideUp("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```

`jQuery slideToggle()`

演示`jQuery slideToggle()`方法。

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideToggle("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
        display: none;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```



---

### `jQuery `滑动方法

通过 `jQuery`，您可以在元素上创建滑动效果。

`jQuery` 拥有以下滑动方法：

- `slideDown()`
- `slideUp()`
- `slideToggle()`

---

### `jQuery slideDown() `方法

 `jQuery slideDown()` 方法用于向下滑动元素。 

**语法**：

```js
$(selector).slideDown(speed,callback);
```

可选的`speed`参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是滑动完成后所执行的函数名称。

下面的例子演示了 `slideDown()` 方法：

**实例**

```js
$("#flip").click(function(){
  $("#panel").slideDown();
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideDown("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
        display: none;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```

---

### `jQuery slideUp()` 方法

 `jQuery slideUp()` 方法用于向上滑动元素。 

**语法**：

```js
$(selector).slideUp(speed,callback);
```

可选的 `speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是滑动完成后所执行的函数名称。

下面的例子演示了 `slideUp() `方法：

**实例**

```js
$("#flip").click(function(){
  $("#panel").slideUp();
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideUp("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```



---

### `jQuery slideToggle()` 方法

`jQuery slideToggle()` 方法可以在 `slideDown()` 与 `slideUp()` 方法之间进行切换。

如果元素向下滑动，则 `slideToggle()` 可向上滑动它们。

如果元素向上滑动，则 `slideToggle()` 可向下滑动它们。

```js
$(selector).slideToggle(speed,callback);
```

可选的 `speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是滑动完成后所执行的函数名称。

下面的例子演示了 `slideToggle()` 方法：

**实例**

```js
$("#flip").click(function(){
  $("#panel").slideToggle();
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $(".flip").click(function() {
            $(".panel").slideToggle("slow");
        });
    });
    </script>
    <style type="text/css">
    div.panel,
    p.flip {
        margin: 0px;
        padding: 5px;
        text-align: center;
        background: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    div.panel {
        height: 120px;
        display: none;
    }
    </style>
</head>

<body>
    <div class="panel">
        <p>W3School - 领先的 Web 技术教程站点</p>
        <p>在 W3School，你可以找到你所需要的所有网站建设教程。</p>
    </div>
    <p class="flip">请点击这里</p>
</body>

</html>
```

---

### `jQuery` 效果参考手册

 如需全面查阅 `jQuery` 效果，请访问 [jQuery 效果参考手册](https://www.w3school.com.cn/jquery/jquery_ref_effects.asp)。 

---

## jQuery 效果 - 动画

---

 **`jQuery animate()` 方法允许您创建自定义的动画。** 

---

### `jQuery` 动画 - `animate()` 方法

`jQuery animate()` 方法用于创建自定义动画。 

**语法**：

```js
$(selector).animate({params},speed,callback);
```

必需的 `params` 参数定义形成动画的 CSS 属性。

可选的 `speed` 参数规定效果的时长。它可以取以下值："`slow`"、"`fast`" 或毫秒。

可选的 `callback` 参数是动画完成后所执行的函数名称。

下面的例子演示 `animate()` 方法的简单应用；它把 `<div>` 元素移动到左边，直到 `left` 属性等于 `250` 像素为止：

**实例**

```js
$("button").click(function(){
  $("div").animate({left:'250px'});
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js">
    </script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("div").animate({ left: '250px' });
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;">
    </div>
</body>

</html>
```

**提示：**默认地，所有 `HTML` 元素都有一个静态位置，且无法移动。

如需对位置进行操作，要记得首先把元素的` CSS position` 属性设置为 `relative`、`fixed` 或 `absolute`！

---

### `jQuery animate()` - 操作多个属性

 请注意，生成动画的过程中可同时使用多个属性： 

**实例**

```js
$("button").click(function(){
  $("div").animate({
    left:'250px',
    opacity:'0.5',
    height:'150px',
    width:'150px'
  });
}); 
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js">
    </script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("div").animate({
                left: '250px',
                opacity: '0.5',
                height: '150px',
                width: '150px'
            });
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;">
    </div>
</body>

</html>
```

**提示：**可以用 `animate()` 方法来操作所有 `CSS `属性吗？

是的，几乎可以！不过，需要记住一件重要的事情：当使用 `animate()`时，必须使用 `Camel` 标记法书写所有的属性名，比如，必须使用 `paddingLeft` 而不是 `padding-left`，使用 `marginRight` 而不是 `margin-right`，等等。

同时，色彩动画并不包含在核心 `jQuery` 库中。

如果需要生成颜色动画，您需要从 `jQuery.com` 下载 `Color Animations` 插件。

---

### `jQuery animate()` - 使用相对值

 也可以定义相对值（该值相对于元素的当前值）。需要在值的前面加上 `+=` 或 `-=`： 

**实例**

```js
$("button").click(function(){
  $("div").animate({
    left:'250px',
    height:'+=150px',
    width:'+=150px'
  });
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("div").animate({
                left: '250px',
                height: '+=150px',
                width: '+=150px'
            });
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;">
    </div>
</body>

</html>
```

---

### `jQuery animate()` - 使用预定义的值

 您甚至可以把属性的动画值设置为 "`show`"、"`hide`" 或 "`toggle`"： 

**实例**

```js
$("button").click(function(){
  $("div").animate({
    height:'toggle'
  });
})
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            $("div").animate({
                height: 'toggle'
            });
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;">
    </div>
</body>

</html>
```

---

### `jQuery animate()` - 使用队列功能

默认地，`jQuery` 提供针对动画的队列功能。

这意味着如果您在彼此之后编写多个 `animate()` 调用，`jQuery` 会创建包含这些方法调用的“内部”队列。然后逐一运行这些 `animate` 调用。

**实例1**

 隐藏，如果您希望在彼此之后执行不同的动画，那么我们要利用队列功能： 

```js
$("button").click(function(){
  var div=$("div");
  div.animate({height:'300px',opacity:'0.4'},"slow");
  div.animate({width:'300px',opacity:'0.8'},"slow");
  div.animate({height:'100px',opacity:'0.4'},"slow");
  div.animate({width:'100px',opacity:'0.8'},"slow");
})
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            var div = $("div");
            div.animate({ height: '300px', opacity: '0.4' }, "slow");
            div.animate({ width: '300px', opacity: '0.8' }, "slow");
            div.animate({ height: '100px', opacity: '0.4' }, "slow");
            div.animate({ width: '100px', opacity: '0.8' }, "slow");
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;">
    </div>
</body>

</html>
```

**实例2**

 下面的例子把 `<div> `元素移动到右边，然后增加文本的字号： 

```js
$("button").click(function(){
  var div=$("div");
  div.animate({left:'100px'},"slow");
  div.animate({fontSize:'3em'},"slow");
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
    $(document).ready(function() {
        $("button").click(function() {
            var div = $("div");
            div.animate({ left: '100px' }, "slow");
            div.animate({ fontSize: '3em' }, "slow");
        });
    });
    </script>
</head>

<body>
    <button>开始动画</button>
    <p>默认情况下，所有 HTML 元素的位置都是静态的，并且无法移动。如需对位置进行操作，记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute。</p>
    <div style="background:#98bf21;height:100px;width:200px;position:absolute;">HELLO</div>
</body>

</html>
```

---

## jQuery 停止动画

---

 **`jQuery stop()` 方法用于在动画或效果完成前对它们进行停止。** 

---

**实例**

`jQuery stop()`滑动

演示`jQuery stop()`方法

```html
<!DOCTYPE html>
<html>

<head>
    <script src="/jquery/jquery-1.11.1.min.js"></script>
    <script>
        $(document).ready(function(){
  $("#flip").click(function(){
    $("#panel").slideDown(5000);
  });
  $("#stop").click(function(){
    $("#panel").stop();
  });
});
</script>
    <style type="text/css">
    #panel,
    #flip {
        padding: 5px;
        text-align: center;
        background-color: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    #panel {
        padding: 50px;
        display: none;
    }
    </style>
</head>

<body>
    <button id="stop">停止滑动</button>
    <div id="flip">点击这里，向下滑动面板</div>
    <div id="panel">Hello world!</div>
</body>

</html>
```

`jQuery stop()`动画(带有参数)

演示`jQuery stop()`方法

```html
<!DOCTYPE html>
<html>
<head>
<script src="/jquery/jquery-1.11.1.min.js">
</script>
<script> 
$(document).ready(function(){
  $("#start").click(function(){
    $("div").animate({left:'100px'},5000);
    $("div").animate({fontSize:'3em'},5000);
  });
  
  $("#stop").click(function(){
    $("div").stop();
  });

  $("#stop2").click(function(){
    $("div").stop(true);
  });

  $("#stop3").click(function(){
    $("div").stop(true,true);
  });
  
});
</script> 
</head>
<body>

<button id="start">开始</button>
<button id="stop">停止</button>
<button id="stop2">停止所有</button>
<button id="stop3">停止但要完成</button>
<p><b>"开始"</b> 按钮会启动动画。</p>
<p><b>"停止"</b> 按钮会停止当前活动的动画，但允许已排队的动画向前执行。</p>
<p><b>"停止所有"</b> 按钮停止当前活动的动画，并清空动画队列；因此元素上的所有动画都会停止。</p>
<p><b>"停止但要完成"</b> 会立即完成当前活动的动画，然后停下来。</p> 

<div style="background:#98bf21;height:100px;width:200px;position:absolute;">HELLO</div>

</body>
</html>

```

---

### `jQuery stop() `方法

`jQuery stop()` 方法用于停止动画或效果，在它们完成之前。

`stop()` 方法适用于所有 `jQuery` 效果函数，包括滑动、淡入淡出和自定义动画。

**语法**

```js
$(selector).stop(stopAll,goToEnd);
```

可选的 `stopAll` 参数规定是否应该清除动画队列。默认是 `false`，即仅停止活动的动画，允许任何排入队列的动画向后执行。

可选的 `goToEnd` 参数规定是否立即完成当前动画。默认是 `false`。

因此，默认地，`stop()` 会清除在被选元素上指定的当前动画。

下面的例子演示 `stop()` 方法，不带参数：

**实例**

```js
$("#stop").click(function(){
  $("#panel").stop();
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
        $(document).ready(function(){
  $("#flip").click(function(){
    $("#panel").slideDown(5000);
  });
  $("#stop").click(function(){
    $("#panel").stop();
  });
});
</script>
    <style type="text/css">
    #panel,
    #flip {
        padding: 5px;
        text-align: center;
        background-color: #e5eecc;
        border: solid 1px #c3c3c3;
    }

    #panel {
        padding: 50px;
        display: none;
    }
    </style>
</head>

<body>
    <button id="stop">停止滑动</button>
    <div id="flip">点击这里，向下滑动面板</div>
    <div id="panel">Hello world!</div>
</body>

</html>
```

---

### `jQuery `效果参考手册

 如需全面查阅` jQuery` 效果，请访问 [jQuery 效果参考手册](https://www.w3school.com.cn/jquery/jquery_ref_effects.asp)。 

---

## jQuery Callback 函数

---

 **`Callback` 函数在当前动画 `100%` 完成之后执行。** 

---

### `jQuery` 动画的问题

许多 `jQuery` 函数涉及动画。这些函数也许会将 *`speed`* 或 *`duration`* 作为可选参数。

例子：**`$("p").hide("slow")`**

*`speed`* 或 `*duration* `参数可以设置许多不同的值，比如 `"slow"`, `"fast"`, `"normal"` 或毫秒。

**实例**

```js
$("button").click(function(){
$("p").hide(1000);
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide(1000);
        });
    });
    </script>
</head>

<body>
    <button type="button">隐藏</button>
    <p>这是一个段落。</p>
    <p>这是另一个段落。</p>
</body>

</html>
```

由于` JavaScript` 语句（指令）是逐一执行的` -` 按照次序，动画之后的语句可能会产生错误或页面冲突，因为动画还没有完成。

为了避免这个情况，您可以以参数的形式添加` Callback` 函数。

---

### `jQuery Callback` 函数

 当动画 `100%` 完成后，即调用 `Callback` 函数。 

**典型的语法**：

```js
$(selector).hide(speed,callback)
```

 *`callback`* 参数是一个在 `hide `操作完成后被执行的函数。 

**错误(没有`callback`)**

```js
$("p").hide(1000);
alert("The paragraph is now hidden");
```

```html
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide(2000);
            alert("The paragraph is now hidden");
        });
    });
    </script>
</head>

<body>
    <button type="button">Hide</button>
    <p>This is a paragraph with little content.</p>
</body>

</html>
```

**正确(有`callback`)**

```js
$("p").hide(1000,function(){
alert("The paragraph is now hidden");
});
```

```html
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("p").hide(1000, function() {
                alert("The paragraph is now hidden");
            });
        });
    });
    </script>
</head>

<body>
    <button type="button">Hide</button>
    <p>This is a paragraph with little content.</p>
</body>

</html>
```

 **结论：**如果您希望在一个涉及动画的函数之后来执行语句，请使用` callback` 函数。 

---

## jQuery - Chaining

---

**通过 `jQuery`，您可以把动作/方法链接起来。**

**`Chaining` 允许我们在一条语句中允许多个 `jQuery` 方法（在相同的元素上）。**

---

### `jQuery` 方法链接

直到现在，我们都是一次写一条 `jQuery` 语句（一条接着另一条）。

不过，有一种名为链接（`chaining`）的技术，允许我们在相同的元素上运行多条 `jQuery` 命令，一条接着另一条。

**提示：**这样的话，浏览器就不必多次查找相同的元素。

如需链接一个动作，您只需简单地把该动作追加到之前的动作上。

**例子1**

 下面的例子把 `css()`, `slideUp()`, `and` `slideDown()` 链接在一起。`"p1"` 元素首先会变为红色，然后向上滑动，然后向下滑动： 

```js
$("#p1").css("color","red").slideUp(2000).slideDown(2000);
```

```html

```

 如果需要，我们也可以添加多个方法调用。 

 **提示：**当进行链接时，代码行会变得很差。不过，`jQuery` 在语法上不是很严格；您可以按照希望的格式来写，包含折行和缩进。 

**例子2**

 这样写也可以运行： 

```js
$("#p1").css("color","red")
  .slideUp(2000)
  .slideDown(2000);
```

 `jQuery` 会抛掉多余的空格，并按照一行长代码来执行上面的代码行。 

---

## jQuery - 获得内容和属性

---

 **`jQuery` 拥有可操作 `HTML` 元素和属性的强大方法。** 

---

### `jQuery DOM` 操作

`jQuery` 中非常重要的部分，就是操作 `DOM` 的能力。

`jQuery` 提供一系列与 `DOM` 相关的方法，这使访问和操作元素和属性变得很容易。

**提示：**`DOM` `=` `Document` `Object` `Model`（文档对象模型）

`DOM` 定义访问 `HTML` 和 `XML` 文档的标准：

“`W3C` 文档对象模型独立于平台和语言的界面，允许程序和脚本动态访问和更新文档的内容、结构以及样式。”

---

### 获得内容 - `text()`、`html()` 以及 `val()`

三个简单实用的用于 `DOM` 操作的 `jQuery` 方法：

- `text()` - 设置或返回所选元素的文本内容
- `html()` - 设置或返回所选元素的内容（包括 `HTML` 标记）
- `val()` - 设置或返回表单字段的值

下面的例子演示如何通过 `jQuery` `text()` 和 `html()` 方法来获得内容：

**实例**

```js
$("#btn1").click(function(){
  alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
  alert("HTML: " + $("#test").html());
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("#btn1").click(function() {
            alert("Text: " + $("#test").text());
        });
        $("#btn2").click(function() {
            alert("HTML: " + $("#test").html());
        });
    });
    </script>
</head>

<body>
    <p id="test">这是段落中的<b>粗体</b>文本。</p>
    <button id="btn1">显示文本</button>
    <button id="btn2">显示 HTML</button>
</body>

</html>
```

 下面的例子演示如何通过 `jQuery val()` 方法获得输入字段的值： 

**实例**

```js
$("#btn1").click(function(){
  alert("Value: " + $("#test").val());
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
        $(document).ready(function(){
  $("button").click(function(){
    alert("Value: " + $("#test").val());
  });
});
</script>
</head>

<body>
    <p>姓名：<input type="text" id="test" value="米老鼠"></p>
    <button>显示值</button>
</body>

</html>
```

---

### 获取属性 - `attr()`

`jQuery attr()` 方法用于获取属性值。

下面的例子演示如何获得链接中 `href` 属性的值：

**实例**

```js
$("button").click(function(){
  alert($("#w3s").attr("href"));
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            alert($("#w3s").attr("href"));
        });
    });
    </script>
</head>

<body>
    <p><a href="http://www.w3school.com.cn" id="w3s">W3School.com.cn</a></p>
    <button>显示 href 值</button>
</body>

</html>
```

---

### `jQuery HTML` 参考手册

如需有关 `jQuery HTML` 方法的完整内容，请访问以下参考手册：

- [jQuery 文档操作](https://www.w3school.com.cn/jquery/jquery_ref_manipulation.asp)
- [jQuery 属性操作](https://www.w3school.com.cn/jquery/jquery_ref_attributes.asp)
- [jQuery CSS 操作](https://www.w3school.com.cn/jquery/jquery_ref_css.asp)

---

## jQuery - 设置内容和属性

---

### 设置内容 - `text()`、`html()` 以及 `val()`

我们将使用前一章中的三个相同的方法来设置内容：

- `text()` - 设置或返回所选元素的文本内容
- `html()` - 设置或返回所选元素的内容（包括 `HTML` 标记）
- `val()` - 设置或返回表单字段的值

下面的例子演示如何通过 `text()`、`html()` 以及 `val()` 方法来设置内容：

**实例**

```js
$("#btn1").click(function(){
  $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
  $("#test2").html("<b>Hello world!</b>");
});
$("#btn3").click(function(){
  $("#test3").val("Dolly Duck");
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
        $(document).ready(function(){
  $("#btn1").click(function(){
    $("#test1").text("Hello world!");
  });
  $("#btn2").click(function(){
    $("#test2").html("<b>Hello world!</b>");
  });
  $("#btn3").click(function(){
    $("#test3").val("Dolly Duck");
  });
});
</script>
</head>

<body>
    <p id="test1">这是段落。</p>
    <p id="test2">这是另一个段落。</p>
    <p>Input field: <input type="text" id="test3" value="Mickey Mouse"></p>
    <button id="btn1">设置文本</button>
    <button id="btn2">设置 HTML</button>
    <button id="btn3">设置值</button>
</body>

</html>
```

---

## `text()`、`html()` 以及 `val()` 的回调函数

上面的三个 `jQuery` 方法：`text()`、`html()` 以及 `val()`，同样拥有回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 `text()` 和 `html()`：

**实例**

```js
$("#btn1").click(function(){
  $("#test1").text(function(i,origText){
    return "Old text: " + origText + " New text: Hello world!
    (index: " + i + ")";
  });
});

$("#btn2").click(function(){
  $("#test2").html(function(i,origText){
    return "Old html: " + origText + " New html: Hello <b>world!</b>
    (index: " + i + ")";
  });
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("#btn1").click(function() {
            $("#test1").text(function(i, origText) {
                return "Old text: " + origText + " New text: Hello world! (index: " + i + ")";
            });
        });

        $("#btn2").click(function() {
            $("#test2").html(function(i, origText) {
                return "Old html: " + origText + " New html: Hello <b>world!</b> (index: " + i + ")";
            });
        });

    });
    </script>
</head>

<body>
    <p id="test1">这是<b>粗体</b>文本。</p>
    <p id="test2">这是另一段<b>粗体</b>文本。</p>
    <button id="btn1">显示旧/新文本</button>
    <button id="btn2">显示旧/新 HTML</button>
</body>

</html>
```

---

### 设置属性 - `attr()`

`jQuery attr()` 方法也用于设置/改变属性值。

下面的例子演示如何改变（设置）链接中 `href` 属性的值：

**实例**

```js
$("button").click(function(){
  $("#w3s").attr("href","http://www.w3school.com.cn/jquery");
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#w3s").attr("href", "http://www.w3school.com.cn/jquery");
        });
    });
    </script>
</head>

<body>
    <p><a href="http://www.w3school.com.cn" id="w3s">W3School.com.cn</a></p>
    <button>改变 href 值</button>
    <p>请把鼠标指针移动到链接上，或者点击该链接，来查看已经改变的 href 值。</p>
</body>

</html>
```

`attr()` 方法也允许您同时设置多个属性。

下面的例子演示如何同时设置 `href` 和 `title` 属性：

**实例**

```js
$("button").click(function(){
  $("#w3s").attr({
    "href" : "http://www.w3school.com.cn/jquery",
    "title" : "W3School jQuery Tutorial"
  });
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#w3s").attr({
                "href": "http://www.w3school.com.cn/jquery/",
                "title": "W3School jQuery 教程"
            });
        });
    });
    </script>
</head>

<body>
    <p><a href="http://www.w3school.com.cn" id="w3s">W3School.com.cn</a></p>
    <button>改变 href 和 title 值</button>
    <p>请把鼠标指针移动到链接上，或者点击该链接，来查看已经改变的 href 值和已经设置的 title 值。</p>
</body>

</html>
```

---

### `attr()` 的回调函数

`jQuery` 方法 `attr()`，也提供回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 `attr()` 方法：

**实例**

```js
$("button").click(function(){
  $("#w3s").attr("href", function(i,origValue){
    return origValue + "/jquery";
  });
});
```

```html
<!DOCTYPE html>
<html>

<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.8.0.js"></script>
    <script type="text/javascript">
    $(document).ready(function() {
        $("button").click(function() {
            $("#w3s").attr("href", function(i, origValue) {
                return origValue + "/jquery/jquery_dom_set.asp";
            });
        });
    });
    </script>
</head>

<body>
    <p><a href="http://www.w3school.com.cn" id="w3s">w3school.com.cn</a></p>
    <button>改变 href 值</button>
    <p>请把鼠标指针移动到链接上，或者点击该链接，来查看已经改变的 href 值。</p>
</body>

</html>
```

---

### `jQuery HTML` 参考手册

如需有关 `jQuery HTML` 方法的完整内容，请访问以下参考手册：

- [jQuery 文档操作](https://www.w3school.com.cn/jquery/jquery_ref_manipulation.asp)
- [jQuery 属性操作](https://www.w3school.com.cn/jquery/jquery_ref_attributes.asp) 
- [jQuery CSS 操作](https://www.w3school.com.cn/jquery/jquery_ref_css.asp) 

---

