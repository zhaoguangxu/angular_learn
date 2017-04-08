# angular_learn
学习angular
---------------------

# AngularJS 表达式
1. 写在双大括号内：{{ expression }}。
2. 表达式把数据绑定到 HTML，这与 ng-bind 类似。

# AngularJS 应用
1. AngularJS 模块（Module） 定义了 AngularJS 应用。
2. AngularJS 控制器（Controller） 用于控制 AngularJS 应用。
3. ng-app指令定义了应用, ng-controller 定义了控制器。

# AngularJS 表达式
1. 类似于 JavaScript 表达式，AngularJS 表达式可以包含字母，操作符，变量。
2. 与 JavaScript 表达式不同，AngularJS 表达式可以写在 HTML 中。
3. 与 JavaScript 表达式不同，AngularJS 表达式不支持条件判断，循环及异常。
4. 与 JavaScript 表达式不同，AngularJS 表达式支持过滤器。

# AngularJS 指令：以ng作为前缀的HTML属性
1. ng-init 指令初始化 AngularJS 应用程序变量。
2. data-开头 AngularJS 属性以 ng- 开头，但是您可以使用 data-ng- 来让网页对 HTML5 有效。
3. AngularJS 通过被称为 指令 的新属性来扩展 HTML。
4. AngularJS 通过内置的指令来为应用添加功能。
5. AngularJS 允许你自定义指令。
6. AngularJS 指令是扩展的 HTML 属性，带有前缀 ng-。
7. ng-app 指令初始化一个 AngularJS 应用程序。
8. ng-init 指令初始化应用程序数据。
9. ng-model 指令把元素值（比如输入域的值）绑定到应用程序。

# ng-app 指令
1. ng-app 指令定义了 AngularJS 应用程序的 根元素。
2. ng-app 指令在网页加载完毕时会自动引导（自动初始化）应用程序。

# ng-init 指令
1. ng-init 指令为 AngularJS 应用程序定义了 初始值。
2. 常情况下，不使用 ng-init。您将使用一个控制器或模块来代替它。



# ng-repeat 指令
1. ng-repeat 指令对于集合中（数组中）的每个项会 克隆一次 HTML 元素。

# 创建自定义的指令
1. 使用 .directive 函数来添加自定义的指令。
2. 要调用自定义指令，HTML 元素上需要添加自定义指令名。
3. 使用驼峰法来命名一个指令， runoobDirective, 但在使用它时需要以 - 分割, runoob-directive
4. 可以通过元素名，属性，类名，注释来调用指令。

### 限制使用
1. 你可以限制你的指令只能通过特定的方式来调用。
2. 通过添加 restrict 属性,并设置只值为 "A", 来设置指令只能通过属性的方式来调用:
3. restrict 值可以是以下几种:
    + E 作为元素名使用
    + A 作为属性使用
    + C 作为类名使用
    + M 作为注释使用
4. restrict 默认值为 EA, 即可以通过元素名和属性名来调用指令。


# ng-model 指令
1. ng-model 指令 绑定 HTML 元素 到应用程序数据。
2. ng-model 指令也可以：
    + 为应用程序数据提供类型验证（number、email、required）。
    + 为应用程序数据提供状态（invalid、dirty、touched、error）。
    + 为 HTML 元素提供 CSS 类:ng-empty,ng-not-empty,ng-touched,ng-untouched,ng-valid,ng-invalid,ng-dirty,ng-pending,ng-pristine
    + 绑定 HTML 元素到 HTML 表单。



# Scope(作用域)
1. Scope(作用域) 是应用在 HTML (视图) 和 JavaScript (控制器)之间的纽带。
2. Scope 是一个对象，有可用的方法和属性。
3. Scope 可应用在视图和控制器上。

### 如何使用 Scope
1. 当你在 AngularJS 创建控制器时，你可以将 $scope 对象当作一个参数传递:
   + 当在控制器中添加 $scope 对象时，视图 (HTML) 可以获取了这些属性。
   + 视图中，你不需要添加 $scope 前缀, 只需要添加属性名即可，如： {{carname}}。

