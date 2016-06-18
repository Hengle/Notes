# Java�﷨��֮foreach
�﷨����һ�ּ���ÿ�����Ի����ٶ��ṩ����һЩ�������Ա����������﷨����ֻ�Ǳ�����ʵ�ֵ�һЩС��Ϸ���ˣ������ڼ����ض����ֽ�������ض��ķ�ʽ����Щ�﷨��һЩ���������߾Ϳ���ֱ�ӷ����ʹ���ˡ���Щ�﷨����Ȼ�����ṩʵ���ԵĹ��ܸĽ����������ǻ���������ܡ����������﷨���Ͻ��ԡ����ܼ��ٱ������Ļ��ᡣJava�ṩ�����û��������﷨�ǣ����緺�͡��Զ�װ�䡢�Զ����䡢foreachѭ�����䳤�������ڲ��ࡢö���ࡢ���ԣ�assert���ȡ�

��ƪ��Ҫ�ǽ���foreach,foreach���﷨��������֮�������ʲô�أ�

��������һ�����ӣ�

```java
package foreach;
 
import java.util.ArrayList;
import java.util.List;
 
public class ForeachTest
{
    public static void main(String[] args)
    {
        List<String> list = new ArrayList<>();
        list.add("s1");
        list.add("s2");
 
        for(String s : list)
        {
            System.out.println(s);
        }
    }
}
```

���������з����룺

```java
javac ForeachTest.java
   javap -verbose ForeachTest > f1.txt
```

��f1.txt,���������ʾ��

```java
Classfile /D:/workspace_jee/JavaTest/src/foreach/ForeachTest.class
  Last modified 2016-2-25; size 798 bytes
  MD5 checksum c64e6f81f34d1dfc7834ad8d5b3b1801
  Compiled from "ForeachTest.java"
public class foreach.ForeachTest
  SourceFile: "ForeachTest.java"
  minor version: 0
  major version: 51
  flags: ACC_PUBLIC, ACC_SUPER
 
Constant pool:
   #1 = Methodref          #14.#26        //  java/lang/Object."<init>":()V
   #2 = Class              #27            //  java/util/ArrayList
   #3 = Methodref          #2.#26         //  java/util/ArrayList."<init>":()V
   #4 = String             #28            //  s1
   #5 = InterfaceMethodref #29.#30        //  java/util/List.add:(Ljava/lang/Object;)Z
   #6 = String             #31            //  s2
   #7 = InterfaceMethodref #29.#32        //  java/util/List.iterator:()Ljava/util/Iterator;
   #8 = InterfaceMethodref #33.#34        //  java/util/Iterator.hasNext:()Z
   #9 = InterfaceMethodref #33.#35        //  java/util/Iterator.next:()Ljava/lang/Object;
  #10 = Class              #36            //  java/lang/String
  #11 = Fieldref           #37.#38        //  java/lang/System.out:Ljava/io/PrintStream;
  #12 = Methodref          #39.#40        //  java/io/PrintStream.println:(Ljava/lang/String;)V
  #13 = Class              #41            //  foreach/ForeachTest
  #14 = Class              #42            //  java/lang/Object
  #15 = Utf8               <init>
  #16 = Utf8               ()V
  #17 = Utf8               Code
  #18 = Utf8               LineNumberTable
  #19 = Utf8               main
  #20 = Utf8               ([Ljava/lang/String;)V
  #21 = Utf8               StackMapTable
  #22 = Class              #43            //  java/util/List
  #23 = Class              #44            //  java/util/Iterator
  #24 = Utf8               SourceFile
  #25 = Utf8               ForeachTest.java
  #26 = NameAndType        #15:#16        //  "<init>":()V
  #27 = Utf8               java/util/ArrayList
  #28 = Utf8               s1
  #29 = Class              #43            //  java/util/List
  #30 = NameAndType        #45:#46        //  add:(Ljava/lang/Object;)Z
  #31 = Utf8               s2
  #32 = NameAndType        #47:#48        //  iterator:()Ljava/util/Iterator;
  #33 = Class              #44            //  java/util/Iterator
  #34 = NameAndType        #49:#50        //  hasNext:()Z
  #35 = NameAndType        #51:#52        //  next:()Ljava/lang/Object;
  #36 = Utf8               java/lang/String
  #37 = Class              #53            //  java/lang/System
  #38 = NameAndType        #54:#55        //  out:Ljava/io/PrintStream;
  #39 = Class              #56            //  java/io/PrintStream
  #40 = NameAndType        #57:#58        //  println:(Ljava/lang/String;)V
  #41 = Utf8               foreach/ForeachTest
  #42 = Utf8               java/lang/Object
  #43 = Utf8               java/util/List
  #44 = Utf8               java/util/Iterator
  #45 = Utf8               add
  #46 = Utf8               (Ljava/lang/Object;)Z
  #47 = Utf8               iterator
  #48 = Utf8               ()Ljava/util/Iterator;
  #49 = Utf8               hasNext
  #50 = Utf8               ()Z
  #51 = Utf8               next
  #52 = Utf8               ()Ljava/lang/Object;
  #53 = Utf8               java/lang/System
  #54 = Utf8               out
  #55 = Utf8               Ljava/io/PrintStream;
  #56 = Utf8               java/io/PrintStream
  #57 = Utf8               println
  #58 = Utf8               (Ljava/lang/String;)V
{
  public foreach.ForeachTest();
    flags: ACC_PUBLIC
 
    Code:
      stack=1, locals=1, args_size=1
         0: aload_0       
         1: invokespecial #1                  // Method java/lang/Object."<init>":()V
         4: return       
      LineNumberTable:
        line 6: 0
 
  public static void main(java.lang.String[]);
    flags: ACC_PUBLIC, ACC_STATIC
 
    Code:
      stack=2, locals=4, args_size=1
         0: new           #2                  // class java/util/ArrayList
         3: dup           
         4: invokespecial #3                  // Method java/util/ArrayList."<init>":()V
         7: astore_1      
         8: aload_1       
         9: ldc           #4                  // String s1
        11: invokeinterface #5,  2            // InterfaceMethod java/util/List.add:(Ljava/lang/Object;)Z
        16: pop           
        17: aload_1       
        18: ldc           #6                  // String s2
        20: invokeinterface #5,  2            // InterfaceMethod java/util/List.add:(Ljava/lang/Object;)Z
        25: pop           
        26: aload_1       
        27: invokeinterface #7,  1            // InterfaceMethod java/util/List.iterator:()Ljava/util/Iterator;
        32: astore_2      
        33: aload_2       
        34: invokeinterface #8,  1            // InterfaceMethod java/util/Iterator.hasNext:()Z
        39: ifeq          62
        42: aload_2       
        43: invokeinterface #9,  1            // InterfaceMethod java/util/Iterator.next:()Ljava/lang/Object;
        48: checkcast     #10                 // class java/lang/String
        51: astore_3      
        52: getstatic     #11                 // Field java/lang/System.out:Ljava/io/PrintStream;
        55: aload_3       
        56: invokevirtual #12                 // Method java/io/PrintStream.println:(Ljava/lang/String;)V
        59: goto          33
        62: return       
      LineNumberTable:
        line 10: 0
        line 11: 8
        line 12: 17
        line 14: 26
        line 16: 52
        line 17: 59
        line 18: 62
      StackMapTable: number_of_entries = 2
           frame_type = 253 /* append */
             offset_delta = 33
        locals = [ class java/util/List, class java/util/Iterator ]
           frame_type = 250 /* chop */
          offset_delta = 28
}
```

