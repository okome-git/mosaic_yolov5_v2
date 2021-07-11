# mosaic_yolov5_v2

![mosaic](_assets/zidane.jpg)

## Case1 : Use like a yolov5
<br>
1. Simply type commands like a yolov5 and add "--mosaic-img" as follows:
  <br>
  
```bash
$ python detect.py --source aaa/bbb.mp4 --mosaic-img
$ # if you want to make mosaic for specific class (ex. person)
$ python detect.py --source aaa/bbb.mp4 --mosaic-img --classes 0
```


<br>
<br>

## Case2 : Use output YOLOv5 labels and original movie
<br>
1. Create label using yolov5 as follows:
<br>

```bash
$ python detect.py --source aaa/bbb.mp4 --save-txt --classes 0
```

<br>
<br>
2. Put original movie and label file
<br>
        mosaic_yolov5
        <br>
        &emsp;└─data
        <br>
            &emsp;&emsp;├─labels
            <br>
            &emsp;&emsp;└─original_movie
            <br>
                      &emsp;&emsp;&emsp;└─bbb.mp4
                      <br>
<br>
<br>
3. Change mp4 file name in mosac.py
<br>

```python
[9] video_path = "./data/original_movie/bbb.mp4" # bbb is your mp4 file name
```

<br>
<br>
4. Create mosaic movie

```bash
$ python mosaic.py
```

<br>

