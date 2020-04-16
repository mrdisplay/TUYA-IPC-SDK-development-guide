# 区域报警功能开发   
# 准备工作：  
* 在iot对应的pid中增加以下dp点：![image-20200416154518565](area.assets/image-20200416154518565.png)  

# 区域报警功能开发流程  
* 说明：app上设定一个区域，限定该区域才可以触发移动侦测，dp点是168和169  

* 开发流程：  
  1、app打开区域告警开关，设定区域，数据格式如下：x表示选择区域的横坐标，y表示选择区域的纵坐标，xlen表示选择区域的长，ylen表示选择区域的宽，需要注意的是string类型数据组合的时候双引号前加三个反斜杠。  
  ![image-20200416155538938](area.assets/image-20200416155538938.png)  

  2、关闭区域告警  

  ![image-20200416155633339](area.assets/image-20200416155633339.png)  