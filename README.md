# CSE 11 kit

What you need to write the book's programs on your own computer, or in a
GitHub Codespace:

```
Pict.java          the book's picture library (leave it as it is)
Example.java       a program that uses it
ExampleTest.java   JUnit tests for it
lib/junit.jar      JUnit 6.1.3 (console standalone), under lib/LICENSE-junit.md
.devcontainer/     the Codespace: Java 25 and the VS Code Java extensions
```

## Run a program

```
java -ea Example.java
```

There is no separate compile step: Java compiles `Example.java`, and the
`Pict.java` next to it, as it starts. `-ea` turns on `assert`. The program
writes `example.png`. `ImageIO_.show` opens a window on your own computer; a
Codespace has no display, so there it writes `shown-0.png` instead.

Java 25 or newer is required (`void main()` with no class around it). The
Codespace has it; on your own computer, install a JDK from
<https://adoptium.net>.

## Run the tests

```
javac -d out -cp lib/junit.jar *.java
java -jar lib/junit.jar execute --class-path out --scan-class-path
```

In VS Code (and so in a Codespace), the Testing panel runs them too.

## Where this comes from

This kit is generated from the `kit/` folder of the CSE 11 book's source, one
branch per edition of the book (`fa26` is Fall 2026). Changes made here are
overwritten by the next publish; send them to the book instead.
