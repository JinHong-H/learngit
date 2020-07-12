### HTML5 Video标签

|标签|描述|
|--|--|
|\<video>|定义一个视频|
|\<source>|定义多种媒体资源,比如 \<video> 和\<audio>|
|\<track>|定义在媒体播放器文本轨迹|

[HTML5 Audio/Video DOM参考手册](https://www.runoob.com/tags/ref-av-dom.html)

实例：

```(html)
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
您的浏览器不支持Video标签。
</video>
```

### HTML5 Audio标签

|标签|描述|
|--|--|
|\<audio>|定义了声音内容|
|\<source>|规定了多媒体资源, 可以是多个，在 \<video> 与 \<audio>标签中使用|

实例：

```(html)
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
您的浏览器不支持 audio 元素。
</audio>
```

+ control 属性供添加播放、暂停和音量控件。

+ 在\<audio> 与 \</audio> 之间你需要插入浏览器不支持的\<audio>元素的提示文本 。

+ \<audio> 元素允许使用多个 \<source> 元素. \<source> 元素可以链接不同的音频文件，浏览器将使用第一个支持的音频文件

