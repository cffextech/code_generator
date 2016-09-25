# code_generator
<!--TODO 持续更新中-->
## 需求分析：   
1. 多种模型表现方式；
2. 多种模板；
3. 命令行接口；
4. 参数设置：模型文件（文件夹），模板文件（文件夹）, 输出文件（文件夹）
5. 前提
（1）pdm产生的json格式是固定的，是规定好的；
（2）用户可以自定义自己的模型和模板，编写特定的json文件和tpl文件；
6. 测试用例，依据模型不同，总共8组测试用例；
<table>
<tr>
    <th>模型(pdm或者json)</th> 
    <th>模板</th>
    <th>输出</th>
</tr>
<tr>
<td>file1</td>
<td>file2</td>
<td>file3</td>
</tr>
<tr>
<td>file1</td>
<td>directory1</td>
<td>directory3</td>
</tr>
<tr>
<td>directory1</td>
<td>file2</td>
<td>file3</td>
</tr>
<tr>
<td>directory1</td>
<td>directory2</td>
<td>directory3</td>
</tr>
</table>

##命令行方式
1. 输入源是pdm或者json
2. 生成out文件夹；
3. 打包成tar包；

##设计模式构建

##存储
1. Mongodb数据库；

##后端
1. 框架：play framework;
2. 接口：restful API（待更新）

##前端
1. 框架：Angular；
2. 设计图

##计划

* 原型demo--->原型Java web demo---->
* ------>实现模板管理功能------>
* 数据接口层优化重构---->丰富模板集----->前端界面优化
* ----->漂亮，高亮显示的模板编辑器
* ------>部署上线
* 模板集
1. Java:bean,engine.dao,engine.action,repository,service,serviceImpl,servlet(controller)
2. js:
3. html:login
4. python:
5. C/C++:
* 模板引擎：freemarker,velocity,artTemplate...  支持多模板引擎
* 数据集：元数据,css格式数据,数据信息(展示页和详情页)
* 程序的展现方式：网站,app,desktop程序,IDE插件,框架插件

##重构需求迭代
* 两种需求：
	有时候要生成一个文件，生成的粒度不一样；
	一个pdm--->可以对应一个文件，也可以对应多个文件，使用build.propertiry来判定
	输出的文件名也不是一种方式：
	1、例如想要取名为模型名的；
	2、还有自定义名字的；
	3、等等；
	4、还要打包成一个压缩包的
* 语言之间的区别：
	数据类型的区别：int<--->bigint
	命名方式的区别：驼峰，匈牙利，Pascal的命名方式

##重构代码迭代
* 设计模式：
	工厂模式
* 模板文件：
    Spring的几种文件形式
    
##命令行运行例子
java -jar codeGenerationDemo.jar "E:\\Projects\\codeGenerationDemo\\code_generator\\examples\\model\\hybrid\\" "E:\\Projects\\codeGenerationDemo\\code_generator\\examples\\template\\"  "E:\\Projects\\codeGenerationDemo\\code_generator\\examples\\output\\"

##入口主类
entry.Runner
	