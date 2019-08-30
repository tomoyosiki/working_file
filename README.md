# working_file
配置解决git bash中文乱码问题

原因 
	在默认设置下，中文文件名在工作区状态输出，中文名不能正确显示，而是显示为八进制的字符编码。

解决办法 
	将git 配置文件 core.quotepath项设置为false。 
	quotepath表示引用路径 
	加上--global表示全局配置

git config --global core.quotepath false

要注意的是，这样设置后，你的git bash终端也要设置成中文和utf-8编码。才能正确显示中文，例如对比如下：

在git bash的界面中右击空白处，弹出菜单，选择选项->文本->本地Locale，设置为zh_CN，而旁边的字符集选框选为UTF-8。

英文显示则是： 
Options->Text->Locale改为zh_CN，Character set改为UTF-8