```java runnable
// { autofold
import static java.nio.file.StandardOpenOption.APPEND;

import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class Main {

public static void main(String[] args) throws Exception {

// }

Path directory = Paths.get("/etc");

// Method 1: using Streams
Files.list(directory)
  .forEach(path -> System.out.println(path));

//{ autofold

}

}
//}
```
