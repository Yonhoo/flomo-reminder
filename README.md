# Flomo Reminder

基于 `github actions` 的定时推送 memo 服务，灵感来自 flomo `每日提醒` 功能。

![](https://i.328888.xyz/2023/04/19/i6vXeH.png)

## 功能

- 在每天 `9:00`、`12:00`、`18:00` 进行推送
- 推送支持 `Bark`
- 支持自定义要推送的 memo 标签

## 用法

1. **fork** 此仓库。
2. 在**自己的仓库**里，定位到 `Settings` -> `Security` -> `Secrets and variables` -> `Actions`

![](https://p.ipic.vip/oygvav.png)

3. 在 `Secrets` 这一栏中，点击右边的按钮 `New repository secret`，添加如下参数

| 参数                | 说明                                                                                   | 示例                        | 必填 |
| ------------------- | -------------------------------------------------------------------------------------- | --------------------------- | ---- |
| FLOMO_AUTHORIZATION | 在 Web 端登录 flomo，打开开发者工具，在随便一个接口请求里复制 authorization 头的值即可 | Bearer 12345678 ｜ xxxxxxxx | ✅   |
| BARK_TOKEN          | Bark 的 推送 token                                                                     | aBcDefg1234HijkLmn          | ✅   |

4. 在 `Variables` 栏中，点击按钮 `New repository variable`，添加如下参数

| 参数      | 说明                                                                                    | 示例                         | 必填 |
| --------- | --------------------------------------------------------------------------------------- | ---------------------------- | ---- |
| PUSH_TAGS | 要推送的 tags，用**英文逗号**分隔。如果设置了「读书」，会推送「读书」标签下所有的子标签 | 学习/前端/知识体系,读书,名言 |      |

## 更新

定期拉取此仓库代码即可。

## 反馈

请直接提 `issue`，谢谢！

## 感谢

flomo
