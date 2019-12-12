
# YOLOv2-photo-mark

### 2017-11-7

----------------------

Make the training data for yolov2, this code will output the label file for every picture.

网上关于制作yolo数据集的代码有好几份，之前看到的有*imageLabel*和*yolo-mark*，这两个功能都比较完善，但是代码比较复杂，后者还需要配置，且得到的数据需要再经过一次转换，如果是像我这样只需要做**一类**物体的标记或者需要制作的数据集较小的朋友，更适合用本代码中的方法。

这个代码是基于网上的一份代码修改的，刚刚找了半天已经找不到出处了，如果知道的同学可以告知一下。

最初的代码比较简陋，运行起来也有一些问题，且输出的格式不能直接用于yolov2的训练,修改过后基本没什么问题。

##### 使用方法

在代码文件所在目录下新建images文件夹、labels文件夹，将需要做标记的图片放到images文件夹中。最后得到的标签文件会存放到labels文件夹下。

代码比较简洁，因此功能也相对来说比较简陋，目前只能对一类物体进行标记，如果需要制作多类的标签数据，只能修改代码*67*行后重复运行代码。以后有时间会将代码进行完善。

本代码用到了*opencv*，利用opencv进行标记，需要提前配置好opencv库（既然要用yolov2，opencv肯定还是要装的）。

在命令行窗口下，输入 ```python YOLOv2_photo_mark.py```进入标记界面。

左键拖动进行绘制，当前图片绘制完成后，点击右键绘制下一张图片，直到标记完成images目录下的所有图片。

----------------------
