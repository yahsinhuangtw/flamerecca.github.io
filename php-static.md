```php

class A {
    public static function getSelf(){
        return new self();    
    }

    public static function getStatic(){
        return new static();
    }
}

class B extends A {}

echo get_class(B::getSelf()); // A
echo get_class(B::getStatic()); // B
echo get_class(A::getSelf()); // A
echo get_class(A::getStatic()); // A
```

self 代表這個實際下 new 這個關鍵字的類別。在上面的例子裡面，就是 A 這個類別。

static 則代表呼叫該函式的物件。所以在上面的例子裡，會是 B 這個類別。

參考資料：[https://stackoverflow.com/questions/5197300/new-self-vs-new-static](https://stackoverflow.com/questions/5197300/new-self-vs-new-static)
