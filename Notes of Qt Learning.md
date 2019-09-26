# Notes of Qt Learning





## 信号槽

`所有类必须继承QObject之后才能有信号槽的能力`

`凡是继承自QObject的类，都应该在类定义的第一行写上Q_OBJECT，以此宏来展开提供信号槽/国际化等机制`



### connect函数

```c++
QMetaObject::Connection connect(const QObject *, const char *,
                                const QObject *, const char *,
                                Qt::ConnectionType);

QMetaObject::Connection connect(const QObject *, const QMetaMethod &,
                                const QObject *, const QMetaMethod &,
                                Qt::ConnectionType);

QMetaObject::Connection connect(const QObject *, const char *,
                                const char *,
                                Qt::ConnectionType) const;

QMetaObject::Connection connect(const QObject *, PointerToMemberFunction,
                                const QObject *, PointerToMemberFunction,
                                Qt::ConnectionType)

QMetaObject::Connection connect(const QObject *, PointerToMemberFunction,
                                Functor);
```

[Qt学习之路2 信号槽](https://www.devbean.net/2012/08/qt-study-road-2-signal-slot/ "https://www.devbean.net/2012/08/qt-study-road-2-signal-slot/")

