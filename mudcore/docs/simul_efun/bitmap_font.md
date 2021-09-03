
点阵字体显示系统，可以在游戏中显示点阵文字。

### 核心方法

```c
varargs string bitmap_font(string str, int size, string fill, string bg, string fcolor, string bgcolor);
```

> 参数说明

    str     要显示的文字
    size    字体大小，限制为12、14、16，如果省略，默认为12
    fill    填充字符，如果省略默认为`88`
    bg      背景字符，如果省略默认为`  `
    fcolor  字符前景颜色，默认为空
    bgcolor 字符背景颜色，默认为空

### 示例

example 1:

    printf("%s\n",bitmap_font("测试abc"));

display:

    8------8---8-----8------8-------------------------------
    -8-888888--8------8-----8-88------------88--------------
    ---8---8-8-8------------8----------------8--------------
    8--8-8-8-8-8-------888888888------888----8-88-----8888--
    -8-8-8-8-8-8----88------8--------8---8---88--8---8---8--
    --88-8-8-8-8-----8--88888---------8888---8---8---8------
    -8-8-8-8-8-8-----8----8-8--------8---8---8---8---8------
    88-8-8-8-8-8-----8----8--8-------8---8---8---8---8---8--
    -8---8---8-8-----8--8-8--8-8------8888--88888-----888---
    -8--8-8----8-----8-8--88-8-8----------------------------
    -8-8---8-8-8-----88-88----88----------------------------
    -88-------8----------------8----------------------------

example 2:

    printf("%s\n",bitmap_font("测试abc", 16));

display:

    ------------88-----------88-8---------------------------
    -8--88888---88---88------88-88--------------------------
    -88-88888-8-88----88-----88--8----------888-------------
    --8-8---8-8-88----88-8888888888----------88-------------
    ----8-8-8-8-88-------8888888888----------88-------------
    -8--8-8-8-8-88--8888-----88------8888----8888----88888--
    -88-8-8-8-8-88--8888-888888---------88---88-88--88---88-
    --8-8-8-8-8-88----88-888888------88888---88--88-88------
    ----8-8-8-8-88----88--88--88----88--88---88--88-88------
    --8-8-8-8-8-88----88--88--88----88--88---88--88-88------
    --8---8---8-88----88--88--88----88--88---88--88-88---88-
    --8--88-8---88----888-8888-8-88--888-88--88888---88888--
    -88--8--88--88----88888888-8888-------------------------
    -8--88---8-888----88-88-----888-------------------------
    -8--8------88----------------8--------------------------
    --------------------------------------------------------

example 3:

    printf("%s\n",bitmap_font("你好", 16, "HI", "  "));

display:

```



      HI    HI                          HI        HI
      HI    HIHIHIHIHIHIHIHI            HI    HIHI  HIHIHI
    HIHI    HI          HI            HI                HI
  HIHIHI  HI            HI            HI            HIHI
      HI          HI              HIHIHIHIHI        HI
      HI          HI                HI    HIHIHIHIHIHIHIHIHIHI
      HI      HI  HI                HI    HI          HI    HI
      HI    HI    HI    HI            HIHI            HI
      HI  HI      HI      HIHI        HIHIHI        HI
      HI          HI              HIHI      HI      HI
      HI          HI              HI            HIHIHI


```