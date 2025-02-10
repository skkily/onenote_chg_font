# onenote_chg_font
OneNote for mac 解决Calibri英文字体自动切换,排版难看问题

# 原理

将 Calibri英文字体 替换为 微软雅黑字体, 此时即使发生了自动切换, 依旧不会导致排版混乱

不过其他设备同步笔记后, 字体将依旧是错误的, 此时可以用格式刷再统一修改英文字体格式.

# 使用方法

* 执行 `wget -qO- https://raw.githubusercontent.com/skkily/onenote_chg_font/refs/heads/main/onenote_chg_font.sh | sudo bash`, 最后一句打印 change ok 即成功执行

* 完全退出 onenote 再打开即可.

# 恢复方法

* 执行 `wget -qO- https://raw.githubusercontent.com/skkily/onenote_chg_font/refs/heads/main/onenote_chg_font.sh | sudo bash -s -- restore`, 最后一句打印 restore ok 即成功执行

* 完全退出 onenote 再打开即可.

参照博客: https://blog.csdn.net/baidu_39347626/article/details/125830894
