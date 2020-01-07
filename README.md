# 前言

## 前言

Elastic Stack 是 原 ELK Stack 在 5.0 版本加入 Beats 套件后的新称呼。

Elastic Stack 在最近两年迅速崛起，成为机器数据分析，或者说实时日志处理领域，开源界的第一选择。和传统的日志处理方案相比，Elastic Stack 具有如下几个优点：

* 处理方式灵活。Elasticsearch 是实时全文索引，不需要像 storm 那样预先编程才能使用；
* 配置简易上手。Elasticsearch 全部采用 JSON 接口，Logstash 是 Ruby DSL 设计，都是目前业界最通用的配置语法设计；
* 检索性能高效。虽然每次查询都是实时计算，但是优秀的设计和实现基本可以达到全天数据查询的秒级响应；
* 集群线性扩展。不管是 Elasticsearch 集群还是 Logstash 集群都是可以线性扩展的；
* 前端操作炫丽。Kibana 界面上，只需要点击鼠标，就可以完成搜索、聚合功能，生成炫丽的仪表板。

当然，Elastic Stack 也并不是实时数据分析界的灵丹妙药。在不恰当的场景，反而会事倍功半。我自 2014 年初开 QQ 群交流 Elastic Stack，发现网友们对 Elastic Stack 的原理概念，常有误解误用；对实现的效果，又多有不能理解或者过多期望而失望之处。更令我惊奇的是，网友们广泛分布在传统企业和互联网公司、开发和运维领域、Linux 和 Windows 平台，大家对非专精领域的知识，一般都缺乏了解，这也成为使用 Elastic Stack 时的一个障碍。

为此，写一本 Elastic Stack 技术指南，帮助大家厘清技术细节，分享一些实战案例，成为我近半年一大心愿。本书大体完工之后，幸得机械工业出版社华章公司青睐，以《ELK Stack 权威指南》之名重修完善并出版，有意收藏者欢迎[购买](http://search.jd.com/Search?keyword=elkstack%E6%9D%83%E5%A8%81%E6%8C%87%E5%8D%97&enc=utf-8)。

本人于 Elastic Stack，虽然接触较早，但本身专于 web 和 app 应用数据方面，动笔以来，得到诸多朋友的帮助，详细贡献名单见[合作名单](contributors.md)。此外，还要特别感谢曾勇\(medcl\)同学，完成 ES 在国内的启蒙式分享，并主办 ES 中国用户大会；吴晓刚\(wood\)同学，积极帮助新用户们，并最早分享了携程的 Elastic Stack 日亿级规模的实例。

博客作者：联系请[点击](https://k8sadmin.info/lian-xi-zuo-zhe)，搬运不易，希望请作者喝咖啡，可以点击[联系博客作者](https://k8sadmin.info/lian-xi-zuo-zhe)

## Version

2016-10-27 发布了 Elastic Stack 5.0 版。由于变动较大，本书 Git 仓库将 master 分支统一调整为基于 5.0 的状态。

想要查阅过去 k3、k4、logstash-2.x 等不同老版本资料的读者，请下载 ELK release：[https://github.com/chenryn/ELKstack-guide-cn/releases/tag/ELK](https://github.com/chenryn/ELKstack-guide-cn/releases/tag/ELK)

## TODO

限于个人经验、时间和场景，有部分 Elastic Stack 社区比较常见的用法介绍未完成，期待各位同好出手。罗列如下：

* es-hadoop 用例
* beats 开发
* codec/netflow 的详解
* filter/elapsed 的用例
* zeppelin 的 es 用例
* kibana的filter交互用法
* painless的date对象用法：同比环比图
* significant\_text aggs用例
* cat nodeattrs接口
* timelion保存成panel的用法
* regionmap用法
* Time Series Visual Builder用法
* Viewing Document Context用法
* Dead Letter Queues讲解
* elastalert 新版说明

