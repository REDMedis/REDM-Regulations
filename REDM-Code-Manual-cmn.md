# RED Medis 代码规范

## 初衷

写出简洁规范的代码对于开发者而言非常重要，它体现了开发者自己的专业性和技术水平，能够赢得别人的称赞，为秉持 RED Medis 在项目开发上注重交流，开源的核心精神，同样为了更好的维护代码库的稳定与和谐，对团队开发中的代码书写作出以下规范。本文档并非指出其他方式是错误的，也不暗示这些规则比其他方式更好。
## 文件
### 文件命名
文件名应为名词或名词的混合体，且各个名词的首字母应大写，相似功能的文件名应类似，在存储时也应同属于一个文件夹内。

### 文件组织内容
为避免文件冗杂，一个文件一般情况下不应容纳多于 2000 行代码。
每个文件起始都应有较为详尽的文件头注释来说明该文件的主要功能，创建及修改日期，参与书写的人员名单等。

## 表达式和基本语句
### 一般表达式
- 如果代码行中的运算符比较多，用括号确定表达式的操作顺序，避免使用默认的优先级。
- 避免组合表达式
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `Total =（aSum = bSum + cSum）+ i;`
> 
### if 语句
- 不可将布尔变量直接与 TRUE、FALSE、1 和 0 进行比较
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `if(seleted == TRUE)`

> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `if(seleted == 0)`

> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> `if(seleted)`

> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> `if(!seleted)`

### 循环语句
- 嵌套循环时，尽量将最长的循环放在最内层，最短的循环放在最外层以减少CPU跨切循环层的次数。
- 循环控制变量的取值采用“半开半闭”写法。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `for(int i = 0; i <= n -1; i-- )`

> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> `for(int i = 0; i < n; i-- )`

## 排版
### 缩进
为保证在所有编辑器下的效果一致，我们统一**使用空格**来控制缩进，而非 Tab 字符。行首使用 4 个空格，若使用 Tab 缩进，需要设置一个 Tab 为 4 个空格。

#### 行宽

每行避免超过 80 个字符，避免由于终端和编辑工具产生的误处理，也保证了代码的观感。
 
#### 换行

当一个表达语句不适合书写在一行的时候（如参数过长），应该用以下的原则进行分行：
* 在逗号之后
* 在一个操作符之前
* 在优先度高的地方
* 新行的开始应该与上一行同一级别的地方对齐
* 如果满足以上的原则的新行的开始比较靠右，应该用 8 个空格进行缩进。

下面是一个例子：
```swift
monthLabel = DiaryLabel(
                        fontname: "Wyue-GutiFangsong-NC",
                        labelText: "三月",
                        fontSize: 16.0,
                        lineHeight: 5.0,
                        color: DiaryRed)
```

### 大括号
缩进风格的主要区别在于复合语句的大括号的位置，这通常是为涵盖一个控制声明（if、while、for...），大括号摆放位置的风格种类有许多，这里不作硬性要求，但在非空代码块中推荐使用 K&R 风格。
下面是 K&R 风格的一个例子：
```C
while (x == y) {
    something();
    somethingelse();
}
```
### 空白
#### 空行

使用空行来将一段逻辑相关的代码与其他代码分开从而提高代码的可读性。

下面的情况应用两行空行：
* 程序文件中两部分之间
* 在两个功能不同的代码块（如方法与接口）之间

下面是一个例子：
```swift
func sizeHeightWithText (){
  
}


class DiaryLabel: UILabel {
  
}
```

下面的情况应用一行空行：
* 两功能相似的代码块（如两方法）之间
* 在变量定义与第一个语句之间
* 在一个块注释或单行注释之间
* 在同一代码块中不同的逻辑操作部分之间

下面是一个例子：
```swift
var diary: Diary!
var webview: UIWebView!
var saveButton: UIButton!
var deleteButton: UIButton!
var editButton: UIButton!
var buttonView: UIView!
    
override func viewDidLoad() {
    super.viewDidLoad()
    setupUI()
}
```

#### 空格

下面的情况应该使用空格：
* 保留字与括号之间应该用空格分开
* 在参数列表中，逗号后应有一个空格
* 所有的二元操作符（除了“.”）都应该与操作数之间用空格分隔，但在一元操作符（“++”， “—”）与其操作符之间不需要空格
* for 语句中的三个表达式应该用空格分隔

下面情况则相反：
* 左小括号和字符之间不出现空格；同样,右小括号和字符之间也不出现空格。

