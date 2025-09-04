文章概述

本文介绍一种简单高效的京东Cookie抓取方法，使用Alook浏览器即可快速获取所需的pt_key和pt_pin值，无需复杂的技术操作。这种方法特别适合京东自动化脚本用户配置使用。

🚀 抓取步骤

准备工作

在应用商店下载安装Alook浏览器（iOS/Android均可）

确保已注册京东账号并记住登录密码

详细操作流程

打开Alook浏览器，访问京东签到页面：

https://bean.m.jd.com/bean/signIndex.action 

登录京东账号：

输入手机号和密码完成登录

如果已登录，请先退出重新登录以确保获取最新Cookie

打开工具箱：

点击浏览器下方三条横线菜单图标

滑动到第二页，找到并点击「工具箱」选项
![工具箱位置]
![IMG_20250903_213413.jpg](https://github.com/user-attachments/assets/062e76fe-2bfd-479e-bc2c-119e0a7b7527)



使用开发者工具：

在工具箱中找到并点击「开发者工具」选项

在弹出的界面中即可找到完整的Cookie信息
![开发者工具]
![IMG_20250903_213500.jpg](https://github.com/user-attachments/assets/8e2f07a0-5c4b-46e4-a821-76fe30fddd2c)



复制Cookie值：

在Cookie列表中查找pt_key和pt_pin的值

将它们组合成以下格式：

pt_key=AAJjzFLLADC...; pt_pin=jd_123456; 

📝 配置脚本

单账号配置

将获取的Cookie值填入jdCookie.js文件中：

let CookieJDs = [ 'pt_key=AAJjzFLLADC...; pt_pin=jd_123456;', // 替换为您的实际Cookie ]

多账号配置

let CookieJDs = [ 'pt_key=AAJjzFLLADC...; pt_pin=jd_123456;', 'pt_key=BBKjzFLLADC...; pt_pin=jd_789012;', // 可继续添加更多账号 ]

⚠️ 注意事项

安全提醒：

Cookie相当于账户密码，请妥善保管不要泄露

Cookie有效期：

京东Cookie通常有1-3个月的有效期

修改密码或退出登录会使Cookie立即失效

建议定期检查并更新Cookie

常见问题：

如果脚本无法正常运行，首先检查Cookie格式是否正确

确保Cookie中没有多余的空格或特殊字符

如遇问题，可重新按照教程获取新Cookie

🔗 相关链接

Alook浏览器官网

京东脚本一键拉库教程

青龙面板使用指南

📝 标签：京东脚本 Cookie抓取 Alook浏览器 教程
👨‍💻 作者：小灰
📅 发布日期：2025年9月4日