### Scope 概述
1. AngularJS 应用组成如下：
    + View(视图), 即 HTML。
    + Model(模型), 当前视图中可用的数据。
    + Controller(控制器), 即 JavaScript 函数，可以添加或修改属性。
2. scope 是模型。
3. scope 是一个 JavaScript 对象，带有属性和方法，这些属性和方法可以在视图和控制器中使用。

### Scope 作用范围

### 根作用域
1. 所有的应用都有一个 $rootScope，它可以作用在 ng-app 指令包含的所有 HTML 元素中。
2. $rootScope 可作用于整个应用中。
3. 创建控制器时，将 $rootScope 作为参数传递，可在应用中使用：


# AngularJS 控制器
1. AngularJS 控制器 控制 AngularJS 应用程序的数据。
2. AngularJS 控制器是常规的 JavaScript 对象。

### AngularJS 控制器
1. AngularJS 应用程序被控制器控制。
2. ng-controller 指令定义了应用程序控制器。
3. 控制器是 JavaScript 对象，由标准的 JavaScript 对象的构造函数 创建。
4. 应用解析：
   + AngularJS 应用程序由 ng-app 定义。应用程序在 <div> 内运行。
   + ng-controller="myCtrl" 属性是一个 AngularJS 指令。用于定义一个控制器。
   + myCtrl 函数是一个 JavaScript 函数。
   + AngularJS 使用$scope 对象来调用控制器。
   + 在 AngularJS 中， $scope 是一个应用对象(属于应用变量和函数)。
   + 控制器的 $scope （相当于作用域、控制范围）用来保存AngularJS Model(模型)的对象。
   + ng-model 指令绑定输入域到控制器的属性

### 控制器方法
1. 控制器也可以有方法（变量和函数）

### 外部文件中的控制器
1. 在大型的应用程序中，通常是把控制器存储在外部文件中。


# AngularJS 过滤器
1. 过滤器可以使用一个管道字符（|）添加到表达式和指令中。

### AngularJS 过滤器
1. AngularJS 过滤器可用于转换数据：
    + currency:格式化数字为货币格式。
    + filter:从数组项中选择一个子集。
    + lowercase:格式化字符串为小写。
    + orderBy:根据某个表达式排列数组。
    + uppercase:格式化字符串为大写。

### 表达式中添加过滤器
1. 过滤器可以通过一个管道字符（|）和一个过滤器添加到表达式中。

### currency 过滤器
1. currency 过滤器将数字格式化为货币格式：

### 向指令添加过滤器
1. 过滤器可以通过一个管道字符（|）和一个过滤器添加到指令中。

### 过滤输入
1. 输入过滤器可以通过一个管道字符（|）和一个过滤器添加到指令中，该过滤器后跟一个冒号和一个模型名称。

### 自定义过滤器

# AngularJS 服务(Service)
1. AngularJS 中你可以创建自己的服务，或使用内建服务。

### 什么是服务？
1. 在 AngularJS 中，服务是一个函数或对象，可在你的 AngularJS 应用中使用。
2. AngularJS 内建了30 多个服务。
3. 有个 $location 服务，它可以返回当前页面的 URL 地址。
4. 注意 $location 服务是作为一个参数传递到 controller 中。如果要使用它，需要在 controller 中定义。

### 为什么使用服务?
1. AngularJS 会一直监控应用，处理事件变化， AngularJS 使用 $location 服务比使用 window.location 对象更好。

### $http 服务
1. $http 是 AngularJS 应用中最常用的服务。 服务向服务器发送请求，应用响应服务器传送过来的数据。

### $timeout 服务
1. AngularJS $timeout 服务对应了 JS window.setTimeout 函数。

### $interval 服务
1. AngularJS $interval 服务对应了 JS window.setInterval 函数。

### 创建自定义服务
1. 你可以创建访问自定义服务，链接到你的模块中：
2. 当你创建了自定义服务，并连接到你的应用上后，你可以在控制器，指令，过滤器或其他服务中使用它。

