# Java基础面试题

### 1. Java有哪些特点

<details class="lake-collapse"><summary id="u645cdbe5"><span class="ne-text">Java的特点</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u1c2b658a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">简单易学：Java有丰富的类库，不用手写轮子</span></li><li id="u3a73d38f" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">面向对象：Java是一门面向对象的语言，支持封装、继承、多态</span></li><li id="ud3b96b05" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">跨平台性：Java程序可以在不同的操作系统和硬件平台上运行，实现了</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">一次编写，到处运行的目标</span></li><li id="u8b6e396f" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">安全性：Java具有高度的安全性，提供了注入类加载器、安全管理器和异常处理机制等安全机制</span></li></ol><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="uefca2042" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java类加载器采用双亲委派模式，即在加载类时先从父类加载器中查找对应的类，如果父类加载器中没有找到，则再去子类加载器中查找。这种机制可以防止对Java核心类库的篡改，并确保应用程序使用的是正确的类。如果你自己手写了一个Object类，这个手写的Object类是不会被加载的，而是会使用Java提供的Object类</span></li><li id="u35f5ccf9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">如果你就是想用自己写的Object类，那么需要自定义类加载器，重写其findClass方法</span></li></ul></ul><ol start="5" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u72b46d38" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">多线程：Java语言支持多线程编程，可以方便的实现并发操作</span></li><li id="ucd317e3e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">开放性：Java是一种开放性语言，具有开放的标准和规范，可以与其他语言进行交互和集成</span></li><li id="ue6f75bff" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">高性能：Java的性能不断提高，特别是JIT编译器的引用使得Java程序的性能可以与C++等编译型语言媲美</span></li></ol><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="u5efea1ad" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">当JIT编译器发现某个方法被频繁调用时，它会将该方法的字节码转换为本地机器码来提高执行速度。这是因为字节码是一种跨平台的中间代码，其性能较低，而本地机器码是针对特定硬件平台的机器指令，其性能更高。</span></li></ul></ul></details>

### 2. 面向对象和面向过程的区别

<details class="lake-collapse"><summary id="u57b36cb4"><span class="ne-text">面向对象和面向过程的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ua2ad2b49" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">面向过程</span><span class="ne-text" style="color: rgb(76, 73, 72)">：是分析解决问题的步骤，然后用函数把这些步骤一步一步地实现，然后在使用时调用即可。性能较高，单片机、嵌入式开发一般采用面向过程开发</span></li><li id="u758bdce5" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">面向对象</span><span class="ne-text" style="color: rgb(76, 73, 72)">：是把构成问题的事物分解成各个对象，而建立对象的目的也不是为了完成一个个步骤，而是为了描述某个事物在解决整个问题的过程中所发生的行为。面向对象有</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">封装</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">继承</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">多态</span><span class="ne-text" style="color: rgb(76, 73, 72)">的特性，所以</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">易维护</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">易复用</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">易扩展</span><span class="ne-text" style="color: rgb(76, 73, 72)">。可以设计出低耦合的系统，但是从性能上来说，要比面向过程要低。</span></li></ul></details>

### 3. 八种基本数据类型？及其封装类

<details class="lake-collapse"><summary id="u4fb53f88"><span class="ne-text">八种基本数据类型</span></summary><p id="u83e0c549" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><img src="https://cdn.nlark.com/yuque/0/2024/png/39001445/1719640742066-0c254fd7-7b77-436d-afc4-8a8ed91c9683.png" width="888" id="ubc008de6" class="ne-image"></p><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u46423875" data-lake-index-type="0"><span class="ne-text">int是基本数据类型，Integer是int的封装类，是引用类型。int默认值是0，而Integer默认值是null，所以Integer能区分出0和null的情况。</span></li><li id="u12bbe6d3" data-lake-index-type="0"><span class="ne-text">基本数据类型在声明时，系统会自动给它分配空间，而引用类型声明也只是分配了引用空间，必须通过实例化开辟数据空间后才可以赋值。</span></li><li id="uc0f58e57" data-lake-index-type="0"><span class="ne-text">数组对象也是一个引用对象，将一个数组赋值给另一个数组时，只是复制了一个引用，所以通过某一个数组所做的修改，在另一个数组中也看得见</span></li><li id="u0e24c6b1" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">虽然Java语言中定义了boolean类型，但是在Java虚拟机中，没有专门的字节码指令用于处理boolean类型的值。相反，编译器将boolean类型的值编译成Java虚拟机中的int类型，其中0表示false，非0表示true。同样，boolean类型的数组在Java虚拟机中被编码为byte类型的数组。这是因为Java虚拟机的设计者们认为，使用int类型来代替boolean类型，不会对性能造成太大的影响，而且可以简化虚拟机的实现。</span></li></ol></details>

### 4. 标识符的命名规则

<details class="lake-collapse"><summary id="u6a4a68e3"><span class="ne-text">标识符的命名规则</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u3ebd02d4" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">标识符的含义：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在程序中，我们自定义的内容，例如类的名字、方法名称、变量名称等，都是标识符</span></li><li id="ue2eea161" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">命名规则：</span><span class="ne-text" style="color: rgb(76, 73, 72)">标识符可以包含英文字母、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">0-9</span><span class="ne-text" style="color: rgb(76, 73, 72)">的数字、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">$</span><span class="ne-text" style="color: rgb(76, 73, 72)">以及</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">_</span><span class="ne-text" style="color: rgb(76, 73, 72)">，标识符不能以数字开头，不能是关键字</span></li><li id="ubaad1a9a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">命名规范：</span><span class="ne-text" style="color: rgb(76, 73, 72)">类名首字母大写，驼峰命名法。变量名、方法名首字母小写，后续也是驼峰命名</span></li></ul></details>

### 5. instanceof关键字的应用

<details class="lake-collapse"><summary id="u074a7d02"><span class="ne-text">instanceof关键字的应用</span></summary><p id="ufc15d6fb" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">instanceof严格来说是Java中的一个双目运算符，用来测试一个对象是否为另一个对象的实例，用法如下</span></p><pre data-language="java" id="hNOy5" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>boolean result = obj instanceof Class</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ufc13f494" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(76, 73, 72)">其中obj为一个对象，Class表示一个类或者一个接口，当obj为Class对象，或为其子类、实现类，结果返回true，否则返回false</span></li></ul><p id="u7ab212cc" class="ne-p" style="margin: 0; padding: 0; min-height: 24px; text-align: left"><span class="ne-text" style="color: rgb(76, 73, 72)">注意：编译器会检查obj是否能转换为右边class类型，如果不能转换则直接报错</span></p><pre data-language="java" id="umGea" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>int i = 1;
boolean res = i instanceof Integer;     
// 编译不通过：不可转换的类型；无法将 'int' 转换为 'java.lang.Integer'</code></pre><p id="u22b0c0b6" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text">正确方式：</span></p><pre data-language="java" id="OPiRF" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>Integer i = new Integer(1);
boolean res = i instanceof Integer;     // true</code></pre><p id="u147ac71b" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">JavaSE规范中对instanceof运算符的规定是：如果obj为null，那么返回结果总为false</span></p><pre data-language="java" id="HzcVd" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>boolean res = null instanceof Integer;  // false</code></pre></details>

### 6. Java自动拆装箱

<details class="lake-collapse"><summary id="ub0cd2817"><span class="ne-text">Java自动拆装箱</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ue5bea14e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">装箱就是自动将基本数据类型转换为包装类型（int -&gt; Integer）；底层调用的是Integer的valueOf(int)方法</span></li></ul><pre data-language="java" id="SOFcY" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>int i = 10;
Integer i = Integer.valueOf(10);</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u6d04ddb9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">拆箱就是自动将包装类型转换为基本数据类型（Integer -&gt; int）；底层调用的是intValue()方法</span></li></ul><pre data-language="java" id="Je6n4" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>Integer i = Integer.valueOf(10); 
int j = i.valueOf(i);</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u98fbe7fb" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">练习题1：</span><span class="ne-text" style="color: rgb(76, 73, 72)">下面的代码会输出什么</span></li></ul><pre data-language="java" id="NMrTV" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Tmp {
    public static void main(String[] args) {
        Integer a = 100;
        Integer b = 100;
        Integer c = 200;
        Integer d = 200;

        System.out.println(a == b);
        System.out.println(c == d);
    }
}</code></pre><p id="ub394d9bb" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text">输出结果：</span></p><pre data-language="java" id="wAU0Q" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>true
false</code></pre><p id="u4ca44287" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text">这是为什么呢？</span></p><p id="u02abf4d9" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">输出表明a和b指向的是同一个对象，而c和d指向的不是同一个对象，答案在Integer.valueOf()方法的底层源码中</span></p><pre data-language="java" id="HECY8" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>/**
 * Returns an {@code Integer} instance representing the specified
 * {@code int} value.  If a new {@code Integer} instance is not
 * required, this method should generally be used in preference to
 * the constructor {@link #Integer(int)}, as this method is likely
 * to yield significantly better space and time performance by
 * caching frequently requested values.
 *
 * This method will always cache values in the range -128 to 127,
 * inclusive, and may cache other values outside of this range.
 *
 * @param  i an {@code int} value.
 * @return an {@code Integer} instance representing {@code i}.
 * @since  1.5
 */
