## 文章概述  
本文介绍一种简单高效的京东Cookie抓取方法，使用Alook浏览器即可快速获取所需的pt_key和pt_pin值，无需复杂的技术操作。这种方法特别适合京东自动化脚本用户配置使用。

---

## 🚀 抓取步骤

### 准备工作
- 在应用商店下载安装Alook浏览器（iOS/Android均可）
- 确保已注册京东账号并记住登录密码

### 详细操作流程

1. **打开Alook浏览器**，访问京东签到页面：
   ```
   https://bean.m.jd.com/bean/signIndex.action
   ```

2. **登录京东账号**：
   - 输入手机号和密码完成登录
   - 如果已登录，请先退出重新登录以确保获取最新Cookie

3. **打开工具箱**：
   - 点击浏览器下方三条横线菜单图标
   - 滑动到第二页，找到并点击「工具箱」选项
   ![工具箱位置]
![IMG_20250903_213413.jpg](https://github.com/user-attachments/assets/e9df1609-2c5c-4fae-95f5-d63e961c4d88)


4. **使用开发者工具**：
   - 在工具箱中找到并点击「开发者工具」选项
   - 在弹出的界面中即可找到完整的Cookie信息
   ![开发者工具]
![IMG_20250903_213500.jpg](https://github.com/user-attachments/assets/afe017ca-a7cd-4d18-aece-3edbd6474365)



5. **复制Cookie值**：
   - 在Cookie列表中查找`pt_key`和`pt_pin`的值
   - 将它们组合成以下格式：
     ```
     pt_key=AAJjzFLLADC...; pt_pin=jd_123456;
     ```

---

## 📝 配置脚本

### 单账号配置
将获取的Cookie值填入jdCookie.js文件中：

```javascript
let CookieJDs = [
  'pt_key=AAJjzFLLADC...; pt_pin=jd_123456;', // 替换为您的实际Cookie
]
```

### 多账号配置
```javascript
let CookieJDs = [
  'pt_key=AAJjzFLLADC...; pt_pin=jd_123456;',
  'pt_key=BBKjzFLLADC...; pt_pin=jd_789012;',
  // 可继续添加更多账号
]
```

---

## ⚠️ 注意事项

1. **安全提醒**：
   - Cookie相当于账户密码，请妥善保管不要泄露

2. **Cookie有效期**：
   - 京东Cookie通常有1-3个月的有效期
   - 修改密码或退出登录会使Cookie立即失效
   - 建议定期检查并更新Cookie

3. **常见问题**：
   - 如果脚本无法正常运行，首先检查Cookie格式是否正确
   - 确保Cookie中没有多余的空格或特殊字符
   - 如遇问题，可重新按照教程获取新Cookie

---




## 🔗 相关链接
- [Alook浏览器官网](https://alookweb.com/)
- [京东脚本一键拉库教程](post/bao-ta-mian-ban-da-jian-jiao-cheng-%F0%9F%9A%80.html)
- [青龙面板使用指南](https://github.com/whyour/qinglong)

---

📝 **标签**：`京东脚本` `Cookie抓取` `Alook浏览器` `教程`  
👨‍💻 **作者**：小灰  
📅 **发布日期**：2025年9月3日  

---

