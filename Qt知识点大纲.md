# Qt 面试知识点大纲

## 一、Qt 整体架构
- 1.1 Qt 框架分层（模块结构图）
- 1.2 Qt4 与 Qt5/Qt6 的主要区别
- 1.3 跨平台原理

## 二、Qt 核心机制 ⭐
- 2.1 信号与槽机制
  - 原理与实现方式
  - Qt::ConnectionType（5种连接方式）
  - 跨线程信号槽
  - 优势与不足
- 2.2 元对象系统
  - Q_OBJECT 宏的作用
  - moc（元对象编译器）
  - 反射机制
- 2.3 事件循环与事件处理
  - 事件循环原理
  - 事件处理顺序
  - 事件过滤器
  - 常见事件类型

## 三、内存管理
- 3.1 对象树机制（父子关系）
- 3.2 内存泄漏防护
- 3.3 智能指针（QPointer、QSharedPointer）

## 四、常用控件详解
- 4.1 QListWidget / QListView（列表控件）
- 4.2 QTreeWidget / QTreeView（树形控件）
- 4.3 QTableWidget / QTableView（表格控件）
  - Model/View 架构
  - 自定义 Model
- 4.4 QChart（图表控件）
  - 折线图、柱状图、饼图
- 4.5 QGraphicsScene / QGraphicsView（图形视图框架）
  - 坐标系统
  - 图形项
  - 碰撞检测

## 五、QSS 样式表
- 5.1 基本语法与加载方式
- 5.2 选择器类型
  - 类型选择器、ID选择器、属性选择器
  - 后代选择器、伪状态、伪元素
- 5.3 常用控件样式示例
  - Button、LineEdit、Table、Tab
- 5.4 完整主题示例

## 六、多线程
- 6.1 QThread 基本用法
- 6.2 moveToThread 模式（推荐）
- 6.3 线程同步机制
  - QMutex、QReadWriteLock
  - QSemaphore、QWaitCondition

## 七、文件与配置
- 7.1 QFile 文件读写
- 7.2 QSettings 配置文件
- 7.3 JSON/XML 解析（QJsonDocument）

## 八、布局管理
- 8.1 基本布局（QVBoxLayout、QHBoxLayout、QGridLayout）
- 8.2 嵌套布局与 Spacer
- 8.3 响应式布局技巧

## 九、对话框与窗口
- 9.1 QDialog 模态/非模态对话框
- 9.2 QMessageBox 消息框
- 9.3 QMainWindow、QWidget、QDialog 区别

## 十、Qt 编译系统 ⭐
- 10.1 moc（元对象编译器）
  - 作用与原理
  - 生成文件规则
- 10.2 qmake
  - .pro 文件结构
  - 常用变量（TEMPLATE、TARGET、SOURCES、QT等）
  - CONFIG 配置
- 10.3 CMake
  - CMakeLists.txt 基本结构
  - find_package(Qt6)
  - qt_automoc
- 10.4 编译流程
  - 预处理 → moc → 编译 → 链接

## 十一、Qt 与 Windows API 互操作 ⭐
- 11.1 获取窗口句柄
  - winId() / WId()
  - QWidget::effectiveWinId()
- 11.2 Qt 调用 Windows API
  - HWND 与 QWidget 互转
  - Windows 消息处理
- 11.3 常用 Windows API 集成
  - 注册表操作
  - 系统托盘
  - DLL 加载

## 十二、C++ 标准库在 Qt 中的应用 ⭐
- 12.1 容器类对比
  - STL vs Qt 容器（QVector vs std::vector）
  - 隐式共享（写时复制）
- 12.2 字符串处理
  - QString vs std::string
  - 编码转换（UTF-8、GBK）
- 12.3 智能指针
  - std::unique_ptr、std::shared_ptr
  - QPointer、QSharedPointer
- 12.4 Lambda 表达式与 STL 算法
- 12.5 std::function 与 std::bind

## 十三、常见面试问题汇总 ⭐
- 13.1 信号槽相关问题
- 13.2 事件处理相关问题
- 13.3 内存管理相关问题
- 13.4 多线程相关问题
- 13.5 Model/View 架构相关问题
- 13.6 编译与构建相关问题

## 十四、调试技巧
- 14.1 qDebug 日志输出
- 14.2 dumpObjectInfo / dumpObjectTree
- 14.3 Qt Creator 调试器使用

## 十五、Qt 特有数据类型与工具类
- 15.1 基本数据类型
  - qint8, qint16, qint32, qint64
  - qreal, quintptr
- 15.2 字符串处理
  - QString, QByteArray, QLatin1String
- 15.3 容器类
  - QList, QVector, QMap, QHash, QSet
- 15.4 日期时间
  - QDateTime, QDate, QTime
- 15.5 文件与路径
  - QDir, QFileInfo, QPath

## 附录：快速参考
- A.1 常用头文件列表
- A.2 .pro 文件模板
- A.3 CMakeLists.txt 模板
- A.4 QSS 常用属性速查
