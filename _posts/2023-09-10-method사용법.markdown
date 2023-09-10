---
layout: post
title: "method사용법"
date: 2023-09-10
last_modified_at: 2023-09-10
categories: [programming]
tags: [Java]
---

# Method 사용법

method 는 java에서 함수 역할을 한다.

```
접근제어자 리턴타입 메서드명 (파라메터1, 파라메터2 ....){
        로직
}
```

형태로 사용한다.  
예를 들어, 사칙연산을 class와 method를 이용하여 구현해보았다.

```
import java.util.Objects;

public class Method01 {
    public static void main(String[] args) {
        Method01 instance1 = new Method01();
        int add = instance1.addNumber(1,2);
        int sub = instance1.subNumber(1,2);
        int mul = instance1.mulNumber(1,2);
        int div = instance1.divNumber(1,2);
        int cal = instance1.calculate(3,2,"+");
        System.out.println(add);
        System.out.println(sub);
        System.out.println(mul);
        System.out.println(div);
        System.out.println(cal);
    }
    public int addNumber(int num,int num2){
        return num + num2;
    }
    public int subNumber(int num,int num2){
        return num - num2;
    }
    public int mulNumber(int num,int num2){
        return num * num2;
    }
    public int divNumber(int num,int num2){
        return num / num2;
    }
    public int calculate(int num, int num2, String type){
        if(Objects.equals(type, "+")){ // type == "+"
            return num + num2;
        }
        else if(Objects.equals(type, "-")){ // type == "-"
            return num - num2;
        }
        else if(Objects.equals(type, "*")){ // type == "*"
            return num * num2;
        }
        else{ // type == "/"
            return num / num2;
        }
    }
}

```

출력결과

```
3    // 1+2
-1   // 1-2
2    // 1*2
0    // 1/2
5    // 3*2
```
