Git is a distributed version control system.
Git is a free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes.
Git tracks changes of files.
Creating a new branch is quick and simple.
haha

线程局部变量：
作用域：每个线程的全局，线程之间不共享，线程安全。可以认为是每个线程自己的全局变量。
静态局部变量：
作用域：线程的函数中，其他函数不能访问，线程安全
所以我认为，如果只是在单个函数中访问某个变量，可以用静态局部变量替代线程局部变量。

静态全局变量在头文件里定义
在对一个变量声明了static之后这个变量只能在当前文件中起作用了，你在头文件里面声明了，那么第一个包含这个头文件的源文件就是这个static变量的作用域了，第二个包含头文件的源文件就是这个变量的第二个作用域，当然也就不一样了。
至于你需要一个全局变量，你可以声明extern，但是要注意在头文件中只能声明，要在cpp文件中再定义一次。这样包含了这个头文件的源文件都能共享同一个全局变量了。不过c++最好的全局变量是类中static。
参考：
https://blog.csdn.net/yockie/article/details/50768753
https://coolshell.cn/articles/10115.html
https://stackoverflow.com/questions/11967502/okay-to-declare-static-global-variable-in-h-file
