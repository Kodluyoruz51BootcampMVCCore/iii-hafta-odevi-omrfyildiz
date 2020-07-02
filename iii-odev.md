# 1 Process vs Thread vs Task

### Process:
A process is an instance of a computer program that is being executed. It contains the program code and its current activity. Depending on the operating system (OS), a process may be made up of multiple threads of execution that execute instructions concurrently. Process-based multitasking enables you to run the Java compiler at the same time that you are using a text editor. In employing multiple processes with a single CPU,context switching between various memory context is used. Each process has a complete set of its own variables.

Process bir çalıştırılan bir bilgisayar programının örneğidir.Program kodunu ve o anki aktivitesini içerir. Çalışan sisteme(operating system) bağlı olarak, bir process mevcut durumda işleyen birden fazla threadden meydana gelebilir. Process temelli çoklu görev size hem bir compilerı hem de text editörünü aynı zamanda çalıştırma imkanı verir. Her bir process kendi değişken setine sahiptir.

### --------------

### Thread:
A thread is a basic unit of CPU utilization, consisting of a program counter, a stack, and a set of registers. A thread of execution results from a fork of a computer program into two or more concurrently running tasks. The implementation of threads and processes differs from one operating system to another, but in most cases, a thread is contained inside a process. Multiple threads can exist within the same process and share resources such as memory, while different processes do not share these resources. Example of threads in same process is automatic spell check and automatic saving of a file while writing. Threads are basically processes that run in the same memory context. Threads may share the same data while execution.

![Thread Diagram i.e. single thread vs multiple threads](https://i.stack.imgur.com/hwH8u.jpg)

Bir thread CPU(işlemci)'nun temel kullanım birimidir. Program sayacı, stack ve bir kayıt setinden oluşur. Threadlerin ya da processlerin uygulanmasının yerine getirilmesi bir çalışan sistemden diğerine göre değişebilir fakat çoğu durumda bir thread processin içinde yer alır. Çoklu threadler aynı processte var olabilir ve hafıza(memory) gibi kaynakları paylaşabilirken farklı processler bu kaynakları paylaşmaz. Aynı processteki threadler örneği otomatik yazım denetimi kontrolü ve bir dosya yazılırken otomatik kaydedilmesi olarak gösterilebilir. Temel olarak threadler aynı memory konteksinde çalışan processler olarak görülebilir. Uygulama çalışırken threadler aynı datayı paylaşabilir.

![Thread diagramı](https://i.stack.imgur.com/hwH8u.jpg)  

### --------------

### Task:
A task is a set of program instructions that are loaded in memory.

Bir task, belleğe yüklenen bir dizi program talimatıdır.

[Kaynak: StackOverFlow](https://stackoverflow.com/questions/3042717/what-is-the-difference-between-a-thread-process-task#:~:text=A%20task%20is%20simply%20a,or%20more%20simultaneously%20running%20tasks.&text=Threads%20differ%20from%20traditional%20multitasking,as%20subsets%20of%20a%20process)

# 2. Extensions
Extension Methods are a language feature that allow you to add methods to an existing type (class, struct, interface, etc). In a language like C#, an Extension Method has at least one parameter (this), which represents the object to operate on. Extension Methods are static methods that are called like class methods. That means that the object it operates on, does not need to be passed to it. Instead it is called on the object itself.

Extension metodlar bizim var olan tiplerimize(class, struct, interface v.b) metodlar eklememizi sağlar. C# dilinde extension metodu ***this*** parametresi ile sağlanır. Class metodları gibi bu metodlar da statik metodlardır. Bu, üzerinde çalıştığı nesnenin ona iletilmesine gerek olmadığı anlamına gelir. Bunun yerine nesnenin üzerinden çağrılır.

``` 
public static void IfType<T>(this object item, Action<T> action) where T : class {
    if (item is T) {
        action(item as T);
    }
}
``` 
Metodun çağrılması:
```
employee.IfType<Manager>(x => x.ActBusy());
```

[Kaynak: Extension Method](http://www.extensionmethod.net/)

## --------------

# 3.SQLite, bunu doğru şekilde (en güncel yol ile) nasıl kullanmalıyız? (Aktif halde kullanıp uygulama)

Bilgisayarımda Visual Studio'da çözemediğim bir hata aldığım için veritabanı işlemleri yapamadığımdan bunu boş bıraktım.
