创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
(0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c

```shell
cd homework/lesson_1/homework_0/
mkdir dir_a dir_b dir_c
```

(1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak

```shell
cd homework/lesson_1/homework_1/
cp a.txt a.txt.bak
cp b.txt b.txt.bak
cp c.txt c.txt.bak
# cp复制不会删除源文件
```

(2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt

```shell
cd
cd homework/lesson_1/homework_2/
mv a.txt a_new.txt
mv b.txt b_new.txt
mv c.txt c_new.txt
#mv 重命名 mv=复制＋剪切
```

(3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下

```shell
cd 
cd homework/lesson_1/homework_3/
mv dir_a/*.txt dir_b/
```

(4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除

```shell
cd
cd homework/lesson_1/homework_4
rm *.txt
```

(5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除

```shell
cd
cd homework/lesson_1/homework_5
rm dir_a dir_b dir_c -r
```

(6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作

```shell
cd             
cd homework/lesson_1/homework_6
cat task.txt
#将task.txt重命名为done.txt, 创建目录dir_a，将done.txt移动到目录dir_a下
mkdir dir_a
mv task.txt dir_a/done.txt #移动done.txt其实是剪贴操作
```

(7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
    将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
    将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
    将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;

```shell
cd
cd homework/lesson_1/homework_7
mkdir dir_0 dir_1 dir_2
cp a.txt dir_0/a0.txt
cp b.txt dir_0/b0.txt
cp c.txt dir_0/c0.txt
cp a.txt dir_1/a1.txt
cp b.txt dir_1/b1.txt
cp c.txt dir_1/c1.txt
cp a.txt dir_2/a2.txt
cp b.txt dir_2/b2.txt
cp c.txt dir_2/c2.txt
```

(8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作

```shell
//切换目录
cd homework/lesson_1/homework_8
ls
dir_a  dir_b  dir_c
cd dir_a#切换到dir_a文件夹
ls
a.txt  task.txt
cat task.txt #显示任务内容
#将a.txt删除
rm a.txt#执行任务

cd
#切换目录
cd homework/lesson_1/homework_8
ls
dir_a  dir_b  dir_c
cd dir_b #切换到dir_b
ls
b.txt  task.txt
cat task.txt #显示任务内容
#将b.txt重命名为b_new.txt
mv b.txt b_new.txt #执行重命名操作

cd
cd homework/lesson_1/homework_8
cd dir_c #切换到dir_c文件夹
 ls
c.txt  task.txt
cat task.txt #显示任务内容
#将c.txt复制成c.txt.bak
cp c.txt c.txt.bak
```

(9) 进入homework_9文件夹，将其中所有txt类型的文件删除

```shell
cd
cd homework/lesson_1/homework_9
rm *.txt
```

