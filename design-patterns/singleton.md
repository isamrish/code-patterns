# Singleton pattern

The singleton pattern is useful when you want to have only single object of a class.

Here is very basic implementation of Singleton pattern in Javascript.

```
class Singleton {
  constructor() {
    if(!Singleton.instance) {
      Singleton.instance = new Singleton();
    }
    return Singleton.instance;
  }
}
```


