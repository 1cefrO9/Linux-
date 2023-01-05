创建好作业后，先进入文件夹/home/acs/homework/lesson_5/，然后：

(0) 在当前目录下创建文件夹homework，并将homework目录配置成git仓库。后续作业均在homework目录下操作；

```shell
mkdir homework
cd homework
git init
```

(1) 创建文件readme.txt，内容包含一行：111；
将修改提交一个commit；

```shell
vim readme.txt
#***
111
#***
git add .
git commit -m "add readme.txt"
```

(2) 在readme.txt文件末尾新增一行：222；
将修改提交一个commit；

```shell
vim readme.txt
#***
111
222
#***
git add .
git commit -m "add 222"
```

(3) 创建文件夹：problem1和problem2；
创建文件problem1/main.cpp。文件内容为下述链接中的代码：https://www.acwing.com/problem/content/submission/code_detail/7834813/；
创建文件problem2/main.cpp。文件内容为下述链接中的代码：https://www.acwing.com/problem/content/submission/code_detail/7834819/；
将修改提交一个commit；

```shell
mkdir problem1 problem2
cd problem1
vim main.cpp
***
#include <iostream>

using namespace std;

int main()
{
    int a, b;
    cin >> a >> b;
    cout << a + b << endl;
    return 0;
}
***
cd ../problem2
vim main.cpp
***
#include <iostream>

using namespace std;

const int N = 1010;

int n, m;
int f[N];

int main()
{
    cin >> n >> m;
    while (n -- )
    {
        int v, w;
        cin >> v >> w;
        for (int j = m; j >= v; j -- )
            f[j] = max(f[j], f[j - v] + w);
    }

    cout << f[m] << endl;

    return 0;
}
***
cd ..
git add .
git commit -m "add problem1 problem2"
```

(4) 删除文件夹problem2；
创建文件夹problem3；
创建文件problem3/main.cpp。文件内容为下述链接中的代码：https://www.acwing.com/problem/content/submission/code_detail/7834841/；
将readme.txt中最后一行222删掉，然后添加一行333；
将修改提交一个commit；

```shell
rm problem2 -r
mkdir problem3
cd problem3
vim main.cpp
***
#include <iostream>

using namespace std;

const int N = 1010;

int n, m;
int f[N];

int main()
{
    cin >> n >> m;

    while (n -- )
    {
        int v, w;
        cin >> v >> w;
        for (int j = v; j <= m; j ++ )
            f[j] = max(f[j], f[j - v] + w);
    }

    cout << f[m] << endl;
    return 0;
}
***

cd ..
vim readme.txt
***
111
333
***

git add .
git commit -m "many operations"
```

(5) 在https://git.acwing.com/上注册账号并创建仓库，仓库名称为homework；
将本地git仓库上传到AC Git云端仓库；

```shell
git remote add origin git@git.acwing.com:injoker/homework.git
git push -u origin master
```

(6) 创建并切换至新分支dev；
在readme.txt文件中添加一行444；
将修改提交一个commit；
将dev分支推送至AC Git远程仓库；

```shell
git checkout -b dev
vim readme.txt
***
111
333
444
***

git add .
git commit -m "add 444"

git push origin dev
```

(7) 切换回master分支；
在readme.txt文件中添加一行555；
将修改提交一个commit；

```shell
git checkout master  # 切换回master分支

vim readme.txt

***
111
333
555
***

git add .
git commit -m "add 555"
```

(8) 将dev分支合并到master分支；
手动处理冲突，使readme文件最终内容包含4行：111、333、555、444；
将修改提交一个commit；

```
git merge dev  # 将dev分支合并到当前分支

vim readme.txt

***
111
333
555
444
***

git add .
git commit -m "fix conflicts"
```

(9) 将master分支的版本库push到AC Git云端仓库；
登录myserver服务器（4. ssh作业中配置的服务器）；
创建并清空文件夹：~/homework/lesson_5/；
将AC Git云端仓库clone到~/homework/lesson_5/中；

```shell
ssh myserver
cd homework
mkdir lesson_5
cd lesson_5

git clone git@git.acwing.com:injoker/homework.git
```