��������������ݺܶ࣬������Ҳû��ϵ���ؼ�����Iterator�����־����ʵ�ڶ���ʵ��Iterable�ӿڵĶ������foreach�﷨�ǵĻ����������Ὣ���for�ؼ���ת��Ϊ��Ŀ��ĵ�����ʹ�á�

����Ĵ���ᱻת��Ϊ���µĴ��룺

```java
package foreach;
 
import java.util.ArrayList;
import java.util.List;
 
public class ForeachTest
{
    //���������û����ʾ���캯���������һ��Ĭ�ϵĹ��캯���������������"�������"�׶���ɵ�
    public ForeachTest()
    {
        super();
    }
 
    public static void main(String[] args)
    {
        List<String> list = new ArrayList<>();
        list.add("s1");
        list.add("s2");
 
        for(java.util.Iterator i$ = list.iterator(); i$.hasNext();)
        {
            String s = (String) i$.next();
            {
                System.out.println(s);
            }
        }
    }
}
```

*ע�����Ҫ��ʹ�Լ��Զ��������Բ���foreach�﷨�Ǿͱ���ʵ��Iterable�ӿڡ�*

ϸ�ĵ����ѿ��ܻ�ע�⵽��java�е�����Ҳ���Բ���foreach���﷨�ǣ��������鲢û��ʵ��Iterable�ӿ�ѽ��

�����پ�һ�����ӣ�

```java
package foreach;
 
public class ForeachTest2
{
    public static void main(String[] args)
    {
        String arr[] = {"s1","s2"};
 
        for(String s:arr)
        {
            System.out.println(s);
        }
    }
}
```

����������

