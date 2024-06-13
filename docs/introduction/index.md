# 引言

数据科学是一门令人兴奋的学科，它允许你将原始数据转化为理解、洞察和知识。《R for Data Science》的目标是帮助你学习R中最重要的工具，以便你能够高效、可重复地进行数据科学，并且在学习过程中享受乐趣 😃。阅读本书后，你将掌握处理各种数据科学挑战的工具，使用R中最优秀的部分。

## 你将学到什么

数据科学是一个广阔的领域，通过阅读一本书是无法掌握所有内容的。本书的目标是为你提供在最重要的工具上打下坚实基础，以及足够的知识，让你在需要时能够找到学习更多的资源。我们对典型数据科学项目步骤的模型如[图一](#fig1)所示。

<figure id="fig1">
  <img src="base.png" alt="base" />
  <figcaption>图一：在我们的数据科学流程模型中，你首先进行数据导入和整理。接下来，你通过一个反复迭代的过程来理解你的数据，包括转换、可视化和建模。最后，你将处理结果有效地传达给其他人。</figcaption>
</figure>

首先，你必须将数据**导入**到 R 中。通常，这意味着你从文件、数据库或网络应用程序编程接口（API）中获取数据，并将其加载到 R 中的数据框中。如果你无法将数据导入到 R 中，那么你就无法对其进行数据科学分析！

一旦你导入了数据，最好对其进行**整理**。整理数据意味着将数据存储在一致的形式中，使其与数据集的语义匹配。简而言之，当你的数据是整洁的时，每一列都是一个变量，每一行都是一个观察值。整洁的数据很重要，因为一致的结构让你能够将精力集中在回答关于数据的问题上，而不是为了使数据适合不同函数的正确形式而苦苦挣扎。

一旦你有了整洁的数据，常见的下一步是对其进行**转换**。转换包括缩小兴趣的观察值（比如同一个城市的所有人或去年的所有数据）、创建新变量（是现有变量的函数，比如从距离和时间计算速度）和计算一组摘要统计信息（比如计数或平均值）。整理和转换的合称为**数据处理**，因为使数据呈自然工作形式往往感觉像是一场战斗！

一旦你有了需要的变量的整洁数据，知识生成的两个主要引擎是可视化和建模。它们各有优势和劣势，所以任何真实的数据分析都会在它们之间进行多次迭代。

**可视化**是一种根本上的人类活动。一幅好的可视化图表会展示出你意想不到的事情，或者提出关于数据的新问题。一幅好的可视化图表也可能暗示你正在问错误的问题，或者你需要收集不同的数据。可视化图表可能会让你感到惊讶，但它们并不特别适合扩展，因为它们需要人类来解释。

**模型**是可视化的补充工具。一旦你的问题足够明确，你就可以使用模型来回答问题。模型基本上是数学或计算工具，因此它们通常能够很好地扩展。即使它们无法扩展，购买更多的计算机通常比购买更多的大脑要便宜！但每个模型都有假设，根据模型的本质，模型不能质疑自己的假设。这意味着模型不能从根本上让你感到惊讶。

数据科学的最后一步是**沟通**，这是任何数据分析项目中绝对关键的一部分。如果你无法将结果传达给其他人，那么你对模型和可视化图表的理解再好也没有用。

在所有这些工具周围是**编程**。编程是一种横跨工具，在数据科学项目的几乎每个部分都会使用。你不需要成为一名专业程序员才能成为一名成功的数据科学家，但学习更多关于编程的知识是值得的，因为成为一名更好的程序员可以让你更轻松地自动化常见任务和解决新问题。

你将在每个数据科学项目中使用这些工具，但对于大多数项目来说，它们是不够的。这里有一个大致的80/20规则：你可以使用本书中学到的工具解决大约80%的项目，但你需要其他工具来解决剩下的20%。在本书中，我们将指引你找到更多学习资源。

## 这本书是如何组织的

前面对数据科学工具的描述大致按照在分析中使用它们的顺序组织（尽管当然，你会多次迭代使用它们）。然而，根据我们的经验，首先学习数据导入和整理是次优的，因为 80% 的时间是例行和乏味的，而另外 20% 的时间是奇怪和令人沮丧的。这是学习一个新主题的糟糕起点！相反，我们将从已经被导入和整理的数据的可视化和转换开始。这样，当你导入和整理自己的数据时，你的动力会保持高涨，因为你知道痛苦是值得的。

在每一章中，我们尽量遵循一个一致的模式：从一些激励性的示例开始，让你能够看到更大的图景，然后深入细节。书中的每个部分都配有练习，帮助你练习所学的知识。尽管跳过练习可能很诱人，但没有比在实际问题上练习更好的学习方法了。

## 你将不会学到的内容

这本书没有涵盖几个重要的主题。我们认为，保持对基础知识的无情关注是非常重要的，这样你就可以尽快上手。这意味着这本书无法涵盖每个重要的主题。

### 建模

建模对于数据科学非常重要，但它是一个庞大的主题，不幸的是，我们在这里没有足够的空间来对它进行充分的覆盖。想要了解更多关于建模的知识，我们强烈推荐我们的同事 Max Kuhn 和 Julia Silge 编写的[《使用 R 进行整洁建模》](https://www.tmwr.org/)。这本书将教你使用 tidymodels 系列包，正如你从名称中猜到的那样，它们与本书中使用的 tidyverse 包共享许多约定。

### 大数据

这本书自豪地并且主要关注小型内存中的数据集。这是正确的起点，因为除非你有小数据的经验，否则无法处理大数据。你将在本书的大部分内容中学习的工具将轻松处理数百兆字节的数据，并且经过一些小心处理，你通常可以使用它们来处理几个千兆字节的数据。我们还将向你展示如何从数据库和 Parquet 文件中获取数据，这两者通常用于存储大数据。你不一定能够处理整个数据集，但这并不是问题，因为你只需要一个子集或子样本来回答你感兴趣的问题。

如果你经常处理较大的数据（比如 10-100 GB），我们建议你学习更多关于 [data.table](https://github.com/Rdatatable/data.table) 的知识。我们在这里不教授它，因为它使用的界面与 tidyverse 不同，并且需要你学习一些不同的约定。然而，它的速度非常快，如果你处理大数据，学习它的性能回报是值得的。

### Python、Julia 和其他语言

在这本书中，你不会学到关于 Python、Julia 或任何其他对数据科学有用的编程语言的知识。这并不是因为我们认为这些工具不好。它们不是！事实上，大多数数据科学团队都使用多种语言，通常至少包括 R 和 Python。但我们坚信，最好一次只掌握一种工具，而 R 是一个很好的起点。

## 先决条件

我们对你已经掌握的知识做了一些假设，以便从本书中获得最大的收益。你应该具备一般的数值素养，如果你已经具备一些基本的编程经验，那会很有帮助。如果你以前从未编程过，你可能会发现 Garrett 的[《Hands on Programming with R》](https://rstudio-education.github.io/hopr/)对本书是一个有价值的补充。

你需要四样东西来运行本书中的代码：R、RStudio、一个名为 tidyverse 的 R 包集合，以及一些其他的包。包是可重现的 R 代码的基本单元。它们包括可重用的函数、描述如何使用它们的文档以及示例数据。

### R

要下载 R，请访问 CRAN（全面的 R 存档网络）<https://cloud.r-project.org>。每年都会发布一个新的主要版本，每年还会发布 2-3 个次要版本。定期更新是个好主意。升级可能有点麻烦，尤其是对于需要重新安装所有包的主要版本来说，但拖延只会让情况变得更糟。我们建议在本书中使用 R 4.2.0 或更高版本。

### RStudio
RStudio 是用于 R 编程的集成开发环境，你可以从 <https://posit.co/download/rstudio-desktop/> 下载。RStudio 每年会更新几次，并且会在新版本发布时自动通知你，所以无需反复检查。定期升级以利用最新和最棒的功能是个好主意。对于本书，确保你至少有 RStudio 2022.02.0。

当你启动 RStudio 时，如[图二](#fig2) 所示，你会看到界面中的两个关键区域：控制台窗格和输出窗格。目前，你只需要知道你在控制台窗格中输入 R 代码，然后按回车键运行它。随着我们的学习，你会了解更多！

<figure id="fig2">
  <img src="console.png" alt="console" />
  <figcaption>图二：RStudio 集成开发环境有两个关键区域：在左侧的控制台窗格中键入 R 代码，在右侧的输出窗格中查找图形。</figcaption>
</figure>


### tidyverse
你还需要安装一些 R 包。R **包**是一组函数、数据和文档，它扩展了基本的 R 功能。使用包是成功使用 R 的关键。你将在本书中学习的大多数包都是所谓的 tidyverse 的一部分。tidyverse 中的所有包都共享数据和 R 编程的共同理念，并且设计成可以一起使用。

你可以使用一行代码安装完整的 tidyverse：

```R
install.packages("tidyverse")
```

在你的计算机上，在控制台中输入这行代码，然后按回车键运行。R 将从 CRAN 下载这些包并安装在你的计算机上。

在使用 `library()` 加载包之前，你将无法使用包中的函数、对象或帮助文件。安装了包后，你可以使用 `library()` 函数加载它：

```shell
library(tidyverse)
#> ── Attaching core tidyverse packages ───────────────────── tidyverse 2.0.0 ──
#> ✔ dplyr     1.1.4     ✔ readr     2.1.5
#> ✔ forcats   1.0.0     ✔ stringr   1.5.1
#> ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
#> ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
#> ✔ purrr     1.0.2     
#> ── Conflicts ─────────────────────────────────────── tidyverse_conflicts() ──
#> ✖ dplyr::filter() masks stats::filter()
#> ✖ dplyr::lag()    masks stats::lag()
#> ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
```

这告诉你 tidyverse 加载了九个包：dplyr、forcats、ggplot2、lubridate、purrr、readr、stringr、tibble 和 tidyr。这些被认为是 tidyverse 的**核心**，因为你几乎在每个分析中都会使用它们。

tidyverse 中的包经常变化。你可以通过运行 `tidyverse_update()` 来查看是否有更新可用。

### 其他包
还有许多优秀的包不属于 tidyverse，因为它们在不同的领域解决问题，或者是基于不同的一套基本原则设计的。这并不意味着它们更好或更差；它们只是不同。换句话说，与 tidyverse 的补充不是 messyverse，而是许多其他相互关联的包的宇宙。随着你用 R 处理更多的数据科学项目，你会学习到新的包和处理数据的新方法。

在本书中，我们将使用许多不属于 tidyverse 的包。例如，我们将使用以下包，因为它们为我们提供了在学习 R 过程中使用的有趣数据集：

```R
install.packages(
  c("arrow", "babynames", "curl", "duckdb", "gapminder", 
    "ggrepel", "ggridges", "ggthemes", "hexbin", "janitor", "Lahman", 
    "leaflet", "maps", "nycflights13", "openxlsx", "palmerpenguins", 
    "repurrrsive", "tidymodels", "writexl")
  )
```

我们还将使用一些其他包来进行一些示例。你现在不需要安装它们，只需记住，每当你看到类似这样的错误时：

```shell
library(ggrepel)
#> Error in library(ggrepel) : there is no package called ‘ggrepel’
```

你需要运行 `install.packages("ggrepel")` 来安装该包。

## 运行 R 代码

上一节展示了几个运行 R 代码的示例。书中的代码如下所示：

```R
1 + 2
#> [1] 3
```

如果你在本地控制台中运行相同的代码，它将如下所示：

```shell
> 1 + 2
[1] 3
```

有两个主要的区别。在你的控制台中，你在 `>` 后面输入，称为**提示符**；我们在书中不显示提示符。在书中，输出被注释为 `#>`；在你的控制台中，它会直接显示在代码之后。这两个区别意味着，如果你正在使用电子版的书，你可以轻松地将书中的代码复制到控制台中进行粘贴。

在整本书中，我们使用一套一致的惯例来引用代码：

- 函数显示为代码字体，后跟括号，如 `sum()` 或 `mean()`。
- 其他 R 对象（例如数据或函数参数）以代码字体显示，不带括号，如 `flights` 或 `x`。
- 有时，为了清楚地表明对象来自哪个包，我们会使用包名称后跟两个冒号，例如 `dplyr::mutate()` 或 `nycflights13::flights`。这也是有效的 R 代码。

## 致谢

这本书不仅仅是 Hadley、Mine 和 Garrett 的成果，也是我们与 R 社区许多人在网上和线下进行的许多对话的结果。我们非常感谢与大家进行的所有对话；非常感谢你们！

这本书是在公开的情况下编写的，许多人通过拉取请求做出了贡献。特别感谢所有 259 位通过 GitHub 拉取请求贡献改进的人（按用户名字母顺序排序）：

@a-rosenberg，Tim Becker (@a2800276)，Abinash Satapathy (@Abinashbunty)，Adam Gruer (@adam-gruer)，adi pradhan (@adidoit)，A. s. (@Adrianzo)，Aep Hidyatuloh (@aephidayatuloh)，Andrea Gilardi (@agila5)，Ajay Deonarine (@ajay-d)，@AlanFeder，Daihe Sui (@alansuidaihe)，@alberto-agudo，@AlbertRapp，@aleloi，pete (@alonzi)，Alex (@ALShum)，Andrew M. (@amacfarland)，Andrew Landgraf (@andland)，@andyhuynh92，Angela Li (@angela-li)，Antti Rask (@AnttiRask)，LOU Xun (@aquarhead)，@ariespirgel，@august-18，Michael Henry (@aviast)，Azza Ahmed (@azzaea)，Steven Moran (@bambooforest)，Brian G. Barkley (@BarkleyBG)，Mara Averick (@batpigandme)，Oluwafemi OYEDELE (@BB1464)，Brent Brewington (@bbrewington)，Bill Behrman (@behrman)，Ben Herbertson (@benherbertson)，Ben Marwick (@benmarwick)，Ben Steinberg (@bensteinberg)，Benjamin Yeh (@bentyeh)，Betul Turkoglu (@betulturkoglu)，Brandon Greenwell (@bgreenwell)，Bianca Peterson (@BinxiePeterson)，Birger Niklas (@BirgerNi)，Brett Klamer (@bklamer)，@boardtc，Christian (@c-hoh)，Caddy (@caddycarine)，Camille V Leonard (@camillevleonard)，@canovasjm，Cedric Batailler (@cedricbatailler)，Christina Wei (@christina-wei)，Christian Mongeau (@chrMongeau)，Cooper Morris (@coopermor)，Colin Gillespie (@csgillespie)，Rademeyer Vermaak (@csrvermaak)，Chloe Thierstein (@cthierst)，Chris Saunders (@ctsa)，Abhinav Singh (@curious-abhinav)，Curtis Alexander (@curtisalexander)，Christian G. Warden (@cwarden)，Charlotte Wickham (@cwickham)，Kenny Darrell (@darrkj)，David Kane (@davidkane9)，David (@davidrsch)，David Rubinger (@davidrubinger)，David Clark (@DDClark)，Derwin McGeary (@derwinmcgeary)，Daniel Gromer (@dgromer)，@Divider85，@djbirke，Danielle Navarro (@djnavarro)，Russell Shean (@DOH-RPS1303)，Zhuoer Dong (@dongzhuoer)，Devin Pastoor (@dpastoor)，@DSGeoff，Devarshi Thakkar (@dthakkar09)，Julian During (@duju211)，Dylan Cashman (@dylancashman)，Dirk Eddelbuettel (@eddelbuettel)，Edwin Thoen (@EdwinTh)，Ahmed El-Gabbas (@elgabbas)，Henry Webel (@enryH)，Ercan Karadas (@ercan7)，Eric Kitaif (@EricKit)，Eric Watt (@ericwatt)，Erik Erhardt (@erikerhardt)，Etienne B. Racine (@etiennebr)，Everett Robinson (@evjrob)，@fellennert，Flemming Miguel (@flemmingmiguel)，Floris Vanderhaeghe (@florisvdh)，@funkybluehen，@gabrivera，Garrick Aden-Buie (@gadenbuie)，Peter Ganong (@ganong123)，Gerome Meyer (@GeroVanMi)，Gleb Ebert (@gl-eb)，Josh Goldberg (@GoldbergData)，bahadir cankardes (@gridgrad)，Gustav W Delius (@gustavdelius)，Hao Chen (@hao-trivago)，Harris McGehee (@harrismcgehee)，@hendrikweisser，Hengni Cai (@hengnicai)，Iain (@Iain-S)，Ian Sealy (@iansealy)，Ian Lyttle (@ijlyttle)，Ivan Krukov (@ivan-krukov)，Jacob Kaplan (@jacobkap)，Jazz Weisman (@jazzlw)，John Blischak (@jdblischak)，John D. Storey (@jdstorey)，Gregory Jefferis (@jefferis)，Jeffrey Stevens (@JeffreyRStevens)，蒋雨蒙 (@JeldorPKU)，Jennifer (Jenny) Bryan (@jennybc)，Jen Ren (@jenren)，Jeroen Janssens (@jeroenjanssens)，@jeromecholewa，Janet Wesner (@jilmun)，Jim Hester (@jimhester)，JJ Chen (@jjchern)，Jacek Kolacz (@jkolacz)，Joanne Jang (@joannejang)，@johannes4998，John Sears (@johnsears)，@jonathanflint，Jon Calder (@jonmcalder)，Jonathan Page (@jonpage)，Jon Harmon (@jonthegeek)，JooYoung Seo (@jooyoungseo)，Justinas Petuchovas (@jpetuchovas)，Jordan (@jrdnbradford)，Jeffrey Arnold (@jrnold)，Jose Roberto Ayala Solares (@jroberayalas)，Joyce Robbins (@jtr13)，@juandering，Julia Stewart Lowndes (@jules32)，Sonja (@kaetschap)，Kara Woo (@karawoo)，Katrin Leinweber (@katrinleinweber)，Karandeep Singh (@kdpsingh)，Kevin Perese (@kevinxperese)，Kevin Ferris (@kferris10)，Kirill Sevastyanenko (@kirillseva)，Jonathan Kitt (@KittJonathan)，@koalabearski，Kirill Müller (@krlmlr)，Rafał Kucharski (@kucharsky)，Kevin Wright (@kwstat)，Noah Landesberg (@landesbergn)，Lawrence Wu (@lawwu)，@lindbrook，Luke W Johnston (@lwjohnst86)，Kara de la Marck (@MarckK)，Kunal Marwaha (@marwahaha)，Matan Hakim (@matanhakim)，Matthias Liew (@MatthiasLiew)，Matt Wittbrodt (@MattWittbrodt)，Mauro Lepore (@maurolepore)，Mark Beveridge (@mbeveridge)，@mcewenkhundi，mcsnowface，PhD (@mcsnowface)，Matt Herman (@mfherman)，Michael Boerman (@michaelboerman)，Mitsuo Shiota (@mitsuoxv)，Matthew Hendrickson (@mjhendrickson)，@MJMarshall，Misty Knight-Finley (@mkfin7)，Mohammed Hamdy (@mmhamdy)，Maxim Nazarov (@mnazarov)，Maria Paula Caldas (@mpaulacaldas)，Mustafa Ascha (@mustafaascha)，Nelson Areal (@nareal)，Nate Olson (@nate-d-olson)，Nathanael (@nateaff)，@nattalides，Ned Western (@NedJWestern)，Nick Clark (@nickclark1000)，@nickelas，Nirmal Patel (@nirmalpatel)，Nischal Shrestha (@nischalshrestha)，Nicholas Tierney (@njtierney)，Jakub Nowosad (@Nowosad)，Nick Pullen (@nstjhp)，@olivier6088，Olivier Cailloux (@oliviercailloux)，Robin Penfold (@p0bs)，Pablo E. Garcia (@pabloedug)，Paul Adamson (@padamson)，Penelope Y (@penelopeysm)，Peter Hurford (@peterhurford)，Peter Baumgartner (@petzi53)，Patrick Kennedy (@pkq)，Pooya Taherkhani (@pooyataher)，Y. Yu (@PursuitOfDataScience)，Radu Grosu (@radugrosu)，Ranae Dietzel (@Ranae)，Ralph Straumann (@rastrau)，Rayna M Harris (@raynamharris)，@ReeceGoding，Robin Gertenbach (@rgertenbach)，Jajo (@RIngyao)，Riva Quiroga (@rivaquiroga)，Richard Knight (@RJHKnight)，Richard Zijdeman (@rlzijdeman)，@robertchu03，Robin Kohrs (@RobinKohrs)，Robin (@Robinlovelace)，Emily Robinson (@robinsones)，Rob Tenorio (@robtenorio)，Rod Mazloomi (@RodAli)，Rohan Alexander (@RohanAlexander)，Romero Morais (@RomeroBarata)，Albert Y. Kim (@rudeboybert)，Saghir (@saghirb)，Hojjat Salmasian (@salmasian)，Jonas (@sauercrowd)，Vebash Naidoo (@sciencificity)，Seamus McKinsey (@seamus-mckinsey)，@seanpwilliams，Luke Smith (@seasmith)，Matthew Sedaghatfar (@sedaghatfar)，Sebastian Kraus (@sekR4)，Sam Firke (@sfirke)，Shannon Ellis (@ShanEllis)，@shoili，Christian Heinrich (@Shurakai)，S’busiso Mkhondwane (@sibusiso16)，SM Raiyyan (@sm-raiyyan)，Jakob Krigovsky (@sonicdoe)，Stephan Koenig (@stephan-koenig)，Stephen Balogun (@stephenbalogun)，Steven M. Mortimer (@StevenMMortimer)，Stéphane Guillou (@stragu)，Sulgi Kim (@sulgik)，Sergiusz Bleja (@svenski)，Tal Galili (@talgalili)，Alec Fisher (@Taurenamo)，Todd Gerarden (@tgerarden)，Tom Godfrey (@thomasggodfrey)，Tim Broderick (@timbroderick)，Tim Waterhouse (@timwaterhouse)，TJ Mahr (@tjmahr)，Thomas Klebel (@tklebel)，Tom Prior (@tomjamesprior)，Terence Teo (@tteo)，@twgardner2，Ulrik Lyngs (@ulyngs)，Shinya Uryu (@uribo)，Martin Van der Linden (@vanderlindenma)，Walter Somerville (@waltersom)，@werkstattcodes，Will Beasley (@wibeasley)，Yihui Xie (@yihui)，Yiming (Paul) Li (@yimingli)，@yingxingwu，Hiroaki Yutani (@yutannihilation)，Yu Yu Aung (@yuyu-aung)，Zach Bogart (@zachbogart)，@zeal626，Zeki Akyol (@zekiakyol)。