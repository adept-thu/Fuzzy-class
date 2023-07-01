# Fuzzy-class
为fuzzy-nms生成模糊分类的代码

生成的.so库用来做模糊分类

1.文件夹目录说明：
src为源文件夹
lib为动态链接库文件夹
include为头文件夹
build为中间编译文件
bin为测试动态链接库生成的可执行文件

2.代码使用说明：
#进入build文件夹
cd build
#进行编译 生成.so文件以及测试代码的二进制文件
cmake ..
make
#进入bin文件夹
./test 即可使用测试代码
