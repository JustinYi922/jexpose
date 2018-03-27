# jexpose

This project can expose class graph inside of jar.

```
jexpose entry entryJarPath libDirPath jrtPath
```

Option | Meaning
-------|--------
entry| the entry point to start our exposing
entryJarPath | path of target jar
libDirPath| path of directory which is comprise of dependencies of target jar
jrtPath| although you've specified the tar jar and all of it's dependencies the java runtime such as `java/lang/*` are still isolated, so you should indicate a path to tell jexpose where to find them

After exposing, jexpose will produce a json file, content of it looks like:

```json
{
  "classes": {
    "com.hsiaosiyuan.ServiceProvider": { ... }
    ...
  },
  "providers": [
    "com.hsiaosiyuan.ServiceProvider"
  ]
}
```
