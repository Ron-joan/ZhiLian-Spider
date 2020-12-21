# 智联招聘爬虫

## 2020年12月版本

<img align="right" alt="GIF" width="400px" src="https://cdn.jsdelivr.net/gh/Jackyu-1999/CDN-Static@main/star.png" />

### 网站特点

* 智联招聘是一个典型的用ajax加载数据的网站
* 我爬了大概七八万条数据，目前还没有被封IP，但请不要滥用。

***

<img>

### 思路实现

* 对jobType、cityId进行url拼接
* 当url返回数据大于270条时，再对cotype进行筛选爬取
* 筛选之后，url返回数据大于270时，再对cosize进行筛选爬取

***



## 可以利用以下参数拼接url：

-   pageSize: 返回数据的数量，默认返回50条，最多返回90条

-   pageNo: 翻页参数，默认为1

-   cityId: 城市id，默认为-1，如：`长沙`的id为 `749`

-   workExperience: 工作经验参数，默认为-1，如：`1-3年` 经验为 `0103`

-   jobType: 职位类型id，默认为-1，如：`javascript前端工程师为` `9000100030000（小类）`

-    education: 学历要求，默认为-1，如：`本科` 为 `4`

-   companyType: 公司性质，默认为-1，如：`国企` 为 `1`

-   companySize: 公司规模，默认为-1，如：`100-299人` 为 `3`

    


## 分析页面变化规律：

`cityId`:

-   北京：530

-   上海：538

-   广州：763

-   深圳：765

-   长沙：749

-   杭州：653

-   成都：801

-   厦门：682

    


`工作经验参数`：

-   无经验：0000

-   一年以下：0001

-   1-3年：0103

-   3-5年：0305

-   5-10年：0510

-   10年以上：1099

    


`职位类型id(大类）：`

-   销售/商务拓展：19000000000000

-   人事/行政/财务/法务 14000000000000

-   互联网/通信及硬件：9000000000000

-   运维/测试：20000000000000

-   视觉/交互/设计：17000000000000

-   运营/专业分析：5000000000000

-   产品/项目/高级管理：3000000000000

-   市场/品牌/公关：16000000000000

-   金融/保险：12000000000000

-   房地产/工程/建筑：7000000000000

-   物流/采购/供应链：2000000000000

-   生产制造/营运管理：15000000000000

-   农业/能源/环保：21000000000000

-   医疗/医美：18000000000000

-   教育/培训/科研：11000000000000

-   编辑/记者/翻译：1000000000000

-   影视传媒：4000000000000

-   商务服务/生活服务：6000000000000

-   管培生/非企业从业者：8000000000000

    


`学历要求：`

-   初中及以下

-   高中

-   中专/中技

-   大专

-   本科

-   硕士

-   博士

-   MBA/EMBA

-   不要求

    
