**React-native环境的搭建**
### 安装依赖
> 在这里我把用的软件全部都传到了我的百度网盘上，可以直接去下载：
#### license文件
- 链接：http://pan.baidu.com/s/1dERyeop
- 密码：wyoq
#### adt文件，包含eclipse和sdk文件
- 链接：http://pan.baidu.com/s/1mhFE3SO
- 密码：atq8
#### jdk文件
- 链接：http://pan.baidu.com/s/1dFvknHf
- 密码：11qg
#### pyhton文件
- 链接：http://pan.baidu.com/s/1jHLioia
- 密码：ab3e
#### gradle文件
- 链接：http://pan.baidu.com/s/1c2aT4xM
- 密码：92tj
### 安装软件
> 我建议大家把软件安装到D盘；
### 安装jdk
##### 修改环境变量
- 在系统变量里添加：

```
变量名：JAVA_HOME
变量值：你安装的jdk的位置
```
- 修改环境变量path

```
%JAVA_HOME%/bin;
```
> 写在变量的最前边；
- 添加环境变量classpath

```
%JAVA_HOME%/lib/dt.jar;%JAVA_HOME%/lib/tools.jar
```
- 验证

```
在命令行里分别输入:
java -version
javac
```
### 搭建android环境
#### 安装sdk和eclipse

```
这里用的就是上面的adt文件，解压完以后，里面就包含了sdk和eclipse
```
#### 配置环境变量

```
变量名：ANDROID_HOME 
变量值：你安装sdk的文件位置
```
#### 修改环境变量path

```
;%ANDROID_HOME%/tools;%ANDROID_HOME%/platform-tools;
```
#### 验证

```
在命令行里输入：
android
```
### 安装Node, Python2

```
安装完以后检查是否安装成功
node -v
python -V
```
### 安装react-native
- 全局安装

```
npm install -g react-native-cli
```
> 如果安装的时候比较慢的话，这里有两个淘宝镜像，可以使用镜像安装：

```
npm config set registry https://registry.npm.taobao.org --global
npm config set disturl https://npm.taobao.org/dist --global
```
- 创建目录

```
react-native init test
```
- 进入项目目录

```
cd test
```
- 连接真机

```
如果要让它跑起来的话就必须要有一个安卓设备，虚拟机和真机都可以，这里我就连接上了一个真机
```
- 运行

```
react-native run-android
```
### 解决运行问题
> 这里我在运行的时候遇到一个错误，报错的是adb没有配置环境：
- 报错内容

```
02:49:39 E/ddms: 'E:\android\sdk\platform-tools\adb.exe,start-server' failed -- run manually if necessary
                                                                                                          :app:installDebug                                                                                                                    FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:installDebug'.
> com.android.builder.testing.api.DeviceException: java.lang.RuntimeException: Timeout getting device list.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

BUILD FAILED

Total time: 43.302 secs
Could not install the app on the device, read the error above for details.
Make sure you have an Android emulator running or a device connected and have
set up your Android development environment:
https://facebook.github.io/react-native/docs/android-setup.html
```
- 解决方法

```
1.把sdk添加到环境变量里面：
变量名：android
变量值：你abd文件所在的位置
2.修改环境变量：
添加%android%
```
> 这样一来我们的问题就解决了，然后重新打开命令窗口，输入react-native run-android就可以了；


















