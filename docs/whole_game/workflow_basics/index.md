# 工作流程：基础知识

你现在已经有了运行 R 代码的一些经验了。我们没有给你太多细节，但显然你已经掌握了基础知识，否则你就会因为沮丧而扔掉这本书！当你开始在 R 中编程时会感到沮丧是自然的，因为它对标点符号要求非常严格，即使一个字符放错位置也会导致它抱怨。但是虽然你应该期望会有一点点沮丧，但请放心，这种经历是典型且暂时的：每个人都会遇到这种情况，而克服它的唯一方法就是继续努力尝试。

在我们进一步深入之前，让我们确保你对运行 R 代码有了扎实的基础，并且你了解了一些最有用的 RStudio 功能。

## 编码基础

让我们回顾一些我们为了尽快让你开始绘图而省略的基础知识。你可以使用 R 进行基本的数学计算：

```R
1 / 200 * 30
#> [1] 0.15
(59 + 73 + 2) / 3
#> [1] 44.66667
sin(pi / 2)
#> [1] 1
```

你可以使用赋值运算符 <- 创建新对象：

```R
x <- 3 * 4
```

请注意，x 的值不会被打印出来，它只是被存储了起来。如果你想查看该值，请在控制台中输入 x。

你可以使用 c() 将多个元素组合成一个向量：

```R
primes <- c(2, 3, 5, 7, 11, 13)
```

并且对向量进行的基本算术运算会应用到向量的每个元素上：

```R
primes * 2
#> [1]  4  6 10 14 22 26
primes - 1
#> [1]  1  2  4  6 10 12
```

所有创建对象的 R 语句，即**赋值**语句，都具有相同的形式：

```R
对象名 <- 值
```

在阅读该代码时，在脑海中说 “对象名获得值”。

你将会进行大量的赋值操作，而 <- 的输入很痛苦。你可以使用 RStudio 的键盘快捷键节省时间：Alt + -（减号）。请注意，RStudio 会自动在 <- 周围加上空格，这是一种良好的代码格式化习惯。在好天气时，代码可能很难阅读，所以请给你的眼睛一个休息，并使用空格。

## 注释

R 会忽略在一行中 # 后面的任何文本。这使你可以编写**注释**，这些注释对 R 来说是被忽略的，但对其他人来说是可读的。我们有时会在示例中包含注释，以解释代码的执行过程。

注释对于简要描述以下代码的功能非常有帮助。

```R
# 创建质数向量
primes <- c(2, 3, 5, 7, 11, 13)

# 将质数乘以 2
primes * 2
#> [1]  4  6 10 14 22 26
```

像这样的短代码片段，可能不需要为每一行代码都添加注释。但随着你编写的代码变得更加复杂，注释可以节省你（和你的协作者）大量的时间，以弄清楚代码中做了什么。

使用注释来解释代码的原因，而不是代码的如何或什么。代码的何和如总是可以通过仔细阅读来弄清楚，即使可能会有些乏味。如果你在注释中描述了每一步，然后更改了代码，那么你将不得不记住在更新代码时同时更新注释，否则当你将来返回代码时会感到困惑。

弄清楚*为什么*要做某事要困难得多，甚至是不可能的。例如，geom_smooth() 有一个称为 span 的参数，它控制曲线的平滑程度，较大的值会产生较平滑的曲线。假设你决定将 span 的值从默认值 0.75 更改为 0.9：对于将来的读者来说，理解正在发生的事情很容易，但除非你在注释中记录你的思考，否则没有人会理解你*为什么*更改了默认值。

对于数据分析代码，使用注释来解释你的总体攻击计划，并记录遇到的重要见解。无法从代码本身重新捕获这些知识。

## 名字中的含义

对象名称必须以字母开头，只能包含字母、数字、_ 和 .. 你希望对象名称具有描述性，因此你需要采用一种多个单词的约定。我们建议使用**蛇形命名法**，其中使用 _ 分隔小写单词。

```plain
i_use_snake_case
otherPeopleUseCamelCase
some.people.use.periods
And_aFew.People_RENOUNCEconvention
```

我们将在第 4 章再次讨论命名。

你可以通过键入其名称来检查对象：

```R
x
#> [1] 12
```

再做一次赋值：

```R
this_is_a_really_long_name <- 2.5
```

要查看此对象，请尝试使用 RStudio 的自动补全功能：键入 “this”，按 TAB 键，添加字符，直到你拥有唯一的前缀，然后按回车键。

