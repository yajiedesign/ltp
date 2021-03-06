2014-10-16
----------
第一届语言技术平台（LTP）用户大会将于2014年10月31日上午在北京召开，欢迎大家参加！会议详细信息见http://ir.hit.edu.cn/ltp-2014/，有意者请于10月20日之前填写在线会议注册表。

2014-10-11
----------
语言技术平台3.1.2版 发布
* [修改] 修改`utils/template.hpp`的实现，提高40%的速度性能
* [修改] 修改`_WIN32`宏在mingw下的歧义，使得LTP在`Codeblocks - Mingw Makefile`模式下正常编译
* [修改] 修改非unix系统的编译目标，使得win32与win64都不进行ltp_server以及unittest的编译
* [增加] 自动化测试脚本

2014-06-18
----------
语言技术平台3.1.1版 发布
* [创建] 创建Java封装，ltp4j：https://github.com/HIT-SCIR/ltp4j
* [创建] 创建Python封装，pyltp：https://github.com/HIT-SCIR/pyltp
* [增加] 词性标注模块添加了词典功能，用户可以为特定词语指定候选词性
* [增加] 训练数据增加微博数据，提高了互联网语料的处理能力
* [增加] 增加编程接口中的数据合法性检查
* [增加] 增加单元测试模块
* [修改] 修改了预处理规则，使得`iphone5s`这样的产品名不会被切开
* [修改] 修改了语义角色标注训练套件的bug

2014-01-20
----------
语言技术平台3.1.0版 发布
* 在分词、词性标注和依存句法分析模块中加入模型裁剪功能，减少了模型大小。用户可以通过配置文件里的rare-feature-threshold参数配置裁剪力度，如果rare-feature-threshold为0，则只去掉为0的特征；rare-feature-threshold大于0时将一步去掉更新次数低于阈值的特征。这一优化方法主要参考[Learning Sparser Perceptron Models](http://www.cs.bgu.ac.il/~yoavg/publications/acl2011sparse.pdf)。
* 增加了`ltp_server`在异常输入情况下返回错误代码，如果输入数据编码错误或者输入xml不符合规则，将返回400
* 修复了词性标注、命名实体识别、依存句法分析训练套件中的内存泄露问题
* 修复了语义角色标注的内存泄露问题
* 修复了词性标注、命名实体识别模型文件的错误标示符，这项修改将导致3.1.0以及之后的版本不能与3.0.x的模型兼容，请务必注意
* 修复了由boost.multi_array.views引起的MSVC下不能以Debug方式编译的问题
* 修复了由打开文件时字符串为空引起的Windows下不能正常运行的bug

2013-09-29
----------
语言技术平台3.0.1版 发布
* 解决windows编译问题
* 实现各模块多线程支持
* 新增linux下多线程LTP工具包，multi_ltp_test
* 实现服务器程序ltp_server多线程支持
* 修复4长度utf-8字符、伪标记导致%的标注结果等bug

2013-09-01
----------
语言技术平台3.0.0版 发布
* 从底层开始，实现了一套中文文本处理库
* 实现在线机器学习算法框架
* 在算法框架基础上实现了分词、词性标注、命名实体识别和依存句法分析四个模块
* 实现模型裁剪，提高内存性能
* 实现L1优化的最大熵模型，大幅度提高内存性能
* 在L1优化最大熵的基础上实现语义角色标注模块
* 在分词模块中实现了用户自定义字典的逻辑
* 在依存句法分析模块中实现了二阶解码，提高分析准确率
* 完善了训练套件，使用户可以更灵活地训练模型

2013-04-03
----------
LTP v2.2 发布
* 项目从采用Automake改为采用CMake编译
* 解决LTP对于boost库以及其他一些第三方库的依赖
* 将分词、词性标注、依存句法分析以及语义角色标注的训练模块开源
* 重制了部分文档
* 修复了高版本GCC不能编译的bug

2011-06-01
----------
LTP正式开源

2009-06-19
----------
LTP v2.1 发布

* 增加CRFWordSeg接口
* 解决了若干svmtagger的bug
* 解决了若干ner的bug
* 解决LTP对文字进行修改的bug
* 解决使用vector作为DLL接口参数类型的bug (VS2008下出错)
* 更新LTP使用文档
* 最新版我们只提供vs2008对应的DLL，如果希望在visual studio其他版本上运行，可以尝试安装Microsoft Visual C++ 2008 Redistributable Package (x86)

2008-07-07
----------
LTP v1.5.0 发布

2008-04-24
----------
LTP v1.4.3 发布

2007-12-03
----------
LTP v1.4.1 发布

2007-12-02
----------
LTP v1.4.0 发布

2007-04-13
----------
LTP v1.3 发布

* IRLAS的extend_dict解密,不采用加密文件
* 解决Parser越界错误
* 采用LTMLv2.0格式
* 发布python包
* 补充英文文档

