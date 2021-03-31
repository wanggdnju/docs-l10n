# TensorFlow Lite 路线图

**更新日期：2020 年 4 月 18 日**

下面提供了我们 2020 年计划的简要概览。请注意，该路线图随时可能发生变化，以下顺序也不代表任何类型的优先级。原则上，我们通常根据受影响的用户数量确定问题优先级。

We break our roadmap into four key segments: usability, performance, optimization and portability. We strongly encourage you to comment on our roadmap and provide us feedback in the [TF Lite discussion group](https://groups.google.com/a/tensorflow.org/g/tflite).

## 易用性

- **扩大了运算范围**
    - 根据用户反馈确定运算添加的优先级
- **在 TensorFlow Lite 中使用 TensorFlow 运算的改进**
    - 通过 Bintray (Android) 和 Cocoapods (iOS) 提供预构建库
    - 通过运算剥离缩减了使用 select TF 运算时的二进制文件大小
- **LSTM/RNN 支持**
    - 全面支持 LSTM 和 RNN 转换，包括 Keras 中的支持
- **预处理和后处理支持库以及代码生成工具**
    - 适用于常见 ML 任务的即用型 API 构建块
    - 支持更多模型（如 NLP）和更多平台（如 iOS）
- **Android Studio 集成**
    - Drag &amp; drop TFLite models into Android Studio to generate model binding classes
- **控制流和设备端训练**
    - 支持设备端训练，专注于个性化和迁移学习
- **TensorBoard 提供的可视化工具**
    - 通过 TensorBoard 提供增强的工具
- **模型生成器**
    - 支持更多任务，包括物体检测和基于 BERT 的 NLP 任务
- **更多模型和示例**
    - 更多演示模型使用方法的示例以及新功能和 API（涵盖不同的平台）。
- **Task Library**
    - Improve the usability of the C++ Task Library, such as providing prebuilt binaries and creating user-friendly workflows for users who want to build from source code.
    - Release reference examples of using the Task Library.
    - 支持更多任务类型。
    - 改善跨平台支持，并使更多任务可以在 iOS 上执行。

## 性能

- **更出色的工具**
    - 用于跟踪每个版本的性能增益的公共信息中心
- **改善的 CPU 性能**
    - 高度优化的新浮点内核库，适用于卷积模型
    - 一流的 x86 支持
- **更新的 NN API 支持**
    - 全面支持新的 Android R NN API 功能、运算和类型
- **GPU 后端优化**
    - Android 上的 Vulkan 支持
    - 支持整数量化模型
- **Hexagon DSP 后端**
    - 适用于通过训练后量化创建的所有模型的按通道量化支持
    - 动态输入批次大小支持
    - 更大的运算范围，包括 LSTM
- **核心 ML 后端**
    - 优化启动时间
    - 动态量化模型支持
    - Float16 量化模型支持
    - 更大的运算范围

## 优化

- **量化**

    - 适用于 (8b) 定点 RNN 的训练后量化
    - 适用于 (8b) 定点 RNN 的训练中量化
    - 训练后动态范围量化的质量和性能改进

- **剪枝/稀疏**

    - TensorFlow Lite 中的稀疏模型执行支持 - [WIP](https://github.com/tensorflow/model-optimization/issues/173)
    - 权重聚类 API

## 可移植性

- **微控制器支持**
    - Add support for a range of 32-bit MCU architecture use cases for speech and image classification
    - 视觉和音频数据的示例代码和模型
    - 微控制器上的全面 TF Lite 运算支持
    - 支持更多平台，包括 CircuitPython 支持