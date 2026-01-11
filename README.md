# R02 基于vue+neo4j的中医中药方剂推荐+知识图谱可视化系统（中药分布地图、知识图谱大屏）

完整项目收费，可联系微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775

# 简要介绍
🩵编码：R02
🩵网站端：neo4j知识图谱+推荐算法、药方查询（带图谱）、中药查询，数据下钻、产地地图、数据纠错，中医中药资讯新闻
🩵管理端：药方、药材、资讯、用户的增删改查管理等
🩵大屏端：超酷知识图库结合可视化
🩵架构： 3+1+2架构 三前端一后端双数据库
🩵技术：vue+springboot+neo4j+mysql （java开发为主）
🩵数据来源：包含scrapy爬虫，数据预处理，图谱生成
🩷展望：R02 新版本正在开发，更多超实用征服答辩、评奖老师的功能
# 视频演示

[video(video-nlZLOu3x-1730521417922)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=113411413247527)(image-https://img-blog.csdnimg.cn/img_convert/36ab1070195d5cef868ccc9e610959a9.jpeg)(title-解说vue+neo4j知识图谱中药大数据+推荐算法+neo4j知识图谱+可视化 java开发vue+springboot)]
# 系统功能架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0902153348304417bcbb0f9f94b2ca62.jpeg)
# 爬虫流程
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6af854818f054b00b3fa1ee3238d2e29.jpeg)
# 网站端介绍
## 药材推荐
集成推荐算法，提供个性化药材推荐，帮助用户根据不同需求选择合适的药材。算法方面集成usercf和itemcf两种算法。药材卡片可以点击下钻：
![请添加图片描述](https://i-blog.csdnimg.cn/direct/f0594058a6364ff183db007ee304a2f7.jpeg)
## 中医知识图谱
中医知识图谱，模糊搜索功能的集成，并且支持力导向图和环形布局两种布局模式之间的切换：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4808fa877de44ccbb89c57dbcd4f98a3.jpeg)
切换到环形视图：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e343634c7f734e7db4a0dc6c49446d2a.jpeg)
模糊搜索石斛：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3cabb14868d74b4cab4b6b908dffeff9.jpeg)
## 中医方剂和药材可视化:

提供中医方剂及其药材的可视化展示，用户可以方便地查询方剂及其组成药材，并深入了解每种药材的特性。
查询功能:

用户可根据中药和方剂进行查询，支持根据方剂查询药材构成，并查看相关知识图谱。用户可下钻至具体药材界面进行详细了解，并可对药材进行评论，利用 **LSTM 算法进行情感分析**，以获取用户反馈。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d704975dbfea4cfa9173dfeeeebeb18a.jpeg)
在方剂的详情页面中可以查看这个处方的【例如**阿魏麝香散**】构成的药材的知识图谱，下面褐色的就是构成的药材，这个药材是可以点击的，点击之后进行下钻，下钻到药材
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4cdc6ee68a7f47fba63920db7e5bf47f.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ff897c75b75e4985a760c6e97f76db2f.jpeg)
同时也支持单独的查询药材
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c494be883ef94a1e847db7cb2eccbe47.jpeg)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bc62f338dd2e47ac82759ef4084c13de.jpeg)

系统支持留言评论功能，用户可以与其他用户进行互动，分享经验和见解。这个留言可以通过后台的paddle飞浆模型情感分析其情感倾向
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/67cd9aa3b38d451a8681cb2f1cddb5d7.jpeg)
## 中医资讯浏览:
提供最新的中医资讯，帮助用户获取中医领域的最新动态和研究成果。支持点赞、评论、收藏等操作：
![用户可以通过输入关键词进行模糊查询，系统支持力导向图和环形布局之间的切换，方便用户探索方剂的相关知识。](https://i-blog.csdnimg.cn/direct/db6144115bfb4b94a817ea742c90cb18.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8c4b5bc4b8e9422b8f807542afd4d690.jpeg)
## 中药产地地图可视化:
根据药材名称在中国地图上高亮显示重要产地，用户可在此界面提交纠错信息，管理员收到后可进行处理，确保信息的准确性。
比如输入青藤子：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bc7e21e56d384c5bb57dc8cb0235d027.jpeg)
## 用户管理与安全性:
提供用户注册和登录功能，通过阿里云短信验证码确保密码修改的安全性。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e2e3b05e2dca4f9f8d5927d6caa3bd21.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f646eeae7e384e5e81a9af9a5ae23bbe.jpeg)
##  技术架构
前端: 使用 Vue.js 构建用户友好的界面，确保良好的用户体验。
后端: 采用 Spring Boot 构建高效的服务端逻辑，支持大并发请求。
数据存储:
Neo4j: 存储和管理中医知识图谱，支持复杂的关系查询。
MySQL: 用于存储其他信息数据，实现高效的数据管理。
# 大屏端介绍
数据大屏，数据大屏支持各种不同形式的展示，以下是**环形布局**：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7c54bc7d39b14702931178a60e351199.jpeg)
**force图布局**展示
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e4aedad3ec484438938dfd1072439993.jpeg)
环形图展示：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/731aeb6aface486d83b57137459ecf08.jpeg)
**图谱构造部分**的代码和过程也很重要，否则很难证明图谱是你自己做的，这个在论文或者比赛中都要需要的，下面图谱构造部分过程的截图:
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5646eb335fa54e3ea28666def361a67a.jpeg)
neo4j截图部分:
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fce1e5705cd544ff949a77c3652e9c86.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/458614e02ecc4ae4bfab2945ad589ec8.jpeg)
整个大屏通过丰富的图表与数据展示了中医药材和药方的多维度信息，包括用户注册数量、中药药材和药方的记录数、热门词汇图、性味比例、中药产地分布及注册情况等。

