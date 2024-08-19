**출처** : <a href="https://www.acmicpc.net/problem/1000" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** : 두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.<br>



1. Scanner 사용
```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        double a = sc.nextDouble(); // 나눗셈이 소수자리까지 계산해야하므로 double 타입선언
        double b = sc.nextDouble();
        
        System.out.print(a/b);

        sc.close();
    }
}
```

