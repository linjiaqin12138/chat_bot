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
