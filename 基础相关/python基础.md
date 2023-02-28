# python基础
    python官网: https://www.python.org
* <b>安装</b> 
    * 安装第一步
        install now(默认安装)
        customize installation(自定义安装)
        下面勾选项第二个选中(添加环境变量)
        
    * 安装第二步
        documentation 加载文档文件
        pip pip指令,用于安装python包
        td/tk and IDLE 图形化界面显示安装
        python test suite测试工具
        py launcher py文件加载器
        for all user

    * 安装第三步
        install for all users
        √ associate files with python
        √ create shortcuts for installed applications
        √ add python toenvironment variables
        precompile standard library
        download debugging symbols
        download debug binaries

    * 修改安装路径

    * 测试是否安装成功
        点击电脑左下角按钮，输入cmd 进入命令行
        在命令行中输入python，正确显示python版本则表示成功

        如果在命令行中输入python出现如下：
            ython不是内部或者外部命令，也不是可运行的程序或批处理文件

        可能因为在安装python的过程中没有勾选add python 3.7 to PATH选项，此时需要手动对Python进行配置。

    * 手动配置python
        注意：如果在安装过程中，已经勾选了add python 3.7 to PATH选项，并且在cmd命令模式下输入python指令不报错，就不需要再手动的配置python
            右键 此电脑 --> 选择 属性
            选择 高级系统设置 --> 环境变量 --> 找到并双击 Path
            双击Path --> 在弹窗里点击新建，找到Python的安装目录，把路径添加进去
            (这里新添加的路径是Python安装好之后，python.exe这个可执行文件所在的目录)
* <b>pip的使用</b>
    pip是一个现代的，通用的Python包管理工具，提供了对Python包的查找、下载、安装、卸载的功能，便于我们对Python的资源包进行管理

    * 安装
        在安装python的时候会自动下载并且安装pip
    * 配置
        在windows命令行输入 pip -V可以查看pip的版本(注意是根目录)

        如果命令里出现：pip不是内部或外部命令，也不是可运行的程序或批处理文件

        可能是因为在安装python的过程中未勾选add python 3.7 to PATH选项，需要手动的配置pip的环境变量
        ·右键 此电脑 --> 环境变量 --> 找到并且双击 Path --> 在弹窗里点击新建 --> 找到pip的安装目录，把路径添加进去(在python下面的scripts里面)
    * 使用pip管理python包(建议安转在 python的文件夹下的scripts的文件夹中)
        如果安装的不是C盘，那么首先切换盘符，切换方式为 盘符加冒号，以E盘为例：E:
        再通过cd加文件夹命的方式进入到文件夹中
        ·pip install <包名> 安装指定的包
        ·pip uninstall <包名> 删除指定的包
        ·pip list 显示已经安装的包
        ·pip freeze 显示已经安装的包，并且以指定的格式显示
    * 修改pip下载源
        运行pip install命令会从网站上下载指定的python包，默认是从 https://files.pythonhosted.org/ 网站上下载。这是个国外的网站，遇到网络情况不好的时候，可能会下载失败，我们可以通过命令，修改pip下载软件时的源

        格式：pip install 包名 -i 国内源地址
        ```
        示例：pip install ipython -i https://pypi.mirrors.ustc.edu.cn/simple/ 就是从中国科技大学的服务器上下载requests(基于python的第三方web框架)

        国内常用的pip下载源列表：
        阿里云 http://mirrors.aliyun.com/pypi/simple/
        中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/
        清华大学 https://pypi.tuna.qinghua.edu.cn/simple/
        中国科学技术大学 http://pypi.mirrors.ustc.edu.cn/simple/
        ```
* <b>运行python程序</b>

    * 终端运行(不使用)
        * 直接在python解释器中书写代码
        先在命令行中输入python然后出现>>>在后面写入要写的代码，例
        print('苍茫的天涯是我的爱')
            * 退出python环境两种方式
                * exit() 回车
                * Ctrl + z 回车
    * 运行python文件
        新建一个txt文档，然后把文档的后缀改成.py。在文档中写入代码，需要运行时进入终端，输入python然后后面加一个空格，再把文件拖进终端里面，后面会显示文件的路径，直接运行即可。
    * pycharm
        尽管上面介绍的方法已经能够提高我们的编码速度，但是仍然无法应对我们开发中更加复杂的要求，一般情况下，我们都要借助工具来辅助我们快速的搭建环境，编写代码以及运行程序。

        * IDE的概念
            IDE又称为集成开发环境，就是一款图形化界面的软件，它集成了编辑代码，编译代码，分析代码，执行代码以及调试代码的功能，在我们python开发中，最常用的IDE就是pycharm http://www.jetbrains.com/pycharm/download(下载社区版本 community，专业版花钱)
        
        * pycharm安装
            * 双击安装

            * 自定义安装路径

            * 编辑设置(全部选中)

            * 开始的文件夹(默认就行)

            * 安装完成后双击
                如果是第一次使用的话选择不导入设置
                设置ui主题，喜欢就好
                下载一些配置可以下可以不下

            * 运行pycharm
                如果要新建项目，选择create new project，创建一个新的python工程
                如果要修改代码或者添加功能选择open

            * 创建文件的位置，并且点开下箭头
                new environment using表示创建一个项目就有一个单独的环境

                选择已存在的解释器(下面一个选项) interpreter
                选择路径，找到安装路径里python文件夹然后找到tools里的python.exe(如果找不到自己python安装在哪可以使用cmd的where python命令来查看路径，在windows环境下可能文件会被隐藏而IDE可能找不到文件夹，解决办法可以点击IDE上眼睛的标志用来显示隐藏文件夹)
                并且勾选上下面的选项，后面都使用这个环境
            
            * 创建新项目时在IDE文件夹上右键选择new --> python file --> 输入文件名，加不加后缀都行

            * 如果要改变文字大小
            File --> Settings --> Editor --> Font

            * 运行
            在代码写好后在空白处右键，Run (文件名) 即可

            * 下部终端可选择terminal，可在其中输入代码，效果和终端是一样的

            * 在实际的开发中可以对pycharm进行设置，在每次写项目的时候都会生成相应的内容(例如修改者之类的)
            File --> Settings --> File and Code Templates --> python script 在文件中添加想要的注释，例如
                ```
                时间 # @Time : ${DATE} ${TIME}
                作者 # @Author : lj
                文件名 # @File : ${NAME}
                项目名 # @Project : ${PROJECT_NAME}
                ```
