# pyce
Html article content extractor in Python2. Going to make it compatible with Python3.

The more advanced Golang version html content extractor is [here](https://github.com/crawlerclub/ce).

## Usage
```python
import requests

url = "http://mil.sohu.com/20150504/n412317568.shtml"
html = requests.get(url).content
encoding, time, title, text, next_link = parse(url, html)
print("编码："+encoding)
print('='*10)
print("标题："+title.encode('utf-8','ignore'))
print("时间："+time.encode('utf-8','ignore'))
print('='*10)
print("内容："+text.encode('utf-8','ignore'))
print("NextPageLink: ", next_link)
```