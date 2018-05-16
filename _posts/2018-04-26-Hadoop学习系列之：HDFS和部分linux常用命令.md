# HDFS和部分linux常用命令

1. `source /opt/client/env` 启动环境配置

2. `hdfs dfs -ls /` 文件目录列表显示， `/`表示根目录

3. `vi 123.txt` 在本文件夹创建`123.txt`文件，vim指令，按`i`	进入编程模式，按`esc`进入命令模式，`:wq`保存退出

4. `hdfs dfs -put 123.txt /tmp`，linux本地`123.txt`文件上传到hdfs文件夹中

   > `hdfs dfs`是固定格式，`hdfs`指执行hdfs文件系统精灵，`dfs`指执行dfs命令
   >
   > linux是服务器，hdfs是在n个服务器上构建的文件系统

5. `hdfs dfs -cat /tmp/123.txt` 在终端显示文件内容

6. `hdfs dfs -get /tmp/123.txt /home/` 下载hdfs中文件到本地

7. `hdfs dfs -mkdir /tmp/zr` 在hdfs上创建文件夹

8. `hdfs dfs -rm -r /tmp/zr` 在hdfs上删除目录，注意linux系统自带文件不可删除

9. `hdfs dfs -mv /tmp/123.txt /tmp/456.txt` hdfs文件重命名

10. `hdfs dfs -moveFromLocal 123.txt /tmp/` 从本地移动文件，移动文件后本地文件消失，但是上传文件操作后本地文件仍然存在。

11. 推荐链接：https://blog.csdn.net/zhaojw_420/article/details/53161624

