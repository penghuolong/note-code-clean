NamingConventions.md

# 命名规范   

### 1. 名副其实   
变量、函数或类的名称就应该告诉了我们 它为什么会存在、做了什么事、应该怎么用。
### 2. 避免误导
    * 不使用专用名词 如（hp、aix、sco是UNIX平台专用名词）（accountList 如果并非真是个List就不要用List）
    * 提防使用不同之处较小的名称
### 3. 做有意义的区分
    * 不使用数字系列做区分（a1、a2、a3）
    * 不使用废话做区分（productInfo 和 productData zork 和 theZork）
### 4. 使用读的出来的名称，不要自己造词   
### 5. 使用可搜索的名称（若变量或常亮可能在代码多处使用，则应给予便于搜索的名称）
### 6. 避免使用编码（）
    * 减少使用成员前缀。把类和函数做的足够小，消除对成员前缀的需要
    * 接口不使用 I 前缀来表示接口
### 7. 避免思维映射（直接的表述）
### 8. 类名（应当是名词或者名词短语）
### 9. 方法名（应当是动词或者动词短语）
