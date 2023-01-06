---
layout: post
title:  "Welcome to Algorithm!"
---

# Welcome

**Hello world**, this is my first Jekyll blog post.

I hope you like it!

## Compiling and running with only a JDK

### Create a classes folder
Test here
```
fun maxArea(a: IntArray): Int {

    var n = a.size
    var i = 0
    var j = n-1

    var m = 0
    while(i<j){
        var area = (j-i) * min(a[i], a[j])
        println("area =($j -$i) * min(${a[i]}, ${a[j]}) = $area")
        m = max(area, m)
        if(a[i] < a[j]){
            i++
        } else {
            j--
        }
    }
    return m
}
```

### Compile the algorithm

```
javac -sourcepath src/main/java -d classes src/main/java/ <relative-path-to-java-source-file>
```

### Run the algorithm

```
java -cp classes <class-fully-qualified-name>
```