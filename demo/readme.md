# 程序说明
该程序通过多线程方式读取交换机列表文件和命令列表文件，对多个交换机进行`命令列表文件`中制定的命令。
运行结果按设备IP独立保存为日志文件。

# 文件说明
config: 脚本程序的配置，可对可配置项进行自定义设置(手动指定读取文件名称，多线程线程数量)
sw_list: 交换机列表文件，格式为：`交换机IP地址   用户名  密码`，如有多台设备，填写多行记录
cmd_list: 配置命令列表文件，将所有在交换机执行的命令保存在该文件中，脚本将逐一执行各命令。
LogFile.py: 日志保存程序，以IP为文件名，分别保存命令执行日志至独立文件。
ssh_client.py: 终端SSH连接操作的主要函数文件
ssh_control.py: 主程序文件，解析配置、读取文件、多线程控制执行等。
ssh_lib.py: netlib源码文件，仅供参考

# 运行结果
程序结果保存为日志文件：192.168.1.1和192.168.1.2