* <b>python语法</b>
    * 注释：
    
        * 在我们工作编码过程中，如果一段代码的逻辑比较复杂，不是特别容易理解，可以适当的添加 注释，以辅助自己或者其他编码人员解读代码

        * 注释以#开头

        * 单行注释以#开头即可
          多行注释以'''开始'''结束 可用作函数功能提示

    * 变量
        对于重复使用，并且经常需要修改的数据，可以定义为变量，来提高编程效率，定义变量的语法为： 变量名 = 变量值
        weather = '今天下雨了'
        变量可以随时进行修改

    *   变量的类型
        * number  
            int(有符号整型)
            long(长整数[也可以代表八进制和十六进制]) (老版本)
            float(浮点型)
            complex(复数)

        * 布尔类型    
            true
            false
    
        * string(字符串)
            如果想要在输出的时候保留字符串的格式，例如古诗之类的可以使用三引号''' '''

        * list(列表)

        * Tuple(元组)

        * Dictionary(字典)

        python的数据交换比较简单，如果想要交换a,b的值，一般情况会需要第三个值作为中转，但是python可以直接交换。
        a,b = b,a

    * 变量类型的基本使用
        ```
        int： money = 500
        float： price = 1.5
        boolean： 一般使用在流程控制上还有性别变量，在表示性别的时候男是true 女是false    sex = True  gender = False
        string： weather = '今天下雨了'
        list: name_list = ['张三','李四','王二麻']
        tuple：age_tuple = (18,19,20)
        dict：应用场景在scrapy框架中使用 person = {'name':'张三','age':18}
        ```

    * 查看数据类型
    在python中只要定义一个变量，而且他有数据，那么他的类型就已经确定了，不需要咱们开发者主动的去说明他的类型，系统会自动辨别。也就是说在使用的时候'变量没有类型，数据才有类型'
    想要查看变量存储的数据类型，可以使用type(变量的名字),来查看变量存储的数据类型

    * 标识符和关键字
    标识符是用户编程时使用的名字，用于给变量、常量、函数、语句块等命名，以建立起名称与使用之间的关系
        * 标识符由字母、下划线和数字组成、且数字不能作为开头
        * 严格区分大小写
        * 不能使用关键字
        * 定义标识符的时候最好是有含义的，可以使用驼峰命名


    * 类型转换
        ```
        int(x) 将x转换为一个整数 
            如果将float转int返回的是小数点前的数
            如果将Boolean转int返回的是 true->1 false->0
            有几种情况会转换失败例如 '1.23'转int会报错
            '12ab'转int会报错

        float(x) 将x转换为一个浮点数
            如果将int转float返回的是 int的值后面加.0

        str(x) 将对象x转换为字符串

        bool(x) 将对象x转换成布尔值
            如果对非0的整数(包含正数和复数)进行bool、类型的转换 那么就全都是True，在整数的范围内0强制转换为bool类型的结果为false

            将浮点数转换为bool类型的数据的时候，正的浮点数和负的浮点数的结果是true，如果是0.0那么结果是false

            只要字符串中有内容(不管是啥哪怕是空格) 那么在强制类型转换为bool的时候返回true，反之为false

            只要列表中有数据 那么强制类型转换为bool的时候 就返回true，反之为false

            只要元组中有数据 那么强制类型转换为bool的时候 就返回true，反之为false

            只要字典中有数据 那么强制类型转换为bool的时候 就返回true，反之为false
        ```
    * 运算符
        ```
        算数运算符 例 a=3 b=2
        '+' 加 a+b = 5
        '-' 减 a-b = 1
        '*' 乘 a*b = 6
        '/' 除 a/b = 1.5
        '//'取整除 整除为取整数没有浮点数 a//b=1
        '%' 取余 a%b = 1
        '**'指数 幂运算
        '()'小括号 提升优先级

        扩展
        a = '123'
        b = '456'
        a+b = '123456'

        a = '123'
        b = 456
        a+b会报错 在python中只有两边都是字符串才会进行拼接

        a = '下雨了'
        a * 3 字符串的乘法是将字符串重复多少次
        ```
    * 赋值运算符

        就是把=号右边的结果赋给左边的变量
        ```
        b = c =20
        print(b)//20
        print(c)//20

        d,e,f = 1,2,3
        print(d)//1
        print(e)//2
        print(f)//3
        ```
    * 符合赋值运算符
        ```
        +=       c+=a 等效于 c=c+a
        -=       c-=a 等效于 c=c-a
        *=       c*=a 等效于 c=c*a
        /=       c/=a 等效于 c=c/a
        //=       c//=a 等效于 c=c//a
        %=       c%=a 等效于 c=c%a
        **=       c**=a 等效于 c=c**a
        ```    

    * 比较运算符
        ```
        == 等于
        != 不等于
        > 大于
        >=大于等于
        < 小于
        <=小于等于
        ```
    * 逻辑运算符
        ```
        and 必须全为true才会返回true

        a = 1
        b = 3
        print(a and b) #输出结果为3 当两个值都是非零数字的情况下输出的是后面的值，只要有一边为0结果为0

        or  有一个true就会返回true

        a = 1
        b = 3
        print(a and b) #输出结果为1 当第一个值为非零数的时候就输出前面的值

        not 非 取反 not true --> false
        ```
    * 逻辑运算符的性能提升
        ```
        a = 36 

        a > 10 and print('成功打印')  // 会打印
        a < 10 and print('成功打印')  // 不会打印
        and的性能优化 当and前面的结果为false的情况下 那么后面的代码就不再执行

        a > 37 or print('成功打印')  // 会打印
        a < 37 or print('成功打印')  // 不会打印
        or的性能优化 只要一方为true了那么结果就是true，下面的代码前半部已经为true了所有后面的代码就不会执行
        ```
    * 位运算符
        ```
        & 按位"与"运算符：参与运算的两个值，如果两个相应位都为1，则结果为1，否则为0

        | 按位"或"运算符：只要对应的两个二进制位有一个为1时，结果为1

        ^ 按位"异或"运算符：当两对应的二进制位相异时，结果为1

        ~ 按位"取反"运算符：对数据的每个二进制位取反，即把1变为0，把0变为1

        << "左移动"运算符：运算数的各二进制位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0  左移1位相当于乘2

        >> "右移动"运算符：运算数的各二进制位全部右移若干位，由">>"右边的数指定移动的位数 右移1位相当于整除2

        [详细解释](https://www.bilibili.com/video/BV1Th411W7bo?p=15&spm_id_from=pageDriver&vd_source=b39e3a2bc7c158b5c72845e8050ac0a7) 2：44位置
        ```
    * 成员运算符
        ```
        in ：当在指定的序列中找到值时返回True，否则返回False
        not in：当在指定的序列中没有找到值时返回True，否则返回False
        ```
    * 身份运算符
        ```
        is ：判断两个标识符是否引用自同一个对象，若引用的是同一个对象返回True，否则返回False
        is not ：判断两个标识符是否引用自不同对象，若引用的不是同一个对象返回True，否则返回False
        ```
    * 输入输出
        ```
        普通输出 
        print

        格式化输出(scrapy框架的时候用到，当把爬取到的数据要放到excel文件 mysql redis中的时候)
        %% 代表的是输出%号
        %s 代表的是字符串  
        %d 代表的是有符号的十进制整数
        %f 代表的是浮点数
        %c 代表的是字符
        %u 代表的是无符号十进制整数
        %o 代表的是八进制整数
        %x 代表的是十六进制整数(小写字母0x)
        %X 代表的是十六进制整数(大写字母0X)
        %e 代表的是科学计数法(小写'e')
        %E 代表的是科学计数法(大写'E')
        %g 代表的是%f和%e的简写
        %G 代表的是%f和%E的简写
        字符串后先写%然后接()，里面是要放进去的数据,如果只有一个数值的话就不用括号了
        
        age = 18
        name = '张三'
        print('我的名字是%s,我的年龄是%d' % (name,age))

        name = '李四'
        age = 26 
        money = 999.9

        print('%d岁的%s一首歌赚了%f块钱' %(age,name,money)) # 26岁的李四一首歌赚了999.9000块钱
        print('%s岁的%s一首歌赚了%s块钱' %(age,name,money)) # 26岁的李四一首歌赚了999.9块钱 
        数据给的整型，而前面的占位符是字符型却依然打印出了正确的结果，是因为此处做了一个强转，把整型转换成了字符型，如果不能转成字符型的则会报错

        print('%d岁的%s一首歌赚了%.1f块钱' %(age,name,money)) # 26岁的李四一首歌赚了999.9块钱 此处的浮点型设置了小数点的位数
        ```

    * 输入
        ```
        input('请输入您的密码')
        可用于定义变量，然后输入
        password = input('请输入您的密码')
        ```
    * 进制转换
        ```
        n = 149
        print(bin(n)) #bin()为十进制转二进制结果为 0b10010101 只要前面有0b就表示为二进制
        
        print(oct(n)) #oct()为十进制转八进制 0o225 0o表示八进制

        n = 221
        print(hex(n)) #hex()为十进制转十六进制 0xdd 0x表示十六进制

        n = 0x558
        print(int(n)) #十六进制转十进制 1368
        print(oct(n)) #十六进制转八进制
        print(bin(n)) #十六进制转二进制 bin()函数无论什么进制的数，放里面都能转为二进制

        如何在手算中快速写出二进制码
        二进制的四位 1111 也叫做 8421码，最大值为15，而十六进制最大值也为15，所以4位能表示十六进制的一位数,而转八进制的话则是3位来表示。即二进制转十六进制，将二进制从右侧开始4位一组，最后不足4位补0，二进制转八进制，将二进制从右侧开始3位一组，最后不足3位补0
        0x  5    5    8
        0b 0101 0101 1000

        0x  a    c     3
        0b 1010 1100  0011
        ```
    * 位运算
        针对二进制进行的运算
        ```
        & | ^ ~ >> <<

        & 类似于and
            F and F -----> F
            T & T -----> T

        n1 = 0b0110 #6
        n2 = 0b0010 #2
        print(n1 & n2) #2 
        计算过程
        1为真 0为假
        上下相同则为相同的数，不同则为0
            0b 0110
            0b 0010
        结果 0b 0010 所以结果为2

        | 类似于 or
            一个为真则为真
        n1 = 0b0110 #6
        n2 = 0b0010 #2
        print(n1 | n2) #2 
        计算过程
        1为真 0为假
        上下相同则为相同的数，不同则为1
            0b 0110
            0b 0010   
        结果 0b 0110 所以结果为6


        ^ 按位异或运算：当两个对应的二进制位相异时，结果为1
        n1 = 0b0110 #6
        n2 = 0b0010 #2
        print(n1 | n2) #2 
        计算过程
        1为真 0为假
        上下相同则为相同为假，不同则为真
            0b 0110
            0b 0010   
        结果 0b 0100 所以结果为4

        ~ 取反运算符
        n1 = 0b0110 #6
        print(~n1)
        整数为
            0b 0110
        结果
        二进制的负数表示(二进制一个字符是8个比特位，前面的表示符号，最高位为1为负数，0为正数)
        原码 0000 0110
        反码 1111 1001
        补码 反码+1  1111 1010 前面再加上表示

        负的二进制转十进制步骤
        1.二进制(负的) 2.二进制减1 3.取反 4.原码 5.转十进制


        n = 12 # 0000 1100

        print(n << 2) #左移两位 0011 0000 = 48
        print(n << 3) #左移三位 0110 0000 = 96
        所以相当于乘以2的移动位数的次方，也就是每移动一位表示乘以2

        print(n >> 1) #右移一位 0000 0110 = 6
        print(n >> 2) #右移两位 0000 0011 = 3
        print(n >> 3) #右移三位 0000 0001 = 1
        所以相当整除2，每移动一位表示除以2
        ```
        
    * 流程控制语句
        * if判断语句
            ```
            如果判断条件为true的时候才会执行if下面的内容
            if语句是用来进行判断的其使用格式如下，下面的代码必须有一个tab缩进

                if 要判断的条件：
                    条件成立时，要做的事
        
            age = 30 
            if age >= 18:
                print('我已经成年了') 
            结果为 输出打印

            如果需要使用input输入参数的话，参数的类型为string类型

            age = input('请输入你的年龄')

            print(type(age)) //str
            所以如果需要和int类型进行比较的话我们就要使用强制类型转换

            age = int(input('请输入你的年龄'))

            if age >= 18:
                print('我已经成年了') 
            这样就可以进行比较了
            ```
            ```
            if else语句
            格式为

            if 判断条件:
                判断条件为true的时候执行的代码
            else:
                判断条件为false的时候执行的代码


            age = 19

            if age > 18:
                print('可以去网吧了')
            else:
                print('回家写作业')

            ```
            ```
            elif的功能
            elif的使用格式如下

                if xxx1:
                    事情1
                elif xxx2:
                    事情2
                elif xxx3:
                    事情3
        
            说明:
                当xxx1满足时，执行事件1，然后整个if结束
                当xxx1不满足时，那么判断xxx2，如果xxx2满足，则执行事件2，然后整个if结束
                当xxx1不满足时，xxx2也不满足，如果xxx3满足，则执行事件3，整个if结束
                (经典的判断分数档次的问题，相当于else if)

            如果if后面的表达式是：None、""(空字符串)、0、0.0、[]、()、{}等都认为是False

            三元表达式
            a = 1
            b = 2 
            c = a if a < b else b
            相当于
            if a < b:
                c = a 
            else:
                c = b
            ```
        * while循环
        首先判断条件表达式的值，其值为True时，则执行代码块中的语句，当执行完毕后，再回过头重新判断表达式的值是否为真，若仍为真，则继续重新执行代码块，如此循环，直到条件表达式的值为False，才终止循环。
            ```
            i = 1
            while i <= 10:
                print(i)
                i+=1
            print('打印完毕')
            while循环务必注意三点1.变量的初始化 2.条件表达式 3循环体重变量要发生变化，否则容易死循环。

            例：
            打印1-50之间能被3整除的数字

            n = 1

            while n <= 50:
                if n%3==0:
                    print(n)
                n += 1
            
            或者
            n = 3

            while n<= 50:
                print(n)
                n += 3
            
            打印1-10之间的数字累加
            n = 1
            sum = 0
            while n <= 10:
                sum += n
                n += 1
            
            购物
            total = 0
            while True:
                # 先买
                price = float(input('输入价格：'))
                number = int(input('输入数量：'))
                # 累加
                total += price * number

                # 判断是否继续购买
                answer = input('当前商品总额：%.2f,是否继续添加商品(q表示退出)？' % total)

                if answer == 'q'
                    break
            print('所有商品的总额是：%.2f' % total)

            多次猜数猜对位置，如果猜错给出提示，猜大了还是猜小了

            import random
            ran = random.randint(1,50)
            #循环猜多次
            while True:
                guess = int(input('猜一个1-50之间的数'))
                #猜对就结束
                if guess == ran:
                    print('恭喜猜对了！')
                    break
                elif guess> ran:
                    print('猜大了，小一点')
                elif guess< ran:
                    print('猜小了，大一点')

            猜拳三局两胜
            import random
            n = 1
            #计数
            p_count = 0
            m_count = 0
            while n <= 3:
                #猜拳
                #机器产生数字0 1 2代表剪刀石头布
                ran = random.randint(0,2)
                #人猜数字
                guess = int(input('请输入：剪刀(0) 石头(1) 布(2)'))
                #比较判断
                if guess== 0 and ran==2 or guess==1 and ran==0 or guess==2 and ran==1:
                    print('我赢了')
                    p_count += 1
                elif ran ==0 and guess == 2 or ran== 1 and guess == 0 or ran == 2 and guess == 1:
                    print('机器赢了')
                    m_count += 1
                else:
                    print('本轮平局')
                n += 1
            #比较胜负
            if p_count > m_count:
                print('我赢了')
            elif p_count < m_count:
                print('机器赢了')
            else:
                print('平局')
            ```

            
        * for循环
            ```
            for循环的格式
                for 临时变量 in 列表或者字符串等可迭代对象
                    循环满足条件时执行的代码
            
            for的运用

            # 循环输出字符串
            s = 'china'
            for i in s:
                print(i)

            #range方法的结果是一个可以遍历的对象
            #range(5) 为 0~4 左闭右开区间
            for i in range(5):
                print(i) // 结果为 0 1 2 3 4

            #range(1,6)
            for i in range(1,6):
                print(i) // 1 2 3 4 5

            #range(1,10,3) // 第三个参数为步长
            for i in range(1,10,3):
                print(i) // 1 4 7

            #循环一个列表
            #使用len()可以来判断列表元素的个数
            a_list = ['周杰伦','林俊杰','陶喆']
            for i in a_list:
                print(i)

            如果想要遍历列表的下标
            for i in range(len(a_list)):
            ```
        * for while 和 else连用
        python中无论是while还是for，其后都可以紧跟着一个else代码块，它的作用是当循环条件为False跳出循环时，程序会最先执行else代码块中的代码
            ```
            i =1
            total = 0
            while i <= 5:
                total += i
                i += 1
            else:
                print('累加和是：'，total)

            i = 1
            total = 0
            while i <= 5:
                total += i
                i += 1
                if i == 3:
                    print('遇到3就跳出循环')
                    break    如果是continue的话就是跳过下面的代码执行下一次的循环
            else:
                print('累加和是：', total)
            
            for循环和else连用的时候，如果上面的for循环没有出现中断(break)的情况,则进入else
            例：密码输错3次账户锁定

            for i in range(3)
                username = input('用户名：')
                password = input('密码：')
                if username == 'admin' and password == '1234':
                    print('用户登录成功！')
                    break
                print('用户密码错误')
            else:
                print('账户锁定')
            
            else的特点：不被中断则执行，否则不执行
            ```


    
    * 数据类型高级

        * 字符串高级
            ```
            可以在字符串中使用"\"来表示转义，也就是说后面的字符不在是原先的意义了例如\n表示换行 \t表示制表符
            字符串可以'r'或者'R'开头，这种字符串被称为原始字符串
            字符串*3是字符串重复出现3次
            获取长度: len 可以获取字符串的长度 len()
            查找内容: find 查找指定内容在字符串中第一次出现的位置，找不到就是-1，默认是从左边开始查，如果想从右边开始查的话就用rfind，index的效果也是查找，但是index找不到不会返回-1而是直接报错
            判断: stratswith endswith (判断以什么开头，以什么结尾) isalpha isdigit isalnum isspace 返回值都是布尔值
            计算出现的次数: count 
            替换内容: replace 
            切割字符串: split
            修改大小写: upper,lower
            空格处理: strip
            字符串拼接: join
            切片：[start:end]  [start:end:step]
            字符串的strip方法可以帮我们去除字符串两端的空格。strip方法还有Istrip和rstrip两个版本，格式化字符串：就是将字符串按照指定的格式输出，可以使用%，format或者字符串前加上'f'来格式化字符串

            s = 'aaab'
            s.count('a') // 3

            s = 'cccddd'
            s.replace('c','a') // 用a替换c aaaddd

            s = '1#2#3'
            s.split('#') // ['1','2','3']

            s = 'china'
            s.upper() // 将小写字母变成大写

            s = 'CHINA'
            s.lower() // 将大写变成小写

            s = 'a'
            s.join('hello') // haealalao

            s = 'sdasdassa56sda54d54'
            s.stratswith('sdsd') #false
            s.endswith('sdsd') #false

            s = 'sds'
            s.isalpha() #是否是纯字母组成的
            s.isdigit() #是否是数字组成的
            s.isalnum() #是否是字母和数字组成的
            s.isspace() #是否是空格


            s = 'abc123456'
            print(s[0:3]) //abc 包前不包后 意为从0到2 如果end不写的话就是从你设置的起始位到最后 如果start不传的话就是从起始一直到end值的前一位
            print(s[0:6:2]) // ac2
            print(s[:6:3]) //a1
            print(s[:6:-1]) //65 如果step为负数的话就是从后往前取
            print(s[:-7:-2]) //642
            
            切片
            切片是指对操作的对象截取其中一部分的操作，字符串、列表、元组都支持切片操作

            切片的语法:[起始:结束:步长]，也可以简化使用[起始:结束]
            注意:选取的区间从'起始'位开始，到'结束'位的前一位结束(不包含结束位本身)，步长表示选取间隔

            s = 'Hello world'

            s[4] // o
            s[3:7] // lo w 从下标3到下标6
            s[1:] // ello world  如果只有起始位没有终止位那么就到最后一位结束
            s[:4] //hell 如果只有结束位没有起始位那就是从头到结束位的前一位位置
            s[0:6:2] // hlo 步长为2的话表示隔一个截取一个

            name = 'lj'
            job = 'it'
            print('%s是一位%s' % (name,job)) // lj是一位it
            print('{}是一位{}'.format(name,job))  // lj是一位it {}里也可以使用索引，例如前一个括号填0后一个括号填1这样显示结果不变
            print(f'{name}是一位{job}') // lj是一位it

            s = 'abcd123'
            for i in s:
                print(i) #可以遍历字符串

            例：找出字符串中的数字相加
            s = 0
            for i in '6dfdf989dfs3':
                i.isdigit():
                    s += int(i)

            str.format方法
            使用方法：print('要借阅的书名是：{}，借阅的数量是：{}'.format(bookname,number))
            
            ```
        * 列表高级
            ```
            append 在末尾添加元素
            insert 在指定位置插入元素,后面的元素往后挪
            extend 合并两个列表
            切片使用和字符串相同
            sort 排序
            clear 删除 清空列表里的所有元素
            reverse 元素反转
            count 获取元素个数

            food_list = ['小炒肉','回锅肉']
            food_list.append('粉蒸肉') //['小炒肉','回锅肉','粉蒸肉']

            char_list = ['a','c','d']
            char_list.insert(1,'b') //['a','b','c','d']

            num_list = ['1','2','3']
            num1_list = ['4','5','6']
            num_list.extend(num1_list) //['1','2','3','4','5','6']

            修改元素
            city_list = ['北京','上海','广州']
            city_list[0] = '南昌' // ['南昌','上海','广州']
            
            查找元素
            python中查找的常用方法
                in(存在),如果存在那么结果为true，否则为false
                not in(不存在),如果不存在那么结果为true，否则为false

                food_list = ['小炒肉','回锅肉']
                food = input('请输入您想吃的食物')
                if food in food_list:
                    print('在')
                else:
                    print('不在')
                
                使用count去进行判断
                n = items.count('要查找的值')  如果为0则表示没有该值
            
            删除元素
                del:根据下标进行删除
                pop:删除最后一个元素 也可以传入下标去指定删除
                remove:根据元素的值进行删除，如果列表中存在多个同名元素只会删除第一个，后面的不会删除

                a_list = [1,2,3,4]
                del a_list[2] //[1,2,4]

                b_list = [1,2,3,4]
                b_list.pop() // [1,2,3]

                c_list = [1,2,3,4]
                c_list.remove(3) //[1,2,4]

                如果里面有多个重复元素，都需要删除
                list = [1,2,5,2,2,88,2]

                n = 0
                while n<len(list):
                    if list[n] == 2:
                        list.remove(2)#此时为了控制连续相同元素挨着然后漏删的问题，在删除之后下标不操作，没删除的时候下标才加一
                    else:
                        n += 1
                
                方法2
                for i in list[::-1]:
                    if i == 2:
                        list.remove(i)
                    

            排序
                list = [1,3,5,89,7,56]
                list.sort() #1 3 5 7 56 89 直接使用的话就是正序
                list.sort(reverse=True) 这么使用的话就是逆序
            反转
                list.reverse()
            
            s = [1,3,5,89,7,56,99,102,85,41]

            s[4] // 7
            s[3:7] // [89,7,56,99] 从下标3到下标6
            s[1:] // [3,5,89,7,56,99,102,85,41]  如果只有起始位没有终止位那么就到最后一位结束
            s[:4] // [1,3,5,89]
            s[0:6:2] // [1,5,7] 步长为2的话表示隔一个截取一个
            s[::-3] #[41,99,89,1] 步长为负数的时候是从后往前


            列表推导式：最终得到一个列表

            例：如果我们要拿到一个1-20的列表
            list = []
            for i in range(1,21):
                list.append(i)
            列表推导式可以对其进行简化
            格式：
                [i(这个i是最终放在列表里的变量) for i in 可迭代的变量]

                如果需要加判断的话
                [i(这个i是最终放在列表里的变量) for i in 可迭代的变量 if 条件]

                如果既有if也有else
                [结果1 if 条件 else 结果2 for i in 可迭代的变量]

                多个循环嵌套
                [(x,y) for x in 可迭代的变量 for y in 可迭代的变量]

            
            list = [ i for i in range(1,21)]
            前面放在列表中的i可以进行一些运算

            例：1-100之间所有偶数 存放在列表中
            list = [ i for i in range(0,101,2)]
            list = [ i for i in range(0,101) if i%2==0]

            例：如果是h开头的则将首字母大写，不是h开头的全部转大写
            title() 首字母大写
            upper() 全部大写
            list2 = ['62','hello','100','world']
            lis3 = [word.title() if word.isalpha() and word.startswith('h') else word.upper()   for word in list2]

            list4 = [(x,y) for x in range(1,3) for y in range(1,3)] #[(1,1),(1,2),(2,1),(2,2)]

            例 实现分组一个list里面的元素，比如[1,2,3,...100] 变成 [[1,2,3],[4,5,6]...]
                a = [x for x in range(1,101)]
                b = [a[i:i+3] for i in range(0,len(a),3)]
               找出里面名字含有两个'e'的放在新列表中
               names = [['Tom','Billy','Jefferson','Andrew','Wesley','Steven','Joe'],['Alice','Jill','Ana','Wendy','Jennifer','Sherry','Eva']]

               new_names = [j for i in names for j in i if j.count('e')>=2]
            ```

        * 元组高级
            python的元组与列表类似，不同之处在于 元组的元素不能修改 元组使用小括号，列表使用方括号
            ```
            a_tuple = (1,2,3,4)
            a_tuple[0] // 1

            a_tuple[3] = 5 //报错 tuple不支持该方式

            注意：定义只有一个元素的元组，需要在唯一的元素后写一个逗号

            a = (11,) 如果不加逗号类型判断会是int

            切片的使用相同

            count 用来计数，使用方法也相同

            list(tuple) ---> 元组转列表 
            tuple(list) ---> 列表转元组
            可以通过元组转列表之后进行修改，再把列表转元组
           
            ```
        * 字典高级
            ```
            字典也有和列表一样的推导式

            person = {'name':'小明','age':18}

            如果出现相同的键的话，运行并不会报错，后面的键的值会替换掉前面键的值。如果值是相同的话则无所谓。
            

            # 访问person的属性
            print(person['name']) // 小明(注音要查询的属性名的写法是str的形式)

            #使用[]的方式，获取字典中不存在的key的时候 会发生异常 keyerror
            #不能使用person.name的方式来访问字典中的数据

            #可以使用如下方式来访问
            print(person.get('name')) // 小明 get后面还可以传第二个参数，意味如果找不到该key的value值的话，显示的就是第二个参数的值
            #使用.的方式，获取字典中不存在的key的时候 不会报错会返回一个none


            字典的修改
            person['name'] = '张三'

            字典的添加
            #给字典添加一个新的key value 这个键如果在字典中不存在 那么就会变成新增元素
            person['sex'] = '男'

            字典的删除
            pop
                删除字典中指定的某一个元素
            popitem
                删除最后面的一个键值
            del
                1.删除字典中指定的某一个元素
                2.删除整个字典
            clear
                1.清空字典 但是保留字典对象

            person = {'name':'小明','age':18}

            person.pop('name')
            

            del person['age']

            del person // 整个删除
            此时如果在下面打印person会出现报错 person is not defined

            person.clear()
            此时如果在下面打印person会打印出 {}


            字典的遍历

            person = {'name':'小明','age':18,'sex':'男'}

            遍历字典的key
            字典.keys() 方法 获取字典中所有的key值
            for key in person.keys():
                print(key)
            
            遍历字典的value
            字典.values() 方法 获取字典中所有的values值
            for value in person.values():
                print(value)

            遍历字典的key和value
            for key,value in person.items():
                print(key,value)

            遍历字典的项/元素
            for item in person.items():
                print(item)
            ```
        
        * set的使用
            集合(set)是一个无序不重复的元素序列，可以使用大括号{}或者set()函数创建集合
            注意：创建一个空集合必须用set()而不是{},因为{}是用来创建一个空字典
            集合也有和列表一样的推导式
            ```
            创建格式
            parame = {value01,value02,...}
            或者
            set(value)

            set可用于快速删除多个重复元素

            list = [1,3,6,8,9,9,1,2,3,9]
            set(list) # {1,2,3,6,8,9}

            添加元素 add
            set.add(10)

            合并 update
            set1.update(set2) #把2并进1

            移除
            set.remove() #如果传入的值不存在的话会报错
            set.discard() #传入的值不存在的话不会报错

            del set #整个删除
            set.clear() # 清空
            set.pop() #随机删除一个元素

            集合
            union 并集 简写 &    set2 & set3
            difference 差集 简写 -  set2 - set3
            intersection 交集 简写 |  set2 | set3

            set2 = {1,2,3,4,5}
            set3 = {3,4,5,6,7}
            print(set2.intersection(set3)) #{3,4,5}

            例 产生5组(不允许重复)，字母和数字组成4位验证码
            import random
            code_set = set()
            s = 'ewqrrtuyyutifgsgsdfg012132254678731'

            while True:
                code = ''
                for i in range(4)
                    # r =random.choice(s) 这是使用choice的，也可以使用randint
                    # code += r

                    index = random.randint(0,len(s)-1) #从0到s的长度中间任取一个数字,当做下标位置
                    code += s[index]
                    
                
                code_set.add(code)
                
                if len(code_set) == 5:
                    break
            
            print(code_set)

            练习 图书馆管理系统
            至少5本书
            library = [{'bookname':'xxx','author':'xxx,'price':100,'number':4},{},{},{}]

            功能：借书 还书 查询(书名/作者) 查看所有 退出

            library = [
                {'bookname':'西游记','author':'吴承恩','price':100','number':40},
                {'bookname':'水浒传','author':'施耐庵','price':100','number':40},
                {'bookname':'红楼梦','author':'曹雪芹','price':100','number':40},
                {'bookname':'三国演义','author':'罗贯中','price':100','number':40},
                {'bookname':'三国演义','author':'罗贯东','price':100','number':40},
            ]

            while True:
                oper = input('\n1. 借书 \n2. 还书\n3. 查询\n4. 查看所有\n5. 退出\n请选择你需要的服务：')

                if oper == '1':
                    #需求：输入书名，查询是否有书，然后再判断作者是否是想要的
                    print('1.借书模块')
                elif oper == '2':
                    #需求：输入书名，输入作者判断是否存在有则还书，无则抛出异常
                    print('2.还书模块')
                elif oper == '3':
                    #需求：输入书名或者输入作者判断是否存在书籍
                    print('3.查询模块')
                elif oper == '4':
                    print('4.查看所有')
                    for i in library:
                        print(f'书名：{i['bookname']},作者：{i['author']}')
                elif oper == '5':
                    print('5.退出')
                    print('系统正常退出')
                    break
                else:
                    print('请重新选择')
            ```
        * 公共方法
            ```
            max()找出最大值

            list = [1,2,5,6,9]
            print(max(list)) # 9

            min()找出最小值
            sum()求和
            abs()绝对值
            sorted()升序排序排序，但是返回的是列表 添加参数 reverse=True 变为降序排序
            chr() 输入ASSC码值返回对应的字母
            ord() 输入字母返回ASSC码值
            isinstance(a,int) 判断类型 第一个参数是变量，第二个参数是类型,如果是则返回True，反之是False
            ```

        * 函数 
            ```
            定义函数的格式如下

            def 函数名():
                代码逻辑

            定义、调用带有参数的函数

            def sum(a,b):
                print(a+b)
            
            #位置传参
            sum(1,2)
            #关键字传参(不推荐)
            sum(b=200,a=100)

            定义时小括号中的参数，用来接收参数用的，称为形参
            调用时小括号中的参数，用来传递给函数用的，称为实参
            import random

            def generate_random(n,m): 
                for i in range(n):
                    ran = random.randint(1,10) #随机生成1-10以内的整数
                    if ran == m:
                        print('我被中断了！')
                        break
                    print(ran)

            generate_random(8,5)
            ```

            也可以使用默认值，就是在形参传的时候给一个值，如果传实参的时候不传该参数，那么函数运行的时候就是用的该值。如果传的话那么还是用传的值。默认值一般放在后面的参数，那如果我们前一个参数想要使用默认参数而后一个参数想要修改的话那我们就要采用关键字传参的形式。
            ```
            def generate_random(n=6,m=3)
            此时我们不想修改n，而是想修改m，那么我们可以如下传参
             generate_random(m=5) 这就表示n依旧使用默认值，而m使用5
            ```

            可变参数：
                *args 可以接收独立的变量
                **kwargs 关键字参数，在函数调用的时候必须传递关键字参数
            ```
            例： 要求数值相加，如果求两个数则需要定义两个参数，如果要求多个数的话我们可以利用可变参数

                def get_sum(*args):
                    print(args)
                
                get_sum(1,2) #(1,2)
                get_sum(1,2,3,4,5) #(1,2,3,4,5)
                所以可变参数相当于一个容器，形成一个元组

                def get_sum(*args):
                    s = 0
                    for i in args:
                        s += i
                    print(s)
            
                拆包和装包
                *a,b,c=1,2,3,4,5
                print(a) #(1,2,3)
                print(b) # 4
                print(c) # 5

                a,b,c = (1,2,3)
                print(a) #1
                print(b) #2
                print(c) #3

                如果此时有一个列表，而我们要使用get_sum求值时
                ren_list = [23,4,53,45,77]
                get_sum(*ren_list)

                **kwargs 
                def show_book(**kwargs)
                    print(kwargs) #{}
                
                所以**kwargs必须传入的是关键字参数
                show_book(bookname='西游记') #{'bookname':'西游记'}

                book = {'bookname':'红楼梦'}
                show_book(**bookname)
            ```
            函数返回值

            带有返回值的函数
            想要在函数中把结果返回给调用者，需要在函数中使用return,如果return后面不加值的话就是结束函数。
        
            ```
            def add2num(a,b):
                return a+b

            #返回值的关键字是return 存在函数中

            def buyIceCream()
                return '冰淇淋'

            #使用一个变量来接受函数的返回值
            food = buyIceCream()
            import random
            def get_total(n=5):
                total = 0
                for i in range(n):
                    ran = random.randint(1,20)
                    total += ran
                
                return total
            result = get_total()
            print(result)

            return可以传多个参数
            import random
            def get_list_total(n=5):
                total = 0
                ran_list = []
                for i in range(n)
                    ran = random.randint(1,20)
                    ran_list.append(ran)
                    total += ran
                return total,ran_list
            result = get_list_total()
            print(result)
            ```

            return和break的区别
            ```
            def abc():
                for i in range(10):
                    if i == 2:
                        break/return
                    print(i)
                print('结束了')
            打印结果： 0 1 结束了
            如果换成return打印结果：0 1
            ```
            

            函数间的调用
            ```
            import random
            def get_list():
                ran_list = []
                for i in range(5):
                    ran = random.randint(1,20)
                    ran_list.append(ran) 
                return ran_list
            
            def get_total():
                r_list = get_list()
                if r_list:
                    total = 0
                    for i in r_list:
                        total += i
                    return total
            
            res = get_total()
            print(res)
            ```
            全局和局部变量：
            ```

            #全局变量
            a = 100
            def test1():
                #局部变量
                a = 0
                print('a =',a)
            test1() # a = 0 #此处打印为函数内部打印，函数在输出的时候会先找自身的值，局部变量的作用范围仅限函数的内部
            print('a =',a) # a = 100 #此处打印的任然为全局变量的100

            如果要改变全局a的值的话需要加上global关键字

            def test2():
                global a
                a = 11
            test2()
            print('a =',a) # a = 11 此时全局的a已经被改变
            ```
            

            global关键字的添加：
                只有不可变的类型才需要添加(int str float bool tuple) 不可变：当改变变量的值时，地址发生了改变
                可变的类型不需要添加(list dict set) 可变：里面的内容发生了改变，但是地址没有发生改变
                python会创建一片小正数空间0-256
            ```
                a = 100
                print(id(a))
                a = 90
                print(id(a))
                二者的地址不一样，因为这属于小整数空间里的值
            ```
            
            引用
            ```
                a = 10
                b = a
                print(b) #10
                a = 5
                print(b) #10
                这个里的b的值没有改变是因为b所指向的a的地址，而a重新赋值之后地址发生了变化，而b指向的地址并没有发生变化所以b依然是等于10，这里所用的到特性跟上面的可变不可变类型是一样的
            ```

            闭包
                函数只是一段可执行代码，编译后就"固化"了，每个函数在内存中只有一份实例，得到函数的入口点便可以执行函数了。
                函数还可以嵌套定义，即在一个函数内部可以定义另一个函数，有了嵌套函数这种结构，便会产生闭包问题
                
                局部变量和全局变量

                #局部变量：在函数的内部定义的变量 我们称之为局部变量

                #特点：其作用域范围是函数内部，而函数的外部是不可以使用

                #全局变量：定义在函数外部的变量 我们称之为全局变量

                #特点：可以再函数的外部使用，也可以在函数的内部使用

            ```
                def outr():
                    a = 100
                    def inner():
                        b = 200
                        #内部函数不能修改外部函数的变量
                        #如果我们在inner里面想要修改a的值我们可以使用nonlocal 
                        nonlocal a
                        a = 200
                        print("我是内部函数",a)
            ```
            闭包的定义
                1.嵌套函数
                2.内部函数引用了外部函数的变量
                3.返回值是内部函数
                4.内部函数引用了外部函数的变量
            ```
            格式：
                def 外部函数():
                    def 内部函数():
                    return 内部函数

                def outer(n):
                    a = 10
                    def inner():
                        b = a+n
                        print('内部函数',b)
                    return inner
                r = outer(5)
                print(r) #打印的是return出来的inner函数的地址
                r() #内部函数 15
            闭包的总结
            1.闭包优化了变量，原来需要类对象完成的工作，闭包也可以完成
            2.由于闭包引用了外币函数的局部变量，则外部函数的局部变量没有及时释放，消耗内存
            3.闭包的好处，使代码变得简洁，便于阅读
            4.闭包是装饰器的基础
            ```

            装饰器
            ```
            相当于给一个函数添加功能，比如说一个函数多处项目引用，但并不需要全部更改的时候我们就可以添加装饰器
            特点：
            1.函数作为参数传递给另一个函数
            2.要有闭包的特点

            #定义一个装饰器
            def decorate(func):
                print('wrapper测试')
                a = 100
                def wrapper():
                    print('111')
                    func()
                    print(a)
                print('wrapper加载完成')
                return wrapper

            #使用装饰器 @装饰器名

            @decorate #如果调用下面的函数的话，在这里wrapper测试和加载完成还是会打印，此时会把下面的参数函数传入到装饰器里面
            def house():
                print('房子')
            
            house() #111 房子 100

            需要传参

            def decorate(func):
                def wrapper(x):
                    print('111')
                    func(x)
                return wrapper
            
            @decorate
            #此时的f1是需要传参的，而我们f1调用的时候实际上是调用的wrapper所以我们要在内层的wrapper上给上参数，然后传给里面的func
            def f1(n):
                print(n)
            
            f1(5)

            如果需要传递的参数不确定的话，在wrapper传参的时候传入的是*args可变参数，如果后面还会传入指定关键字的话我们还可以加上**kwargs，这样任何函数都可以使用
             def decorate(func):
                def wrapper(*args,**kwargs):
                    print('111')
                    func(*args,**kwargs)
                return wrapper
            
            可以使用多个装饰器，并且执行顺序是从下往上，所以先执行装饰器1再执行装饰器2
            @decorate2
            @decorate1
            def func
            func()
            
            带参数的装饰器
            def outer(a):
                def decorate(func):
                    def wrapper(*args,**kwargs):
                        func()
                        print('111',a)
                    return wrapper
                return decorate
            @outer(a=10) #只要在这里传了参数的，上面装饰器就得在加一层
            def house():
                print('222')
            
            house()
            ```


            匿名函数
            ```
            作用：简化函数定义
            格式
                lambda 参数1,参数2...:运算

            s = lambda a,b:a+b

            result = s(1,2)
            print(result)

            匿名函数作为参数

            def fun(a,b,func):
                s = func(a,b)
                print(s)
            
            fun(1,2,lambda a,b:a+b)

            匿名函数与内置函数的结合使用

            list = [{a:'10',b:'20'},{a:'13',b:'20'},{a:'9',b:'20'}]
            如果直接使用max函数会报错，我们可以看到max函数内部可以传入参数
            m = max(list,key=lambda x:x['a'])
            print(m) #{a:'13',b:'20'}
            ```


            递归函数
            ```
            特点：
            递归函数必须要设定终点
            通常都会有一个入口


            def sum(n):
                if n == 0:
                    return 0
                else:
                    return n + sum(n-1)
                    
            
            print(sum(10))
            ```
            
            
            
            异常：
            ```

            def chu(a,b):
                return a/b
            
            chu(1,0)
            只要代码异常了后面的代码就不会执行
            
            异常处理：
            try:
                把可能出现异常的代码放在try里面
            except:
                如果有异常执行的代码
            finally:(可要可不要，一般用在文件处理和数据库操作中，因为无论是否异常都要关闭)
                无论是否存在异常都会被执行的代码
            
            def func():
                stream = None
                try:
                    stream = open(r'文件路径')
                    container = steam.read()
                    print(container)
                except Exception as err:
                    print(err)
                finally:
                    if stream:
                        stream.close()

            如果有多种错误需要判断的话可以在except后面加错误类型，因为所有的错误类型都是从Exception里面衍生出来的，所以错误类型直接使用Exception的话会接纳所有的错误，所以一般Exception放在最后面，最大的放在最下面
            except ZeroDivisionError:
                print('被除数不能为0')
            except ValueError:
                print('必须输入(需要输入的类型)')
            except Exception:
                print('出错了')
            如果要打印出错的原因的话
            except Exception as err:
                print('出错了',err)


            try和else连用
            如果使用了else则在try代码中不能出现return
            try:
                把可能出现异常的代码放在try里面
            except:
                如果有异常执行的代码
            else:
                没有异常才会执行的代码


            抛出异常 raise 可以自己定义报错
            #注册 用户名必须6位
            def register():
                username = input('输入用户名')
                if len(username)<6:
                    raise Exception('用户长度必须6位以上')
                else:
                    print('输入的用户名是：',username)
            
            try:
                register()
            except Exception as err:
                print(err)
                print('注册失败')
            else:
                print('注册成功')
            ```

            
            生成器
            ```
            通过列表推导式，我们可以直接创建一个列表，但是受到内存限制，列表容量肯定是有限的，而且，创建一个包含100万个元素的列表，不仅占用很大的存储空间。如果我们仅仅需要前面几个元素，那后面绝大多数元素占用的空间都白白浪费了。所以，如果列表元素可以按照某种算法推算出来，那我们是否可以在循环的过程中不断推算出后续的元素呢？这样就不必创建一个完整的list，从而节省大量的空间。在python中，这种一边循环一边计算的机制被称作生成器 generator

            得到生成器方式：
            1.通过列表推导式得到生成器
            通过列表推导式生成的结果会占用内存，所以我们可以使用()替换[]来对代码进行包裹

            #得到生成器
            g = (x*3 for x in range(20))
            print(type(g)) # generator
            如果直接打印g的话会得到一个内存地址

            print(g.__next__())#0
            print(g.__next__())#3
            每调用一次__next__得到一个元素

            print(next(g))#6
            系统内置的next方法里面放的是生成器对象，每次调用会产生一个元素

            这里我们就可以使用循环来做操作
            g = (x*3 for x in range(20))

            while True:
                try:
                    e = next(g)
                    print(e)
                except:
                    print('没有更多元素啦')
                    break
            
            2.借助函数
            只要函数中出现了yield关键字，说明该函数是一个生成器
            步骤：
            1.定义一个函数，函数中使用yield关键字
            2.调用函数，接收调用的结果
            3.得到的结果就是生成器
            4.借助next()或者__next__()得到元素

            def func():
                n = 0
                while True:
                    n +=1
                    yield n #相当于return + 暂停

            g = func()
            print(next(g))


            def fib(length): #斐波那契数列
                a,b = 0,1
                n = 0

                while n < length:
                    yield b
                    a,b = b,a+b
                    n+=1

            g = fib(8)
            print(next(g))
            print(g.__next__())


            生成器方法：
            __next__():获取下一个元素
            send():向每次生成器调用中传值 注意：第一次电泳send(None)

            def gen():
                i = 0
                while i < 5:
                    temp = yield i 
                    print('temp',temp)
                    for x in range(temp):
                        print('---->',x)
                    print('****')
                    i+=1
                return '没有更多的数据'

            g = gen()

            g.send(None)
            n1 = g.send(3)
            print('n1:',n1)
            运行结果：
                0
                temp:3
                ---> 0
                ---> 1
                ---> 2
                *******
                n1:1


            生成器的应用：协程

            def task1(n):
                for i in range(n):
                    print('正在搬第{}块砖！'.format(i))
            
            def task2(n):
                for i in range(n):
                    print('正在听第{}首歌！'.format(i))

            #如果让任务交替运行要改写为

            def task1(n):
                for i in range(n):
                    print('正在搬第{}块砖！'.format(i))
                    yield None
            
            def task2(n):
                for i in range(n):
                    print('正在听第{}首歌！'.format(i))
                    yield None

            g1 = task1(10)
            g2 = task2(5)

            while True:
                try:
                    g1.__next__()
                    g2.__next__()
                except:
                    pass

            #可迭代的对象：1.生成器 2.元组 列表 集合 字典 字符串
            #如何判断一个对象是否是可迭代的 使用isinstance()
            传入两个参数，第一个参数是判断的值，第二个参数是类型

            from collections import Iterable
            list1 = [1,4,7,8]
            isinstance(list1,Iterable)

            迭代是访问集合元素的一种方式，迭代器是一个可以记住遍历的位置的对象
            迭代器对象从集合的第一个元素开始访问，直到所有的元素被访问完结束
            迭代器只能往前不会后退

            可以被next()函数调用并不断返回下一个值的对象称为迭代器：Iterator

            可迭代的不一定是迭代器，比如说元组，列表等
            但是我们可以借助系统的iter()函数，把他们变成迭代器
            ```



            面相对象，常用术语包括：
                类：可以理解是一个模板抽象的，通过它可以创建出无数个具体实例对象
                对象：类并不能直接使用，通过类创建出的实例(又称对象)才能使用
                属性：用于描述类的特征的称为属性
                方法：用于描述类的动作的称为方法
            ```
            
            创建类
            格式：
                class 类名：
                    类属性
                    类方法
                
                注意，无论是属性还是方法，对于类来说，他们都不是必需的，可以有也可以没有。另外，Python类中属性和方法所在的位置是任意的，即它们之间并没有固定的前后次序

                类方法特点(在对象没有创建的时候已经加载了，所以可以不需要创建对象就能使用，使用方法 类名.方法名())
                1.定义需要依赖装饰器@classmethod
                2.类方法中参数不是一个对象，而是类
                3.类方法只能使用类属性
                4.类方法不能使用普通方法
                
                类方法的作用
                因为只能访问类属性和类方法，所以可以在对象创建之前，如果需要完成一些动作(功能)

                静态方法：非常类似于类方法
                1.需要装饰器@staticmethod
                2.静态方法是无需传递参数的
                3.也只能访问类的属性和方法，对象是无法访问的
                4.加载时机同类方法

            
            class是关键字，类名根据自己需求起名
                类名的首字母要求大写，不要使用英文
                类名后面是有冒号的
                类体像函数体一样需要缩进的

            class Phone:
                #属性(当然属性也可以不赋值，比如是None或者0)
                brand = '华为'
                color = '黑色'
                type = 'Mate30'
                price = 3999

                #方法(只要在类中定义方法，里面的self是默认的，是要依赖self)
                def call(self):
                    print('可以打电话！')

                def send_message(self):
                    print('可以发消息！')
                
                #类方法(没有对象也可以使用，因为是依靠类来存在的,里面传入的cls是类本身，可以访问私有变量类似于__age=20)
                @classmethod #使用装饰器
                def test(cls): #cls是class的简写
                    print(cls)

                #静态方法
                @staticmethod
                def test():
                    里面所能用的东西和类方法一样

            
            #创建对象
            p = Phone()
            p.brand = '小米' #修改phone中的属性

            这种创建类的方法的话就把属性都给固定了，而如果我们想要自己定义属性的话就得使用 __init__方法
            普通方法格式： def 方法名(self[,参数]) 谁调用self指向谁



            class Phone:
                #魔法方法,只要创建对象的时候就会默认执行的方法
                #魔法方法1 __init__(self)初始化魔术方法
                #在初始化对象的时候触发
                #加上了后面的参数之后在定义对象的时候就必须传入这两个参数
                def __init__(self,brand,price):
                    self.brand = brand
                    self.price = price

                #魔法方法2 __new__(cls)实例化魔术方法
                #在实例化时进行触发
                def __new__(cls):
                    print('---->new')

                #在方法中也可以使用属性
                def call(self):
                    print('可以使用'+self.brand+'打电话！')

            p = Phone('华为',1999)
            print(p.brand)
            p.call()

            类方法的调用
            一个类中可以定义多个方法，而且方法之间是可以互相调用的。而且方法中还可以使用属性。
            class Person：
                def __init__(slef,name,age):
                    self.name = name
                    self.age = age

                #对象方法
                def eat(self,food):
                    print(self.name + '喜欢吃:')
                    for i in food:
                        print(i)
                
                def sleep(self,hours):
                    print('{}睡觉啦，一下子睡了{}小时'.format(self.name,hours))
                
                def paly(self,gname):
                    self.sleep(1)
                    print('{}喜欢玩{}'.format(self.name,gname))

            
            dong = Person('xindong',18)
            dong.eat('士力架')
            dong.sleep(10)

            qiang = Person('aqiang',20)
            qiang.sleep(2)
            foods = ['麦当劳','鱼非鱼','大鸭梨烤鸭']
            qiang.eat(foods)
            qiang.sleep(8)
            qiang.play('足球')
            ```


            私有化
            ```
            私有化的好处在于不让外界随便修改属性,并且访问范围也仅限于这个类中
            封装：
            1.私有化属性
            2.定义共有set和get方法

            class Student:
                #__age = 18

                def __init__(self,name,age):
                    self.name = name
                    self.age = age
                    self.__score = 59
                
                #定义公有的set和get方法
                #set为了赋值
                def setScore(self,score):
                    #定义成函数的好处在于可以进行判断
                    self.__score = score

                #get为了取值
                def getScore(self):
                    return self.__score     

                def __str__(self):
                    return '姓名：{},年龄：{},考试分数{}'.format(self.name,self.age,self.__score)

            lisi = Student('lisi',18)
            print(lisi)
            lisi.age = 21  #可以修改
            lisi.__score = 95  #不能直接修改私有变量，必须得使用set函数修改
            lisi.setScore(95)
            lisi.getScore()

            私有化的property装饰器
            class Student:
                def __init__(self,name,age):
                    self.__name = name
                    self.__age = age
                
                def setName(self,name):
                    self.__name = name
                
                def getName(self):
                    return self.__name

                def __str__(self):
                    return '姓名:{},年龄:{}'.format(self.__name,self.__age)

            s = Student('lisi',20)
            #如果我们想要修改name值必须调用setName,想要拿到name必须得调用getName
            s.setName(30)
            print(s.getName())

            #但是这么使用过于繁琐，我们可以使用property装饰器
             class Student:
                def __init__(self,name,age):
                    self.__name = name
                    self.__age = age
                
                @property #一定要先定义get的age，然后才能利用其来绑定下面的setter
                def age(self):
                    return self.__age
                
                @age.setter #因为set依赖于get
                def age(self,age):
                    self.__age = age

                def __str__(self):
                    return '姓名:{},年龄:{}'.format(self.__name,self.__age)

             s = Student('lisi',20)
             print(s.age)#只要加了装饰就可以使用参数一样用不用加括号，就可以这样取值
             print(s.__dir__())#可以打印出里面的变量参数

            例题：
            公路(Road):
                属性：公路名称，公路长度
            车(Car):
                属性：车名，时速
                方法：1.求车名在那条公路上以多少的时速行驶了多长
                    get_time(self,road)
                    2.初始化车属性信息__init__方法
                    3.打印对象显示车的属性信息
            
            class Road:
                def __init__(self,name,len):
                    self.name = name
                    self.len = len
            class Car:
                def __init__(self,brand,speed):
                    self.brand = brand
                    self.speed = speed
                
                def get_time(self,road):
                    ran_time = random.randint(1,10)
                    msg = '{}品牌的车在{}上以{}速度行驶了{}小时'.format(self.brand,road.name,self.speed,ran_time)
                
                def __str__(self):
                    return '{}品牌的,速度:{}'.format(self.brand,self.speed)

            #创建实例
            r = Road('青藏高速',5000)
            audi = Car('奥迪',120)
            audi.get_time(r)
             
             
            ```
            继承
            ```
            has a和is a

            has a 一个类中使用了另外一种自定义的类型(自定义的类)

            is a 
            特点：
            1.如果类中不定义__init__ 调用父类super 就会调用父类的init
            2.如果类继承了父类，并且也需要定义自己的init的时候，就需要在当前类的init中调用下父类的init
            3.调用父类的两种方式 super().__init__(参数)  super(类名,self).__init__(参数)
            4.如果父类和子类都有相同的方法名，那默认的搜索原则是先找当前类，再去找父类。如果在该方法中还是需要父类的操作的话，
              只需要在方法中加super().方法名()即可  override：重写，覆盖

            class Student:
                def __init__(self,name,age):
                    self.name = name
                    self.age = age
            
            class Employee:
                def __init__(self,name,age):
                    self.name = name
                    self.age = age

            class Doctor:
                def __init__(self,name,age):
                    self.name = name
                    self.age = age
            
            三个类里面都要定义name,age就显得比较繁琐，所以我们可以把每个类都定义的类型给提出来

            class Person: #基类
                def __init__(self,name,age):
                    self.name = name
                    self.age = age
            
            class Student(Person): #子类
                pass
            
            class Employee(Person): #子类
                pass

            class Doctor(Person): #子类
                pass

            s = Student('lisi',18)

            那紧接着就会出现问题，如果我还想在子类里面使用__init__的时候，如果直接使用会导致基类的init丢失，那么我们就需要在子类里面调用父类的init。
            这时候我们就要使用super关键字，super表示的是上层的父类
            class Person: #基类
                def __init__(self):
                    self.name = '匿名'
                    self.age = 18
            

            class Student(Person): #子类
                def __init__(self):
                    print('----->student的init')
                    #调用父类的init super()表示找到父类
                    super().__init__()
            
            s = Student()

            如果此时还需要传参的话
            class Person: #基类
                def __init__(self,name):
                    self.name = name
                    self.age = 18
                
                def eat(self):
                    print(self.name + '正在吃饭(父类)')
            
            class Student(Person): #子类
                def __init__(self,name,class):
                    self.class = class
                    print('----->student的init,{}'.format(self.class))

                    #调用父类的init super()表示找到父类
                    super().__init__(name)

                def eat(self):
                    print(self.name + '正在吃饭')

            s = Student('李四','大数据')
            s.eat() #如果子类和父类的方法有相同的方法名的话会调用子类自己的方法


            多继承和搜索顺序

            class Person:
                def __init__(self,name):
                    self.name = name
                
                def eat(self):
                    print('----->eat1')

                def eat(self,food):
                    print('----->eat:',food)
            
            p = Person('李四')
            p.eat() 
            #结果会报错，报没有传参的错。因为如果方法名相同的话后面的会覆盖掉前面的

            多继承

            class A:
                def test(self):
                    print('AAAAAAAAAA')
            
            class B:
                def test1(self):
                    print('BBBBBBBBBB')
            
            class C(A,B):#C继承A和B
                def test2(self):
                    print('CCCCCCC')
            
            c = C()
            c.test()
            c.test1()
            c.test2()

            搜索原则

            class Base:
                def test(self):
                    print('----Base----')

            class A(Base):
                def test(self):
                    print('AAAAAAAAAA')
            
            class B(Base):
                def test1(self):
                    print('BBBBBBBBBB')
            
            class C(Base):#C继承A和B
                def test2(self):
                    print('CCCCCCC')
            class D(A,B,C):
                pass
            
            d = D()
            d.test() #结果打印的是AAAAAA
            import inspect
            print(inspect.getmro) #返回一个元组，就是一个搜索顺序
            或者使用
            print(D.__mro__) #来进行搜索顺序的查找


            多态

            class Person:
                role = 'Pet'
                def __init__(self,name):
                    self.name = name
                
                def feed_pet(self,pet):
                    if isinstance(pet,Pet): #判断传过来的参数是什么类型的，这里加上判断是因为上层并不会判断pet的类型，也就是说不管是不是pet类型都能传进来，所以在这里做了限制
                        print('{}喜欢养宠物:{}'.format(self.name,pet.nickname))
                    else:
                        print('不是宠物类型的')
            
            class Pet:
                def __init__(self,nickname,age):
                    self.nickname = nickname
                    self.age = age
                
                def show(self):
                    print('昵称:{},年龄:{}'.format(self.nickname,self.age))
            
            class Cat(Pet):
                role = '猫'
                def catch_mouse(self):
                    print('抓老鼠...')
            
            class Dog(Pet):
                role = '狗'
                def watch_house(self):
                    print('看家高手')
            
            #创建对象
            cat = Cat('花花',2)
            dog = Dog('大黄',4)

            person = Person('李四') 

            person.feed_pet(cat)

            ```

            开发模式
            ```
            单例模式
            对内存的优化，保证创建的对象都在一个地址上，并不是所有的场景都适合

            class Student:
                pass
            
            s = Student()
            s1 = Student()
            s2 = Student()
            每创建一个对象，内存中就会开辟一片空间

            class Singleton:
                #私有化
                __instance = None

                #重写__new__
                def __new__(cls):
                    print('----> __new__')
                    if cls.__instance is None:
                        cls.__instance = object.__new__(cls)
                        return cls.__instance
                    else:
                        return cls.__instance
            
            s = Singleton()
            s1 = Singleton()

            print(s) #地址产生了
            print(s1) #地址没有发生变化 
            
            ```



            模块
            在python中一个脚本(.py)文件就是一个模块，创建模块实际上就是创建一个.py文件，可以被其他模块导入并使用。
            在python中，模块是代码组织的一种方式，把功能相近的函数放到一个文件中，一个文件就是一个模块
            这样做的好处：
                提高代码的可复用、可维护性。一个模块编写完毕后，可以很方便的在其他项目中导入
                解决了命名冲突，不同模块中相同的命名不会冲突
            
            模块的导入
            ```
                import导入 
                #例 
                import 文件名
                然后下面就可以使用文件中的函数及属性了
                使用方法： 文件名.属性名  文件名.函数  文件名.类

                例如：我创建了一个calculate.py里面写了add mainus等方法。然后我在另一个test.py文件中想要使用这些方法
                我就需要在test.py文件中写 import calculate  要使用里面的方法的话我们用 calculate.add()


                还可以使用 import...as... 使用as的目的就是重新命名，比如说文件名特别长，就使用as进行别名
                import 文件名 as 别名


                from...import导入
                #例
                使用from...import可以直接导出里面的函数，属性之类的。可以导出多个使用逗号隔开，也可以使用*导出该模块中的所有

                from 模块名 import 变量
                from 模块名 import 变量1,变量2,变量3
                from 模块名 import *  但是如果想限制获取的内容，可以在模块中使用__all__=[使用*可以访问到的内容]  __all__=['add','Calculate']

                无论是import还是from的形式，都会将模块内容进行加载，那如果我模块里面本身包含的是有函数调用，但是我被加载的时候不想被执行，那就要使用__name__
            
                __name__
                __name__是python的一个内置类属性，它存储模块的名称。python的模块即可以被调用，也可以独立运行。而被调用时__name__存储的是py文件名(模块名称)，独立运行时存储的__main__.
                那么它的作用主要就是用来区分，当前模块是独立运行还是被调用

                if __name__ == '__main__':
                    print('独立运行')
                else:
                    print('被调用')
            ```

            
            包
            ```
            为了更好的组织模块，会将多个模块存到包。python处理包也是相当的方便的。简单来说，包就是文件夹，但该文件夹下必须存在__init__.py文件。
            创建包的时候选择 new package

            包的导入类似模块的导入
                import 包名
                from 包名.模块名 import *
                例如：在user的包里面有一个models模块，models模块里面有一个show方法，我们可以 from user.models import show
            
            如果是在包里的同级文件想要导入的话还是需要使用 from 包名.模块名 import 来导入或者前面的包名可以省略 from .模块名 import


            __init__文件
            当你在导入这个包的时候就会自动执行 __init__这个文件，如果有一些必须执行的话就可以放入这个文件中。例如初始化的函数，变量，类。
            此文件中函数，变量等的访问，只需要通过 包名. 来访问

            循环导入

            A模块中的函数需要使用B模块中函数，B模块中函数需要使用A模块中的函数
            如果两个文件中的第一句都是导入语句的话，那就会陷入一个循环导入的地步。

            A:
                import B
                def test():
                    f()

            B:
                def f():
                    import A
                    test()        
           

            如何避免产生循环导入：
            把导入语句不要放在第一句，而是放在需要的函数前！
            把导入语句放在最后
 
            sys模块

            模块和包的搜索路径
            当python执行import语句的时候，它会在一些路径中搜索python模块和扩展模块。可以通过sys.path查看路径，比如在包中新建一个test.py文件，里面内容如下
            
            import sys
            print(sys.path) #结果是一个列表
            #遍历列表更加清楚
            for p in sys.path
                print(p)
            搜索的顺序是 脚本的当前目录、PYTHONPATH环境变量、python安装时的系统目录
            ```

            进程
            ```
            单核CPU：多任务交替进行
            多核CPU：如果任务数超过CPU的核数则也是任务交替进行

            优点：稳定性高，一个进程奔溃了，不会影响其他进程
            缺点：创建进程开销巨大 操作系统能同时运行进程数目有限

            一个进程里面可以包含多个线程，一个线程里面可以包含多个协程

            进程的创建
            在linux下可以使用fork函数创建进程，在windows系统上可以引入multiprocessing模块，创建进程。我们可以使用multiprocessing模块中Process类创建新的进程

            Process类说明
            
            方法名：__init__()   功能：构造方法
            参数： name:进程名称 args:任意位置参数 kwargs:任意关键字参数 target:进程实例所调动的对象  

            方法名：start()   功能：启动进程
            方法名：terminate()   功能：结束进程
            方法名：join()   功能：是否等等进程执行结束
            参数：timeout:等等数秒，可选

            def task1():
                while True:
                    sleep(1)
                    print('这是任务1')
            
            def task2():
                while True:
                    sleep(1)
                    print('这是任务2')
            
            if__name__ == '__main__':
                task1()
                task2()
            
            运行结果:
                这是任务1
                这是任务1
                这是任务1
                ...
            因为任务1一直不结束就不会执行任务2
            from multiprocessing import Process

            number = 1
            if__name__ == '__main__':
                p1 = Process(target = task1)//进程需要传值的话可以使用args后面可以是元组也可以是列表，然后可以在task里面使用
                p1.start()
                p2 = Process(target = task2)
                p2.start()

                while True:
                    number +=1
                    if number == 100:
                        p1.terminate()
                        p2.terminate()
            运行结果:
                这是任务1
                这是任务2
                这是任务1
                这是任务2
                ...

            如果全局变量在各个子进程里面修改的话，实际上是各个子进程都会复制当前变量，并且在自己里面修改互不干涉。

            
            自定义进程

            from multiprocessing import Process

            class MyProcess(Process):

                def __init__(self,name):
                    super(MyProcess,self).__init__()
                    self.name = name

                #重写run方法，因为所有得线程都要放到run方法里面
                def run(self):
                    print('进程名字'+self.name) //这里的name是继承的类里面的
            
            if__name__ == '__main__':
                p = MyProcess('小明')
                p.start()
                p1 = MyProcess('小王')
                p1.start()

            进程池

            当需要创建的子进程数量不多的时候，可以直接利用multiprocessing中的Process动态生成多个进程，但如果是上百甚至是上千个目标，手动的去创建进程的工作量巨大，此时就可以用到multiprocessing模块提供的poll方法。初始化Pool时，可以指定一个最大进程数，当有新的请求提交到pool中时，如果池还没满，那么就会创建一个新的进程来执行该请求；但如果池中的进程数已经达到了指定的最大值，那么该请求就会等待，直到池中有进程结束，才会创建新的进程来执行
            
            阻塞式：
            非阻塞式：        

    
            from multiprocessing import Pool
            import time
            #非阻塞
            
            def task(task_name):
                print('开始做任务啦',task_name)
                start = time.time()
                #使用sleep
                time.sleep(random()*2)
                end = time.time()
                print('完成任务',(end-start))

            if __name__ == '__main__':
                pool = Pool(5)
                tasks = ['听音乐','吃饭','打游戏']
                for i in tasks:
                    pool.apply_async(task,args=(i,))
                pool.close() #添加任务结束
                pool.join() #插入主进程
                print('over!!!')
            

            ```
            并发与并行
            ```
            -并发：当多个线程在操作的时候，如果系统只有一个CPU，则他根本不可能真正同时进行一个以上的线程，它只能把CPU运行时间划分成若干个时间段，再将时间段分配给各个线程执行，在一个时间段的线程代码运行时，其他线程处于挂起状态。这种方式我们称之为并发(concurrent)
            -并行：当系统有一个以上CPU时，则线程的操作有可能非并发。当一个CPU执行一个线程时，另一个CPU可以执行另一个线程，两个线程互不抢占CPU资源，可以同时进行，这种方式我们称之为并行(Parallel)
            ```

    * 文件

        文件的打开与关闭
        ```

        打开文件/创建文件
        在python，使用open函数，可以打开一个已经存在的文件，或者创建一个新文件

        open(文件路径,访问模式)

        示例：
        f = open('test.txt','w')

        文件路径

            绝对路径：值得是绝对位置，完整的描述了目标的所在地，所有目录层级关系一目了然的。
            例如：E:\python 从电脑的盘符开始，表示的就是一个绝对路径

            相对路径：是从当前文件所在的文件夹开始的路径

            text.txt 是当前文件夹查找 test.txt文件
            ./text.txt 是在当前文件夹里查找text.txt文件 ./表示的是当前文件夹
            ../text.txt 从当前文件夹的上一级文件夹里查找 text.txt 文件 ../表示的是上一级文件夹
            demo/text.txt 在当前文件夹里查找demo这个文件夹，并在这个文件夹里查找 test.txt文件


        访问模式




        #创建一个test.txt文件
        #open(文件的路径,模式)
        
        open('test.txt','w') //当当前文件夹没有这个文件的时候使用open是在当前文件夹中创建了这个文件

        #打开文件
        fp = open('test.txt','w')
        fp.write('hello world')

        #文件的关闭
        #养成习惯在文件打开并且写入数据之后，一定要关闭,如果不关闭会造成大量的内存消耗

        fp = open('a.txt','w')
        fp.write('hello')
        fp.close()


        #文件的读写
        #write方法

        fp = open('test.txt','w')
        fp.write('hello world' * 5) //如果要写入多条相同的内容的话可以在后面写乘号加遍数
        fp.close()
        #如果再次运行这段代码 文件中的内容还是5遍
        #意味着如果文件存在 会先清空原来的数据然后再写，如果想要在每一次执行之后都要追加数据，则需要把模式改为'a'
        fp = open('test.txt','a')

        #读数据
        fp = open('test.txt','r')
        #默认情况下 read是一字节一字节的读 效率比较低
        content = fp.read()

        #readline是一行一行的读取 但是只能读取一行
        content = fp.readline() //只读第一行

        #readlines可以按照行来读取 但是会将所有的数据都读取到 并且以一个列表的形式返回
        #而列表中的元素是一行一行的元素
        content = fp.readlines()

        文件的序列化和反序列化

        通过文件操作，我们可以将字符串写入到一个本地文件。但是，如果是一个对象(例如列表、字典、元组等)，就无法直接写入到一个文件里，需要对这个对象进行序列化，然后才能写入到文件里

        设计一套协议，按照某种规则，把内存中的数据转换为字节序列，保存到文件，这就是序列化，反之，从文件的字节序列恢复到内存中，就是反序列化

        对象 --> 字节序列 === 序列化

        字节序列 --> 对象 === 反序列化

        python中提供了json这个模块用来实现数据的序列化和反序列化

        使用JSON实现序列化

        fp = open('test.txt','w')//对文件操作的习惯最好在写之前就把close写好，不然容易忘

        name_list = ['张三','李四','王五']
        如果直接把name_list写入write的括号中会报错，意思是write接收的参数必须是字符串的类型

        fp.write('hello world')

        fp.close()



        #序列化的两种方式
        #dumps()
        1.创建一个文件
        fp = open('test.txt','w')
        2.定义一个列表
        name_list = ['张三','李四','王五']
        3.引入json模块
        import json
        4.序列化 将python对象 变成json字符串
        此时names的类型为str
        names = json.dumps(name_list)
        5.将names写入到文件中
        fp.write(names)
        fp.close()
        //写入到文件中的为 ['张三','李四','王五']
        //我们在使用scrapy框架的时候 该框架会返回一个对象 我们要将对象写入到文件中 就要使用json.dumps


        #dump
        #在将对象转换为字符串的同时 指定一个文件的对象 然后把转换后的字符串写入到这个文件里
        1.创建一个文件
        fp = open('test.txt','w')
        2.定义一个列表
        name_list = ['张三','李四','王五']
        3.引入json模块
        import json
        4.使用dump写入
        相当于names = json.dumps(name_list)和fp.write(names)
        json.dump(name_list,fp)
        fp.close()
        

        反序列化

        将json的字符串变成一个python对象
        fp = open('test.txt','r')

        content = fp.read()

        #loads
        import json

        //将json字符串变成python对象
        json.loads(content)

        #load

        fp = open('test.txt','r')
        import json
        json.load(fp)
        fp.close()


        异常

        异常的处理 
        异常的格式
        try:
            可能出现异常的代码
        except 异常的类型
            友好的提示

        例如读文件失败

        try:
            fp = open('text.txt','r')
            fp.read()
        except FileNotFoundError:
            print('系统正在升级，请稍后再试')
        ```

