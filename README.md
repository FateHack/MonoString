# MonoString
il2cpp游戏的string类实现char*与std::string的转换和修改

## 使用方法

```c++
//public static string get_applicationBundleIdentifier() { }

MonoString *(*get_applicationBundleIdentifier)();
MonoString *$get_applicationBundleIdentifier() {
    MonoString *str = get_applicationBundleIdentifier();
    const char *s = str->toChars(); //转const char*
    std::string ss = str->toString(); //转std::string
    str->setMonoString("monoString"); 
    str->setMonoString(string("monoString"));
    return get_applicationBundleIdentifier();
}
```

