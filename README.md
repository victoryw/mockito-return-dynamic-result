# mockito-return-dynamic-result

这个练习是想展示 `mockito` 在 stub 一个方法时，如何在多次调用时返回动态的结果：

* 方法1：通过 `thenReturn().thenReturn()` 这样的链式方法依次定义每次调用的返回结果。[官方说明](https://javadoc.io/static/org.mockito/mockito-core/4.10.0/org/mockito/Mockito.html#stubbing_consecutive_calls)

* 方法2：通过 `thenAnswer(Answer object)` 这样的参数提供对于 stub 结果的 callback。[官方说明](https://javadoc.io/static/org.mockito/mockito-core/4.10.0/org/mockito/Mockito.html#answer_stubs)。这里使用 `java` 的 `lambada` 函数代替了对 `Answer` 的抽象类定义。