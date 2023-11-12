# Java基础知识笔记

静态方法:多用在测试类和工具类中.

![1699761110962](image/JavaSE/1699761110962.png)


工具类的介绍:![1699761350575](image/JavaSE/1699761350575.png)

详细情况要看Eclipse的Student的实操 其中有相应的实例

其中重点;:

❶：ArrayList `<student>` list = newArrayList<>();:

1. `ArrayList`: 这是Java中的一个动态数组实现，它允许你在运行时动态添加或删除元素。`ArrayList`属于 `java.util`包。
2. `<Student>`: 这是泛型的使用，它表示这个ArrayList只能存储 `Student`类型的对象。泛型提供了在编译时期强类型检查的好处，可以防止在运行时出现类型不匹配的错误。
3. list: 这是变量名，你可以使用任何合法的Java标识符作为变量名。在这里。
4. `= new ArrayList<>();`: 这是创建一个新的 `ArrayList`对象并将其分配给变量 `list`。右侧的 `new ArrayList<>();`是通过默认构造函数创建一个新的 `ArrayList`实例。在Java 7及以后的版本中，可以使用 `<>`来表示泛型类型，而无需再次指定泛型类型参数。

❷：StringBuilder的作用

`StringBuilder` 是 Java 中的一个类，它属于 `java.lang` 包。`StringBuilder` 的主要作用是提供一个可变的字符序列，允许你对字符串进行动态的操作，例如追加、插入、删除字符等。与之类似的类是 `StringBuffer`，也提供了类似的功能，但它是线程安全的，而 `StringBuilder` 则不是。因此，如果在单线程环境中进行字符串操作，通常推荐使用 `StringBuilder`，因为它的性能更好。

`StringBuilder` 的主要方法之一是 `append`，它用于在字符串的末尾追加新的内容。除了 `append`，`StringBuilder` 还提供了其他一些方法，如 `insert`（在指定位置插入字符或字符串）、`delete`（删除指定范围内的字符）、`reverse`（反转字符串）等，使得你能够方便地对字符串进行修改。

使用 `StringBuilder` 的好处在于避免了在每次对字符串进行修改时都创建新的字符串对象，这样可以提高性能。这在需要频繁修改字符串内容的情况下尤为重要，比如在循环中拼接字符串或动态生成大量字符串时。



## Java基础变量

## Java面向对象
