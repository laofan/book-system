# 毕业设计-图书管理系统

#### 介绍
本系统为采用Springboot + Mysql + MybatisPlus+Thymeleaf技术架构开发的单端电脑端图书管理系统。该系统有两个登入身份、共8个功能模块（修改密码为共用模块）

#### 软件架构
Springboot | MybatisPlus | Thymeleaf | Maven | Mysql 

#### 功能结构
该系统支持两种不同的身份登入，分别是读者与管理员。不同身份的对应功能如下：
![1685331418(1)](https://github.com/laofan/book-system/assets/12497380/a571b521-2c8b-4813-b3a4-2a1eb72220b2)


#### 功能介绍
##### 【代码结构与数据库截图】
![code](https://github.com/laofan/book-system/assets/12497380/fc89e317-4b66-4f1f-9c40-0d0ed2af4f26)
![image](https://github.com/laofan/book-system/assets/12497380/00c97e28-1288-4f6a-a630-57b332bb911b)
##### 【功能详述】 
管理员与读者使用相同登录界面，在登录页进行身份的选择
![image1](https://github.com/laofan/book-system/assets/12497380/89d120cd-6461-4d50-8016-b6010d05a1f1)
   以管理员身份登录后，首页显示该系统的基本功能介绍。此时左侧工具栏可以看到管理员身份的所有功能：图书管理、人员管理、借还管理、密码修改。


△图书管理
   图书管理模块中可进行【添加图书】与【图书管理】。
   图书添加中，在录入界面录入图书名、作者、出版社、ISBN等图书相关信息，分类的填写会影响图书在图书管理中的检索。点击“添加”后，即可成功添加图书。添加的图书可在二级菜单“图书管理”中查看。
![image3](https://github.com/laofan/book-system/assets/12497380/0a8a0fb0-4856-4e74-ada1-ef298508405f)
 图书管理列表中为系统的现有图书，可以通过界面上方的分类、图书名进行检索。列表中的图书可以进行“查看详情”、“编辑”、“删除”操作。
![image4](https://github.com/laofan/book-system/assets/12497380/c4d486d6-6eee-457e-9ad3-b4b92f5dcca5)


△人员管理
   人员管理与图书管理结构相同，可进行【添加人员】与【人员管理】。
   添加人员时需录入姓名、用户名、密码、性别、生日、地址、电话、及角色信息。成功添加的人员可以在【人员管理】中查看。
![image5](https://github.com/laofan/book-system/assets/12497380/99551d6b-da70-40ea-a575-593db79a3b62)
   人员管理列表中现有的人员信息，可以通过界面上方的角色、姓名进行检索。列表中的人员可以进行“编辑”、“删除”操作。
![image6](https://github.com/laofan/book-system/assets/12497380/c5a90390-64e5-41da-8ba2-adccdaede159)


△借还管理
   借还管理模块显示当前图书借还的流水日志，支持通过借还状态与图书名进行搜索。按借出时间顺序显示借还日志，日志列表中显示书籍当前的还书状态。状态包含“未还”、“超期”、“已还”、“已催还”
![image7](https://github.com/laofan/book-system/assets/12497380/27f10e21-b580-4590-90f1-c80bd9a1d730)


△密码修改
   密码修改模块中用户可以通过录入旧密码与新密码，并确认新密码来修改密码。
![image8](https://github.com/laofan/book-system/assets/12497380/ffc8ba38-7e06-43a1-a38a-b75fecd78ab6)
   以读者身份登录后，首页显示该系统的基本功能介绍。此时左侧工具栏可以看到读者身份的所有功能：图书查询、我的借还、图书挂失、个人信息、密码修改。

△图书查询
   图书查询模块中可以通过分类与图书名搜索图书。图书列表显示系统的所有图书，可以“查看详情”与“借阅图书”。
![image9](https://github.com/laofan/book-system/assets/12497380/399ae011-ea0f-4035-b307-9242441dbc06)


△我的借还
   我的借还可以进行【我要还书】与【借还管理】。
   我要还书页面可以看到当前账号的借阅书籍，书籍列表显示书籍基本信息、借出天数、应还天数、图书状态与还书续借操作。其中包含了已经超期、挂失的图书无法续借，未还图书可以归还与续借的规则逻辑。
![image10](https://github.com/laofan/book-system/assets/12497380/3bbd614d-8742-4850-a9a8-d13c5a5d31d7)

借还管理中显示账户的借还流水，包含借阅、归还的操作日志，并显示该条日志的图书状态。可以对日志进行“删除”操作。  
![image11](https://github.com/laofan/book-system/assets/12497380/14a9fad5-440c-4d7d-b896-71bb55f4cfa3)


△图书挂失
   图书挂失分为【挂失】和【解挂】。
   挂失列表中显示正在借阅与挂失的图书，显示其借阅状态与挂失状态，对未挂失的图书可以进行“挂失”操作。  
![image12](https://github.com/laofan/book-system/assets/12497380/0626710d-2d7d-4911-abe0-aa6cf6bd8264)
   解挂列表中显示正在挂失中的书籍，可以进行“解挂”与“赔偿”操作。   
![image13](https://github.com/laofan/book-system/assets/12497380/821418b7-5891-4517-b037-acbc65183ef3)


△个人信息
   个人信息显示当前账户的个人信息，点击“修改”可以修改个人信息。    
![image14](https://github.com/laofan/book-system/assets/12497380/1f011427-8111-4e5f-8bc4-0553df06f0fb)


△密码修改
   本功能模块与管理员身份中的【密码修改】功能一致。

#### 使用说明
1. 创建数据库，执行数据库脚本
2. 修改jdbc数据库连接参数
3. 下载安装maven依赖jar
4. 在tomcat服务器部署项目  
    请求地址： http://localhost:8080/book    
    用户名：admin  
    密码：admin  

#### 联系作者
这是作者的微信二维码，如需本项目源代码，可扫码联系联系作者  
![xunmaw001](https://github.com/laofan/book-system/assets/12497380/1f434271-e6d5-44c0-94e2-0c1973d863d4)

这是作者的公众号二维码，是不是推一些新开发的项目源码与高效软件工具，感兴趣的朋友给个关注  
![xunmaw公众号](https://github.com/laofan/book-system/assets/12497380/6e145cb0-7a39-4155-b25b-46c735aa400d)
