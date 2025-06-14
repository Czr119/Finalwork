# 垃圾分类识别应用

这是一个基于Android的垃圾分类识别应用，使用Jetpack Compose构建现代化UI界面，结合机器学习技术实现实时垃圾分类识别功能。应用使用TensorFlow Lite模型进行垃圾分类识别，该模型经过大量垃圾分类数据集训练，具有较高的识别准确率。

## 主要功能

-  实时相机拍照识别
-  相册图片选择识别
-  支持多种垃圾类别识别：
  - 有害垃圾
  - 厨余垃圾
  - 其他垃圾
  - 可回收物
-  识别结果可视化展示
-  支持重新拍照和切换图片

## 技术特点

- 使用 Jetpack Compose 构建现代化UI
- 采用 CameraX 实现相机功能
- 集成 TensorFlow Lite 机器学习模型进行图像分类
- 支持多种图像格式处理
- 完善的权限管理系统

## 模型说明

本项目使用TensorFlow Lite模型进行垃圾分类识别：
- 模型基于大量垃圾分类数据集训练
- 支持实时图像处理和分类
- 模型经过优化，在移动设备上运行流畅
- 识别准确率经过验证和测试

## 系统要求

- Android 5.0 (API 21) 或更高版本
- 相机权限
- 存储权限

## 权限说明

应用需要以下权限：
- 相机权限：用于拍照功能
- 存储权限：用于访问相册和保存图片

## 使用说明

1. 启动应用后，默认进入相机界面
2. 可以选择以下操作：
   - 点击"拍照"按钮进行实时拍照识别
   - 点击"相册"按钮从相册选择图片识别
3. 识别结果将显示在界面下方，包含：
   - 垃圾类别
   - 识别置信度
   - 可视化进度条
4. 可以点击"重新拍照"返回相机界面

## 开发环境

- Android Studio
- Kotlin
- Jetpack Compose
- CameraX
- Android SDK

## 注意事项

- 首次使用需要授予相机和存储权限
- 建议在光线充足的环境下使用相机功能
- 图片识别准确度可能受图片质量影响

## 项目结构

- `garbage_classification_model.ipynb`: 用于训练垃圾分类模型的Jupyter Notebook
- `app/`: Android应用源代码
  - `src/main/java/com/android/example/finalwork/GarbageClassifier.kt`: TensorFlow Lite模型加载和推理类
  - `src/main/java/com/android/example/finalwork/MainActivity.kt`: 应用主界面和相机功能

## 数据集

本项目使用的是Garbage classification数据集，包含4个类别：harmful,recycle,kitchen,other。

## 技术栈

- TensorFlow/Keras: 用于模型训练
- TensorFlow Lite: 用于Android设备上的模型推理
- CameraX: 用于相机功能
- Jetpack Compose: 用于UI构建
- Android Photo Picker API: 用于从相册选择图片

## 注意事项

- 模型精度取决于训练数据和训练参数，可以通过调整模型结构和训练参数来提高准确率。

- 在低光照条件下，识别效果可能不佳，请尽量在光线充足的环境下使用。

- 量化模型可能会略微降低准确率，但能显著减小模型大小，提高在移动设备上的性能。

- 如果应用依然出现闪退，请确保已授予所有必要权限。

  
