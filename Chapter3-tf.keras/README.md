## 1. Tensorflow-keras 介绍        

### 1.1 keras 是什么

- 基于python的高级神经网络API

- 以Tensorflow、CNTK、Theano为后端运行，keras必须有后端才可以运行

  - 后端可以切换，现多以tensorflow为后端

- 方便快速试验，帮助用户以最少的时间验证自己的想法

  

### 1.2 Tensorflow-keras 是什么   

- Tensorflow 对 keras API规范的实现
- 相较于以tensorflow为后端的keras，Tensorflow-keras与Tensorflow结合更为紧密
- 实现在 `tf.keras`空间下



### 1.3  二者的联系

- 基于同一套API
  - keras 程序可以通过改变导入方式转为 tf.keras 程序
  - 反之可能不成立，`tf.keras`有其它特性
- 相同的JSON和HDF5模型序列化格式和语义



### 1.4 二者的区别     

（1）`tf.keras` 全面支持eager mode      

- 只使用`keras.Sequential`和`keras.Model` 时没影响
- 自定义Model内部逻辑运算的时候会有影响
  - tf 底层API可以使用keras的model.fit 等抽象

（2）训练     

- `tf.keras`支持基于`tf.data`的模型训练   
- `tf.keras`支持TPU的训练
- `tf.keras`支持`tf.distribution`中的分布式策略
- 其它
  - `tf.keras`可以与tf 中的estimator集成
  - `tf.keras`可以保存为 SavedModel

### 1.5 如何选择

- 若须使用`tf.keras`的任何一个特性，选用`tf.keras`
- 若后端**互换性**很重要，选用keras

