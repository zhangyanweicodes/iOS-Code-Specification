# 开发规范文档

## 目录

1. 工程目录规范
2. 代码规范
3. 框架使用规范

## 工程目录规范

创建项目以后，必须注意的是将对象进行归类。

**正确做法**：在工程项目中创建文件夹，保证项目内目录与外部文件夹结构一致。

**错误做法**：创建项目之后，直接在工程中创建项目，而对象一直存储在工程目录的同级目录，导致所有资源文件全部存放在一起，难以管理。

### 图文说明:

![工程目录](resource/proj_tree.png)

上图为项目中的管理对象属性图，而项目工程文件夹的管理需要进行相应的树形结构管理。 

下面则为两种不同的项目工程管理方式。

#### 错误做法

![工程目录](resource/proj_tree_wrong.png)

当创建对象达到上百个时，此时工程项目中将会变得非常杂乱，这样也会导致将来想引用该工程的部分组件时，找起来非常的不便。

#### 推荐做法

![工程目录](resource/proj_tree_right.png)

做到工程文件与文件夹结构一致，清晰明了，易于管理。

## 代码规范

开发项目时，应该做到的代码规范。

### 命名规范

命名规范推荐使用驼峰式。

|类型|格式|举例|
|---|---|---|
|类名|大驼峰|`NSString，NSArray，UIView`  |
|变量|小驼峰|`string，dataArray，userInfoView`|  
|函数|小驼峰|`- (void)addSubview:(UIView *)view;`  |
|宏定义|全大写|`VIEW_HEIGHT，VIEW_WIDTH`|

### 注释规范

注释分为两类

1. 函数注释
2. 执行代码注释


#### 注释参考

```
/**
 *  打印函数
 */
- (void)log
{
    // 打印内容
    NSLog(@"Hello World");
}
```

可能你会问为什么这么注释呢？

如下图所示，调用的时候，函数的具体信息将会告诉调用者，清晰明了

![注释提示](resource/func_statement_alert.png)

