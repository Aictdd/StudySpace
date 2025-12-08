# Settings 设置模块

## 功能描述
管理员设置页面，用于配置系统参数、预约规则、权限等。

## 对应 Axure 原型
- `桌面管理员端-设置.html`

## 页面列表
| 页面 | 文件 | 说明 |
|-----|------|-----|
| 设置首页 | pages/index.html | 设置入口页 |
| 预约设置 | pages/reservation.html | 预约规则配置 |
| 权限设置 | pages/permissions.html | 权限管理（可选） |

## 依赖组件
- `/core/components/sidebar` - 侧边栏
- `/core/components/navbar` - 顶部导航
- `/core/components/form-controls` - 表单控件
- `/core/components/filter-dropdown` - 下拉选择
- `/core/components/button` - 按钮
- `/core/components/modal` - 弹窗

## 页面功能

### 管理员信息卡片
- 显示当前管理员信息
- 点击可跳转修改个人信息

### 设置菜单
| 菜单项 | 说明 |
|-------|------|
| 预约设置 | 配置预约规则 |
| 权限设置 | 管理用户权限 |
| 二级设置菜单跳转-1 | 其他设置项 |
| 二级设置菜单跳转-2 | 其他设置项 |
| 二级设置菜单跳转-3 | 其他设置项 |

### 预约设置区域
| 设置项 | 类型 | 默认值 | 说明 |
|-------|------|-------|-----|
| 单次预约最长时间 | 下拉选择 | 3小时 | 单次预约的最大时长 |
| 每日最多预约次数 | 下拉选择 | 2次 | 每人每天最多预约次数 |
| 允许提前取消的时间 | 下拉选择 | 30分钟 | 预约开始前多久可取消 |

## 数据结构
```json
{
  "admin": {
    "id": 1,
    "name": "管理员",
    "avatar": "/assets/images/avatar.png",
    "role": "super_admin"
  },
  "reservationSettings": {
    "maxDuration": 180,
    "maxDailyReservations": 2,
    "cancelBeforeMinutes": 30
  },
  "menuItems": [
    { "id": "reservation", "label": "预约设置", "icon": "calendar" },
    { "id": "permissions", "label": "权限设置", "icon": "lock" }
  ]
}
```

## 交互说明
1. 修改设置项 → 点击"保存规则"按钮
2. 保存成功 → 显示成功提示
3. 点击菜单项 → 跳转到对应设置页面

## AI 生成提示
```
请为 settings 模块生成 index.html 页面：
1. 使用 /core/layouts/admin-layout 布局
2. 左侧显示管理员信息卡片和设置菜单
3. 右侧显示预约设置表单
4. 表单包含 3 个下拉选择项
5. 底部有"保存规则"按钮
```
