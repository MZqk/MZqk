# test
## test语法
参数|说明
---|---
-d|如果文件为一个目录，则为真   
-e|如果文件存在，则为真     
-G|如果文件存在且归该组所有，则为真     
-O|如果文件存在并且归该用户所有，则为真  
-s|如果文件的长度不为零，则为真     
-r|如果文件可读，则为真        
-w|如果文件可写，则为真        
-x|如果文件可执行，则为真
|
-eq|数值等于,则为真
-ne|数值不等于,则为真
-gt|数值大于,则为真
-ge|数值小于等于,则为真
-lt|数值小于,则为真
-le|数值小于等于,则为真
|
=|字符相等，则为真
!=|字符不相等，则为真
-z|字符串长度为零，则为真
-n|字符串长度不为零，则为真
**Shell还提供了与( -a )、或( -o )、非( ! )三个逻辑操作符用于将测试条件连接起来，其优先级为："!"最高，"-a"次之，"-o"最低。**
## test用法
### 文件测试
```
cd /bin
if test -e ./bash 
then
    echo '文件已存在!'  
else
    echo '文件不存在!' 
fi
```
输出结果
>文件已存在!

### 数值测试
```
num1=100 
num2=100
if test $[num1] -eq $[num2]
then    
    echo '两个数相等！'   
else
    echo '两个数不相等！' 
fi
```
输出结果
>两个数相等！
### 字符串测试
```
num1="ru1noob"
num2="runoob"
if test $num1 = $num2
then
    echo '两个字符串相等!'
else
    echo '两个字符串不相等!'
fi
```
输出结果
>两个字符串不相等!