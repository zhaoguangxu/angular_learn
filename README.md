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

### 输入验证
1. AngularJS 表单和控件可以提供验证功能，并对用户输入的非法数据进行警告。
2. 客户端的验证不能确保用户输入数据的安全，所以服务端的数据验证也是必须的。
3. HTML 表单属性 novalidate 用于禁用浏览器默认的验证。

# AngularJS API
1. API 意为 Application Programming Interface（应用程序编程接口）。

### AngularJS 全局 API
1. AngularJS 全局 API 用于执行常见任务的 JavaScript 函数集合，如：
    + 比较对象
    + 迭代对象
    + 转换对象
2. 全局 API 函数使用 angular 对象进行访问。
3. 以下列出了一些通用的 API 函数：
    + angular.lowercase() 转换字符串为小写
    + angular.uppercase() 转换字符串为大写
    + angular.isString()  判断给定的对象是否为字符串，如果是返回 true。
    + angular.isNumber()  判断给定的对象是否为数字，如果是返回 true。

### AngularJS Bootstrap
1. AngularJS 的首选样式表是 Twitter Bootstrap， Twitter Bootstrap 是目前最受欢迎的前端框架。

### Bootstrap
1. 你可以在你的 AngularJS 应用中加入 Twitter Bootstrap，你可以在你的 <head>元素中添加

# AngularJS 包含
1. 在 AngularJS 中，你可以在 HTML 中包含 HTML 文件。

### 在 HTML 中包含 HTML 文件
1. 在 HTML 中，目前还不支持包含 HTML 文件的功能。

### 服务端包含
1. 大多服务端脚本都支持包含文件功能 (SSI： Server Side Includes)。
2. 使用 SSI, 你可在 HTML 中包含 HTML 文件，并发送到客户端浏览器。

### 客户端包含
1. 通过 JavaScript 有很多种方式可以在 HTML 中包含 HTML 文件。
2. 通常我们使用 http 请求 (AJAX) 从服务端获取数据，返回的数据我们可以通过 使用 innerHTML 写入到 HTML 元素中。

### AngularJS 包含
1. 使用 AngularJS, 你可以使用 ng-include 指令来包含 HTML 内容:

### 包含 AngularJS 代码
1. ng-include 指令除了可以包含 HTML 文件外，还可以包含 AngularJS 代码:

### 跨域包含
1. 默认情况下， ng-include 指令不允许包含其他域名的文件。
2. 如果你需要包含其他域名的文件，你需要设置域名访问白名单：

# AngularJS 动画
1. AngularJS 提供了动画效果，可以配合 CSS 使用。
2. AngularJS 使用动画需要引入 angular-animate.min.js 库。
3. 还需在应用中使用模型 ngAnimate：
4. 应用中动画不宜太多，但合适的使用动画可以增加页面的丰富性，也可以更易让用户理解。
5. 如果我们应用已经设置了应用名，可以把 ngAnimate 直接添加在模型中

### ngAnimate 做了什么?
1. ngAnimate 模型可以添加或移除 class 。
2. ngAnimate 模型并不能使 HTML 元素产生动画，但是 ngAnimate 会监测事件，类似隐藏显示 HTML 元素 ，如果事件发生 ngAnimate 就会使用预定义的 class 来设置 HTML 元素的动画。
3. AngularJS 添加/移除 class 的指令:
   + ng-show
   + ng-hide
   + ng-class
   + ng-view
   + ng-include
   + ng-repeat
   + ng-if
   + ng-switch
4. ng-show 和 ng-hide 指令用于添加或移除 ng-hide class 的值。
5. 其他指令会在进入 DOM 会添加 ng-enter 类，移除 DOM 会添加 ng-leave 属性。
6. 当 HTML 元素位置改变时，ng-repeat 指令同样可以添加 ng-move 类 。
7. 此外， 在动画完成后，HTML 元素的类集合将被移除。例如： ng-hide 指令会添加一下类：
   + ng-animate
   + ng-hide-animate
   + ng-hide-add (如果元素将被隐藏)
   + ng-hide-remove (如果元素将显示)
   + ng-hide-add-active (如果元素将隐藏)
   + ng-hide-remove-active (如果元素将显示)