```java
Classfile /D:/workspace_jee/JavaTest/src/foreach/ForeachTest2.class
  Last modified 2016-2-25; size 581 bytes
  MD5 checksum 51656b3d3812c5ae3977fffd897a3441
  Compiled from "ForeachTest2.java"
public class foreach.ForeachTest2
  SourceFile: "ForeachTest2.java"
  minor version: 0
  major version: 51
  flags: ACC_PUBLIC, ACC_SUPER
 
Constant pool:
   #1 = Methodref          #8.#19         //  java/lang/Object."<init>":()V
   #2 = Class              #20            //  java/lang/String
   #3 = String             #21            //  s1
   #4 = String             #22            //  s2
   #5 = Fieldref           #23.#24        //  java/lang/System.out:Ljava/io/PrintStream;
   #6 = Methodref          #25.#26        //  java/io/PrintStream.println:(Ljava/lang/String;)V
   #7 = Class              #27            //  foreach/ForeachTest2
   #8 = Class              #28            //  java/lang/Object
   #9 = Utf8               <init>
  #10 = Utf8               ()V
  #11 = Utf8               Code
  #12 = Utf8               LineNumberTable
  #13 = Utf8               main
  #14 = Utf8               ([Ljava/lang/String;)V
  #15 = Utf8               StackMapTable
  #16 = Class              #29            //  "[Ljava/lang/String;"
  #17 = Utf8               SourceFile
  #18 = Utf8               ForeachTest2.java
  #19 = NameAndType        #9:#10         //  "<init>":()V
  #20 = Utf8               java/lang/String
  #21 = Utf8               s1
  #22 = Utf8               s2
  #23 = Class              #30            //  java/lang/System
  #24 = NameAndType        #31:#32        //  out:Ljava/io/PrintStream;
  #25 = Class              #33            //  java/io/PrintStream
  #26 = NameAndType        #34:#35        //  println:(Ljava/lang/String;)V
  #27 = Utf8               foreach/ForeachTest2
  #28 = Utf8               java/lang/Object
  #29 = Utf8               [Ljava/lang/String;
  #30 = Utf8               java/lang/System
  #31 = Utf8               out
  #32 = Utf8               Ljava/io/PrintStream;
  #33 = Utf8               java/io/PrintStream
  #34 = Utf8               println
  #35 = Utf8               (Ljava/lang/String;)V
{
  public foreach.ForeachTest2();
    flags: ACC_PUBLIC
 
    Code:
      stack=1, locals=1, args_size=1
         0: aload_0       
         1: invokespecial #1                  // Method java/lang/Object."<init>":()V
         4: return       
      LineNumberTable:
        line 3: 0
 
  public static void main(java.lang.String[]);
    flags: ACC_PUBLIC, ACC_STATIC
 
    Code:
      stack=4, locals=6, args_size=1
         0: iconst_2      
         1: anewarray     #2                  // class java/lang/String
         4: dup           
         5: iconst_0      
         6: ldc           #3                  // String s1
         8: aastore       
         9: dup           
        10: iconst_1      
        11: ldc           #4                  // String s2
        13: aastore       
        14: astore_1      
        15: aload_1       
        16: astore_2      
        17: aload_2       
        18: arraylength   
        19: istore_3      
        20: iconst_0      
        21: istore        4
        23: iload         4
        25: iload_3       
        26: if_icmpge     49
        29: aload_2       
        30: iload         4
        32: aaload        
        33: astore        5
        35: getstatic     #5                  // Field java/lang/System.out:Ljava/io/PrintStream;
        38: aload         5
        40: invokevirtual #6                  // Method java/io/PrintStream.println:(Ljava/lang/String;)V
        43: iinc          4, 1
        46: goto          23
        49: return       
      LineNumberTable:
        line 7: 0
        line 9: 15
        line 11: 35
        line 9: 43
        line 13: 49
      StackMapTable: number_of_entries = 2
           frame_type = 255 /* full_frame */
          offset_delta = 23
          locals = [ class "[Ljava/lang/String;", class "[Ljava/lang/String;", class "[Ljava/lang/String;", int, int ]
          stack = []
           frame_type = 248 /* chop */
          offset_delta = 25
 
}
```

��������ͬ��û��ϵ~�������ע�⵽�����foreach�﷨�ǲ�û�в���Iterableʵ��ת�������������Ϣֻ���漰һЩѹջ��վ�����ݡ������Ľ������������ʾ��

```java
package foreach;
 
public class ForeachTest2
{
    public ForeachTest2()
    {
        super();
    }
 
    public static void main(String[] args)
    {
        int arr[] = {1,2};
        int [] arr$ = arr;
        for(int len$ = arr$.length, i$ = 0; i$<len$; ++i$ )
        {
            int i = arr$[i$];
            {
                System.out.println(i);
            }
        }
    }
}
```

