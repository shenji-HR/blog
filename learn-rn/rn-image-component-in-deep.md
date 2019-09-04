# 深入理解 Image 组件
> 源码版本: [react-native-0.57.5](https://github.com/facebook/react-native/releases/tag/v0.57.5)

## Image 源码目录
```bash
/Libraries/Image
.
├── AssetRegistry.js
├── AssetSourceResolver.js
├── Image.android.js
├── Image.ios.js
├── ImageBackground.js
├── ImageEditor.js
├── ImageProps.js
├── ImageResizeMode.js
├── ImageSource.js
├── ImageSourcePropType.js
├── ImageStore.js
├── ImageStylePropTypes.js
├── RCTGIFImageDecoder.h
├── RCTGIFImageDecoder.m
├── RCTImage.xcodeproj
│   └── project.pbxproj
├── RCTImageBlurUtils.h
├── RCTImageBlurUtils.m
├── RCTImageCache.h
├── RCTImageCache.m
├── RCTImageEditingManager.h
├── RCTImageEditingManager.m
├── RCTImageLoader.h
├── RCTImageLoader.m
├── RCTImageShadowView.h
├── RCTImageShadowView.m
├── RCTImageStoreManager.h
├── RCTImageStoreManager.m
├── RCTImageUtils.h
├── RCTImageUtils.m
├── RCTImageView.h
├── RCTImageView.m
├── RCTImageViewManager.h
├── RCTImageViewManager.m
├── RCTLocalAssetImageLoader.h
├── RCTLocalAssetImageLoader.m
├── RCTResizeMode.h
├── RCTResizeMode.m
├── RelativeImageStub.js
├── __tests__
│   ├── __snapshots__
│   │   └── assetRelativePathInSnapshot.js.snap
│   ├── assetRelativePathInSnapshot.js
│   ├── img
│   │   ├── img1.png
│   │   └── img2.png
│   └── resolveAssetSource-test.js
├── nativeImageSource.js
└── resolveAssetSource.js
```

先从 `Image.ios.js` 或 `Image.android.js` 开始看。

## JS 端
### resolveAssetSource 核心代码注解
Libraries/Image/resolveAssetSource.js

## iOS 端
### RCTImageView
Libraries/Image/RCTImageView.h
Libraries/Image/RCTImageView.m

[Talk about ReactNative Image Component](https://awhisper.github.io/2016/07/17/Talk-about-ReactNative-Image-Component/)

## Android 端
> 依赖 [fresco](https://github.com/facebook/fresco)

ReactImageManager: ReactAndroid/src/main/java/com/facebook/react/views/image/ReactImageManager.java