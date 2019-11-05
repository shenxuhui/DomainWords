# 领域文本的短语抽取
>本项目使用SmoothNLP中的extract_phrase函数，从不同领域的文本中抽取领域专有词汇，并进行结果展示。


## 数据
本实验采用的数据来源于**复旦大学计算机信息与技术系国际数据库中心自然语言处理小组提供的复旦文本语料库**,包括`经济`、`计算机`、`环境`、`体育`、`艺术`、`农业`、`政治`、`历史`、`宇航`、`教育`、`法律`、`哲学`、`军事`、`文学`、`交通`、`医疗`、`矿业`、`能源`、`电子`、`通信`共20个领域的文本。

* 经济领域文本示例：  
>【 文献号 】2-1275  
【原文出处】《中国投资》  
【原刊地名】京  
【原刊期号】199911  
【分 类 号】F61  
【分 类 名】财政与税务  
【复印期号】200004  
【 标  题 】利息所得税：启动经济的新尝试  
【 作  者 】李奎  
【 正  文 】  
    经国务院批准，《对储蓄存款利息所得征收个人所得税的实施办法》于近日颁布，并将于1999年11月1日起实施，适用20%的比例税率。这表明，根据我国国民经济总量结构和国民收入结构的重大变化，1958年取消的《个人所得税法》免征的利息所得税即将重新征收。  
    征收利息所得税将有效刺激消费品需求的增加，扩大社会总需求，带动经济增长，并将转变居民的投资观念和消费观念。  
    第一，在扩大内需方面，征收利息所得税将比降息更加有效。储蓄存款利率下降与社会消费品增长有一定的相关关系：利率下降1个百分点，市场商品销售将增加1.8个百分点。但是1996年5月以来的7次降息实践表明，降息对扩大内需、增加社会投资的作用越来越弱。其主要原因在于：首先，目前不仅城乡居民的即期收入上不去，而且对未来的预期收入也不佳，同时政府机构精简、国有企业改革以及住房、养老、医疗、教育等各种制度的改革，使居民普遍感到预期支出的提高，我国又没有建立起完善的社会保障制度，从而增强了居民的储蓄动机，以增强安全感。其次，由于社会消费需求不足以及私人投资难以获得融资，降息并没有有效增加社会投资需求，但货币供给量增加，大量资金沉淀于银行，货币流通速度降低，造成货币政策作用不明显，一旦经济启动引起资金需求增加，货币流通速度加快，容易形成货币供应过多、经济过热的隐患。有可能隐入“启动—紧缩—再启动—再紧缩”的怪圈。    
    
* 计算机领域文本示例：  
>计算机应用  
COMPUTER APPLICATIONS  
1999年 第19卷 第6期 Vol.19 No.6 1999  
Domino环境中的数据加密技术  
李俊海　耿继秀　钱丽瑾　刘彦丽　张德壮  
　　摘　要　在企业网络实践的基础上，讨论了数据加密技术在企业网络中的应用。为了防止对非授权的数据库和文档的存取，可以对数据库进行选择算法的加密和使用私钥/公钥加密机制，对数据库文档的字段加密。  
　　关键词　数据库文档，数据加密，密钥，存取授权  
1　引言  
　　加密技术可以使我们在不安全的通道上建立安全的连接。在Domino环境中，为了防止对非授权的数据库、文档或者邮件的存取，除对数据库进行不同级别的授权外（七种级别），我们能够对数据库、对某个库中的一个文档、多个文档或者全部文档进行加密。通过加密的办法，使得系统中的各种数据的安全在三个面上得到保障。加密的办法有多种多样的，但是总离不开加密用的密钥。Domino提供了对称和非对称的两种加密机制。在对称的加密机制中，用户需要在阅读加密文档时具备密钥。我们着重讨论对数据库中的一般文档、对使用指定表单产生的所有文档、文档中的全部字段或部分字段使用指定密钥进行加密、对数据库进行选择算法的加密以及指定用户解密的方法和技术。  
2　数据库文档加密  
　　在Domino环境中，数据库是文档的集合。一个数据库可以包含最多不超过4GB大小的数据文档。对一个文档加密的含义是， 使用公钥或某个密钥应用到一个或多个的域（字段）上进行加密。如果密钥是特选的，就需要将该密钥发送给所指定的用户。拥有一个文档密钥的任何用户都可以读该文档加密域。没有密钥的用户则只可以读在该文档中没有被加密的域。对一个文档进行加密保护，它的表单必须具备一个或多个系统开发者定义的可加密的域。实际上，为了醒目起见，在填写一个文档时就可以看到加密域用红色的标记来识记。我们在对域加密时，可以使用系统为用户生成的公钥或者创建一个新的密钥。在一个文档中，对可加密的域都可使用所选定的密钥进行加密；用户不允许为某个文档的可加密域选择不同的密钥。除了对数据库中的某个文档进行加密外，我们还可以对数据库中使用特定的表单创建的全部文档加密。  
　　数据库的拥有者可以对特定的表单创建的所有文档进行加密。用户可通过将密钥加入到表单中或者把相关密钥的关键字加入到该表单来达到目的。数据库的“设计者”有权决定该表单将使用何种类型和哪些密钥。如果将密钥加入到某个表单中，那么通过该表单构造的所有文档都用这个密钥加密。这里我们给出一个对数据库中全部文档使用给定密钥进行加密的例子。加密是通过LotosScript（一种类似VisualBasic面向对象的语言,功能上更强于该语言）来实现的。 以下的程序用密钥“绝密” 和“Top Secret”加密文档中的每一域。   
  


