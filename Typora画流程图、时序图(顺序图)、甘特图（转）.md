

# Typora画流程图、时序图(顺序图)、甘特图（转）



[原文连接]:https://www.jianshu.com/p/7ddbb7dc8fec



# 横向流程图源码格式：



```rust
graph LR
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    F[横向流程图]
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-ce6ef47a2fbdb235.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# 竖向流程图源码格式



```rust
graph TD
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    F[竖向流程图]
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-0d1cfb526789d01d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# 标准流程图源码格式



```php
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-624ab65e5eb19825.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# 标准流程图源码格式（横向）



```php
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st(right)->op(right)->cond
cond(yes)->io(bottom)->e
cond(no)->sub1(right)->op
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-e622f3fa505eadb6.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# UML时序图源码样例



```rust
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象A->对象B: 你真的好吗？
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-d981aa819b33a8ff.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# UML时序图源码复杂样例



```rust
Title: 标题：复杂使用
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象B->小三: 你好吗
小三-->>对象A: 对象B找我了
对象A->对象B: 你真的好吗？
Note over 小三,对象B: 我们是朋友
participant C
Note right of C: 没人陪我玩
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-0e38c2e50c3ff4a5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# UML标准时序图样例



```rust
%% 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant 张三
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-1aa4e0de189d2529.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)



# 甘特图样例



```css
%% 语法示例
        gantt
        dateFormat  YYYY-MM-DD
        title 软件开发甘特图

        section 设计
        需求                      :done,    des1, 2014-01-06,2014-01-08
        原型                      :active,  des2, 2014-01-09, 3d
        UI设计                     :         des3, after des2, 5d
    未来任务                     :         des4, after des3, 5d

        section 开发
        学习准备理解需求                      :crit, done, 2014-01-06,24h
        设计框架                             :crit, done, after des2, 2d
        开发                                 :crit, active, 3d
        未来任务                              :crit, 5d
        耍                                   :2d

        section 测试
        功能测试                              :active, a1, after des3, 3d
        压力测试                               :after a1  , 20h
        测试报告                               : 48h
```



![img](https:////upload-images.jianshu.io/upload_images/15296782-ca096c7a57a3314d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)





