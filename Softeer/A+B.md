**출처** : <a href="https://softeer.ai/app/assessment/index.html?xid=254738&xsrfToken=LSjjgSH3MxU35htgAjSC7i9jRAjR1FXC&testType=practice" style="color: blue; text-decoration: underline;">Softeer</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** : 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.<br>
**제약조건** : 두 정수 A와 B는 1이상 9이하의 정수이다.<br>
**입력형식** : 첫째 줄에 테스트 케이스의 T의 정수가 주어진다.<br> 각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다.<br>
**출력형식** : 각 테스트 케이스 마다 "Case #(테스트 케이스 번호) : "를 출력한다음 , A+B를 출력한다.<br>테스트 케이스 번호는 1부터 시작한다.

```JAVA
// code
import java.io.*;
import java.util.*;

public class Main {

     public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //편의상 sc라고 했으나 fullname 표기가 나았으려나?
        int T = sc.nextInt(); // tc 
        for (int i = 1; i <= T; i++) {
            int A = sc.nextInt();
            int B = sc.nextInt(); 
            System.out.println("Case #" + i + ": " + (A + B));
        }
        //선언해주지 않아도 되나 메모리 누수, 성능저하등 이슈가 생길 원인이 될 수 있으므로 닫아주는게 좋음.
        sc.close();
    }
  }






