# icommunity
一、entity层
同类： model层 = entity层 = domain层
作用： 用于存放我们的实体类，与数据库中的属性值基本保持一致。

二、mapper层
同类： mapper层 = dao层
作用：现在用mybatis逆向工程生成的mapper层，其实就是dao层。对数据库进行数据持久化操作，他的方法语句是直接针对数据库操作的，而service层是针对我们controller，也就是针对我们使用者。service的impl是把mapper和service进行整合的文件。

三、service层
同类： 只有一个 service层
作用： 存放业务逻辑处理，也是一些关于数据库处理的操作，但不是直接和数据库打交道，他有接口还有接口的实现方法，在接口的实现方法中需要导入mapper层，mapper层是直接跟数据库打交道的，他也是个接口，只有方法名字，具体实现在mapper.xml文件里，service是供我们使用的方法。

四、controller层
同类： controller层 = web 层
作用： 控制器，导入service层，因为service中的方法是我们使用到的，controller通过接收前端传过来的参数进行业务操作，再将处理结果返回到前端。

五、dto层

同类：只有一个dto层

作用：DTO(数据传输对象层)，该层负责屏蔽后端的实体层，将UI层需要的数据进行重新的定义和封装，在实际的业务场景下，后端实现或存储的数据远比用户需要的数据要庞大和复杂，所以前端需要的数据相对来说要么是组合的，要么是抽取的，不是完整的，因为我们在设计数据存储格式上都会有一些额外的设计和考虑。前端的UI层，只是知道DTO的存在，同时前端需要的数据都在一个DTO中，这样，每次调用服务层的时候，只需要调用一次就可以完成所有的业务逻辑操作，而不是原来的直接调用业务逻辑层那样的，需要调用多次，对于分布式场景下，减少服务调用的次数，尤其重要

dto与dao的区别：
DTO
Data Transfer Object，数据传输对象（User.java）

    功能：用于传输对象，在前后端（界面，数据库之间进行数据传递）。 

    1、临时存储界面提交的数据，并将数据通过jdbc加入到数据库中

    2、取出数据库中数据，临时存储到对象，并转运到界面展示。

DAO
Data Access Object，数据访问对象（USerDao.java）

    功能：负责对数据库进行CRUD相关的访问操作
#资料
[Spring文档](https://spring.io/guides)
[Spring Web文档](https://spring.io/guides/gs/serving-web-content/)
[Bootstrap 起步文档](https://v3.bootcss.com/getting-started/)
[github 创建SSH key](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
[github 创建OAuth app](https://docs.github.com/en/developers/apps/creating-an-oauth-app)
[Elastic中文社区](https://elasticsearch.cn/explore/)

#工具
[git](https://git-scm.com/downloads)
[VP](https://www.visual-paradigm.com/cn/)