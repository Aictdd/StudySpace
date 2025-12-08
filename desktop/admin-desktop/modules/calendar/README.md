# Calendar 日历模块

## 功能描述
管理员日历视图，展示预约安排和重要事件。

## 页面列表
| 页面 | 文件 | 说明 |
|-----|------|-----|
| 日历视图 | pages/index.html | 日历主页 |

## 依赖组件
- `/core/components/sidebar` - 侧边栏
- `/core/components/navbar` - 顶部导航
- `/core/components/filter-dropdown` - 月份/视图切换
- `/core/components/modal` - 事件详情弹窗

## 模块私有组件
| 组件 | 路径 | 说明 |
|-----|------|-----|
| CalendarGrid | components/calendar-grid/ | 日历网格 |
| EventCard | components/event-card/ | 事件卡片 |

## 数据结构
```json
{
  "currentMonth": "2025-11",
  "events": [
    {
      "id": 1,
      "date": "2025-11-29",
      "title": "座位维护",
      "type": "maintenance",
      "time": "09:00-12:00"
    }
  ]
}
```

## AI 生成提示
```
请为 calendar 模块生成 index.html 页面：
1. 使用 /core/layouts/admin-layout 布局
2. 顶部有月份切换和视图切换（月/周/日）
3. 主体展示日历网格
4. 日期格子内显示当日事件
```
