# DSS-写作规范

## 初衷
每个人都有着不同的书写和排版习惯，为使所有文档的风格一致，增强文可读性，我们对于文档写作制定了一些规范化要求。这些规则并非都是绝对的，也不暗示这些规则比其他方式更好，他们都将在一定的弹性下被使用。

> 规章制度，本质上，并非永恒不变的定律。它们仅针对一般案例，必须在某程度的弹性下应用。  
> ——《芝加哥格式手册》（The Chicago Manual of Style，CMS）

{{Cquote|直接引用的文段一……
直接引用的文段二……
直接引用的文段三……}}

## 一般
### Markdown
DSS 的所有文档都使用 **Markdown** 撰写

### i18n
开源与分享是我们的初衷，为便利更多人的阅读、理解，我们所有的文档都将实现  [i18n](https://zh.wikipedia.org/wiki/%E5%9B%BD%E9%99%85%E5%8C%96%E4%B8%8E%E6%9C%AC%E5%9C%B0%E5%8C%96)（Internationalization）。我们将撰写简体中文的文档并提供对应的英文翻译版本，同时注意以下规则：
- 统一使用[现代标准汉语（简体字写法）](https://zh.wikipedia.org/wiki/%E7%8F%BE%E4%BB%A3%E6%A8%99%E6%BA%96%E6%BC%A2%E8%AA%9E)([ISO 639-3](https://en.wikipedia.org/wiki/ISO_639-3) `cmn-Hans`) 以确保准确性。
- 统一使用[英语](https://zh.wikipedia.org/wiki/%E8%8B%B1%E8%AF%AD) （[ISO 639-3](https://en.wikipedia.org/wiki/ISO_639-3) `eng`）翻译。
- 英语翻译应与现代标准汉语（简体字写法）版本保持一致（表意一致）。
- 尚未完成或通过审核的文档，不需要进行翻译。

### 命名
**命名**是对文档命名的简单规范。一篇文档的命名应该包括“所属”、“标题”、“语种代号”三个组成部分，用短横杠 `-` 分隔，即“所属-标题-语种代号”。

注意以下规则：
- “所属”指的是文档所属的最具体的部门或项目。
- “标题”若由多个词语组成，用短横杠 `-` 分隔。
- “语种代号”使用 [ISO 639-3](https://zh.wikipedia.org/wiki/ISO_639-3) 标准，简体中文文档使用 `cmn-Hans`，英文文档使用 `eng`。
- 文档统一以 `.md` 格式保存。

例如本文档属于 DSS 的简体中文格式手册，命名为：
> DSS-Format-Manual-cmn.md

属于项目“Project”的英文策划书，命名为：
> Project-Proposal-eng.md

## 内容
### 标题
- 尽量使用名词
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 关于人文素养
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 人文素养

### 链接
适当的链接数量提供快速通道前往计划内部或外部，并增进读者了解身旁的主题。
- 标题不应添加链接
- 大部分中文读者均能理解的常见中文字词，不需要创建链接
- 杜绝自我引用或重定向连回条目页面本身
- 不要为了突显特定文字或想法而创建链接，链接应该用来帮助阐明链接文字，而非强调文字。
- 在文章内存在的词语或短语上创建链接，不要说“请点击这里”。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 要查看DSS组织形式，[请点击这里](https://github.com/DSSOFFICIAL/DSS-Regulations/blob/master/DSS-Organize-Form-cmn.md)
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 查看[DSS组织形式](https://github.com/DSSOFFICIAL/DSS-Regulations/blob/master/DSS-Organize-Form-cmn.md)

### 语言表述
文档多以事实陈述和提供指导意见为主，注重客观性，在写作时应注重以下规则：
  - 严禁使用诋毁或带有歧视嫌疑的表述
  - 避免使用没有意义、意义不明确或模棱两可的词语
  - 避免使用语气傲慢的表述
  - 避免使用过时的表述
  - 避免使用过于极端或绝对的表述
  - 避免自我提及

## 格式
### 空格
> 汉学家称这个空白字元为「盘古之白」，因为它劈开了全角字和半角字之间的混沌。另有研究显示，打字的时候不喜欢在中文和英文之间加空格的人，感情路都走得很辛苦，有七成的比例会在 34 岁的时候跟自己不爱的人结婚，而其余三成的人最后只能把遗产留给自己的猫。毕竟爱情和书写都需要适时地留白。
> ——[GitHub - vinta/pangu.js: 為什麼你們就是不能加個空格呢？](https://github.com/vinta/pangu.js)  

此处规范的是用浏览器查看页面时可被察觉的空格，需要注意以下规则：
- 中文语境内文字间不应该留空格
- 用一个空格代替多个空格
- 除非特别情况，一般请使用半角空格
- 中英文之间需要添加空格
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 使用Workflow来自定义一个工作流  
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 使用 Workflow来制定一个工作流。  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 使用 Workflow 来自定义一个工作流。  
- 中文与数字之间需要添加空格
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 这份文件已经被修改了100次。  
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 这份文件已经被修改了100 次。  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 这份文件已经被修改了 100 次。  
- 反应具体数量时数字与计量单位之间需要添加空格（百分号与度、分、秒除外）。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 这张图片的大小为 10MB。  
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 明天的最高气温达到了 38°C。  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 倒入 200 mL 的水。  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 公司有 30% 的员工是本地人。  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 35° 的大斜坡对于这辆车来说可能过于吃力。  
- 中文与 @ # ¥ % ^ & * ( ) - + 等特殊符号之间需要添加空格。
- 产品名词等特殊定义的词语按照定义书写。
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 豆瓣FM是一款由豆瓣开发的个性化的音乐收听工具。  
- 当半角符号 / 表示“或者”之意时，与前后的字符之间均不加空格。

### 标点符号
规范地使用标点符号有助于标明语句逻辑和语气。需要注意以下规则：
- 不重复使用标点符号
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 喵喵喵？？？？  
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 他竟然输了？？！！  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 喵喵喵？  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 他竟然输了 ？！  
- 使用全角中文标点
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 很高兴认识你!你叫什么名字?  
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 很高兴认识你！你叫什么名字？
- 遇到整句英文时使用半角标点符号。
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 正如那句老话，“Where there is a will, there is a way”。
- 输入非中文内容时，则应当使用该语言规定的标准标点符号。
- Microsoft Word 等文字处理软件可能会替您将标点符号自动转换成错误的形式，请在编辑中多加注意。

### 数字与日期
规范地使用数字能够准确地传递信息，避免误读。需注意以下规则：
- 使用半角数字。
- 使用阿拉伯数字或简体中文数字,但不在一句中混合使用。
- 使用中文的连接号，即英文全角的“-”，以表示延续范围，并非破折号“—”。浪号“~”和“～”。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 在 10～15 米出处做标记。
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 于 2015年-2017 年间有效。
- 公元纪年以年月日表示时，不加上不必要的零。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 2018 年 01 月 01 日
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 2018 年 1 月 1 日 
- 公元纪年以全阿拉伯数字和符号表示时，年月日之间以半字线“-”隔开；当月和日是个位数时，十位上加“0”。（该写法不可出现在正文中，可以于结尾用于注明著作日期）
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 1998-8-1
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 2018-08-01
- 书写时、分、秒等时刻时，应该使用阿拉伯数字,使用24小时制。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 下午七点五十分
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 19 点 50 分
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 19:50
- 使用三位撇节法对多位数字进行分节（半角）
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 1500000.00 元
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 1,500,000.00 元

### 缩写
缩写（包括简称）是避免超长词汇的有效手段。当一个词以缩写的形式出现的频率多于以全称出现的频率，我们没有理由不使用缩写。但如若使用不当，可能会造成语义混淆，或让读者产生疑惑。在使用缩写时必须确保其正确规范性。需注意以下规则：

- 外文缩写应当采用拉丁字母表示，同时也应尽量避免英文字母以外的拉丁字母。
- 按照习惯正确大小写。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> github
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> Github
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> GitHub
- 不使用不地道的缩写。
> <img src="https://png.icons8.com/windows/100/e74c3c/multiply.png" widht="15px" height="15px"> 熟悉运用 Js、H5 的前端工作者。
> <img src="https://png.icons8.com/color/100/000000/checkmark.png" widht="15px" height="15px"> 熟悉运用 JavaScript、HTML5 的前段工作者。
- 在文档第一次使用一个缩写时应当用某种方式告知读者其含义，极广泛使用的缩写和型号除外。

## 授权协议
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。
