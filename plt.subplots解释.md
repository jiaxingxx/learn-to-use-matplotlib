在matplotlib中，整个图像为一个Figure对象。

在Figure对象中可以包含一个或者多个Axes对象。

每个Axes(ax)对象都是一个拥有自己坐标系统的绘图区域。

参数：

nrows，ncols：

子图的行列数。
sharex, sharey：

设置为 True 或者 ‘all’ 时，所有子图共享 x 轴或者 y 轴，
设置为 False or ‘none’ 时，所有子图的 x，y 轴均为独立，
设置为 ‘row’ 时，每一行的子图会共享 x 或者 y 轴，
设置为 ‘col’ 时，每一列的子图会共享 x 或者 y 轴。
squeeze：

默认为 True，是设置返回的子图对象的数组格式。
当为 False 时，不论返回的子图是只有一个还是只有一行，都会用二维数组格式返回他的对象。
当为 True 时，如果设置的子图是（nrows=ncols=1），即子图只有一个，则返回的子图对象是一个标量的形式，如果子图有（N×1）或者（1×N）个，则返回的子图对象是一个一维数组的格式，如果是（N×M）则是返回二位格式。
subplot_kw:

字典格式，传递给 add_subplot() ，用于创建子图。
gridspec_kw：

字典格式，传递给 GridSpec 的构造函数，用于创建子图所摆放的网格。
class matplotlib.gridspec.GridSpec(nrows, ncols, figure=None, left=None, bottom=None, right=None, top=None, wspace=None, hspace=None, width_ratios=None, height_ratios=None)
如，设置 gridspec_kw={'height_ratios': [3, 1]} 则子图在列上的分布比例是3比1。
**fig_kw :

所有其他关键字参数都传递给 figure（）调用。
如，设置 figsize=(21, 12) ，则设置了图像大小。

返回值
fig： matplotlib.figure.Figure 对象

ax：子图对象（ matplotlib.axes.Axes）或者是他的数组

原文：https://blog.csdn.net/qq_39622065/article/details/82909421 
