Cd no argument:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cd
@alif1383 ➜ ~ $ pwd
/home/codespace
```

I got this result from doing cd with no argument because cd with no argument sets the directory to the main directory

This is not an error, everything is working as expected since cd is supposed to move directory. 

Cd one path to directory:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cd messages
@alif1383 ➜ /workspaces/lecture1/messages (main) $ 
```


I got this result because I passed messages as the argument to cd, so cd opened that directory.

This is not an error.

CD one path to file:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cd Hello.java
bash: cd: Hello.java: Not a directory
@alif1383 ➜ /workspaces/lecture1 (main) $ 
```


I got this output because cd only works with directories not files

This is an error because cd expects directories not path to a specific file, so it resulted in this error and the directory wasn’t changed.

Ls:

No Argument:
```
p@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ ls
Hello.java  README  messages
@alif1383 ➜ /workspaces/lecture1 (main) $ 
```

I got this result because ls shows all things in this directory, and since these three items are there, it showed these

This isn’t an error.


Path to file:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ ls Hello.java
Hello.java
@alif1383 ➜ /workspaces/lecture1 (main) $ 
```
I got this result because I provided the path to a file, so ls gave out the name of that file as that was the only thing in that specific path to the file

This isn’t an error

Path to directory:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ ls messages
en-us.txt  es-mx.txt  zh-cn.txt
@alif1383 ➜ /workspaces/lecture1 (main) $ 
```

I got this result because ls showed all of the files in the /messages directory

This isn’t an error.

CAT:
No Argument:
```
@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cat
```


I got no result because no arguments was passed, so it just skips and makes empty lines when return is pressed.

This isn;t an error

One Argument to Directory:
```

p@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cat messages
cat: messages: Is a directory
```

This result popped up because the argument was a directory, not a file as expected

This is an error as cat expects a file path

File path:
```

@alif1383 ➜ /workspaces/lecture1 (main) $ pwd
/workspaces/lecture1
@alif1383 ➜ /workspaces/lecture1 (main) $ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}@alif1383 ➜ /workspaces/lecture1 (main) $ 
```

As expected, the cat command printed out all lines written in the Hello.java file

This is not an error.



