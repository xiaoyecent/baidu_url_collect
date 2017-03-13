# baidu_url_collect

百度url采集脚本,挖洞的人都懂这是什么.. win和linux下均可使用,亲测速度比较快(多线程加队列的写法~)
```
usage: bd_url.py [-h] [-p PAGECOUNT] [-t THREAD_COUNT] [-o OUTFILE] keyword

baidu_url_collect py-script by xiaoye

positional arguments:
  keyword               keyword like inurl:.?id= for searching sqli site

optional arguments:
  -h, --help            show this help message and exit
  -p PAGECOUNT, --page PAGECOUNT
                        page count
  -t THREAD_COUNT, --thread THREAD_COUNT
                        the thread_count
  -o OUTFILE, --outfile OUTFILE
                        the file save result

```
keyword为关键字,如site:.kr即为搜寻韩国网站; 
-p指定要采集的页数,一页10条url,实际采集中会比这个数字少,因为有的网站已经无法访问;
-t指定线程数,默认为10,建议开到40左右;
-o指定输出文件位置,默认为当前目录的result.txt下

```
demo: python bd_url.py "site:.kr" -p 20 -t 20 -o result1.txt
```
