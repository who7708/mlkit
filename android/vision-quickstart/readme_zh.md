# ML Kit 视觉快速入门示例应用

## 简介

本 ML Kit 快速入门应用演示了如何在您的应用中集成和使用各种基于视觉的 ML Kit 功能。

## 功能列表

本快速入门应用包含以下功能：
* [目标检测](https://developers.google.com/ml-kit/vision/object-detection/android) — 在实时画面和静态图像中检测、跟踪和分类目标。
* [人脸检测](https://developers.google.com/ml-kit/vision/face-detection/android) — 在实时画面和静态图像中检测人脸。
* [人脸网格检测](https://developers.google.com/ml-kit/vision/face-mesh-detection/android) — 在实时画面和静态图像中检测人脸网格。
* [文字识别](https://developers.google.com/ml-kit/vision/text-recognition/android) — 在实时画面和静态图像中识别文字。
* [条码扫描](https://developers.google.com/ml-kit/vision/barcode-scanning/android) — 在实时画面和静态图像中扫描条码。
* [图像标注](https://developers.google.com/ml-kit/vision/image-labeling/android) — 在实时画面和静态图像中为图像添加标签。
* [自定义图像标注 - 鸟类](https://developers.google.com/ml-kit/vision/image-labeling/custom-models/android) — 使用自定义 TensorFlow Lite 模型为鸟类图像添加标签。
* [姿态检测](https://developers.google.com/ml-kit/vision/pose-detection/android) — 在实时画面中检测人体位置。
* [自拍分割](https://developers.google.com/ml-kit/vision/selfie-segmentation/android) — 在实时画面中将人物从背景中分割出来。
* [主体分割](https://developers.google.com/ml-kit/vision/subject-segmentation/android) — 在静态图像中将多个主体从背景中分割出来。

<img src="../screenshots/quickstart-picker.png" width="220"/> <img src="../screenshots/quickstart-image-labeling.png" width="220"/> <img src="../screenshots/quickstart-object-detection.png" width="220"/> <img src="../screenshots/quickstart-pose-detection.png" width="220"/>

## 开始使用

* 在您的 Android 设备或模拟器上运行示例代码
* 尝试扩展代码以添加新功能和增强功能

## 如何使用本应用

本应用支持三种使用场景：实时相机、静态图像和 CameraX 实时预览。

### 实时相机场景

它以相机预览作为输入，包含以下 API 流程：目标检测与跟踪、人脸检测、人脸网格检测、文字识别、条码扫描、图像标注和姿态检测。还有一个设置页面，允许您配置多个选项：

* **相机**
    * **预览尺寸** — 手动指定后置/前置相机的预览尺寸（默认尺寸根据屏幕尺寸自动选择）
    * **启用实时视口** — 切换是否由 API 处理和结果渲染阻塞相机预览
* **目标检测 / 自定义目标检测**
    * **启用多目标检测** — 允许同时检测多个目标
    * **启用分类** — 对每个检测到的目标进行分类
* **人脸检测**
    * **关键点模式** — 切换是否显示所有面部关键点
    * **轮廓模式** — 切换是否显示所有轮廓
    * **分类模式** — 切换是否显示所有分类（微笑、睁眼/闭眼）
    * **性能模式** — 在两种运行模式之间切换（快速或精准）
    * **人脸跟踪** — 启用或禁用人脸跟踪
    * **最小人脸尺寸** — 选择头部宽度与图像宽度的比例
* **人脸网格检测**
    * **使用场景** — 在 `仅边界框` 和 `人脸网格` 之间选择
* **姿态检测**
    * **性能模式** — 允许在"快速"和"精准"运行模式之间切换
    * **显示画面内置信度** — 显示每个关键点的 InFrameLikelihood 分数
    * **可视化 z 值** — 使用不同颜色表示 z 值差异（红色：较小 z，蓝色：较大 z）
    * **重新缩放 z 值以可视化** — 将最小 z 值映射为最红，最大 z 值映射为最蓝，使 z 值差异更明显
    * **运行分类** — 对深蹲和俯卧撑姿态进行分类，在流式模式下计数次数
* **自拍分割**
    * **启用原始尺寸遮罩** — 要求分割器返回与模型输出尺寸匹配的原始尺寸遮罩

### 静态图像场景

静态图像场景与实时相机场景相同，但依赖通过相册传入的图像。

### CameraX 实时预览场景

CameraX 实时预览场景与原生实时相机场景非常相似，但依赖 CameraX 实时预览。注意：CameraX 仅在 API 级别 21+ 上受支持。

## 支持

* [文档](https://developers.google.com/ml-kit/guides)
* [API 参考](https://developers.google.com/ml-kit/reference/android)
* [Stack Overflow](https://stackoverflow.com/questions/tagged/google-mlkit)

## 许可证

Copyright 2020 Google, Inc.

根据一个或多个贡献者许可协议授权给 Apache 软件基金会（ASF）。有关版权所有权的更多信息，请参阅本作品随附的 NOTICE 文件。ASF 根据 Apache 许可证 2.0 版（"许可证"）向您许可本文件；除非符合许可证规定，否则您不得使用本文件。您可以在以下网址获取许可证副本：

  http://www.apache.org/licenses/LICENSE-2.0

除非适用法律要求或书面同意，否则根据许可证分发的软件按"原样"分发，不提供任何明示或暗示的保证或条件。请参阅许可证以了解有关权限和限制的详细规定。
