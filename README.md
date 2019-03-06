## Ubuntu聊天机器人

可以通过语音对话进行聊天,通过讯飞的语音接口和图灵机器人的文本聊天接口实现

在ubuntu下用cmake->make编译该文件,即可直接使用

在工程文件夹下建立文件夹build

```sh
cd build
cmake ..
make

```
中间报错可能是源文件中找不到<jsoncpp/json/json.h>和<curl/curl.h>这两个库

命令行中输入：
```sh
sudo apt-get install libjsoncpp-dev curl 
```
安装,一般应该都会有这两个库
