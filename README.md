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