**详细部分**
顶部区域：展示了系统的总体统计信息，包括平台总用户数、中药药材记录数和中药药方记录数，为用户提供整体数据的概览。

**左上角图表**：展示了各种古籍的收录排行，说明了中药材信息主要来源于哪些古籍，反映了古籍在中医药材数据中的重要性。

**左下角图表**：展示性味比例图，不同颜色的扇形代表不同性味的中药材数量占比，帮助用户直观了解中医药性味的分布情况。

**中部主要区域**：中药药方关系图谱展示了不同药方和药材之间的关系，节点以 “Book” 和 “Prescription” 两种颜色区分，青色节点代表书籍，橙色节点代表药方，各个节点之间的连线展示了它们之间的关系，帮助识别药材和药方的联系网络。

**右上角图表**：通过词云图展示了中药相关的大数据热词，可以用户快速了解当前中药领域的热点话题和研究方向。

**右中部图表**：中药产地分布图，通过辐射状的图形展示了中药材的主要产地分布信息，图上的不同区域代表不同省份，每个省份用不同的颜色标记。

**右下角时间轴**：展示了项目的设计过程和时间节点，包括服务器端开发、前端页面设计、数据爬取和大屏设计等步骤，帮助用户了解该项目的开发过程和时间线。

**左下角登陆情况**：折线图展示了用户登录的时间分布情况，通过数据点和连线观察用户访问的高峰和低谷时段。

这个大屏将复杂的中药材和药方数据通过可视化方式展示出来，为用户提供了一目了然的中药材数据查询和分析服务，充分展现了**中医药数据**的多样性和丰富性。
# 管理端介绍
提供主页功能：管理员可以直观查看系统数据情况、用户登录的信息、3D词云
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d51697574aee4bc697286cee38b8efac.jpeg)

用户信息管理：可以进行用户增删改查的操作

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e1e676261c5f4fb9907294e2e20bfa2e.jpeg)

中药材信息查询：用户可以点击系统名称进行模糊查询，或通过搜索框自主输入想要查询的信息进行中药材查询，另外支持增删改：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cf4b00cb92bb463a87545e81937f2289.jpeg)
中药的方剂管理，支持增删改查：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/47a26badb14a40ecb45b9a1993387e0e.jpeg)


中药材资讯管理：后台可以进行咨询管理。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/46877c59090b4b1a8832a7a7339ce7ea.jpeg)

**中药材产地可视化**：内含全国省份的中药材种类分布地图，这个数据是从scrapy爬虫爬取到的数据进行提取之后使用echarts可视化进行提取的
比如我们输入了青酒缸，在中国地图上金色的点位展示了产地的信息
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d93e3efd128b435a93de0074a139d1d3.jpeg)

用户可以向后台管理员发送中药药材和药方的纠错申请，管理员可以进行处理
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6cb6fb1407d24c79b7ee9f7f55025292.jpeg)
**评论管理**
用户的登录和退出功能
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2341601611aa4c41b2c577f8cfa9608f.jpeg)
# 爬虫介绍
爬取逻辑非常简单，根据url来处理翻页，然后获取到详情页面的链接，再去爬取详情页面的内容即可！
需要注意的是：这里面有一个方剂多个来源的情况，这个没有处理。
最终数据落地到excel中。
经测试，总计获取 24909条中医方剂数据。
```python
import pandas as pd
import scrapy


class ZhongyaofangSpider(scrapy.Spider):
    name = 'fangji'
    allowed_domains = ['zysj.com.cn']
    start_urls = [f"https://www.zysj.com.cn/zhongyaofang/index_{i}.html" for i in range(1, 27)]

    def __init__(self, *args, **kwargs):
        self.data = []

    def parse(self, response):
        # 提取包含链接和标题的部分
        for li in response.css('div#list-content ul li'):
            a_tag = li.css('a')
            title = a_tag.css('::attr(title)').get()
            href = a_tag.css('::attr(href)').get()
            if title and href:
                # 构建完整的详情页 URL
                detail_url = response.urljoin(href)
                yield scrapy.Request(detail_url, callback=self.parse_detail, meta={'title': title})

    # 如果没有这个元素，就设置空就行
    # 处方： div[class="item prescription"]/div[class="item-content"]/p/text
    # 制法： div[ class="item making"]/div[class="item-content"]/p/text
    # 主治： div class="item functional_indications"]/div[class="item-content"]/p/text
    # 用法用量： class="item usage"]/div[class="item-content"]/p/text
    # 注意事项： class="item care"]/div[class="item-content"]/p/text
    # 摘录： class="item excerpt"]/div[class="item-content"]/text
    def parse_detail(self, response):
        title = response.meta['title']

        # 提取各个字段
        prescription = response.css('div.item.prescription div.item-content p::text').get(default='').strip()
        making = response.css('div.item.making div.item-content p::text').get(default='').strip()
        functional_indications = response.css('div.item.functional_indications div.item-content p::text').get(
            default='').strip()
        usage = response.css('div.item.usage div.item-content p::text').get(default='').strip()
        care = response.css('div.item.care div.item-content p::text').get(default='').strip()
        excerpt = response.css('div.item.excerpt div.item-content::text').get(default='').strip()

        item = {
            'title': title,
            'prescription': prescription,
            'making': making,
            'functional_indications': functional_indications,
            'usage': usage,
            'care': care,
            'excerpt': excerpt
        }

        self.data.append(item)

        yield item

    def closed(self, reason):
        # 当爬虫关闭时，保存数据到 Excel 文件
        df = pd.DataFrame(self.data)
        df.to_excel('zhongyaofang_data.xlsx', index=False)

```
##  爬取截图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a2d2ee080207412586752ce3d0c14a14.png)
## 爬取后的数据
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a80e520160344cb2b0a1bfa8bbc4380c.png)


