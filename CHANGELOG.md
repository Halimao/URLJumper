# 更新日志

## [2.0.0] - 2026-01-18

### 新增功能

1. **自定义重定向延迟时间**
   - 添加了 `wait` URL参数来控制自动跳转的等待时长
   - 参数值为毫秒（ms），例如：`?jump=https://example.com&wait=5000` 表示等待5秒
   - 如果未指定 `wait` 参数，系统使用默认值 3000ms
   - 仅接受正整数，无效的值会被忽略并使用默认值

2. **网站图标（Favicon）**
   - 添加了精美的SVG格式favicon图标
   - 图标展示链接符号，与网站的重定向功能相吻合
   - 使用蓝色主题色（#3B82F6），与网站设计风格保持一致

### 使用示例

#### 默认延迟（3秒）
```
https://yourdomain.com/?jump=https://example.com
```

#### 自定义延迟（5秒）
```
https://yourdomain.com/?jump=https://example.com&wait=5000
```

#### 自定义延迟（10秒）
```
https://yourdomain.com/?jump=https://example.com&wait=10000
```

### 技术细节

- `wait` 参数通过 URL 查询字符串传递
- 值必须是正整数（单位：毫秒）
- 倒计时显示以秒为单位，自动向上取整
- favicon 使用 Data URI 格式，无需额外文件存储