### 过滤器中，使用自定义服务
1. 当你创建了自定义服务，并连接到你的应用上后，你可以在控制器，指令，过滤器或其他服务中使用它。

### Angular的很多服务，在DOM中有对应的对象，那为什么不使用这些对象，而是要用服务呢？
1. 因为这些服务可以获取到Angular应用声明周期的每一个阶段，并且和$watch整合，让Angular可以监控应用，处理事件变化。普通的DOM对象则不能在Angular应用声明周期中和应用整合。


# AngularJS XMLHttpRequest
1. $http 是 AngularJS 中的一个核心服务，用于读取远程服务器的数据。
2. 简写方法:
    + $http.get
    + $http.head
    + $http.post
    + $http.put
    + $http.delete
    + $http.jsonp
    + $http.patch

### AngularJS $http
1. AngularJS $http 是一个用于读取web服务器上数据的服务。
2. $http.get(url) 是用于读取服务器数据的函数。

# AngularJS Select(选择框)
1. AngularJS 可以使用数组或对象创建一个下拉列表选项。

### 使用 ng-options 创建选择框
1. 在 AngularJS 中我们可以使用 ng-option 指令来创建一个下拉列表，列表项通过对象和数组循环输出.
2. ng-init 设置默认选中值。

### ng-options 与 ng-repeat
1. ng-repeat 指令是通过数组来循环 HTML 代码来创建下拉列表，但 ng-options 指令更适合创建下拉列表，它有以下优势：
使用 ng-options 的选项的一个对象， ng-repeat 是一个字符串。

# AngularJS 表格
1. ng-repeat 指令可以完美的显示表格。

### 显示序号 ($index)
1. 表格显示序号可以在 <td> 中添加 $index:

### 使用 $even 和 $odd

# AngularJS SQL
1. 在前面章节中的代码也可以用于读取数据库中的数据。
### 服务端代码
1. 以下列出了几种服务端代码类型：
    + 使用 PHP 和 MySQL。返回 JSON。
    + 使用 PHP 和 MS Access。返回 JSON。
    + 使用 ASP.NET, VB, 及 MS Access。 返回 JSON。
    + 使用 ASP.NET, Razor, 及 SQL Lite。 返回 JSON。

### 跨域 HTTP 请求
1. 如果你需要从不同的服务器（不同域名）上获取数据就需要使用跨域 HTTP 请求。
2. 跨域请求在网页上非常常见。很多网页从不同服务器上载入 CSS, 图片，Js脚本等。


# AngularJS HTML DOM
1. AngularJS 为 HTML DOM 元素的属性提供了绑定应用数据的指令。

### ng-disabled 指令
1. ng-disabled 指令直接绑定应用程序数据到 HTML 的 disabled 属性。

### ng-show 指令
1. ng-show 指令隐藏或显示一个 HTML 元素。

### ng-hide 指令
1. g-hide 指令用于隐藏或显示 HTML 元素。

# AngularJS 事件
1. AngularJS 有自己的 HTML 事件指令。

### ng-click 指令
1. ng-click 指令定义了 AngularJS 点击事件。

### 隐藏 HTML 元素
1. ng-hide 指令用于设置应用部分是否可见。

### 显示 HTML 元素
1. ng-show 指令可用于设置应用中的一部分是否可见


# AngularJS 模块
1. 模块定义了一个应用程序。
2. 模块是应用程序中不同部分的容器。
3. 模块是应用控制器的容器。
4. 控制器通常属于一个模块。


# AngularJS 表单
1. AngularJS 表单是输入控件的集合。

### HTML 控件
1. 以下 HTML input 元素被称为 HTML 控件:
   + input 元素
   + select 元素
   + button 元素
   + textarea 元素

### HTML 表单
1. HTML 表单通常与 HTML 控件同时存在。 


# AngularJS 输入验证
1. AngularJS 表单和控件可以验证输入的数据。