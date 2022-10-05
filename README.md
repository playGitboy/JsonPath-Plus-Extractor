# JsonPath-Plus数据提取工具
仿DevUtils的JSON工具，Windows平台"UI界面操作/系统兼容性佳/便携离线/支持格式化、自动纠错、数据过滤提取"的JSON数据提取工具

基于开源项目JSONPath Plus和json-viewer，使用语句测试如下([ 完整帮助文档 ](https://jsonpath-plus.github.io/JSONPath/docs/ts/index.html))：
```
| JSONPath                                  | 备注                                                 
|-------------------------------------------|------------------------------------------------------
| $..*                                      | 提取所有值                                           
| $..type                                   | 提取全部type字段值                                   
| $.uuids..type或者$.uuids[*].type          | 提取uuids节点下面全部type字段值                   
| $.uuids.*~                                | 提取uuids节点下面所有key名称                         
| $..*[?(@.str)][id,str]                    | 提取包含str字段的全部节点id和str字段值               
| $..*@number()                             | 提取全部数字值                                       
| $..*@string()                             | 提取全部文本值                                 
| $..*[?(@.id>5005)].type                   | 提取id大于5005的全部type字段值                       
| $..toppings[1:3]                          | 提取toppings下面第2、3个节点                         
| $..toppings[1:9:2]                        | 从toppings下面第2节点开始在范围内每隔2个提取         
| $.toppings.*[?(@property.match(/^str/i))] | 提取toppings节点下面所有以"str"开头(正则)的key对应值 
```

### 说明
1. 功能增强：支持JSONPath Plus表达式(兼容JSONPath)，功能更强、例见上表；
   富文本框支持JSON文件拖放打开(兼容常见文本格式)、按住Ctrl+滚轮 无极缩放字体大小
2. 便利性增强：增加常用格式化、排序、缩进等功能；输入JSONPath时"$"字符可省略；  
   右下角编辑框不输入内容直接回车，可快捷触发格式化功能  
3. 容错增强：修复JSON格式常见错误(如"样例"JSON格式有误，纠错后可正确解析)

![主界面](https://github.com/playGitboy/JsonPath-Tool/blob/main/img/%E4%B8%BB%E7%95%8C%E9%9D%A2.png)

![使用演示](https://github.com/playGitboy/JsonPath-Tool/blob/main/img/%E6%BC%94%E7%A4%BA.gif)
