**출처** : <a href="https://www.acmicpc.net/problem/1001" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** : 두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.<br>

1. Scanner 사용
```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        System.out.print(a-b);

        sc.close();
    }
}
메모리:17708, 시간:168ms
```
  
2. String.split() 사용
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // BufferedReader 객체 생성

            String str = br.readLine(); // 사용자로부터 한 줄 입력받기
            String[] tokens = str.split(" "); // 입력받은 문자열을 공백 기준으로 분리
            
            int a = Integer.parseInt(tokens[0]); // 첫 번째 숫자를 받아 정수로 변환
            int b = Integer.parseInt(tokens[1]); // 두 번째 숫자를 받아 정수로 변환

            System.out.println(a - b); // - 출력

        } catch (IOException e) { 
            e.printStackTrace();
        }
    }
}
메모리:14340, 시간:100ms
```

3. StringTokenizer 사용
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

            String str = br.readLine(); 
            StringTokenizer st = new StringTokenizer(str, " "); 
            int a = Integer.parseInt(st.nextToken()); 
            int b = Integer.parseInt(st.nextToken()); 
  
            System.out.println(a - b); 
        } catch (IOException e) { 
            e.printStackTrace();
        }
    }
}
메모리:14328, 시간:100ms
```
메모
```
String.split() 을 사용해서 훨씬 더 간결하게 만들어봄.
소스 자체도 간결하며 현대에서도 더 많이 쓰임.
대신 StringTokenizer는 한번에 하나씩만 처리가능하므로 성능적으로 더 우수하다고함(현재는 코드가 짧아서 똑같이 나옴)
```
