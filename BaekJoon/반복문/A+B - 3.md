**출처** : <a href="https://www.acmicpc.net/problem/10950" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** :두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.<br>

**입력** : 첫째 줄에 테스트 케이스의 개수 T가 주어진다.<br>

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10) <br>
**문제** :각 테스트 케이스마다 A+B를 출력한다.<br>



```
import java.util.Scanner;

public class App{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int t = sc.nextInt();

        for(int i=0; i<t; i++){
            System.out.println("A를 입력해주세요: ");
            int a = sc.nextInt();
            System.out.println("B를 입력해주세요: ");
            int b = sc.nextInt();
            System.out.println(a + b);
        }

        sc.close();
    }
}

메모리 : 18560kb, 시간:196ms
```
