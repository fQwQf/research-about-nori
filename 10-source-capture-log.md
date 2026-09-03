# 公开来源采集记录

采集时间：2026-09-01（中国标准时间）；采集者：fQwQf。

## Bilibili API

通过公开接口 `https://api.bilibili.com/x/web-interface/view?bvid=...` 读取页面元数据，未登录。时间戳按 Unix 秒转换为中国标准时间。

### 官方主宣发片

- URL：[BV1h8uq6SECj](https://www.bilibili.com/video/BV1h8uq6SECj/)
- 作者：白夜 Tira（Bilibili mid `3234445`）
- 标题：`她明明是AI，但我想拯救她。独立游戏《I_NORI》【B站AI创造公开赛】`
- `pubdate` / `ctime`：`1786433812` → **2026-08-11 15:36:52 CST**
- 简介明确列出：Steam `app/4996280/I_NORI`；ARG 入口 `os.inori.ai/landing`；作品含 AI 伴侣、叙事探索和平行世界冒险；主催/程序/AI 为白夜 Tira。
- 采集时快照：约 1,073,837 播放、79,769 点赞、60,342 收藏、2,467 评论、4,943 分享。

这些字段支持“8 月 11 日 15:36 是最早可确认的公开宣发/入口证据”。

### 早期玩家传播样本

| BVID | 作者 | 发布时间（CST） | 页面标题/用途 |
|---|---|---|---|
| [BV1yLgL6CEsq](https://www.bilibili.com/video/BV1yLgL6CEsq/) | 盐巴P | 2026-08-13 02:33:26 | 先行版 ARG 全流程存档；简介有 8 月 13 日更新、原作与入口链接 |
| [BV1GXgH6CEnF](https://www.bilibili.com/video/BV1GXgH6CEnF/) | 秦心桜 | 2026-08-13 20:15:00 | 全流程攻略/实况；简介称无提示约 6 小时并列 QQ 群 |
| [BV1xHbU6WEff](https://www.bilibili.com/video/BV1xHbU6WEff/) | 萨立亚 | 2026-08-16 03:53:33 | 算力超限攻略/彩蛋入口 |
| [BV1Bfbm6uEwT](https://www.bilibili.com/video/BV1Bfbm6uEwT/) | 萨立亚 | 2026-08-16 04:57:15 | Doodle 词条/彩蛋 |
| [BV1zobm66E3A](https://www.bilibili.com/video/BV1zobm66E3A/) | 萨立亚 | 2026-08-16 05:00:52 | 彩蛋邮件/觉醒者叙事 |
| [BV1gbbe6pEJP](https://www.bilibili.com/video/BV1gbbe6pEJP/) | 一顿吃几顿 | 2026-08-17 18:30:55 | 先导全流程速通，简介记录当时 39:20 世界记录 |
| [BV1F68V6EErG](https://www.bilibili.com/video/BV1F68V6EErG/) | 孤独音符 | 2026-08-19 12:00:00 | 网页解谜全流程精剪实况 |
| [BV1T3886GEaR](https://www.bilibili.com/video/BV1T3886GEaR/) | 饭饭爱吃炒饭QAQ | 2026-08-24 02:18:50 | 群史/愿望单过 5000 庆祝特辑，简介列 QQ 群 |
| [BV1qth36rEsB](https://www.bilibili.com/video/BV1qth36rEsB/) | 被丢弃在路边的麦当劳 | 2026-08-25 10:45:28 | 标题为“8月31号nori再见”，可作为关停消息传播的玩家材料 |
| [BV1nghj6bEMt](https://www.bilibili.com/video/BV1nghj6bEMt/) | 热可可Leo | 2026-08-26 02:10:06 | 直播回放，标题标明 8 月 23 日晚间直播 |
| [BV1m8tN6NE4e](https://www.bilibili.com/video/BV1m8tN6NE4e/) | 饭饭爱吃炒饭QAQ | 2026-08-28 21:03:30 | 关服纪念/期待正式版 |
| [BV1WStn6qEzC](https://www.bilibili.com/video/BV1WStn6qEzC/) | 此身忆在真无改 | 2026-08-30 22:33:57 | 二通全流程录屏；简介称得知网页先导版月底关闭 |

注意：第三方上传时间是“内容公开时间”，不等于作者首次游玩时间。上传者可以延迟发布、补档或修改简介。

## 官方网站与基础设施

- `https://inori.ai/` 在 2026-09-01 22:30 CST 左右返回 HTTP 301，`Location: https://x.com/inori_hub`。开发者已确认该 X 账号为官方入口（见 13）；账号历史发布时间线仍待采集。
- `https://os.inori.ai/` 在 2026-09-01 15:51 CST 左右返回 NoriOS HTML，响应中的 `/api/entry-status` 返回 `{"status":"ok","machineId":"..."}`。在社群转述的 16:00 节点前后继续轮询：15:57:50、15:59:58、16:00:20、16:01:46 均为 HTTP 200 / `status: ok`；16:02:25 根页和 `/landing` 也为 HTTP 200。该记录支持“截至 16:02 尚未观察到入口关停”，不证明剧情内的休眠状态或后续可用性。
- [`crt.sh` 查询结果](https://crt.sh/?q=os.inori.ai)显示 `os.inori.ai` 于 2026-08-09 08:23:17 CST 获得以该主机名签发的 Let's Encrypt 证书。
- 客户端公开静态资源和脚本包含 `Memory`、`Datasea`、`Farewell`、棋类/你画我猜/Codenames/Cake Duel、聊天及媒体 WebSocket 等标识；这些支持功能存在性走查，不足以证明后端模型、记忆保存政策或运营时间表。

## 引用规则

论文正文中使用“截至 2026-09-01 核查”“公开页面显示”等限定语。对社群转述和玩家视频简介，先作为线索；只有经过原始公告、作者确认或多源交叉验证后，才升级为时间线事实。所有平台指标注明采集日期。
