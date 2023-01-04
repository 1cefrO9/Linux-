创建好作业后，先进入文件夹/home/acs/homework/lesson_2/，然后：
(0) 进入homework_0文件夹，创建文件names.txt，并顺次将下列姓名写入该文件，每个名字占一行。 AcWing、yxc、Bob、张强、李明、Alice 

```shell
cd homework/lesson_2/homework_0/
vim names.txt
输入i进入编辑模式
AcWing
yxc
Bob
张强
李明
Alice
按Esc
进入一般命令模式
:wq
保存并退出
```

(1) 进入homework_1文件夹，打开problem.txt，并依次删除下列字符：
    [1] 最后一行第101个字符
    [2] 第3行第8个字符
    [3] 第1行第30个字符
    [4] 第16行第55个字符
    [5] 第9行第80个字符
    最后保存文件并退出。

```shell
cd ../homework_1
vim problem.txt
G // 进入最后一行
101 //进入编辑模式
i进入编辑模式
2).
3G //进入编辑模式
8 //第8个字符
i进入编辑模式
3).
gg //进入第一行
30 //找到第30个字符
i //进入编辑模式
4).
:16//进入第16行
55 //找到第55个字符
i //进入编辑模式
5).
:9//进入第9行
80 //找到第80个字符
i//进入编辑模式

:wq//保存并退出
```

(2) 进入homework_2文件夹，打开problem.txt，并依次执行如下操作：
    [1] 在第1个"two"的后面添加"abc"
    [2] 在第2个"two"的前面添加"def"
    [3] 将第3个"two"后面的连续12个字符删掉
    [4] 将第4个"two"所在的行删掉
    最后保存文件并退出。

```shell
cd homework/lesson_2/homework_2
vim problem.txt
gg//先到第1行
然后输入 /two,回车
i进入编辑模式
1).在第一个two后面输入 “abc”
2).在第二个two前面输入def
3).在第三个two，删除12个字符
4).定位到第四个two，退出编辑模式输入dd，删除该行
```

(3) 进入homework_3文件夹，打开problem.txt，并依次执行如下操作：
    [1] 将第5行至第15行中所有of替换成OF。
    [2] 将全文中所有的the替换成THE。
    [3] 将第偶数个is替换成IS，第奇数个is不变。下标从1开始。

```shell
cd ../homework_3
vim problem.txt
1).:5,15s/of/OF/g //将在5行和第15行之间的of全部换成OF
2).:1,$s/the/THE/g //将所有的the换成THE
3):1,$s/is/IS/gc 然后ny交替按即可//将所有偶数个is换成IS
```

(4) 进入homework_4文件夹，打开problem.txt，并依次执行如下操作：
    [1] 删除第11行
    [2] 将所删除的行粘贴到文件最后一行的下一行
    [3] 复制第5行
    [4] 将所复制的行粘贴到文件当前最后一行的下一行

```shell
cd ../homework_4
1).11G dd//删除第11行
2).Gp //先到最后一行，然后按p粘贴
3).5Gyy//将第5行复制
4).Gp//先到最后一行，然后按p粘贴
:wq //保存并退出
#粘贴时不会另起一行 只会在最后一行的复制粘贴
```

(5) 进入homework_5文件夹，打开problem.txt，并依次执行如下操作：
    [1] 删除第11行第15个字符（包含该字符）至第13行第5个字符（包含该字符）
    [2] 将所删除的内容粘贴到文件末尾（注意不要另起一行）
    [3] 复制第5行第88个字符（包含该字符）至第7行第6个字符（包含该字符）
    [4] 将所复制的内容粘贴到当前文件末尾（注意不要另起一行）

```shell
cd ../homework_5
1).11G14<Space>//跳到第11行第14个单词
   v//选中文本
   13G5<Space>//到第13行第5个单词
   d//删除选中文本
2).G$//到达最后一行的最后一个位置
   p//粘贴文本
3).5G87<Space>//跳到第5行第87个单词（因为第88个单词要保留）
   v//选中文本
   7G6<Space>//跳到第7行第6个单词（因为第7个要保留）
   y//复制文本
4).G$p
:wq //保存并退出
```

(6) 进入homework_6文件夹，并依次执行如下操作：
    [1] 清空source0.cpp
    [2] 将source1.cpp中的第1-3行和第12-24行复制到source0.cpp中

```shell

cd ../homework_6
1).gg+d+G//删除全部文本
2).ctrl+a shift+" //打开一个新的pane
   vim source1.cpp
   :set nonu //隐藏行号
   shift //选中前3行
   ctrl+insert //复制选中内容
   在source0.cpp中
   :set paste //进入粘贴模式
   i进入编辑模式
   shift+insert //进行粘贴
 同理操作12-24行
 source0.cpp :wq//保存并退出
 source1.cpp :q//退出
```

(7) 进入homework_7文件夹，格式化source.cpp

```shell
cd ../homework_7
vim source.cpp
gg=G //将全部内容格式化
:wq //保存并退出
```

(8) 进入homework_8文件夹，打开source.cpp，并依次执行如下操作：
    [1] 将第15-21行向右缩进2次。
    [2] 将第22-23行向左缩进1次。

```shell
cd ../homework_8
vim source.cpp
下面两行操作重复两次
15Gv21G  //选中15-21行
> >  //向右缩进

22Gv23G //选中22-23行
<    //向左缩进1次
:wq
```

(9) 进入homework_9文件夹，打开链接：https://www.acwing.com/activity/content/code/content/1694465/
    新建文件source.cpp，将链接中的代码抄进source.cpp文件中。

```shell
vim source.cpp

#include<iostream>                                                                                                                            

using namespace std;

int main(){
    int a, b;
    cin >> a >> b;
    cout << a + b < <endl;
    return 0;
}
//输入以上代码即可
```

