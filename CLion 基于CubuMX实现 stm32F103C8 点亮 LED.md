@[toc]

# 一、准备工作

## 1、CLion简介

Clion是一款专门开发C以及C++所设计的跨平台的IDE。它是以IntelliJ为基础设计的，包含了许多智能功能来提高开发人员的生产力。这种强大的IDE帮助开发人员在Linux、OS X和Windows上来开发C/C++,同时它还能使用智能编辑器来提高代码质量、自动代码重构并且深度整合Cmake编译系统，从而提高开发人员的工作效率。

## 2、CLion安装

参考：[Windows上CLion配置和使用教程](https://blog.csdn.net/lu_linux/article/details/88713355?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164006425516780274194703%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=164006425516780274194703&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-88713355.pc_search_result_cache&utm_term=clion%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B&spm=1018.2226.3001.4187)

## 3、安装GCC
官方下载地址：[https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)
![在这里插入图片描述](https://img-blog.csdnimg.cn/388fe9efdc7a4ed0b9f100d7871e53b5.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 将bin路径添加到环境变量中
![在这里插入图片描述](https://img-blog.csdnimg.cn/1cb1cef3a2a54c1cadc5cfec25090596.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
 - 右键**此电脑**选择属性

![在这里插入图片描述](https://img-blog.csdnimg.cn/96baf1706c464e518f4566480a98c774.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_15,color_FFFFFF,t_70,g_se,x_16)

 - 选择高级系统设置

![在这里插入图片描述](https://img-blog.csdnimg.cn/9655e8528b6447b99e83f07e0b1adec4.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_15,color_FFFFFF,t_70,g_se,x_16)

 - 选择环境变量

![在这里插入图片描述](https://img-blog.csdnimg.cn/b180be37ceb74eccb1d57300601910a0.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_19,color_FFFFFF,t_70,g_se,x_16)

 - 双击path

![在这里插入图片描述](https://img-blog.csdnimg.cn/8b6ce7c7d00f4bdca1887ee8402e1e56.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 选择新建

![在这里插入图片描述](https://img-blog.csdnimg.cn/8a51e00b982d4334935842cd05fb5fe3.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 将bin目录地址粘贴进去

![在这里插入图片描述](https://img-blog.csdnimg.cn/58ad825c5be14817bfcfd7578f8e9a94.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
打开命令提示符，输入`arm-none-eabi-gcc -v`

![在这里插入图片描述](https://img-blog.csdnimg.cn/f3d07ec3d2924b87bc02298bfdb6d6d3.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
如出现以上内容，则gcc配置完毕。

## 4.安装OpenOCD
官网下载地址：[https://gnutoolchains.com/arm-eabi/openocd/](https://gnutoolchains.com/arm-eabi/openocd/)
![在这里插入图片描述](https://img-blog.csdnimg.cn/4d606fda834843c5906151482fe89e79.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 解压

![在这里插入图片描述](https://img-blog.csdnimg.cn/e8b8656212fd43f3bc54b64d33496802.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

## 5.配置CLion

1、进入 CLion，新建一个工程
![在这里插入图片描述](https://img-blog.csdnimg.cn/c71852067e1d4b22803318864382a8bc.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
2、选择File-Settings-Build-Embedded Development，将右侧的 OpenOCD 文件目录转换到自己下载的位置，最后点击 Test 发现提示颜色为墨绿色，即代表配置成功 。
![在这里插入图片描述](https://img-blog.csdnimg.cn/58faddc9b08a4aadbf7083f30518e15d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 点击test，出现下面提示则代表成功。

![在这里插入图片描述](https://img-blog.csdnimg.cn/1f3b49a387d84852ba74b09947db7c7d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 顺便也更改一下cubeMX。

![在这里插入图片描述](https://img-blog.csdnimg.cn/2f0b6e708ecf443a978bd41a3d758c42.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

# 二、在CLion中使用CubeMX

 - 新建一个STM32CubeMX工程

![在这里插入图片描述](https://img-blog.csdnimg.cn/46ac2d162a034bdea9aa05378dfa894d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 点击`Open with STM32CubeMX`

![在这里插入图片描述](https://img-blog.csdnimg.cn/cba35b8d316c4a9587dfa554c30edf94.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 更换芯片为`STM32F103C8`

![在这里插入图片描述](https://img-blog.csdnimg.cn/d992c3b22591423d80830f4e055d36d3.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 配置`SYS`
![在这里插入图片描述](https://img-blog.csdnimg.cn/cba3156b1da64e02a149cfe2698a1e6c.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
 - 配置`RCC`

![在这里插入图片描述](https://img-blog.csdnimg.cn/92351e0aeaa84d6a9daa0c3d0c79a730.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
选择`PC13`为GPIO_Output来点亮LED灯
![在这里插入图片描述](https://img-blog.csdnimg.cn/6dcaca3a198d4e72958668c5e1f6b9dd.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 配置串口`USTART1`
![在这里插入图片描述](https://img-blog.csdnimg.cn/d696db9cf4754c26aad21784d20c9d61.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
 - 将工程文件名和路径设置成与CLion工程相同，以覆盖原有文件，" Toolchain/IDE "选择 SW4STM32。

![在这里插入图片描述](https://img-blog.csdnimg.cn/5ef8420bc5d94c3d9327f0be2c2e6363.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 覆盖成功

![在这里插入图片描述](https://img-blog.csdnimg.cn/4da3fe952d0d42f78ffbae415decb285.png)

 - 回到clion会弹出一个页面，选择`stm32f103c8_blue_pill.cfg`
![在这里插入图片描述](https://img-blog.csdnimg.cn/a86e6b5735934cc29511120f32e0484f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_14,color_FFFFFF,t_70,g_se,x_16)
 - 在`main.c`中添加以下代码：

```cpp
while (1)
  {
    /* USER CODE END WHILE */
      HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, GPIO_PIN_SET);
      HAL_Delay(500);
      HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, GPIO_PIN_RESET);
      HAL_Delay(500);
    /* USER CODE BEGIN 3 */
  }
  /* USER CODE END 3 */
}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/76b6d02f83334c228361aba49dfbefa9.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)

 - 然后`File-Settings-Build-CMake`，如下图修改，点击OK
![在这里插入图片描述](https://img-blog.csdnimg.cn/f3b55c14a50d481aa20dfee56d3dd443.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
点击绿色小锤子编译，编译成功。
![在这里插入图片描述](https://img-blog.csdnimg.cn/d79717667a594faa8b24adf15ac49e3d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
 - 烧录

![在这里插入图片描述](https://img-blog.csdnimg.cn/c28af331e81a440faf0fb49577e05835.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6I-c5b6Q5Z2kMDAx,size_20,color_FFFFFF,t_70,g_se,x_16)
运行结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/67f549a2a5314455a76911e057dbc7af.gif#pic_center)

# 三、总结
CLion相对于keil方便了很多，减少了很多工作量。

# 四、参考资料
[https://blog.csdn.net/m0_58892312/article/details/121866325](https://blog.csdn.net/m0_58892312/article/details/121866325)
[https://blog.csdn.net/qq_60678931/article/details/121866156](https://blog.csdn.net/qq_60678931/article/details/121866156)
