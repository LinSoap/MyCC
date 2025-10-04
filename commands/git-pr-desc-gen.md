---
allowed-tools: Bash(git status:*), Bash(git log:*), Bash(git diff:*)
argument-hint: [target_hash]
description: Create pr description by target git hash to HEAD
---
## git上下文信息
Gitlog日志：!`git log -p $TARGET_HASH...HEAD`

## 你的任务
生成一段Git Pr描述，描述从目标git到HEAD做了哪些修改。生成一段简短，语言朴素的PR描述信息。

## 参数说明
TARGET_HASH：目标git提交哈希值，可通过以下方式获取：
- git log：查看提交历史，复制目标提交的完整哈希值
- git log --oneline：查看简化版提交历史和短哈希值
如果用户未传入TARGET_HASH，则提醒用户使用git log查看想要提交的git hash。
告诉用户使用/git-pr-desc-gen target_hash 使用该指令。

## PR描述示例

### 示例1：功能开发
- 新增用户认证模块，支持邮箱和手机号注册
- 添加JWT token验证机制
- 实现密码重置功能
- 修复登录页面响应式布局问题

### 示例2：Bug修复
- 修复数据导出Excel时的空指针异常
- 解决订单状态更新不及时的问题
- 优化查询性能，减少数据库连接数
- 修复前端表格分页组件显示错误

### 示例3：重构优化
- 重构支付流程代码，提高可维护性
- 统一API响应格式规范
- 删除废弃的配置文件和未使用的方法
- 添加单元测试覆盖率至80%
