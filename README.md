原包链接https://bitmiracle.com/zh-cn/libtiff/
该库是C#常用的tiff解析库，不支持big tiff。
在读取由几十万张小图构成的tiff文件时报错，报错信息为 out of index，数组超出索引
经排查，发现是由于该库代码内部采用short类型来表示单个图像的索引，导致超过short类型最大值时报错
因此通过下载源码，并将所有short类型改为int，编译测试通过。百万级别的图像数量无报错。
此处提供包文件供下载，感兴趣的开源自行修改github源码，前后耗时在半小时内即可完成。

转载无需注明出处，请随意修改和转载。




LibTiff.NET
===========

The .NET version of original libtiff library written by Sam Leffler and others.

LibTiff.Net provides support for the Tag Image File Format (TIFF), a widely used format for storing image data.

Sample code
===========

Sample code for C# and VB.NET

https://github.com/BitMiracle/libtiff.net/tree/master/Samples


Documentation
=============

Help pages can be found here

https://bitmiracle.github.io/libtiff.net/help/


License
=======

LibTiff.Net is freely available for all uses under the New BSD license.

The library is free and can be used in commercial applications without royalty.

We don't promise that this software works. But if you find any bugs, please let us know!
