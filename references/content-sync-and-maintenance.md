# Content Sync & Maintenance

## Style-only request

如果用户只要求“改成 Warm 风格”：

- 数据不变
- 账号不变
- 金额不变
- 卡号不变
- 密码不变
- 功能不变

除非用户明确要求删除或同步。

## Latest-content priority

要求“按最新标准同步”时：

1. 当前对话最新明确确认
2. 最新完成独立页
3. 最新上传文件
4. 聚合页旧副本
5. 历史文件

## Maintenance

应该：
- 变量集中
- 一套最终 CSS
- 合并重复 media query
- 删除旧 patch
- 清楚注释
- 保留数据

不要：
- v1/v2/v3/v4 CSS 叠补丁
- `!important` 泛滥
- 修手机端时破坏桌面
- 无必要引入框架
- 依赖外部资源才能看到风格
