# MAC配置maven

1. 首先去官网http://maven.apache.org/download.html下载最新的maven，解压到你想放位置

2. 获取JAVA_HOME地址：在终端中输入

   `/usr/libexec/java_home -V`

3. 建议另外打开一个终端，输入：

   `vi ~/.bash_profile`

   进入vim界面，输入“`i`”进入编辑界面，在其中添加如下：

   ```
   MAVEN_HOME=/Users/***/maven-3.5.3 //自定义地址
   PATH=$MAVEN_HOME/bin:$PATH
   export MAVEN_HOME
   exoprt PATH
   export JAVA_HOME=Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home
   ```

   按下“`esc`”键，输入`wq!`保存输入的配置内容。

4. 在终端输入`source ~/.bash_profile`

5. 检验maven是否装好了，在终端输入`mvn -v`，如果出现maven版本信息，代表我们安装成功。

   ​