下面是一个例子：
```swift
let mainHTML = Bundle.main.url(forResource: "DiaryTemplate", withExtension: "html")
var contents: NSString = ""

do {
    contents = try NSString(contentsOfFile: mainHTML!.path, encoding: String.Encoding.utf8.rawValue)
} 
catch let error as NSError{
    print(error)
}
```

## 注释
代码是供人阅读的，注释是编辑者之间传递思路的重要途径。注释分为两种：代码注释（Implementation Comments）与文档注释（Documentation Comments），不同语言各有其不同的注释语法。注释往往关系到代码的品质，注释应当简洁明了，应尽量使用较为简单常见的英文或中文短句。同时要保证注释的时效性，在修改代码时也应对响应的注释进行修改。

### 代码注释

代码注释用于一段代码的执行说明。
常有以下三种形式：

**块（block）**
	常用于文件，方法，数据结构以及算法等方面的描述，块注释应在每个文件的开头或每个代码块前面，也可以用在代码块内，但一定要与代码的缩进保持一致，块注释也应与前面代码有一行空行。

**单行（single-line）**
	短的说明可以用一行注释并且要与代码缩排一致对齐，并且前面一般要有一行空行。
  
**行尾（end-of-line）, （trailing）**
	很短的注释可以跟代码在同一行上，但必须跟代码有足够的距离， 如果在一块代码中有许多这样的注释， 它们必须用tab键设置来进行缩排对齐。如下例：
```java
private String projectKey;			/*项目编号*/
private String projectname;			/*项目名称*/
private String peoplenumber;			/*项目组人数*/
private String startdate;			/*项目开始的时间*/
private String enddate;				/*结束时间*/
private String createKey;			/*创建人的ID*/
private String createDate;			/*创建时间*/
```

### 文档注释

文档注释常用于文件最前面，有些语言对其有区别于普通注释的语法格式（Java），通常用来描述该文件的主要功能，并且包含项目名称，修改时间及人员名单等内容。

下面是一个例子：
```java
/**
 * @Title：${enclosing_method}
 * @Description: [功能描述]
 * @Param: ${tags}
 * @Return: ${return_type}
 * @author <a href="mail to: *******@******.com" rel="nofollow">作者</a>
 * @CreateDate: ${date} ${time}</p> 
 * @update: [序号][日期YYYY-MM-DD] [更改人姓名][变更描述]     
 */
```

## 内部命名

规范的命名可以让程序更易懂，更易读。并能够提供它的功能信息等，比如它是否是一个常量，包名，或类等等都将有助于理解程序。
下表为一些较为常用的例子：

| 标识符类型 | 命名规则 | 例子 |
| ---- | ------ | ------ |
|  变量 | 采用 [LowerCamelCase][1]（小驼峰命名法）| `String projectKey;` |
|  常量 | 全部为大写的字符，并且用下划线分隔 | `let NUMBER` |
|  方法 | 采用 [LowerCamelCase][1]| `getPuserName();` |
---
另外，请注意以下规则：
- 不推荐使用令人费解的单个字符作为变量名称，一些临时的变量可以除外。
- 杜绝完全不规范的缩写,避免望文不知义。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `AbsClass` （AbstractClass）
- 严禁使用拼音与英文混合的方式，更不允许直接使用中文的方式来命名。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> `getPingJunFenByName()` 

> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> `getAverangeByName()`

- 变量名不应该以下划线`_`或美元符号`$`打头（尽管它们是合法的）。
- 具体语言的命名依照习惯即可，如在 Java 语言的类命名时，推荐使用 [UpperCamelCase][3]（帕斯卡命名法）
>
## 参考文献

1. [代码风格][2]
2. [阿里巴巴Java开发手册v1.2.0.pdf][4]（Download Link）
3. [PROGRAM LAYOUT - THE ART OF MAKING PROGRAMS READABLE][5]

## 相关信息
- 执笔：高建、王雨阳
- 审核：梁正弘
- 最后修改于：2018 年 8 月 20 日
- 即日生效

[1]: https://zh.wikipedia.org/wiki/%E5%B8%95%E6%96%AF%E5%8D%A1%E5%91%BD%E5%90%8D%E6%B3%95
[2]:
https://zh.wikipedia.org/wiki/%E4%BB%A3%E7%A0%81%E9%A3%8E%E6%A0%BC
[3]:
https://zh.wikipedia.org/wiki/%E5%B8%95%E6%96%AF%E5%8D%A1%E5%91%BD%E5%90%8D%E6%B3%95
[4]:
http://techforum-img.cn-hangzhou.oss-pub.aliyun-inc.com/阿里巴巴Java开发手册v1.2.0.pdf
[5]:
http://www.ibiblio.org/pub/languages/fortran/ch1-6.html