### 使用 CSS 动画
1. 我们可以使用 CSS transition(过渡) 或 CSS 动画让 HTML 元素产生动画效果

##### CSS 过渡
1. CSS 过渡可以让我们平滑的将一个 CSS 属性值修改为另外一个：

##### CSS 动画
1. CSS 动画允许你平滑的修改 CSS 属性值:

# AngularJS 依赖注入

### 什么是依赖注入
1. wiki 上的解释是：依赖注入（Dependency Injection，简称DI）是一种软件设计模式，在这种模式下，一个或更多的依赖（或服务）被注入（或者通过引用传递）到一个独立的对象（或客户端）中，然后成为了该客户端状态的一部分。
2. 该模式分离了客户端依赖本身行为的创建，这使得程序设计变得松耦合，并遵循了依赖反转和单一职责原则。与服务定位器模式形成直接对比的是，它允许客户端了解客户端如何使用该系统找到依赖
3. 一句话 --- 没事你不要来找我，有事我会去找你。
4. AngularJS 提供很好的依赖注入机制。以下5个核心组件用来作为依赖注入：
    + value
    + factory
    + service
    + provider
    + constant

### value
1. Value 是一个简单的 javascript 对象，用于向控制器传递值（配置阶段）：

### factory
1. factory 是一个函数用于返回值。在 service 和 controller 需要时创建。
2. 通常我们使用 factory 函数来计算或返回值。

### provider
1. AngularJS 中通过 provider 创建一个 service、factory等(配置阶段)。
2. Provider 中提供了一个 factory 方法 get()，它用于返回 value/service/factory。

### constant
1. constant(常量)用来在配置阶段传递数值，注意这个常量在配置阶段是不可用的。


# AngularJS 路由
1. AngularJS 路由允许我们通过不同的 URL 访问不同的内容。
2. 通过 AngularJS 可以实现多视图的单页Web应用（single page web application，SPA）。
3. 通常我们的URL形式为 http://runoob.com/first/page，但在单页Web应用中 AngularJS 通过 # + 标记 实现
4. 当我们点击以上的任意一个链接时，向服务端请的地址都是一样的 (http://runoob.com/)。 因为 # 号之后的内容在向服务端请求时会被浏览器忽略掉。 所以我们就需要在客户端实现 # 号后面内容的功能实现。 AngularJS 路由 就通过 # + 标记 帮助我们区分不同的逻辑页面并将不同的页面绑定到对应的控制器上。

### 实例解析：
1. 载入了实现路由的 js 文件：angular-route.js。
2. 包含了 ngRoute 模块作为主应用模块的依赖模块。
3. 使用 ngView 指令。
4. 配置 $routeProvider，AngularJS $routeProvider 用来定义路由规则。

注：AngularJS 模块的 config 函数用于配置路由规则。通过使用 configAPI，我们请求把$routeProvider注入到我们的配置函数并且使用$routeProvider.whenAPI来定义我们的路由规则。

注：$routeProvider 为我们提供了 when(path,object) & otherwise(object) 函数按顺序定义所有路由，函数包含两个参数:
    + 第一个参数是 URL 或者 URL 正则规则。
    + 第二个参数是路由配置对象。



### 路由设置对象
1. AngularJS 路由也可以通过不同的模板来实现。
2. $routeProvider.when 函数的第一个参数是 URL 或者 URL 正则规则，第二个参数为路由配置对象。
3. 路由配置对象语法规则如下：
$routeProvider.when(url, {
    template: string,
    templateUrl: string,
    controller: string, function 或 array,
    controllerAs: string,
    redirectTo: string, function,
    resolve: object<key, function>
});

4. 参数说明：
    + template: 如果我们只需要在 ng-view 中插入简单的 HTML 内容，则使用该参数
    + templateUrl: 如果我们只需要在 ng-view 中插入 HTML 模板文件，则使用该参数
    + controller：function、string或数组类型，在当前模板上执行的controller函数，生成新的scope。
    + controllerAs: string类型，为controller指定别名。
    + redirectTo: 重定向的地址。
    + resolve: 指定当前controller所依赖的其他模块。