# 全网最好用的 IDE 股票看盘插件「LEEK」，摸鱼党最爱 🚀

> 在 IDE 里一边写代码一边看股票行情，这大概是程序员专属的快乐了吧！支持 VS Code、Cursor、Antigravity、Trae CN 等主流编辑器。

---
## 功能

- **持仓管理** — 持仓 TreeView 面板，添加/编辑/删除股票和基金持仓，实时计算盈亏
- **状态栏盈亏** — 底部状态栏实时显示总盈亏（赚钱绿色/亏钱红色），鼠标悬浮查看明细（总成本/总市值/逐条盈亏）
- **自选股面板** — 侧边栏 TreeView，实时显示自选股价格和涨跌幅，可选显示成交量/成交额/换手率/振幅。支持**置顶**、**上下移动**、**按涨幅/跌幅/名称/现价自动排序**
- **分组自选股** — 独立于普通自选股，可按自己的需要创建多个分组、重命名或删除分组，并向每个分组添加不同股票；原自选股右键即可直接加入指定分组
- **自选基金面板** — 场外基金显示实时估值，场内 ETF 使用交易所实时价格和当日涨跌幅；点击可查看走势。支持**置顶**、**上下移动**、**按涨幅/跌幅/名称/净值自动排序**
- **市场概览** — 四大分类：A股指数 / 全球指数 / 中概股 / 美股龙头，可选显示主力资金流向等；中概股和美股龙头支持自由添加、移除股票
- **A股大盘云图** — 覆盖约 5500 只股票，按「一级行业 → 二级行业 → 个股」三级结构展示；支持沪深、科创板、创业板和北交所筛选，方块面积表示总市值、颜色表示涨跌幅
- **行业行情弹框** — 悬浮云图行业标题即可查看行业涨跌分布、涨停/跌停数量和成分股实时行情；双击个股可打开详情
- **股票详情** — K 线图（日K + 分时）+ MA5/10/20/60 + 十字光标 + 滚动缩放，支持美股行情。详情页顶部 **Action Bar** 一键添加状态栏 / 添加持仓
- **基金详情** — 净值走势图（单位净值 + 累计净值 + 日涨跌柱状图），近一年统计指标。详情页顶部 **Action Bar** 一键添加状态栏 / 添加持仓
- **状态栏行情** — 底部实时显示自选指数/股票价格，可选显示成交量/成交额/换手率/振幅
- **设置面板** — 支持直接显示/隐藏大盘云图、自选基金、自选股、分组自选股、市场概览和持仓管理栏，并提供各类配置的快捷入口


