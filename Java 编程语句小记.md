# Java 编程语句小记



## 字符操作

### 集合数组之间变换

```java
String s = "abcsdasfg"
char[] c;
c = s.toCharArray();   //转换为字符数组

List<String> res = new LinkedList<>();
String[] ss= res.toArray(new String[res.size()]);  //字符串集合转数组
//数组转集合列表
String[] str ={"leet", "code"};
List<String> wordDict = Arrays.asList(str);

String.valueOf()  //将其他变量或者字符数组转换为字符串
Arrays.toString(int[])  //数组转字符串
```

**提取数字的其中某一位置的数字**：

```java
Long.toString(num).charAt((n - 1) % digit) - '0'; 
//基础数据类型之间用toString转为字符转，再用字符串方法提取对应位置数字为字符，再根据ASCII码操作减法可得对应数字
```



### Integer数组转化为int数组

```java
return res.stream().mapToInt(Integer::intValue).toArray();
//等价于循环赋值
int[] resArr = new int[resSet.size()];
        int index = 0;
        //将结果几何转为数组
        for (int i : resSet) {
            resArr[index++] = i;
        }
        return resArr;
```

### 匿名内部类，比较器的正则表达式

```java
(o1, o2) -> o1.getValue() - o2.getValue()
```

### 根据值在map中返回键

```java
res[i] = queue.poll().getKey();//根据值返回键
```