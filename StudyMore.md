# 知识学杂了!

## linux

#### linux 查看当前时间和时区

```linux
date -R
```

## Redis

#### redis 切换db

```
SELECT 2 
切换到db2
```

#### redis 获取键的具体值

```
GET ahhuali.com
```

## Python

#### 字符串截取

```python
str = '12345678'
print str[0:1]  # 注意是:不是,
>> 1			# 输出str位置0开始到位置1以前的字符
```

#### 字符串删除空格

```python
a.strip()
```

# bug解决

#### selenium.common.exceptions.WebDriverException: Message: ‘chromedriver‘解决

找到对应本地浏览器的chromedriver 放置到python根目录下就行了
