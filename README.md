1. [Lambda 表达式](#lambda)
2. [函数式接口](#FunctionalInterface)
3. [方法引用与构造器引用](#method)
4. [Stream API](#stream)
5. [默认方法与静态方法](#static)
6. [新时间日期API](#localdate)
7. [其他新特性](#other)

### <span id ="lambda">1. 为什么使用Lambda 表达式
Lambda 是一个匿名函数，我们可以把Lambda 表达式理解为是一段可以传递的代码（将代码像数据一样进行传递）。可以写出更简洁、更灵活的代码。作为一种更紧凑的代码风格，使Java的语言表达能力得到了提升。

![这里写图片描述](http://img.blog.csdn.net/20171130174750571?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![这里写图片描述](http://img.blog.csdn.net/20171130174921507?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### Lambda 表达式语法
Lambda 表达式在Java 语言中引入了一个新的语法元素和操作符。这个操作符为“->” ，该操作符被称为Lambda 操作符或剪头操作符。它将Lambda 分为两个部分：

- 左侧：指定了Lambda 表达式需要的所有参数
- 右侧：指定了Lambda 体，即Lambda 表达式要执行的功能。

![这里写图片描述](http://img.blog.csdn.net/20171130180202406?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![这里写图片描述](http://img.blog.csdn.net/20171130180217370?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

####类型推断
上述Lambda 表达式中的参数类型都是由编译器推断得出的。Lambda 表达式中无需指定类型，程序依然可以编译，这是因为javac根据程序的上下文，在后台推断出了参数的类型。Lambda 表达式的类型依赖于上下文环境，是由编译器推断出来的。这就是所谓的“类型推断”

###<span id="FunctionalInterface"> 2. 什么是函数式接口

- 只包含一个抽象方法的接口，称为函数式接口。

- 你可以通过Lambda 表达式来创建该接口的对象。（若Lambda 表达式抛出一个受检异常，那么该异常需要在目标接口的抽象方法上进行声明）。
- 我们可以在任意函数式接口上使用@FunctionalInterface注解，这样做可以检查它是否是一个函数式接口，同时javadoc也会包含一条声明，说明这个接口是一个函数式接口。

#### 自定义函数接口
![这里写图片描述](http://img.blog.csdn.net/20171130180850256?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### 作为参数传递Lambda 表达式

![这里写图片描述](http://img.blog.csdn.net/20171130181121373?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### Java 内置四大核心函数式接口
![这里写图片描述](http://img.blog.csdn.net/20171130181358771?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
#### 其他接口
![这里写图片描述](http://img.blog.csdn.net/20171130181425298?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcHl5Y3Nk/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
