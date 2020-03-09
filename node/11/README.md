# 进程的当前工作目录是什么？有什么作用？

进程的当前工作目录默认值是当前进程启动的目录，通过 `process.cwd()` 可以获取当前工作目录（current working directory），文件操作等使用相对路径时会相对当前工作目录来获取文件。

一些获取配置的第三方模块（例如 webpack）就是通过你的当前工作目录来获取对应的配置文件的，在程序中可以通过 `process.chdir()` 来改变当前的工作目录。