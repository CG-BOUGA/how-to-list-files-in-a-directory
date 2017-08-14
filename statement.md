```java runnable
// { autofold
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class Main {

public static void main(String[] args) throws Exception {

// }

Path directory = Paths.get("/");

// Method 1: get the files in the given directory
Files.list(directory)
    .filter(Files::isDirectory)
    .forEach(System.out::println);

// Method 2: recursively run through the tree (at a maximum depth of 2)
Files.walk(directory, 2)
    .filter(Files::isRegularFile)
    .forEach(System.out::println);

//{ autofold

}

}
//}
```