![展示页面](https://raw.githubusercontent.com/zswlp/-/refs/heads/main/444.png#pic_center)
![设置页面](https://raw.githubusercontent.com/zswlp/-/refs/heads/main/ScreenShot_2026-07-01_165331_272.png#pic_center)


## 使用方法

1. 点击侧边栏「股票看盘」图标
2. 在自选股面板点击 `+` 添加股票代码（支持 6 位数字自动识别沪深市场）
3. 在「分组自选股」标题栏点击新建分组按钮，按需要创建长期持有、短线观察等分组
4. 在原自选股中右键股票，选择「加入分组自选股」，再选择目标分组；股票会保留在原自选股中
5. 在自选基金面板点击 `+` 添加基金代码（6 位数字）
6. 点击股票/基金查看详情 K 线 / 净值走势图
7. 在持仓面板点击 `+` 添加持仓，输入成本价和数量，状态栏自动显示盈亏
8. 通过命令面板 (`Ctrl+Shift+P`) 搜索「搜索股票」
9. 右键自选股/基金可快速添加持仓、置顶/取消置顶、上下移动调整顺序
10. 点击自选股/基金面板标题栏排序图标，可切换排序方式（默认/涨幅/跌幅/名称/价格/净值）
11. 在设置栏展开「栏目显示 / 隐藏」，点击栏目即可切换显示状态
12. 展开侧栏中的「大盘云图」并点击打开，可切换全市场、沪市、深市、科创板、创业板和北交所；悬浮行业标题查看行业行情，双击个股查看详情
13. 在详情页顶部 Action Bar，可一键添加股票/基金到状态栏或持仓

## 配置

| 配置项                                   | 默认值                                                         | 说明                                                                                                |
| ---------------------------------------- | -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `hgleek.watchlist`                       | `["sz000001", "sz000651", "sh600519", "sz000858", "sz300750"]` | 自选股代码列表（需带市场前缀：sz/sh）                                                               |
| `hgleek.groupedWatchlists`               | `[]`                                                           | 分组自选股数据；建议通过「分组自选股」栏的新建、添加和右键菜单管理                                  |
| `hgleek.watchlistPinned`                 | `[]`                                                           | 自选股置顶列表（置顶的股票始终显示在最前面）                                                        |
| `hgleek.watchlistSortMode`               | `"default"`                                                    | 自选股排序方式：`default` 默认 / `changePercent` 涨幅 / `decline` 跌幅 / `name` 名称 / `price` 现价 |
| `hgleek.watchlist.showVolume`            | `false`                                                        | 自选股显示成交量                                                                                    |
| `hgleek.watchlist.showAmount`            | `false`                                                        | 自选股显示成交额                                                                                    |
| `hgleek.watchlist.showTurnoverRate`      | `false`                                                        | 自选股显示换手率                                                                                    |
| `hgleek.watchlist.showAmplitude`         | `false`                                                        | 自选股显示振幅                                                                                      |
| `hgleek.fundWatchlist`                   | `["000001", "110011"]`                                         | 自选基金代码列表（纯数字）                                                                          |
| `hgleek.fundWatchlistPinned`             | `[]`                                                           | 自选基金置顶列表（置顶的基金始终显示在最前面）                                                      |
| `hgleek.fundWatchlistSortMode`           | `"default"`                                                    | 自选基金排序方式：`default` 默认 / `changePercent` 涨幅 / `decline` 跌幅 / `name` 名称 / `nav` 净值 |
| `hgleek.refreshInterval`                 | `5`                                                            | 行情刷新间隔（秒，1-60）                                                                            |
| `hgleek.statusBar.codes`                 | `["sh000001"]`                                                 | 状态栏显示股票代码列表                                                                              |
| `hgleek.statusBar.showVolume`            | `false`                                                        | 状态栏显示成交量                                                                                    |
| `hgleek.statusBar.showAmount`            | `false`                                                        | 状态栏显示成交额                                                                                    |
| `hgleek.statusBar.showTurnoverRate`      | `false`                                                        | 状态栏显示换手率                                                                                    |
| `hgleek.statusBar.showAmplitude`         | `false`                                                        | 状态栏显示振幅                                                                                      |
| `hgleek.statusBar.upColor`               | `#ffffff`                                                      | 涨的颜色                                                                                            |
| `hgleek.statusBar.downColor`             | `#2ecc71`                                                      | 跌的颜色                                                                                            |
| `hgleek.statusBar.flatColor`             | `#ffffff`                                                      | 平盘颜色                                                                                            |
| `hgleek.statusBar.fontSize`              | `12`                                                           | 状态栏字体大小（10-18）                                                                             |
| `hgleek.marketOverview.showTurnoverRate` | `true`                                                         | 市场概览显示换手率                                                                                  |
| `hgleek.marketOverview.showVolume`       | `false`                                                        | 市场概览显示成交量                                                                                  |
| `hgleek.marketOverview.showAmount`       | `false`                                                        | 市场概览显示成交额                                                                                  |
| `hgleek.marketOverview.showMainNetFlow`  | `false`                                                        | 市场概览显示主力净流入                                                                              |
| `hgleek.marketOverview.showAmplitude`    | `false`                                                        | 市场概览显示振幅                                                                                    |
| `hgleek.views.marketMap`                 | `true`                                                         | 显示独立的大盘云图栏                                                                                |
| `hgleek.views.fundWatchlist`             | `true`                                                         | 显示自选基金栏                                                                                      |
| `hgleek.views.watchlist`                 | `true`                                                         | 显示自选股栏                                                                                        |
| `hgleek.views.groupedWatchlist`          | `true`                                                         | 显示分组自选股栏                                                                                    |
| `hgleek.views.marketOverview`            | `true`                                                         | 显示市场概览栏                                                                                      |
| `hgleek.views.position`                  | `true`                                                         | 显示持仓管理栏                                                                                      |

## 数据源

数据来源于东方财富、腾讯、天天基金等公开接口。

## 打赏作者 (^\_^)

赢钱了记得打赏作者～

| 微信                                                                                                          | 支付宝                                                                                                          |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| ![微信收款码](https://raw.githubusercontent.com/zswlp/-/refs/heads/main/c21d300ae733abbc92b8820b97935cce.jpg) | ![支付宝收款码](https://raw.githubusercontent.com/zswlp/-/refs/heads/main/7a7fa884c8d07b16d8a4c06840e4252b.jpg) |

## 免责声明

1. **非投资建议**：本插件仅为行情数据展示工具，所有信息仅供学习参考，不构成任何投资建议、荐股或交易指导。投资有风险，入市需谨慎。
2. **数据准确性**：行情数据来源于东方财富、腾讯、天天基金等公开接口，插件不对数据的实时性、准确性、完整性作任何保证，数据可能存在延迟或误差。
3. **盈亏自负**：使用者基于本插件数据作出的任何投资决策，由使用者自行承担全部风险与责任，开发者不承担由此产生的任何损失。
4. **合规声明**：本插件不提供任何形式的荐股、代客理财或投资咨询等服务，不涉及内幕信息，不引导用户进行任何特定投资操作。
5. **仅供看盘，无任何不良引导。**
