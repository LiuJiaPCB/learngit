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
