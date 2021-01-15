# 更新记录

## 202101015
- 时间格式修改
- 优化倒计时  
- 集成pyautogui，避免被淘宝检测出是无头浏览器的点击（解决提交结算无效的情况，此原因由淘宝检测导致）
    - 安装命令：```python -m pip install pyautogui```
- 增加getxy.py文件，输出自己电脑屏幕的宽高  
- 增加四个参数，config.ini文件中配置
  - 屏幕的宽高，单位：毫米
  - 结算按钮的宽高，单位：毫米
  - （浏览器全屏，在购物车页面，量出结算按钮的坐标。购物车只有一个商品的情况）



以上是基于原作者的代码进行的一些优化和修改。  

以下为原作者的说明：

# taobao_seckill
淘宝、天猫半价抢购，抢电视、抢茅台，干死黄牛党
## 依赖
### 安装chrome浏览器，根据浏览器的版本找到对应的[chromedriver](http://npm.taobao.org/mirrors/chromedriver/)

## 使用说明
1、安装Python3.7.3
2、安装第三方依赖文件，在根目录下执行 ```pip3 install -r 3.txt```
3、安装pyautogui，避免被淘宝检测出是无头浏览器的点击，```python -m pip install pyautogui```
4、安装chrome驱动，[chromedriver](http://npm.taobao.org/mirrors/chromedriver/)，下载驱动后Mac osx将驱动放入任意位置，修改seckkill/settings.py文件中的文件位置；Windows将驱动放入chrome与Python根目录。
1、抢购前需要校准本地时间，然后把需要抢购的商品加入购物车  
2、直接在项目根目录下 执行 ```python3 main.py```  
3、程序运行后，会打开淘宝登陆页，需要自己手动点击切换到扫码登陆  

## 淘宝有针对selenium的检测，如果遇到验证码说明被反爬了，遇到这种情况应该换一个方案，凡是用到selenium的都会严重依赖网速、电脑配置。
## 如果想直接绕过淘宝的检测，可以手动打开浏览器登陆淘宝，然后再用selenium接管浏览器。只提供思路，具体实现大佬们可以自己摸索。
