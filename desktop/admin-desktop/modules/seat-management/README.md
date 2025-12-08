# SeatManagement 座位管理模块

## 功能描述
管理员座位管理页面，用于查看和管理所有座位的状态、预约情况。

## 对应 Axure 原型
- `桌面管理员端-座位管理.html`

## 页面列表
| 页面 | 文件 | 说明 |
|-----|------|-----|
| 座位列表 | pages/seat-list.html | 座位网格视图 |
| 座位详情 | pages/seat-detail.html | 单个座位详情（可选） |

## 依赖组件
- `/core/components/sidebar` - 侧边栏
- `/core/components/navbar` - 顶部导航
- `/core/components/filter-dropdown` - 筛选下拉框
- `/core/components/modal` - 弹窗（编辑座位）
- `/core/components/button` - 按钮

## 模块私有组件
| 组件 | 路径 | 说明 |
|-----|------|-----|
| SeatGrid | components/seat-grid/ | 座位网格布局 |
| SeatCard | components/seat-card/ | 单个座位卡片 |

## 页面功能

### 筛选区域
- 楼层选择（下拉框）
- 日期选择（日期选择器）
- 搜索座位号

### 座位网格
以网格形式展示所有座位，每个座位显示：
- 座位编号
- 当前状态（空闲/已预约/使用中/维护中）
- 预约人信息（如有）

### 座位状态
| 状态 | 颜色 | 说明 |
|-----|------|-----|
| available | 绿色 | 空闲可预约 |
| reserved | 蓝色 | 已被预约 |
| occupied | 橙色 | 使用中 |
| maintenance | 灰色 | 维护中 |

## 数据结构
```json
{
  "floor": "1",
  "date": "2025-11-29",
  "seats": [
    {
      "id": "A-01",
      "status": "available",
      "reservation": null
    },
    {
      "id": "A-02",
      "status": "reserved",
      "reservation": {
        "user": "张三",
        "time": "09:00-12:00"
      }
    }
  ]
}
```

## 交互说明
1. 点击座位 → 打开座位详情弹窗
2. 在弹窗中可以：
   - 查看预约详情
   - 取消预约
   - 设置座位状态（维护中）
3. 切换楼层/日期 → 刷新座位数据

## AI 生成提示
```
请为 seat-management 模块生成 seat-list.html 页面：
1. 使用 /core/layouts/admin-layout 布局
2. 顶部包含楼层和日期筛选
3. 主体区域展示座位网格（5列布局）
4. 每个座位卡片显示编号和状态
5. 点击座位弹出详情弹窗
```
