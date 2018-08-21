# DSS-代码规范
- - - -
## 初衷

写出简洁规范的代码对于开发者而言非常重要，它体现了开发者自己的专业性和技术水平，而且能够赢得别人的称赞，为秉持 DSS 在项目开发上交流，开源的核心精神，同样为了更好的维护代码库的稳定与和谐，对团队开发中的代码书写作出以下规范。
## 文件组织
- - - -
#### 文件名

>文件名应为名词或名词的混合体，且各个名词的首字母应大写，相似功能的文件名应类似，在物理存储时也应同属于一个文件夹内。

#### 文件组织内容

>一个文件超过 2000 行会变得冗长，应当尽量避免。同时每个文件起始都应有较为详尽的文件头注释来说明该文件的主要功能，创建及修改日期，参与书写的人员名单等。

## 缩进格式
- - - -
> 对于代码中的缩进大小，标准的宽度应为四个空格大小，在 DSS 内对于使用空格键还是 TAB 键实现缩进没有限制，但必须保证的是，缩进的宽度都应是一致的，这一点对于部分强缩进类型的语言尤其重要。

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

## 空白
- - - -
#### 空行

> 使用空行来将一段逻辑相关的代码与其他代码分开从而提高代码的可读性

**下面的情况应用两行空行**
* 程序文件中两部分之间
* 在两个功能不同的代码块（如方法与接口）之间
**下面是一个例子：**
```swift
func sizeHeightWithText (){
  
}


class DiaryLabel: UILabel {
  
}
```

**下面的情况应用一行空行**
* 两功能相似的代码块（如两方法）之间
* 在变量定义与第一个语句之间
* 在一个块注释或单行注释之间
* 在同一代码块中不同的逻辑操作部分之间
**下面是一个例子**
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

**下面的情况应该使用空格**
* 关键字与括号之间应该用空格分开
* 在参数列表中，逗号后应有一个空格
* 所有的二元操作符（除了“.”）都应该与操作数之间用空格分隔，但在一元操作符（“++”， “—”）与其操作符之间不需要空格
* for 语句中的表达式应该用空格分隔
**空格的使用情况应如以下例子所示**
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
- - - -
>注释分为两种：代码注释（implementation comments）与文档注释（documentation comments），不同语言各有其不同的注释语法。注释往往关系到代码的品质，注释应当简洁明了，应尽量使用较为简单常见的英文或中文短句。同时要保证注释的时效性，在修改代码时也应对响应的注释进行修改。

#### 代码注释

>代码注释用于一段代码的执行说明。
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
private String peoplenumber;		/*项目组人数*/
private String startdate;			/*项目开始的时间*/
private String enddate;				/*结束时间*/
private String createKey;			/*创建人的ID*/
private String createDate;			/*创建时间*/
```

#### 文档注释

>文档注释常用于文件最前面，有些语言对其有区别于普通注释的语法格式（JAVA），通常用来描述该文件的主要功能，并且包含项目名称，修改时间及人员名单等内容。
>下面是一个例子：
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

## 命名规范
- - - -
>命名规范可以让程序更易懂， 更易读。 并能够提供它的功能信息等， 比如它是否是一个常量， 包名， 或类等等都将有助于理解程序。在 DSS 我们采用较为常用的[帕斯卡命名法][1]（大驼峰式命名法）
>下表为一些较为常用的例子：

| 标识符类型 | 命名规则 | 例子 |
| ---- | ------ | ------ |
|  变量 | 首字母要小写， 内部的单词首字母要大写。 变量名不应该以_或$打头， 尽管它们也是合法的。变量应尽可能的短小并且意思明确。单个字符不推荐使用， 有些临时的变量可以除外，如：整型变量 i, j, k, m, n; 字符变量c,d; 例外变量e等。| `String projectKey;` |
|  常量 | 常量应该全部为大写的字符， 并且用下划线分隔 | `let NUMBER` |
|  方法 | 方法应该为动词， 且第一个字母为小写，后面的每个单词首字母大写。| `getPuserName();` |
|  包名 | 包名前缀不应该重复，并且一律小写， 一般为一些最高级别的域名如com, edu, gov, mil, net, org, 或者以两个字母缩写的国家代号， 或者一个项目的名称。 接下来的名字可以用公司的产品名， 功能块名， 组织名，机器名等等来进行命名。| `com.dss.keith.beans` |


---
## 相关文档
----
[代码风格][2]

## 相关信息
----

*2018/08/21*
*by keith*

[1]: <https://zh.wikipedia.org/wiki/%E5%B8%95%E6%96%AF%E5%8D%A1%E5%91%BD%E5%90%8D%E6%B3%95>
[2]:<https://zh.wikipedia.org/wiki/%E4%BB%A3%E7%A0%81%E9%A3%8E%E6%A0%BC>

