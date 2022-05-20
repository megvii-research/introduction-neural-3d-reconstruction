###前言
1. 本次小作业旨在让大家熟悉第二节课的第二部分的内容，基于NeRF pipeline和SDF的三维重建，尝试去重建出自己感兴趣的物体。我们将挑选出其中的10个为大家3D打印出来。
2. 本指引以NeuS为参考，但大家可以选取 NeuS 之外任意可导出 obj/stl 的重建方法。我们不对 NeuS 及其他方法本身的使用做支持。
3. 10 件作品的选取本身有一定的主观性，解释权在主办方。

###题目
基于第二节课介绍的方法（NeuS或者其他类似的方法），重建身边自己感兴趣的小物体

###参考代码
https://github.com/Totoro97/NeuS
请仔细阅读README安装相应的代码运行环境

###参考步骤
1. 找到一个自己感兴趣的物体，大小或者长度不要超过你打印出来的aruco board（aruco board见下文数据处理部分）大小。比如如果您用A4纸打印aruco board，那这个物体就不要超过A4纸的大小；A3纸同理
2. 打印出aruco board (https://github.com/Totoro97/NeuS/blob/main/preprocess_custom_data/static/aruco_board.png)
3. 将物体放在aruco board的中间，围绕物体360ª拍40张到60张左右的照片，可以大部分集中在正面（比如拍40张的话，35张拍正面，5张拍背面），也可以尝试360ª均匀拍照。拍照可以直接用手机拍，拍照效果可以参考ppt第四部分practice，大致拍出那个小新模型的效果
4. 基于下述连接处理步骤3得到的图片，请仔细阅读链接中的README并安装环境，然后处理图片，得到NeuS可以用的数据
https://github.com/Totoro97/NeuS/tree/main/preprocess_custom_data#option-1-use-aruco
5. 最后根据下面代码的README训练网络和inference，没有错的话将会得到一个ply文件，也就是我们说的mesh文件。可以通过三维软件（比如MeshLab）来看您具体得到的ply文件是个什么东西
https://github.com/Totoro97/NeuS

###建议
1. 提问之前请仔细阅读相关链接中的README，很多问题都在其中说的很清楚了，请耐心阅读和理解英语
2. 也可以关注链接中的issue，看看是否有和您类似的问题
