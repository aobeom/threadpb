### 简介

一个基于multiprocessing的简单多线程进度条。

### 说明

初始化时需要一个任务函数和待处理的任务列表，以及线程数（默认CPU数量的线程）

### 例子
```python
from threadpb import threadProcBar
import time

def dosth(l):
    # Do something
    time.sleep(1)

thread_num = 2
task_list = [1, 2, 3, 4, 5]
t = threadProcBar(dosth, task_list, thread_num)
t.worker()
t.process()
```