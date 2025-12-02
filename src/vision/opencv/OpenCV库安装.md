<h1 id="gqqX0">更新软件源</h1>
```bash
sudo apt update
```

<h1 id="bNARX">安装依赖库</h1>
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential libgtk2.0-dev libavcodec-dev libavformat-dev libjpeg-dev libswscale-dev
sudo apt-get install libtiff-dev
sudo apt-get install libgtk2.0-dev
sudo apt-get install pkg-config
```

<h1 id="Idg3l">安装 C++ 版 OpenCV 开发库  </h1>
 最常用的一般就这两个包：  

```bash
sudo apt install libopencv-dev opencv-data
```

装完之后：

+ 头文件大多在：`/usr/include/opencv4`
+ 库文件大多在：`/usr/lib/x86_64-linux-gnu`
+ 可以使用opencv_version来查看安装的OpenCV版本![](https://cdn.nlark.com/yuque/0/2025/png/60941281/1763985405492-deee50bb-9275-4db3-852c-08751ccae20c.png)

<h1 id="ffW6x">CMake引入OpenCV库</h1>
在 CMake 里可以这样引入OpenCV 库（学习CMake时的万能工程头）：

```cmake
cmake_minimum_required(VERSION 3.22)
project(test LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

file(GLOB_RECURSE SRC_FILES "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include")

add_executable(${PROJECT_NAME} ${SRC_FILES} main.cpp)

find_package(OpenCV REQUIRED)

target_include_directories(${PROJECT_NAME} PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} PRIVATE ${OpenCV_LIBS})

```



<h1 id="qCJ6s">最小可运行样例</h1>
 目录结构  

```bash
zjq@LAPTOP-SC5UT2N7:~/opencv_test$ tree
.
├── CMakeLists.txt
├── lenna_img.webp
└── main.cpp

0 directories, 3 files
```

/main.cpp

```cpp
#include <opencv2/opencv.hpp> //加载 OpenCV 4.1 头文件
#include <iostream>

int main() {
    cv::Mat img; //声明一个保存图像的类
    img = cv::imread("lenna_img.webp"); //读取图像，根据图片所在位置填写路径即可
    if (img.empty()) { //判断图像文件是否存在
        std::cout << "请确认图像文件名称是否正确" << std::endl;
        return -1;
    }
    cv::imshow("test", img); //显示图像
    cv::waitKey(0); //等待键盘输入

    return 0; //程序结束
} 
```

/CMakeLists.txt

```cmake
cmake_minimum_required(VERSION 3.22)
project(test LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(${PROJECT_NAME} main.cpp)

find_package(OpenCV REQUIRED)

target_include_directories(${PROJECT_NAME} PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} PRIVATE ${OpenCV_LIBS})

```

效果展示：

[OpenCV.mp4](https://www.yuque.com/attachments/yuque/0/2025/mp4/60941281/1763987657772-484000ee-2a15-4862-87e6-5f2c6ad82dce.mp4)

