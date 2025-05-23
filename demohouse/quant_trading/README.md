# 股票交易 AI 辅助预测工具

股票交易是一个挺个性化的事情，每个人有自己的买卖策略，各不相同。

不过，不论你怎么操作交易，总离不开**资金面、大盘面、消息面**三个方面。能够利用 AI 来实现自动量化交易是个极具定制化、个性化的需求。市面上的量化交易软件，要么需要收费，要么有较高使用门槛。所以，我们想利用 AI 做一款开源的股票量化交易系统，**让每个人都能用上量化交易，并且每个人都能定制自己的交易策略**。


## 安装方法 Installation

提供不同操作平台的安装方法

### [Linux安装方法](../../demohouse/quant_trading/docs/linux_installation.md)

### [Windows安装方法]() TODO

- 对于许多股民来说，并不会编程，也不使用 Linux，因此在 Windows 上的安装，我打算提供一体化打包安装。

## 使用方法

整个界面，依然是对话模式啦！不过，针对特定任务，我做了流程化处理。

- 1、让 AI 预测今天推荐购入或卖出哪些股票，具体到股票名称；
- 2、给 AI 说出一只股票，让 AI 分析是该买入还是卖出。
- 3、其它自由问答内容，你可以随意发挥。


## 原理介绍

股票交易，总离不开**资金面、大盘面、消息面**三个方面。这款智能股票交易软件主要从资金面、消息面制定了操作流程，针对几个特定任务的处理流程如下：

- 1、预测今日股票，给出推荐结果
```
[抓取新闻网页]                    [消息侧建议]
      ● ------> (分析新闻数据) ------> □ --------|   (股票推荐)  (自动交易)
                                                |------ □ -------> ◘
[抓取股票数据]                    [资金侧建议]    |
      ● ------> (分析股价数据) ------> □ --------|

```

- 2、分析指定股票数据，给出建议
```
[抓取指定股票新闻]
        ● ------> (分析新闻数据) ------|   (分析数据)  (自动交易)
                                      |------ □ -------> ◘
[抓取指定股票数据]                     |
        ● ------> (分析股价数据) ------|

```



### TODO

**当然，量化交易是个非常复杂的学问，我的工具刚开源，不足之处还是很多，欢迎大家给建议和意见。**

我自己总结，目前工具仍存在一些问题和功能需要完善：

- 优化量化分析策略，使结果泛化稳定。
- 接入正规交易平台的 qmt，ptrade 接口
- 允许简便、灵活地定制化交易策略
- 目前仅接入 A股，需要补充港股、美股等。各股市策略差异也很大，需要针对性优化。