数据预处理：从药材数据中提取药材的产地信息
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a482c7617f574b0d81f4b58f2f8a9ff1.jpeg)
从药材和药方数据中提取知识图谱信息并且构建到neo4j数据库中
系统的图谱构建由于时间比较长，我们加上了进度条日志，可以方便用户在导入数据的时候去预估时间：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9858bcb6768a4bb1ae6be3fed40ca137.jpeg)

图谱信息（由于前端显示限制，只展示冰山一角）：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/15b4ffe01f6242938d2aea99221107af.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cafd1950565242feb044660938eff5b6.jpeg)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/17de23a50542418e82800aff910aa8fa.jpeg)
### 推荐算法
**算法说明**：
该推荐算法基于ItemCF（物品协同过滤）实现中药药方的推荐。首先，算法通过构建药方的相似度矩阵，计算每个药方与其他药方之间的相似性（如余弦相似度或Jaccard相似度）。然后，根据目标药方的相似药方及其用户的历史行为，生成个性化的推荐列表。算法分为两部分：1）数据预处理与相似度计算；2）推荐生成。
在实现中，首先读取用户与药方的交互数据，构建用户-药方的交互矩阵，并将其转换为药方的特征向量。接着，通过计算每对药方之间的相似度，构建药方的相似度矩阵。最后，针对目标药方，找到其最相似的药方，并根据用户的历史行为生成推荐列表。
**流程图**：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a6fad08238834f7d8648bae192d32634.png)

**代码**：
```java
import numpy as np
from collections import defaultdict

class ItemCFRecommender:
    def __init__(self, data_path, similarity_metric="cosine"):
        self.data_path = data_path
        self.similarity_metric = similarity_metric
        self.user_item_matrix = self._read_data()
        self.item_sim_matrix = None
    
    def _read_data(self):
        # 读取用户-药方交互数据
        data = defaultdict(dict)
        with open(self.data_path, 'r') as f:
            for line in f:
                user, item, rating = line.strip().split(',')
                data[user][item] = float(rating)
        return data
    
    def _calc_item_sim(self):
        # 构建药方的特征向量
        items = list(self.user_item_matrix.values())[0].keys()
        item_features = {}
        for user, item_dict in self.user_item_matrix.items():
            for item, rating in item_dict.items():
                if item not in item_features:
                    item_features[item] = []
                item_features[item].append(float(rating))
        
        # 计算相似度矩阵
        self.item_sim_matrix = {}
        for item1 in items:
            self.item_sim_matrix[item1] = {}
            for item2 in items:
                if item1 == item2:
                    continue
                vector1 = item_features[item1]
                vector2 = item_features[item2]
                sim = self._cosine_sim(vector1, vector2)
                self.item_sim_matrix[item1][item2] = sim
    
    def _cosine_sim(self, vec1, vec2):
        dot = sum(a*b for a,b in zip(vec1, vec2))
        norm1 = sum(a**2 for a in vec1)**0.5
        norm2 = sum(b**2 for b in vec2)**0.5
        return dot / (norm1 * norm2 + 1e-9)
    
    def recommend(self, target_item, top_k=5):
        if not self.item_sim_matrix:
            self._calc_item_sim()
        sims = sorted(self.item_sim_matrix[target_item].items(), key=lambda x: x[1], reverse=True)
        return [item for item, sim in sims[:top_k]]

# 示例用法
recommender = ItemCFRecommender("drug_formula_data.csv")
recommended = recommender.recommend("药方A")
print("推荐的药方：", recommended)

```
