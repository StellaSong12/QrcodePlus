QRCodePlus for Android
===================
1. qrcodescanner/src/main/java/com/m2x/qrcodescanner/camera/CameraManager.java
setManualFramingRect(int width, int height)
修改 int topOffset = (screenResolution.y - height) / 3;
使二维码扫描框垂直方向偏上

2. qrcodescanner/src/main/java/com/m2x/qrcodescanner/QRCodeScanner.java
resumeDecode()
qrcodescanner/src/main/java/com/m2x/qrcodescanner/ViewfinderView.java
DoubleTapListener#onDoubleTap(MotionEvent e)
增加 try-catch 保护

3. qrcodescanner/src/main/java/com/m2x/qrcodescanner/camera/CameraConfigurationUtils.java
findBestPreviewSizeValue(Camera.Parameters parameters, Point screenResolution)
修改相机分辨率选择算法，选择长宽比最适合预览视图的相机分辨率，避免拉伸导致的失真
