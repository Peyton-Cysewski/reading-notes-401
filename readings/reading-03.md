# System.IO

## File and Stream I/O
- Using System.IO you can read data from storage, or from a stream of data.
- It is important to have a robust system of exception handling in place when dealing with external files.
- Streams deal with three main types of transactions: Reading, Writing, and Seeking.
- Encoded characters can also be read such as binary, characters, strings, and text.
- Asynchronous operations can be used when a file can have excessive amounts of data to the point where the overall process is too resource intensive to do all the operations at the same time.
- There are many methods that allow for data to be compressed (or zipped).
- Isolated storage can be used during any of these processes for safely dealing with code.
- Keep in mind that there are several security protocols to follow to to ensure the safe handling of data.

## Write to a File
Here is an example of code that writes three lines of strings to a file called WriteLines.txt:
```
using System;
using System.IO;

class Program
{
    static void Main(string[] args)
    {

        // Create a string array with the lines of text
        string[] lines = { "First line", "Second line", "Third line" };

        // Set a variable to the Documents path.
        string docPath =
          Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        // Write the string array to a new file named "WriteLines.txt".
        using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt")))
        {
            foreach (string line in lines)
                outputFile.WriteLine(line);
        }
    }
}

```

## Read from a File
This examples shows a program that creates a file and writes the integers 1 through 10 in it. It then takes that file and reads directly from it outputting the integers in the console.
```
using System;
using System.IO;

class MyStream
{
    private const string FILE_NAME = "Test.data";

    public static void Main()
    {
        if (File.Exists(FILE_NAME))
        {
            Console.WriteLine($"{FILE_NAME} already exists!");
            return;
        }

        using (FileStream fs = new FileStream(FILE_NAME, FileMode.CreateNew))
        {
            using (BinaryWriter w = new BinaryWriter(fs))
            {
                for (int i = 0; i < 11; i++)
                {
                    w.Write(i);
                }
            }
        }

        using (FileStream fs = new FileStream(FILE_NAME, FileMode.Open, FileAccess.Read))
        {
            using (BinaryReader r = new BinaryReader(fs))
            {
                for (int i = 0; i < 11; i++)
                {
                    Console.WriteLine(r.ReadInt32());
                }
            }
        }
    }
}

```



[Table of Contents](../README.md)