假设你犯了一个错误，this_is_a_really_long_name 的值应该是 3.5，而不是 2.5。你可以使用另一个键盘快捷键来帮助你进行修复。例如，你可以按 ↑ 键来查看你输入的最后一个命令并编辑它。或者，键入 “this” 然后按 Cmd/Ctrl + ↑ 来列出所有以这些字母开头的命令。使用箭头键进行导航，然后按回车键重新输入命令。将 2.5 更改为 3.5，然后重新运行。

再做一次赋值：

```R
r_rocks <- 2^3
```

让我们尝试来查看它：

```R
r_rock
#> Error: object 'r_rock' not found
R_rocks
#> Error: object 'R_rocks' not found
```

这说明了你和 R 之间的默契：R 将为你处理繁琐的计算，但作为交换条件，你必须在指令中完全准确。如果不是，你很可能会收到一个错误，说找不到你要查找的对象。拼写错误很重要；R 无法读取你的想法并说：“哦，他们可能是想输入 r_rock 时不小心输入了 r_rocks”。大小写也很重要；同样地，R 无法读取你的想法并说：“哦，他们可能是想输入 R_rocks 时不小心输入了 r_rocks”。

## 调用函数

R 拥有大量内置函数，调用方式如下：

```R
function_name(argument1 = value1, argument2 = value2, ...)
```

让我们尝试使用 seq() 函数，它可以生成一系列连续的数字，并在此过程中学习 RStudio 的更多有用功能。输入 se 并按下 TAB 键。会弹出一个窗口显示可能的补全选项。通过输入更多字符（例如 q）来指定 seq() 函数，或者使用 ↑/↓ 键选择。注意弹出的悬浮工具提示，提醒你函数的参数和用途。如果需要更多帮助，按下 F1 键可以在右下角的帮助选项卡中获取所有详细信息。

当你选择好要使用的函数后，再次按下 TAB 键。RStudio 会为你添加匹配的左（()）和右（()）括号。然后，输入第一个参数的名称 from，并将其设置为 1。然后，输入第二个参数的名称 to，并将其设置为 10。最后，按下回车键。

```R
seq(from = 1, to = 10)
#>  [1]  1  2  3  4  5  6  7  8  9 10
```

通常我们会在函数调用中省略前几个参数的名称，所以上面的代码可以简写如下：

```R
seq(1, 10)
#>  [1]  1  2  3  4  5  6  7  8  9 10
```

输入以下代码并注意 RStudio 在配对引号方面提供了类似的帮助：

```R
x <- "hello world"
```

引号和括号必须始终成对出现。RStudio 尽力帮助你，但仍然有可能出错导致配对不匹配。如果出现这种情况，R 会显示续行字符“+”：

```R
> x <- "hello
+
```

+ 符号告诉你 R 正在等待更多输入；它认为你还没有完成。通常情况下，这意味着你可能忘记了一个 " 或一个 \)。你可以添加缺失的配对，或者按下 ESCAPE 键中止表达式，然后重新尝试。

请注意，右上角的环境选项卡显示了你创建的所有对象：

<figure id="fig1">
  <img src="rstudio-env.png" alt="rstudio-env.png" />
</figure>

## 练习

为什么这段代码不能运行？

```R
my_variable <- 10
my_varıable
#> Error in eval(expr, envir, enclos): object 'my_varıable' not found
```

仔细看！（这可能看起来毫无意义，但训练你的大脑注意到甚至最微小的差异，将在编程时产生回报。）

调整以下每个 R 命令，使其能够正确运行：

```R
library(tidyverse)

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy)) +
  geom_smooth(method = "lm")
```

按下 Option + Shift + K / Alt + Shift + K。会发生什么？如何通过菜单达到相同的位置？

让我们重新看一下第 1.6 节的一个练习。运行以下代码行。哪一个图保存为 mpg-plot.png？为什么？

```R
my_bar_plot <- ggplot(mpg, aes(x = class)) +
  geom_bar()
my_scatter_plot <- ggplot(mpg, aes(x = cty, y = hwy)) +
  geom_point()
ggsave(filename = "mpg-plot.png", plot = my_bar_plot)
```

## 总结

现在你已经了解了一些关于 R 代码如何工作的知识，并学会了一些在将来重返代码时帮助你理解代码的技巧。在下一章中，我们将继续你的数据科学之旅，教你关于 dplyr 的知识，这是 tidyverse 包中帮助你转换数据的工具，无论是选择重要变量、筛选感兴趣的行，还是计算汇总统计信息。