领域文本包含的文档数和总字数统计如下：

|**数据领域**|**文件数**|**总字数**|
| :-:|:---:|:---:|
|Economy|3201|2083,5291|
|Computer|2714|1625,7862|
|Enviornment|2435|1294,4809|
|Sports|2507|1136,6098|
|Art|1482|1054,7150|
|Agriculture|2043|1027,1244|
|Politics|2050|994,2158|
|History|934|774,8028|
|Space|1282|500,0878|
|Education|120|15,1783|
|Law|103|14,9372|
|Philosophy|89|14,4040|
|Military|150|11,0303|
|Literature|67|9,1466|
|Transport|116|7,5620|
|Medical|104|6,5853|
|Mine|67|5,6017|
|Energy|65|4,6160|
|Electronics|55|3,8597|
|Communication|52|2,9893|


## 短语抽取函数调用

**SmoothNLP**提供了一个短语抽取函数`extract_phrase`，使用词语本身及其上下文特征进行短语抽取。  

```python
from smoothnlp.algorithm.phrase import extract_phrase
extract_phrase(corpus,top_k,chunk_size,max_n,min_freq)
```
  
参数说明：
```text
corpus:     必需，file open()、database connection或list
top_k:      float or int,表示短语抽取的比例或个数
chunk_size: int,用chunksize分块大小来读取文件
max_n:      int,抽取ngram及以下
min_freq:   int,抽取目标的最低词频
```


## 不同领域效果展示

经过对短语抽取结果的分析，我们认为该短语抽取方法适用于不同领域，且文本量大的时候会有更好的效果。

下面为`经济`,`计算机`,`艺术`领域文本的短语抽取结果展示：  
### 经济  
![经济](https://github.com/smoothnlp/DomainWords/blob/master/img/%E7%BB%8F%E6%B5%8E.PNG?raw=true)  
  
### 计算机
![计算机](https://github.com/smoothnlp/DomainWords/blob/master/img/%E8%AE%A1%E7%AE%97%E6%9C%BA.PNG?raw=true)

### 环境
![](https://github.com/smoothnlp/DomainWords/blob/master/img/%E7%8E%AF%E5%A2%83.PNG?raw=true)

### 体育
![](https://github.com/smoothnlp/DomainWords/blob/master/img/%E4%BD%93%E8%82%B2.PNG?raw=true)

### 艺术  
![艺术](https://github.com/smoothnlp/DomainWords/blob/master/img/%E8%89%BA%E6%9C%AF.PNG?raw=true)


* 领域词汇获取方式：
`https://github.com/smoothnlp/DomainWords.git`
  

## 注：

* 本项目所用数据来自`复旦大学计算机信息与技术系国际数据库中心自然语言处理小组提供的复旦文本语料库`.

* 本项目所用代码已在SmoothNLP中开源：
https://github.com/smoothnlp/SmoothNLP.

  

## 没想到吧,还有彩蛋 
如果您对NLP感兴趣,欢迎加入我们的团队,我们招收全职/实习nlp算法工程师.  

cv投递**hr@smoothnlp.com**.