���Կ�������������ԣ���ʵ����ת��Ϊ��ͨ�ı������ѣ�

����foreach�﷨�ǵ���Ϣ�����������ˇ��� ��Ȼû�У�

����ʵ��RandomAccess�ӿڵļ��ϱ���ArrayList��Ӧ��ʹ������ͨ��forѭ��������foreachѭ�������������Ե�һ����������Ƿ��֮����

���ȿ�һ��jdk1.7�ж�RandomAccess�ӿڵĶ��壺

java.util

**Interface RandomAccess**

All Known Implementing Classes:

ArrayList, AttributeList, CopyOnWriteArrayList, RoleList, RoleUnresolvedList, Stack, Vector

**public interface RandomAccess**

Marker interface used by List implementations to indicate that they support fast (generally constant time) random access. The primary purpose of this interface is to allow generic algorithms to alter their behavior to provide good performance when applied to either random or sequential access lists.

The best algorithms for manipulating random access lists (such as ArrayList) can produce quadratic behavior when applied to sequential access lists (such as LinkedList). Generic list algorithms are encouraged to check whether the given list is an instanceof this interface before applying an algorithm that would provide poor performance if it were applied to a sequential access list, and to alter their behavior if necessary to guarantee acceptable performance.

It is recognized that the distinction between random and sequential access is often fuzzy. For example, some List implementations provide asymptotically linear access times if they get huge, but constant access times in practice. Such a List implementation should generally implement this interface. **As a rule of thumb, a List implementation should implement this interface if, for typical instances of the class, this loop:**

for (int i=0, n=list.size(); i < n; i++)

list.get(i);

runs faster than this loop:

for (Iterator i=list.iterator(); i.hasNext(); )

i.next();

This interface is a member of the Java Collections Framework.

**�����°汾��ʼ��**

1.4

������Ӣ��Ҳû��ϵ����������һ�����һ��ӴֵĻ���ʵ�ʾ��������ʵ��RandomAccess�ӿڵ���ʵ����������������ʵģ�ʹ����ͨforѭ��Ч�ʽ�����ʹ��foreachѭ�����������������˳����ʵģ���ʹ��Iterator��Ч�ʸ��ߡ�

����ʹ���������µĴ������жϣ�

```java
if (list instanceof RandomAccess) { 
	for (int i = 0; i < list.size(); i++){}
} else {
	Iterator<?> iterator = list.iterable(); while (iterator.hasNext()){iterator.next()}
}
```

��ʵ�������ArrayListԴ���ͬѧҲ����ע�⵽��ArrayList�ײ��ǲ�������ʵ�ֵģ��������Iterator��������ô��Ҫ�������ָ��ȥִ����Щֵ������next();hasNext()���ȣ�������Ȼ�������ڴ濪���Լ�ִ��Ч�ʡ�

**����javap(���������)���**

javap��JDK�Դ��ķ�����������Բ鿴java������Ϊ�������ɵ��ֽ��롣ͨ���������ǿ��Զ���Դ������ֽ��룬�Ӷ��˽�ܶ�������ڲ��Ĺ�����

�﷨��

```
javap [ ����ѡ�� ] class��
```

javap �������ڽ������ļ��������ȡ�������õ�ѡ���û��ʹ��ѡ�javap ��������ݸ�������� public �򼰷�����javap �����������׼����豸�ϡ�

**����ѡ��**

- `-help` ��� javap �İ�����Ϣ��

- `-l` ����м��ֲ�������

- `-b` ȷ���� JDK 1.1 javap ���������ԡ�

- `-public` ֻ��ʾ public �༰��Ա��

- `-protected` ֻ��ʾ protected �� public �༰��Ա��

- `-package` ֻ��ʾ����protected �� public �༰��Ա������ȱʡ���á�

- `-private` ��ʾ������ͳ�Ա��

- `-J[flag]` ֱ�ӽ� flag ��������ʱϵͳ��

- `-s` ����ڲ�����ǩ����

- `-c` ������и�������δ�����Ĵ��룬������ Java �ֽ����ָ�

- `-verbose` �����ջ��С���������� locals �� args ��,�Լ�class�ļ��ı���汾

- `-classpath[·��]` ָ�� javap �����������·������������˸�ѡ�����������ȱʡֵ�� CLASSPATH ����������Ŀ¼��ð�ŷָ���

- `- bootclasspath[·��]` ָ�������Ծ������õ�·����ȱʡ����£��Ծ�����ʵ�ֺ��� Java ƽ̨���࣬λ�� jrelibt.jar �� jrelibi18n.jar �С�

- `-extdirs[dirs]` ����������װ��ʽ��չ��λ�á���չ��ȱʡλ���� jrelibext��