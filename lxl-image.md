# 使用python合成多个图像文件到一个文件

### 步骤

* 保存ipad mini的截图到这里
* 执行ls IMG*png > aaa.txt
* 执行Python lxlImageDeal.py
* 上传生成的文件到onlineOCR
* 根据ipad mini进行文档整理
* 编写阅读后感


### 以下是代码部分

```python

#--*-- coding:utf-8 --*--
from PIL import Image
import ImageFilter
import sys

global ext
ext = ".png"

#filename = sys.argv[1]
filename = 'aaa.txt'

# Create a image file with you want to genenrate one.
im = Image.new('RGB', (1536, len(open(filename).readlines()) * 1782), 0xffffff)

print im.size[0], im.size[1]

fp = open(filename)

cur = 0

left = 196
top = 128
width = 1528
height = 1910 
box = (left, top, width, height)

for strAAA in fp.readlines():
    bbb = strAAA.split('.')
    img = Image.open(bbb[0]+ext)
    pimg = img.crop(box)
    print pimg.size[0],pimg.size[1]
    im.paste(pimg, (0,cur))
    cur += pimg.size[1]

im.save('lxl-cur'+ext)

```

