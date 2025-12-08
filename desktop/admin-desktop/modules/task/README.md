# Task 任务模块

## 功能描述
管理员任务管理页面，用于查看和管理待办任务。

## 页面列表
| 页面 | 文件 | 说明 |
|-----|------|-----|
| 任务列表 | pages/index.html | 任务管理主页 |

## 依赖组件
- `/core/components/sidebar` - 侧边栏
- `/core/components/navbar` - 顶部导航
- `/core/components/table` - 任务列表
- `/core/components/button` - 操作按钮
- `/core/components/modal` - 任务详情弹窗

## 数据结构
```json
{
  "tasks": [
    {
      "id": 1,
      "title": "处理违约用户",
      "status": "pending",
      "priority": "high",
      "dueDate": "2025-11-30",
      "assignee": "管理员"
    }
  ]
}
```

## AI 生成提示
```
请为 task 模块生成 index.html 页面：
1. 使用 /core/layouts/admin-layout 布局
2. 展示任务列表（使用 table 组件）
3. 支持任务状态筛选
4. 可添加/编辑/完成任务
```