public static Integer valueOf(int i) {
    if (i &gt;= IntegerCache.low &amp;&amp; i &lt;= IntegerCache.high)
        return IntegerCache.cache[i + (-IntegerCache.low)];
    return new Integer(i);
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uc32cd3f5" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">从注释中我们可以看到，此方法将始终缓存-128到127之间的值</span></li><li id="u9b24144a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">也就是如果数值在-128和127之间，就会返回IntegerCache.cache中已经存在的对象的引用，否则创建一个新的Integer对象。所以上面的代码中，a和b的数值为100，就是从缓存中取的已存在的对象，指向的是同一个对象，所以返回true；而c和d的值为200，并不在缓存中，所以是新建的Integer对象，所以返回false</span></li></ul></details>

### 7. 重载和重写的区别

<details class="lake-collapse"><summary id="uba2a715c"><span class="ne-text">重载和重写的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u55659415" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">重载(Overload)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指在一个类中定义多个方法，它们具有相同的名称，但具有不同的参数列表（个数、类型、顺序），一边在不同的情况下可以调用不同的方法，重载方法可以在一个类中定义，也可以在不同类种定义，只要它们的方法签名不同即可</span></li><li id="u626a8f18" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">例如下面的代码定义了一个名为sum的重载方法，它可以接收</span><strong><span class="ne-text" style="color: rgb(76, 73, 72)">不同类型和数量的参数</span></strong></li></ul><pre data-language="java" id="lNHte" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MathUtils {
    public static int sum(int a, int b) {
        return a + b;
    }
    
    public static double sum(double a, double b) {
        return a + b;
    }
    
    public static int sum(int a, int b, int c) {
        return a + b + c;
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u6e925dde" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">重写(Override)</span><span class="ne-text" style="color: rgb(76, 73, 72)">：是指在子类中重新定义（覆盖）父类中已有的方法，以便实现不同的功能或适应不同的需求。重写方法必须和父类中的方法具有相同的方法名称、参数列表和返回值类型，并且访问权限</span><strong><span class="ne-text" style="color: rgb(76, 73, 72)">不能</span></strong><span class="ne-text" style="color: rgb(76, 73, 72)">比父类中的方法更严格</span></li></ul><pre data-language="java" id="nEi7Q" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Animal {
    public void eat() {
        System.out.println("Animal is eating");
    }
}

public class Dog extends Animal {
    @Override
    public void eat() {
        System.out.println("Dog is eating");
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ua6dd24c9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过重写方法，我们可以在子类中实现特定的功能，同时也可以保留父类中的方法实现。重写方法通常用于实现多态性和集成特性。</span></li></ul></details>

### 8. equals和==的区别

<details class="lake-collapse"><summary id="u45c772e8"><span class="ne-text">equals和==的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u61d64d6b" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">==</span><span class="ne-text" style="color: rgb(76, 73, 72)">比较两个对象的引用是否相同，也就是比较它们在内存中的地址是否相同，如果两个对象的引用相同，则返回true，否则返回false</span></li><li id="uc22a5c42" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">例如下面代码中创建两个String类型的对象，他们的值相同但是引用不同，使用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">==</span><span class="ne-text" style="color: rgb(76, 73, 72)">比较会返回</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">false</span></li></ul><pre data-language="java" id="e8Yhd" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Tmp {
    public static void main(String[] args) {
        String a = new String("Hello");
        String b = new String("Hello");
        System.out.println(a == b);
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u147879a7" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals</span><span class="ne-text" style="color: rgb(76, 73, 72)">是比较两个对象的内容是否相同，也就是比较它们的值是否相同。如果两个对象的内容相同，则返回true，否则返回false。在Java中，Object类的equals()方法默认实现是使用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">==</span><span class="ne-text" style="color: rgb(76, 73, 72)">比较两个对象的引用，但可以在子类中重写该方法以实现比较对象内容的功能。</span></li><li id="u1f8cab7f" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">例如下面的代码中创建了两个String类型的对象，它们的值相同，所以使用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals</span><span class="ne-text" style="color: rgb(76, 73, 72)">比较会返回</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">true</span></li></ul><pre data-language="java" id="RrTdS" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Tmp {
    public static void main(String[] args) {
        String a = new String("Hello");
        String b = new String("Hello");
        System.out.println(a.equals(b));
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u7656e23f" data-lake-index-type="0"><span class="ne-text" style="font-size: 14px">equals方法可以被重写为自定义判断逻辑的方法</span></li></ul></details>

### 9. hashCode的作用

<details class="lake-collapse"><summary id="u2b1ccd97"><span class="ne-text">hashCode的作用</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ubc34f68c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Java</span><span class="ne-text" style="color: rgb(76, 73, 72)">的集合有两类，一类是</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">List</span><span class="ne-text" style="color: rgb(76, 73, 72)">，另一类是</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Set</span><span class="ne-text" style="color: rgb(76, 73, 72)">。前者有序可重复，后者无序不可重复。当我们在</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Set</span><span class="ne-text" style="color: rgb(76, 73, 72)">中插入的时候，如何判断已经存在该元素了呢？</span></li></ul><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="u9bd9f1ba" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">可以通过</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals</span><span class="ne-text" style="color: rgb(76, 73, 72)">方法来判断，但是如果元素太多，用这样的方法就会比较慢</span></li></ul></ul><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uac8d8b92" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">于是就有人发明了哈希算法来提高集合中查找元素的效率，这种方式将集合分成若干个存储区域，每个对象可以计算出一个哈希码，可以将哈希码分组，每组分别对应某个存储区域，根据一个对象的哈希码就可以确定该对象应该存储的那个区域</span></li><li id="u1760082b" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">hashCode</span><span class="ne-text" style="color: rgb(76, 73, 72)">可以这样理解：它返回的是根据对象内存地址换算出的一个值。这样一来，当set需要添加新元素时，先调用这个元素的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">hashCode</span><span class="ne-text" style="color: rgb(76, 73, 72)">方法，就能一下子定位到它应该放置的物理位置上。如果这个位置上没有元素，它就可以直接存储在这个位置上，不需要再进行任何比较了；如果这个位置上已经有元素了，就调用它的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals</span><span class="ne-text" style="color: rgb(76, 73, 72)">方法与新元素进行比较，如果相同就不用存了，不相同就散列其他的地址。这样一来实际调用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals</span><span class="ne-text" style="color: rgb(76, 73, 72)">方法的次数就大大降低了。</span></li></ul></details>

### 10. String、StringBuilder、StringBuffer的区别

<details class="lake-collapse"><summary id="u78e3f50f"><span class="ne-text" style="color: rgb(76, 73, 72)">String、StringBuilder、StringBuffer的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ubdb90fe8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">String是只读字符串，并不是基本数据类型，而是一个对象，从底层源码来看是一个final类型的字符数组，所引用的字符串不能被改变，一经定义，无法再增删改，每次对String的操作都会生成新的String对象</span></li></ul><pre data-language="java" id="kcP2p" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>private final char value[];</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u16d1fa00" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">每次</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">+</span><span class="ne-text" style="color: rgb(76, 73, 72)">操作：隐式在堆上</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">new</span><span class="ne-text" style="color: rgb(76, 73, 72)">了一个跟原字符串相同的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">StringBuilder</span><span class="ne-text" style="color: rgb(76, 73, 72)">对象，再调用append方法，拼接</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">+</span><span class="ne-text" style="color: rgb(76, 73, 72)">后面的字符</span></li><li id="u541ff8b9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">StringBuffer和StringBuilder都继承了AbstractStringBuilder抽象类，从AbstractStringBuilder抽象类中我们可以看到</span></li></ul><pre data-language="java" id="aFx9s" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>/**
 * The value is used for character storage.
 */
char[] value;</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u9cee2c54" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">他们的底层都是可变的字符数组，所以在进行频繁的字符串操作时，建议使用StringBuilder和StringBuffer来进行操作。</span></li><li id="uc16acc2c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">另外StringBuffer对方法加了同步锁或者对调用的方法加了同步锁（底层源码方法都加了synchronized），所以线程是安全的。</span></li></ul><pre data-language="java" id="KafQL" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>
···

    @Override
    public synchronized StringBuffer append(long lng) {
        toStringCache = null;
        super.append(lng);
        return this;
    }

    @Override
    public synchronized StringBuffer append(float f) {
        toStringCache = null;
        super.append(f);
        return this;
    }

···
</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ub38810ae" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">StringBuilder没有对方法进行加同步锁，所以是非线程安全的</span></li></ul><pre data-language="java" id="RItLm" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>
···

    @Override
    public StringBuilder append(long lng) {
        super.append(lng);
        return this;
    }

    @Override
    public StringBuilder append(float f) {
        super.append(f);
        return this;
    }

···
</code></pre></details>

### 11. ArrayList和LinkedList的区别

<details class="lake-collapse"><summary id="u1ec1f39f"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList和LinkedList的区别</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u9a6f81e7" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">内部实现：</span><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList是基于动态数组实现的，内部使用Object[]数组来存储元素。而LinkedList是基于双向链表实现的，内部使用Node节点来存储元素</span></li><li id="uc4d42066" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">插入和删除操作：</span><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList对于中间位置的插入和删除需要移动元素，因为它的底层是数组，需要将后面的元素往后移动，而LinkedList只需要修改节点的指针即可。因此，LinkedList在插入和删除操作方面比ArrayList效率更高</span></li><li id="uf2bc0d1d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">随机访问：</span><span class="ne-text" style="color: rgb(76, 73, 72)">由于ArrayList的底层是数组，所以可以根据下标快速随机访问元素，时间复杂度为O(1)；而LinkedList是基于链表实现的，不能直接根据下标访问元素，需要从头或者从尾遍历到指定位置，时间复杂度为O(n)。</span></li><li id="u91139996" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">内存占用：</span><span class="ne-text" style="color: rgb(76, 73, 72)">由于LinkedList的每个元素都需要一个额外指针来指向下一个节点，因此占用的内存空间会比ArrayList多</span></li></ol></details>

### 12. HashMap和Hashtable的区别

<details class="lake-collapse"><summary id="u7bb94647"><span class="ne-text">H</span><span class="ne-text" style="color: rgb(76, 73, 72)">ashMap和Hashtable的区别</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u8decafb9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">二者父类不同：</span><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap是继承自AbstractMap类，而HashTable是继承自Dictionary类。不过它们都实现了Map、Cloneable、Serializable这三个接口</span></li></ol><pre data-language="java" id="GWHDI" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class HashMap&lt;K,V&gt; extends AbstractMap&lt;K,V&gt; implements Map&lt;K,V&gt;, Cloneable, Serializable {}

public class Hashtable&lt;K,V&gt; extends Dictionary&lt;K,V&gt; implements Map&lt;K,V&gt;, Cloneable, java.io.Serializable {}</code></pre><ol start="2" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ubcd75761" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">线程安全：</span><span class="ne-text" style="color: rgb(76, 73, 72)">Hashtable是线程安全的，它的所有方法都是同步的（所有方法都用synchronized修饰），即对于多个线程同时访问一个Hashtable实例时，可以保证数据的唯一性。而HashMap不是线程安全的，如果多个线程同时访问一个HashMap实例，可能会出现数据不一致的情况</span></li><li id="ua8d2e27b" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">null键和null值的支持：</span><span class="ne-text" style="color: rgb(76, 73, 72)">Hashtable不允许键或值为null，否则会抛出NullPointerException异常；而HashMap可以允许null键和null值</span></li><li id="uca137fe2" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">初始容量和负载因子：</span><span class="ne-text" style="color: rgb(76, 73, 72)">Hashtable的初始容量和负载因子是固定的，在创建Hashtable实例时必须指定；而HashMap可以在创建时指定初始容量和负载因子，也可以在运行时动态调整</span></li><li id="ua3f63db6" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">性能：</span><span class="ne-text" style="color: rgb(76, 73, 72)">因为Hashtable是线程安全的，因此在多线程环境下使用时，会存在一定的性能问题；而HashMap不是线程安全的，在单线程环境下使用时，性能要比Hashtable高</span></li></ol></details>

### 13. Collection包结构，与Collections的区别

<details class="lake-collapse"><summary id="uf3a407bf"><span class="ne-text">C</span><span class="ne-text" style="color: rgb(76, 73, 72)">ollection包结构，与Collections的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ucfdbf0c4" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的Collection包含了一组接口，用于表示一组对象的集合。它提供了一些通用的操作，如添加、删除、遍历等。Collection包中的主要接口有</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="u1bc5b3d8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">List：</span><span class="ne-text" style="color: rgb(76, 73, 72)">有序集合，可以有重复元素</span></li><li id="u5768bc4a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Set：</span><span class="ne-text" style="color: rgb(76, 73, 72)">无序集合，不允许有重复元素</span></li><li id="u2b645a96" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Queue：</span><span class="ne-text" style="color: rgb(76, 73, 72)">队列，通常用于实现先进先出(FIFO)的数据结构</span></li><li id="u1e2caa49" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Deque：</span><span class="ne-text" style="color: rgb(76, 73, 72)">双端队列，可以在队头或队尾进行插入和删除操作</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u7ea35970" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Collections是Java中的一个工具类，它包含了一组静态方法，用于操作各种集合类型。它提供了一些常用的算法和工具方法，如排序、查找、复制等。Collections类中的方法通常是针对Collection类型的实例进行操作的</span></li><li id="ud1943eb8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">简单来说，Collection是一组结构，定义了集合的基本操作和属性，而Collections是一个工具类，提供了一些常用的算法和工具方法，用于操作各种集合类型的实例</span></li><li id="ud080c398" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">需要注意的是：Collection和Collections之间是没有继承或实现关系的，它们是两个独立的概念</span></li></ul></details>

### 14. Java的四种引用，强弱软虚

<details class="lake-collapse"><summary id="ucbe38754"><span class="ne-text">J</span><span class="ne-text" style="color: rgb(76, 73, 72)">ava的四种引用，强弱软虚</span></summary><p id="u93242fc1" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">在Java中有四种类型的引用：强引用、软引用、弱引用、虚引用</span></p><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u8af0d442" data-lake-index-type="0"><span class="ne-text">强引用：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是最常见的引用类型，它指向一个对象，只要强引用存在，垃圾回收器就不会回收该对象，可以通过new操作符、赋值操作符或方法调用等方式创建强引用</span></li></ol><pre data-language="java" id="GeTCF" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>String str = new String("Hello");</code></pre><ol start="2" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u6af61ec6" data-lake-index-type="0"><span class="ne-text">软引用：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是一种比较灵活的引用类型，它用来描述一些还有用，但是非必须的对象。只有当内存不足时，才会回收这些对象，可以通过SoftReference类创建软引用</span></li></ol><pre data-language="java" id="biyCB" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>SoftReference&lt;String&gt; str = new SoftReference&lt;String&gt;(new String("Hello"));</code></pre><ol start="3" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u9aba8742" data-lake-index-type="0"><span class="ne-text">弱引用：</span><span class="ne-text" style="color: rgb(76, 73, 72)">它指向的对象只要没有强引用指向它时，就会被回收。可以通过WeakReference类创建弱引用</span></li></ol><pre data-language="java" id="XgJAW" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>WeakReference&lt;String&gt; str = new WeakReference&lt;&gt;(new String("Hello"));</code></pre><ol start="4" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u0497f0ca" data-lake-index-type="0"><span class="ne-text">虚引用：</span><span class="ne-text" style="color: rgb(76, 73, 72)">虚引用的回收机制与弱引用差不多，但是它在被回收之前，会被放入ReferenceQueue中。而其他引用是被JVM回收后才被传入ReferenceQueue中的。由于这个机制的存在，虚引用大多是被用于引用销毁前的处理工作。同时，虚引用在创建时，必须带有ReferenceQueue</span></li></ol><pre data-language="java" id="PxK9v" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>PhantomReference&lt;String&gt; str = new PhantomReference&lt;String&gt;(new String("str"), new ReferenceQueue&lt;&gt;());</code></pre></details>

### 15. 泛型常用特点

<details class="lake-collapse"><summary id="u1490f18e"><span class="ne-text">泛型常用特点</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="udaf29f95" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的泛型是一种类型参数化机制，它可以让代码更加灵活、可读性更强，同时也可以提高代码的安全性和可维护性。泛型的常用特点包括</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="u07bc0c5f" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">类型安全：</span><span class="ne-text" style="color: rgb(76, 73, 72)">泛型可以让编译器在编译时就检查类型是否匹配，从而避免了很多类型转换和运行时错误</span></li><li id="u60b10be5" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">可重用性：</span><span class="ne-text" style="color: rgb(76, 73, 72)">泛型可以让同一个类或方法适用于不同的数据类型，从而提高了代码的可重用性</span></li><li id="u5f1aa164" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">可读性：</span><span class="ne-text" style="color: rgb(76, 73, 72)">泛型可以让代码更易读，因为它可以让代码更具有表现力和可理解性</span></li><li id="uce0303f4" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">性能优化：</span><span class="ne-text" style="color: rgb(76, 73, 72)">泛型可以让代码更加高效，因为它可以避免在运行时进行类型转换，从俄提高了程序的性能</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u7b7db4fe" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">注意：Java中的泛型是在编译时实现的，而不是在运行时实现的。在编译时，Java编译器会进行类型擦除(Type Erasure)，将泛型类型转换为普通的类型。因此，在运行时无法获取泛型类型的具体信息</span></li></ul></details>

### 16. Java创建对象的几种方式

<details class="lake-collapse"><summary id="ua732c320"><span class="ne-text">Java创建对象的几种方式</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ubae1b136" data-lake-index-type="0"><span class="ne-text">使用new关键字</span></li></ol><pre data-language="java" id="cpSIy" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MyClass {
   public MyClass() {
      System.out.println("对象已创建");
   }

   public static void main(String[] args) {
      MyClass obj = new MyClass();
   }
}</code></pre><ol start="2" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u499385c4" data-lake-index-type="0"><span class="ne-text">使用Class类的newInstance方法</span></li></ol><pre data-language="java" id="qomB3" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MyClass {
   public MyClass() {
      System.out.println("对象已创建");
   }

   public static void main(String[] args) throws Exception {
      Class cls = Class.forName("MyClass");
      MyClass obj = (MyClass) cls.newInstance();
   }
}</code></pre><ol start="3" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u9ff3138a" data-lake-index-type="0"><span class="ne-text">使用Constructor类的newInstance方法</span></li></ol><pre data-language="java" id="L21Cr" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MyClass {
   public MyClass() {
      System.out.println("对象已创建");
   }

   public static void main(String[] args) throws Exception {
      Constructor&lt;MyClass&gt; constructor = MyClass.class.getConstructor();
      MyClass obj = constructor.newInstance();
   }
}</code></pre><ol start="4" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u29edb77a" data-lake-index-type="0"><span class="ne-text">使用clone方法</span></li></ol><pre data-language="java" id="sRUib" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MyClass implements Cloneable {
   public MyClass() {
      System.out.println("对象已创建");
   }

   public static void main(String[] args) throws Exception {
      MyClass obj1 = new MyClass();
      MyClass obj2 = (MyClass) obj1.clone();
   }
}</code></pre><ol start="5" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u01bb20ed" data-lake-index-type="0"><span class="ne-text">使用反序列化</span></li></ol><pre data-language="java" id="cNagt" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>import java.io.*;

public class MyClass implements Serializable {
   public MyClass() {
      System.out.println("对象已创建");
   }

   public static void main(String[] args) throws Exception {
      MyClass obj1 = new MyClass();
      ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("myFile.txt"));
      out.writeObject(obj1);
      out.close();

      ObjectInputStream in = new ObjectInputStream(new FileInputStream("myFile.txt"));
      MyClass obj2 = (MyClass) in.readObject();
      in.close();
   }
}</code></pre></details>

### 17. 有没有可能两个不相等的对象有相同的hashCode

<details class="lake-collapse"><summary id="ufdd63ec2"><span class="ne-text" style="color: rgb(76, 73, 72)">有没有可能两个不相等的对象有相同的hashCode</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uac2fec2a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">是有可能的，这种情况被称为</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">哈希冲突(Hash Collision)</span><span class="ne-text" style="color: rgb(76, 73, 72)">，也叫哈希碰撞，是哈希算法中一种常见的情况。</span></li><li id="u17a75d70" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">但是哈希冲突不是问题，因为哈希表实现了一种解决冲突的方法，当发生哈希冲突时，哈希表会在相应的桶中存储一个链表或树（红黑树），以容纳具有相同哈希码的所有元素。因此，即使练个不同对象具有相同的哈希码，他们也可以被正确的插入和检索</span></li></ul></details>

### 18. 深拷贝和浅拷贝的区别是什么

<details class="lake-collapse"><summary id="u57c7ce1b"><span class="ne-text" style="color: rgb(76, 73, 72)">深拷贝和浅拷贝的区别是什么</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u0e5ae480" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">深拷贝：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指将一个对象复制到另一个对象，新对象与原对象</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">不共享</span><span class="ne-text" style="color: rgb(76, 73, 72)">引用类型属性（如数组、集合、对象等），也就是说，新对象和原对象的引用类型属性指向的是不同的地址，修改其中一个对象中的引用类型属性，不会影响另一个对象中的属性值。</span></li><li id="u5e05030d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">浅拷贝：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指将一个对象复制到另一个对象，新对象与原对象</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">共享</span><span class="ne-text" style="color: rgb(76, 73, 72)">引用类型属性，也就是说，新对象与原对象中的引用类型属性指向的是同一个地址，修改器中一个对象的引用类型属性，会影响到另一个对象的属性值，Java中的Object类提供了clone方法来实现浅拷贝</span></li></ul></details>

### 19. final有哪些用法

<details class="lake-collapse"><summary id="u5e5eb007"><span class="ne-text">final的作用</span></summary><p id="u18c2c6fe" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">final是Java中的关键字，可以用来修饰类、方法、变量等，它的主要作用是用于定义常量、防止继承、防止重写方法等</span></p><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u299beb46" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">定义常量：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用final关键字定义的变量称为常量，它的值在定以后就不能被修改。常量命名规范一般是大写字母加下划线，例如</span></li></ol><pre data-language="java" id="Vtl5p" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>final int MAX_VALUE = 99999;</code></pre><ol start="2" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="uf2199226" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">用于防止继承：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用final关键字修饰的类不能被继承，例如</span></li></ol><pre data-language="java" id="ztK8E" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>final class MyClass{

}</code></pre><ol start="3" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u6fb6826c" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">防止重写方法：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用final关键字修饰的方法不能被子类重写，例如</span></li></ol><pre data-language="java" id="ou7Pu" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public final void myMethod(){

}</code></pre><ol start="4" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="uad56e4c7" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">优化性能：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用final关键字可以优化代码性能。被final修饰的方法和变量在编译时就已经确定了值，因此在运行时不需要进行计算，可以减少运行时的开销，提高程序的执行效率。同时，被final修饰的方法，JVM会尝试将其内联，以提高运行效率</span></li><li id="u1709d657" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">优化代码可读性：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在代码中使用final关键字可以使代码更易读。通过将变量声明为final，可以明确其含义，使代码更易于理解和维护</span></li></ol></details>

### 20. static的用法

<details class="lake-collapse"><summary id="ucb4f1595"><span class="ne-text">static的用法</span></summary><p id="u457cbde1" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">static是Java中的关键字，可以用来修饰类、方法、变量等，它的主要作用是创建静态成员，可以通过类名直接访问，而不需要实例化对象</span></p><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="uf50fdf66" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">用于创建静态变量：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用static关键字定义的变量称为静态变量，它的值与所有该类的对象共享，并且可以直接通过类名访问</span></li></ol><pre data-language="java" id="JNjvF" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Tmp {
    static String str = "Hello";
}

public class Main {
    public static void main(String[] args) {
        System.out.println(Tmp.str);
    }
}</code></pre><ol start="2" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ud9241970" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">用于创建静态方法：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用static关键字定义的方法称为静态方法，同样可以直接通过类名调用</span></li></ol><pre data-language="java" id="UuP8K" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Tmp {
    static void myMethod() {
        System.out.println("Hello");
    }
}

public class Main {
    public static void main(String[] args) {
        Tmp.myMethod();
    }
}</code></pre><ol start="3" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u88aa3987" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">用于创建静态代码块：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用static关键字定义的代码块称为静态代码块，它在类加载时执行，且只执行一次，一般用于初始化静态变量</span></li></ol><pre data-language="java" id="ak4SR" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class MyClass {
    static List&lt;String&gt; myStaticList;
    
    static {
        // 从文件中加载数据并进行解析
        try {
            File file = new File("mydata.txt");
            BufferedReader reader = new BufferedReader(new FileReader(file));
            String line;
            myStaticList = new ArrayList&lt;&gt;();
            while ((line = reader.readLine()) != null) {
                myStaticList.add(line);
            }
            reader.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
    
    public static void main(String[] args) {
        System.out.println("My static list contains: " + myStaticList);
    }
}</code></pre><ol start="4" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ubd4f31f7" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">创建静态内部类：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使用static关键字定义的内部类被称为静态内部类，它与外部类的对象无关，可以直接访问外部类的静态成员</span></li></ol><pre data-language="java" id="eflsA" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class OuterClass {
    private static int staticVar = 1;
    private int instanceVar = 2;

    public static class StaticInnerClass {
        public void print() {
            // 静态内部类可以直接访问外部类的静态变量
            System.out.println("StaticVar from inner class: " + staticVar);
        }
    }

    public void createInnerClass() {
        // 不需要创建OuterClass实例，但是可以直接创建StaticInnerClass实例，并且使用它访问外部类的静态成员
        StaticInnerClass staticInnerClass = new StaticInnerClass();
        staticInnerClass.print();
    }
}</code></pre></details>

### 21. a = a + b和a += b有什么区别

<details class="lake-collapse"><summary id="uadfa07f7"><span class="ne-text">a = a + b和a += b有什么区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u64f04cbd" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">+=</span><span class="ne-text" style="color: rgb(76, 73, 72)">操作会进行隐式自动类型转换，例如这里的 </span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">a += b</span><span class="ne-text" style="color: rgb(76, 73, 72)">会隐式的将加操作的结果类型强制转换为持有结果的类型，而a = a + b则不会自动进行类型转换</span></li></ul><pre data-language="java" id="mWozd" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>// 两个byte类型的变量相加时，结果会被自动提升为int类型。这种类型提升被称为"拓宽原始转换"，它适用于所有原始类型，包括byte、short、char和int。
byte a = 127;
byte b = 127;
a = a + b;      // 编译报错：不兼容的类型。实际为 int'，需要 'byte'
a += b;         // a = (byte)(a + b)</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u4469141d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">再来看一个小案例，以下代码是否存在错误</span></li></ul><pre data-language="java" id="wXZ6G" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>short a = 1;
a = a + 1;</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ucd666e6f" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">有错误，short类型在进行运算时，会自动提升为int类型，也就是说</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">a + 1</span><span class="ne-text" style="color: rgb(76, 73, 72)">的运算结果是int类型，而a是short类型，此时编译器会报错</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">不兼容的类型。实际为 int'，需要 'short'</span><span class="ne-text" style="color: rgb(76, 73, 72)">，改成</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">+=</span><span class="ne-text" style="color: rgb(76, 73, 72)">的方式就好了</span></li></ul><pre data-language="java" id="g40Vu" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>short a = 1;
a += 1;</code></pre></details>

### 22. try catch finally，try里有return语句，finally还会执行吗

<details class="lake-collapse"><summary id="ubf06f381"><span class="ne-text" style="color: rgb(76, 73, 72)">try catch finally，try里有return语句，finally还会执行吗</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ude2cc77a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">无论try代码块中是否包含return语句，finally块中的代码都会被执行。无论try块中有没有抛出异常，finally快中的代码都会被执行。finally块通常用于在代码中执行清理操作，例如：释放资源、关闭文件等</span></li><li id="u62387865" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">需要注意的是，如果在finally块中使用了return语句，那么这个返回值会覆盖掉try块中的返回值，因此，finally块中的返回值将成为整个方法的返回值，这种做法是不推荐的。</span></li></ul><pre data-language="java" id="dvVWe" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Demo_35 {
    public static void main(String[] args) {
        int result = test();
        System.out.println(result);
    }

    private static int test() {
        try {
            return 10;
        } finally {
            return 20;
        }
    }
}</code></pre><p id="u8ab75ee7" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text">以上输出结果为20</span></p><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u24521bd7" data-lake-index-type="0"><span class="ne-text">再来看看另一种情况</span></li></ul><pre data-language="java" id="pFiu9" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>public class Demo_37 {
    public static void main(String[] args) {
        int result = test();
        System.out.println(result);
    }

    private static int test() {
        int i = 10;
        try {
            return i;
        } finally {
            i = 20;
        }
    }
}</code></pre><p id="u68b1c4ee" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text">输出结果为10,因为此时虽然赋值了,但已经先执行了上一阶段的返回数据,所以返回的是10</span></p></details>

### 23. Exception和Error包结构

<details class="lake-collapse"><summary id="u56556d30"><span class="ne-text" style="color: rgb(76, 73, 72)">Exception和Error包结构</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ua78ecf12" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的异常分为两类：</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Error</span><span class="ne-text" style="color: rgb(76, 73, 72)">和</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Exception</span><span class="ne-text" style="color: rgb(76, 73, 72)">，二者都是</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Throwale</span><span class="ne-text" style="color: rgb(76, 73, 72)">类的子类。</span></li></ul><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="u2b554b63" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Error</span><span class="ne-text" style="color: rgb(76, 73, 72)">表示虚拟机本身的错误或资源耗尽等严重情况，应用程序不应该视图去捕获这些异常，例如</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">OOM(OutOfMemoryError)</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">SOF(StackOverFlowError)</span><span class="ne-text" style="color: rgb(76, 73, 72)">等</span></li><li id="u93eb6437" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Exception</span><span class="ne-text" style="color: rgb(76, 73, 72)">表示程序运行中的异常情况，应该对其进行捕获和处理，</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Exception</span><span class="ne-text" style="color: rgb(76, 73, 72)">又分为</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">可检查异常(Checked Exception)</span><span class="ne-text" style="color: rgb(76, 73, 72)">和</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">不可检查异常(Unchecked Exception)</span></li></ul></ul><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="2" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: square"><li id="uc55927c8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">可检查异常需要程序显式地捕获并处理，例如</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IOException</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">SQLException</span><span class="ne-text" style="color: rgb(76, 73, 72)">等</span></li><li id="u547db098" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">而不可检查异常一般是程序运行时遇到的无法处理的错误，如</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">NullPointerException</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">ArrayIndexOutOfBoundsException</span><span class="ne-text" style="color: rgb(76, 73, 72)">等，这些异常都继承自</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">RuntimeException</span><span class="ne-text" style="color: rgb(76, 73, 72)">类，也被称为运行时异常，程序不需要显式地去捕获这类异常</span></li></ul></ul></ul></details>

### 24. OOM你遇到过那些情况，SOF你遇到过哪些情况

<details class="lake-collapse"><summary id="u4f315efa"><span class="ne-text" style="color: rgb(76, 73, 72)">OOM你遇到过那些情况，SOF你遇到过哪些情况</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u93f4599d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">OOM</span><span class="ne-text" style="color: rgb(76, 73, 72)">和</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">SOF</span><span class="ne-text" style="color: rgb(76, 73, 72)">都是Java程序中可能遇到的异常情况</span></li></ul><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="u8d0dc936" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">OOM(OutOfMemory)</span><span class="ne-text" style="color: rgb(76, 73, 72)">即内存溢出，一般是指JVM内存不足以分配新对象，导致无法继续运行程序。出现OOM的情况很多，例如</span></li></ul></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="2" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-roman"><li id="u7dd19067" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">程序中创建了太多的对象，占用了过多的内存空间</span></li><li id="u18d5dbe0" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">代码中存在内存泄漏，导致不再使用的对象没有被及时释放，导致内存空间被占用</span></li><li id="u9724a318" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">虚拟机参数设置不合理，导致JVM无法分配足够的内存等</span></li></ol></ol></ol><ul class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ul ne-level="1" class="ne-ul" style="margin: 0; padding-left: 23px; list-style: circle"><li id="u1d1857ba" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">SOF(StackOverFlow)</span><span class="ne-text" style="color: rgb(76, 73, 72)">即栈溢出，一般是指线程请求的栈深度大于</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">JVM</span><span class="ne-text" style="color: rgb(76, 73, 72)">所允许的深度，导致</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">StackOverFlowError</span><span class="ne-text" style="color: rgb(76, 73, 72)">异常。出现SOF的情况也有很多，例如</span></li></ul></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="2" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-roman"><li id="u3ffc8759" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">递归调用层数过多，导致栈空间被耗尽</span></li><li id="ufefc7160" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">代码中存在死循环或循环调用，导致栈空间被耗尽</span></li><li id="udef71517" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">虚拟机参数设置不合理，导致栈空间太小等</span></li></ol></ol></ol></details>

### 25. 简述线程、程序、进程的基本概念，以及他们之间的关系是什么

<details class="lake-collapse"><summary id="u6171f75d"><span class="ne-text" style="color: rgb(76, 73, 72)">线程、程序、进程</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u480a7ba5" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">程序：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指一组指令和数据的有序集合，用于完成特定的任务。程序是存储在磁盘等外部存储介质中，只有在被加载到内存中才会被执行。</span></li><li id="u3387da64" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">进程：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指正在执行的程序的一个实例，是操作系统进行资源分配和调度的基本单位。进程拥有独立的内存空间和系统资源，可以包含多个线程</span></li><li id="u67ce775c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">线程：</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指进程中的一个执行单元，是操作系统进行调度的最小单位。线程与进程共享内存空间和系统资源，每个线程拥有自己的程序计数器和栈空间</span></li><li id="u6c9f9ae8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">进程和线程都是程序执行的基本单位，进程和线程之间的关系是一对多的关系，即一个进程可以包含多个线程。多个线程可以并发地执行，共享进程的内存空间和系统资源</span></li></ul></details>

### 26. 说说Java中的IO流

<details class="lake-collapse"><summary id="udbb78e97"><span class="ne-text" style="color: rgb(76, 73, 72)">说说Java中的IO流</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uf941d780" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的IO流是Java提供的一种用于输入和输出数据的机制，主要分为字节流和字符流两种类型，它们可以用于读取和写入不同种类的数据源，例如文件、网络连接、内存缓冲区等。具体来说，Java中的IO流可以分为以下几种类型</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="uddb6506e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">字节流(InputStream和OutStream)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">以字节为单位读写数据，适用于读写二进制文件和图片等数据</span></li><li id="u3f8ac2bc" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">字符流(Reader和Writer)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">以字符为单位读写数据，适用于读写文本文件</span></li><li id="u759d9a53" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">缓冲流(BufferedInputSteam、BufferedOutputSteam、BufferedReader和BufferedWriter)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在字节流和字符流的基础上增加了缓冲功能，提高读写数据的效率</span></li><li id="u5bf3d635" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">对象流(ObjectInputSteam和ObjectOutputStream)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">用于序列化和反序列化Java对象，将Java对象转换为字节流进行存储和传输</span></li><li id="u00b02dea" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">转换流(InputStreamReader和OutputStreamWriter)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">将字节流转换为字符流或将字符流转换为字节流，提供了从字节流读取Unicode字符的方法</span></li><li id="u843f8c13" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">文件流(FileInputStream和FileOutputStream)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">用于读写文件，支持读写字节和字节数组</span></li><li id="ub1b622bb" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">管道流(PipedInputStream和PipedOutputStream)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">用于线程之间的数据传输</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uc8cb63e7" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过使用不同类型的IO流，可以很方便地完成文件的读写、网络数据的传输、对象的序列化等操作</span></li></ul></details>

### 27. Java序列化中如果有某些字段不想进行序列化，怎么办

<details class="lake-collapse"><summary id="ub459c550"><span class="ne-text" style="color: rgb(76, 73, 72)">Java序列化中如果有某些字段不想进行序列化，怎么办</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u7aa802e3" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">可以使用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">transient</span><span class="ne-text" style="color: rgb(76, 73, 72)">关键字修饰不想被序列化的字段，这样在序列化过程中这些字段就会被忽略掉。在反序列化时，这些字段的值会被设置成默认值，例如数值类型会被设置成</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">0</span><span class="ne-text" style="color: rgb(76, 73, 72)">，布尔类型会被设置成</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">false</span><span class="ne-text" style="color: rgb(76, 73, 72)">，引用类型会被设置成</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">null</span><span class="ne-text" style="color: rgb(76, 73, 72)">。</span></li></ul><pre data-language="java" id="sDenx" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>import java.io.Serializable;

public class Person implements Serializable {
    private static final long serialVersionUID = 1L;
    
    private String name;
    private transient int age; // transient修饰的字段
    
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    public String getName() {
        return name;
    }
    
    public int getAge() {
        return age;
    }
    
    public void setAge(int age) {
        this.age = age;
    }
    
    @Override
    public String toString() {
        return "Person [name=" + name + ", age=" + age + "]";
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uf770c850" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">上面的代码中，</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Person</span><span class="ne-text" style="color: rgb(76, 73, 72)">类实现了</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Serializable</span><span class="ne-text" style="color: rgb(76, 73, 72)">接口，并且</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">age</span><span class="ne-text" style="color: rgb(76, 73, 72)">字段被</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">transient</span><span class="ne-text" style="color: rgb(76, 73, 72)">关键字修饰，那么在序列化过程中，</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">age</span><span class="ne-text" style="color: rgb(76, 73, 72)">字段会被忽略掉，在反序列化时，</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">age</span><span class="ne-text" style="color: rgb(76, 73, 72)">字段会被设置为默认值</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">0</span></li></ul><pre data-language="java" id="DJHOb" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>import java.io.*;

public class SerializationTest {
    public static void main(String[] args) {
        Person person = new Person("John", 30);
        System.out.println("序列化前: " + person);

        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("person.dat"))) {
            oos.writeObject(person);
        } catch (IOException e) {
            e.printStackTrace();
        }

        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("person.dat"))) {
            Person restoredPerson = (Person) ois.readObject();
            System.out.println("序列化后: " + restoredPerson);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uec904b7c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">在上面的代码中，我们创建了一个</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Person</span><span class="ne-text" style="color: rgb(76, 73, 72)">对象，并将其序列化到文件</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">person.dat</span><span class="ne-text" style="color: rgb(76, 73, 72)">中，然后再从文件中反序列化得到一个新的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Person</span><span class="ne-text" style="color: rgb(76, 73, 72)">对象，运行结果如下</span></li></ul><pre data-language="java" id="K282v" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>序列化前：Person [name=John, age=30]
序列化后：Person [name=John, age=0]</code></pre><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u4df4641d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">需要注意的是：使用</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">transient</span><span class="ne-text" style="color: rgb(76, 73, 72)">修饰的字段</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">不能</span><span class="ne-text" style="color: rgb(76, 73, 72)">是</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">static</span><span class="ne-text" style="color: rgb(76, 73, 72)">或</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">final</span><span class="ne-text" style="color: rgb(76, 73, 72)">修饰的</span></li></ul></details>

### 28. JavaIO和NIO的区别

<details class="lake-collapse"><summary id="uccefe303"><span class="ne-text" style="color: rgb(76, 73, 72)">JavaIO和NIO的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u6a809a47" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IO(Input/Output)</span><span class="ne-text" style="color: rgb(76, 73, 72)">是指对数据的输入和输出操作，其中包含了许多输入输出流。Java的IO主要基于阻塞式IO模型实现的，即在读写数据时会一直阻塞，直到数据读写完成，而</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">NIO(NEW IO)</span><span class="ne-text" style="color: rgb(76, 73, 72)">是Java1.4引入的一组新IO API，也成为</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">non-nlocking IO</span><span class="ne-text" style="color: rgb(76, 73, 72)">。NIO主要是基于</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">非阻塞式IO模型</span><span class="ne-text" style="color: rgb(76, 73, 72)">实现，可以在单个线程上进行多个IO操作，提高了IO效率</span></li><li id="u7a24c91b" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">一下是Java IO和NIO的主要区别</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="u5c09b41c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IO是面向流的，而NIO是面向缓冲区的。</span><span class="ne-text" style="color: rgb(76, 73, 72)">Java的IO中，数据总是通过InputStream或OutputStream等流的形式传输，而在NIO中，数据是从通道读入缓冲区，从缓冲区写入通道</span></li><li id="u5d119fad" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IO是阻塞的，而NIO是非阻塞的。</span><span class="ne-text" style="color: rgb(76, 73, 72)">Java的IO读取或写入数据时，会一直阻塞当前线程，直到操作完成或发生异常，而在NIO中，可以进行异步读写操作，即一个线程可以处理多个连接</span></li><li id="u126aff17" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IO是单向的，而NIO是双向的。J</span><span class="ne-text" style="color: rgb(76, 73, 72)">ava中的IO是单向的，即一个输入流只能读取数据，一个输出流只能写入数据，而在NIO中，缓冲区既可以读，也可以写</span></li><li id="u27e5eae2" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">IO使用字节流和字符流进行操作，而NIO使用Channel和Buffer进行操作。</span><span class="ne-text" style="color: rgb(76, 73, 72)">在Java的IO中，数据总是通过InputStream和OutputStream等流的形式传输，可以进行字节流和字符流的操作。而在NIO中，数据是从通道读入缓冲区，可以使用ByteBuffer、CharBuffer等缓冲区进行读写操作</span></li></ol></ol></details>

### 29. Java反射的作用与原理

<details class="lake-collapse"><summary id="ud1b0449f"><span class="ne-text" style="color: rgb(76, 73, 72)">反射的作用与原理</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uf5353641" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java反射是指在程序运行时</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">动态地获取</span><span class="ne-text" style="color: rgb(76, 73, 72)">类的信息并操作类的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">属性</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">方法</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">构造器</span><span class="ne-text" style="color: rgb(76, 73, 72)">等，它允许程序在运行时动态地</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">创建对象</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">调用方法</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">获取字段值</span><span class="ne-text" style="color: rgb(76, 73, 72)">等。Java反射的作用非常广泛，例如在</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">框架</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">ORM映射</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">RPC调用</span><span class="ne-text" style="color: rgb(76, 73, 72)">等领域都有应用</span></li><li id="u143a6897" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java反射的原理是通过Java的类加载机制，在运行时获取类的信息，包括类名、方法名、字段名、注解等，并生成类的Class对象，这个Class对象提供了操作类的各种方法和属性的API。反射可以通过Class类的一些方法来获取</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Constructor</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Method</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">Filed</span><span class="ne-text" style="color: rgb(76, 73, 72)">等类的信息，通过这些信息可以实现对类的</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">实例化</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">调用方法</span><span class="ne-text" style="color: rgb(76, 73, 72)">、</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">获取字段值</span><span class="ne-text" style="color: rgb(76, 73, 72)">等操作</span></li><li id="uaca21503" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java反射的主要优点是可以动态地加载类和调用类的方法、字段等，使得程序具有更高的灵活性和扩展性。不过由于反射是一种非常底层的操作，使用不当也容易导致性能问题，同时反射也存在安全隐患，因此在使用反射时需要谨慎处理</span></li></ul></details>

### 30. 说说List、Set、Map的区别

<details class="lake-collapse"><summary id="u14fadd40"><span class="ne-text" style="color: rgb(76, 73, 72)">说说List、Set、Map的区别</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u70debe34" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">List、Set、Map是Java集合框架中最基础的三种容器，它们的区别如下</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="ucda3f3dc" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">List接口表示有序的集合，元素可以重复，每个元素都有一个索引。常用的实现类有ArrayList和LinkedList。ArrayList基于数组实现，插入、删除操作效率低，查询效率高；LinkedList基于链表实现，插入、删除效率高，查询效率低</span></li><li id="u11f12f31" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Set接口表示无序的集合，元素不可重复。常用的实现类有HashSet、TreeSet。HashSet基于哈希表实现，查询、插入、删除效率都很高；TreeSet基于红黑树实现，元素有序，插入、删除、查询效率都很高</span></li><li id="u0b1579b3" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Map接口表示键值对集合，每个元素包含一个键和对应的值，键不可重复。常用的实现类有HashMap和TreeMap。HashMap基于哈希表实现，查询、插入、删除效率都很高；TreeMap基于红黑树实现，元素有序，插入、删除、查询效率都很高。</span></li></ol></ol></details>

### 31. Object有哪些常用方法？大致说一下每个方法的含义

<details class="lake-collapse"><summary id="udb839b01"><span class="ne-text" style="color: rgb(76, 73, 72)">Object有哪些常用方法？大致说一下每个方法的含义</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ued88676b" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Object类是Java中所有类的基类，她定义了一些常用的方法，包括</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="uc18ca30d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">equals(Object obj)：</span><span class="ne-text" style="color: rgb(76, 73, 72)">判断当前对象是否与另一个对象相等，通常需要重写该方法</span></li><li id="u18e24c7c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">hashCode()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">返回当前对象的哈希码，用于哈希表等数据结构</span></li><li id="u31fa3c79" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">toString()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">返回当前对象的字符串表示，通常需要重写该方法</span></li><li id="u4e6d4027" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">getClass()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">返回当前对象的类类型</span></li><li id="u047751ff" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">wait()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">使当前线程等待，直到其他线程调用该对象的notify()或notifyAll()方法</span></li><li id="uea80c78e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">notify()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">唤醒一个等待中的线程</span></li><li id="u89f8b8fe" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">notifyAll()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">唤醒所有等待中的线程</span></li><li id="ubb58d666" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">finalize()：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在垃圾回收器回收对象之前调用，用于释放资源等清理工作</span></li></ol></ol></details>

### 32. Java获取一个类Class对象的方式有哪些

<details class="lake-collapse"><summary id="ua3c0ef92"><span class="ne-text" style="color: rgb(76, 73, 72)">获取一个类Class对象的方式有哪些</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u46108fd8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过对象的getClass()方法获取</span></li><li id="u665d8adb" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过类名.class获取</span></li><li id="u1eba2420" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过Class.forName()方法获取</span></li><li id="uc8a2e648" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">通过ClassLoader.loadClass()方法获取</span></li></ol></details>

### 33. 说一下ArrayList的特点

<details class="lake-collapse"><summary id="u53e858a3"><span class="ne-text" style="color: rgb(76, 73, 72)">说一下ArrayList的特点</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="u6dd4f7d1" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">内部实现是数组，支持动态扩容。再添加元素时，如果数组已满，则会重新创建一个更大的数组，并将原来数组中的元素复制到新数组中，这会导致添加元素的时间复杂度为O(n)</span></li><li id="u92ae9050" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">支持随机访问，可以通过元素下标直接访问数组中的元素，时间复杂度为O(1)</span></li><li id="uae9d3435" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList中的元素允许为null</span></li><li id="u466d1359" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList是非线程安全的，不适合在多线程环境下使用</span></li><li id="u88fcbba3" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList的默认初始化容量为10，可以在创建ArrayList时指定初始化容量，可以一定程度上提升运行效率（避免扩容复制数组）</span></li><li id="ue03aec13" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList支持插入和删除操作，但是在插入和删除元素时，需要将插入点后的元素全部后移，时间复杂度为O(n)</span></li></ol></details>

### 34. 有数组了为什么还要搞个ArrayList

<details class="lake-collapse"><summary id="u4ad43067"><span class="ne-text" style="color: rgb(76, 73, 72)">有数组了为什么还要搞个ArrayList</span></summary><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ud08e59f7" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList可以动态扩容，而数组的容量是固定的</span></li><li id="uced9a9ac" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList可以直接存储对象类型，而数组则只能存储基本数据类型和对象的引用</span></li></ol><pre data-language="java" id="bAeWj" class="ne-codeblock language-java" style="border: 1px solid #e8e8e8; border-radius: 2px; background: #f9f9f9; padding: 16px; font-size: 13px; color: #595959"><code>int[] intArray = new int[3];        // 数组存储基本数据类型
Object[] objArray = new Object[3];  // 数组存储对象的引用

// ArrayList可以直接存储对象类型本身
ArrayList&lt;Person&gt; personList = new ArrayList&lt;&gt;();
personList.add(new Person("Alice"));
personList.add(new Person("Bob"));
personList.add(new Person("Charlie"));</code></pre><ol start="3" class="ne-ol" style="margin: 0; padding-left: 23px"><li id="ue56af1a9" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList提供了一些方便的方法，如add、remove、size等，对于操作元素的需求更加灵活</span></li><li id="u3c96f4e0" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList支持泛型，可以指定容器中存储的数据类型</span></li><li id="u7f788b36" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">ArrayList可以和其他集合类进行互操作，如Collection.sort等，提供了更多的使用方式</span></li></ol></details>

### 35. 说说什么是fail-fast

<details class="lake-collapse"><summary id="u1160aade"><span class="ne-text" style="color: rgb(76, 73, 72)">说说什么是fail-fast</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="ue6fc527e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">fail-fast是指当集合在遍历中被修改了，那么就会抛出</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">ConcurrentModificationException</span><span class="ne-text" style="color: rgb(76, 73, 72)">异常，这样可以保证多个线程并发修改时能够及时发现问题，它是一种机制，可以让程序出现并发修改时，尽早发现问题并迅速报错</span></li><li id="u32853ef8" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">Java中的某些集合类，例如ArrayList、HashMap等，都不是线程安全的。在许多县城环境中，可能会发生并发修改，也就是多个线程同时对集合进行添加、删除、修改等操作，这样会破坏集合的结构，导致数据不一致。fail-fast机制的出现就是为了解决这个问题，它在多线程并发修改集合时可以快速发现问题并报错，从而避免数据不一致的问题</span></li></ul></details>

### 36. HashMap中的key我们可以使用任意类作为key吗

<details class="lake-collapse"><summary id="ubbb880ac"><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap中的key我们可以使用任意类作为key吗</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u9356580a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">可以使用任意类作为key，但是使用时我们需要保证该类实现了hashCode()和equals()方法，以确保可以正确地进行散列和查找操作。否则，可能会导致key无法正确地被存储或查找。同时，key所述的类也需要实现Serializable接口，以便在需要时可以对HashMap进行序列化和反序列化操作。</span></li><li id="u0b3d05fc" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">在Java中，String、Long、Integer等常见的数据类型已经实现了hashCode()和equals()方法，因此可以直接作为HashMap的key</span></li></ul></details>

### 37. 为什么HashMap的长度是2的N次方呢

<details class="lake-collapse"><summary id="u0aa7c333"><span class="ne-text" style="color: rgb(76, 73, 72)">为什么HashMap的长度是2的N次方呢</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u224a998d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">HashMap</span><span class="ne-text" style="color: rgb(76, 73, 72)">的长度为 2 的 N 次方是为了在存储和访问数据时提高效率，并尽可能减少哈希碰撞的发生。这是通过采用位操作 &amp; 来取代取模 % 运算来实现的。</span></li><li id="ue58962e6" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">当</span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">HashMap</span><span class="ne-text" style="color: rgb(76, 73, 72)">的长度是 2 的幂次时，取余操作等效于与操作，即</span><span class="ne-text" style="color: rgb(76, 73, 72)"> </span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">hash % length</span><span class="ne-text" style="color: rgb(76, 73, 72)"> </span><span class="ne-text" style="color: rgb(76, 73, 72)">等价于</span><span class="ne-text" style="color: rgb(76, 73, 72)"> </span><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">hash &amp; (length - 1)</span><span class="ne-text" style="color: rgb(76, 73, 72)">。位操作 &amp; 在运算效率上具有优势。</span></li><li id="ue93bbf6d" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">这样设计的目的是使数据能够均匀分布在 HashMap 的桶中，使每个链表或红黑树的长度尽可能相等。这样可以减少链表过长或红黑树过深的情况，提高数据的存取效率。</span></li><li id="ua5f675b2" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">因此，选择 HashMap 的长度为 2 的 N 次方是为了在哈希表的设计中兼顾了效率和均匀性，以提供更好的性能和较低的碰撞率。</span></li></ul></details>

### 38. HashMap和ConcurrentHashMap的异同

<details class="lake-collapse"><summary id="u8d9ec815"><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap和ConcurrentHashMap的异同</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u5e993d3e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">相似点：</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="udd0da311" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">都是Map接口的实现类，底层数据结构都是哈希表（数组+链表/红黑树）</span></li><li id="u0ea2c449" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">都允许存储键值对，key和value都可以为null</span></li><li id="ub20d41ac" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">都支持快速的插入、删除和查找操作</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u4f5bc2cf" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">不同点</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="uf578d2c1" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">线程安全型：</span><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap是非线程安全的，而ConcurrentHashMap是线程安全的。在多线程环境下，ConcurrentHashMap的表现更优</span></li><li id="ub7c7ea90" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">性能：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在并发场景下，ConcurrentHashMap要比HashMap表现更好，尤其是当写操作很多的情况下。因为ConcurrentHashMap使用了分段锁的机制，使得多线程能够同时操作不同的段，减少了线程的竞争，从而提高了并发的效率</span></li><li id="u206be20c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">扩容机制：</span><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap扩容时会将原来的数组复制到新的更大的数组中，然后重新计算每个元素在新数组中的位置，这个过程比较耗时。而ConcurrentHashMap在扩容时，只需要复制里面的一部分短，不需要复制整个Map，因此速度相对更快</span></li><li id="uf1627f0e" data-lake-index-type="0"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">null key和null value：</span><span class="ne-text" style="color: rgb(76, 73, 72)">HashMap允许key和value都未null，但是ConcurrentHashMap不允许key和value为null</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u3307eae2" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">总体来说，如果在多线程环境下需要使用Map，建议使用ConcurrentHashMap，否则使用HashMap即可。</span></li></ul></details>

### 39. 红黑树有哪几个特征

<details class="lake-collapse"><summary id="u8e3ad3b5"><span class="ne-text" style="color: rgb(76, 73, 72)">红黑树有哪几个特征</span></summary><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="uf4161a5a" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">红黑树是一种自平衡的二叉搜索树，具有以下特征</span></li></ul><ol class="ne-list-wrap" style="margin: 0; padding-left: 23px; list-style: none"><ol ne-level="1" class="ne-ol" style="margin: 0; padding-left: 23px; list-style: lower-alpha"><li id="u700d7dcb" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">每个节点要么是黑色，要么是红色</span></li><li id="uc4c94bff" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">根节点是黑色的</span></li><li id="ufee94dca" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">所有叶子结点都是黑色的空节点(NIL节点)</span></li><li id="u79a07d65" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">如果一个节点是红色的，则它的啷个子节点都是黑色</span></li><li id="u8f55199c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">任意衣蛾节点到其每个叶子结点的所有路径都包含相同数目的黑色节点</span></li></ol></ol><ul class="ne-ul" style="margin: 0; padding-left: 23px"><li id="u7ab4987c" data-lake-index-type="0"><span class="ne-text" style="color: rgb(76, 73, 72)">这些特征保证了红黑树在插入和三处节点时能够保持平衡，从而保证了其查找、插入、删除操作的时间复杂度都是O(log n)级别的</span></li></ul></details>

### 40. 说说你平时是怎样处理Java异常的

<details class="lake-collapse"><summary id="u32acf0f8"><span class="ne-text" style="color: rgb(76, 73, 72)">说说你平时是怎样处理Java异常的</span></summary><p id="u1261470d" class="ne-p" style="margin: 0; padding: 0; min-height: 24px"><span class="ne-text" style="color: rgb(76, 73, 72)">我通常遵循以下几个规则</span></p><ol class="ne-ol" style="margin: 0; padding-left: 23px"><li id="uaf9544e3" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">按照异常类型分类处理：</span><span class="ne-text" style="color: rgb(76, 73, 72)">对于不同的异常类型，我会根据实际情况进行不同待处理。例如对于业务异常，我通常会将异常信息记录到日志中，并给出友好提示；对于系统异常，我会打印异常的堆栈信息，将异常信息记录到日志中以便排查问题</span></li><li id="u2cf14803" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">异常不要吞掉：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在处理异常时，我不会简单的将异常捕获并吞掉，而是尽可能的将异常处理完毕，避免出现未处理的异常导致系统不稳定或者出现非预期的问题</span></li><li id="u2e710541" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">日志记录：</span><span class="ne-text" style="color: rgb(76, 73, 72)">在处理异常时，我通常会将异常信息记录到日志中，以便后续的问题排查与分析</span></li><li id="u1a2aa648" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">异常处理要及时：</span><span class="ne-text" style="color: rgb(76, 73, 72)">及时处理异常可以避免问题的扩大和影响范围的扩大，同时也可以减轻排查问题的难度</span></li><li id="u42ff9fe4" data-lake-index-type="0" style="text-align: left"><span class="ne-text" style="color: rgb(244, 116, 102); font-size: 14px">代码的健壮性：</span><span class="ne-text" style="color: rgb(76, 73, 72)">尽可能的在代码的设计和编写阶段考虑各种异常情况，图稿代码的健壮性，减少出现异常的可能性</span></li></ol></details>