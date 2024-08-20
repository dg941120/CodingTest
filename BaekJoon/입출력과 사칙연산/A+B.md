**출처** : <a href="https://www.acmicpc.net/problem/1000" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** : 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.<br>


1. Scanner 사용
```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in); //System.in은 inputStream의 정적필드
        int A = sc.nextInt();
        int B = sc.nextInt();

        System.out.println(A+B);
        sc.close(); //걸어줬을때 시간이 164ms, 아닐시 180ms로 차이가 있음. 용량도 유의미하게 차이남
    }
}

메모리 : 17700KB , 시간 : 164ms
```

2. BufferedReader(IOEception try-catch 구현)
```
// 
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); //BufferedReader 객체 생성

            String str = br.readLine(); // 사용자로부터 한줄 입력받기
            StringTokenizer st = new StringTokenizer(str, " "); // 입력받은 문자열 공백기준으로 분리
            int a = Integer.parseInt(st.nextToken()); // 첫번째 숫자를 받아 정수로 변환
            int b = Integer.parseInt(st.nextToken()); // 두번째 숫자를 받아 정수로 변환
  
            System.out.println(a + b); // 합출력
        } catch (IOException e) { 
            e.printStackTrace();
        }
    }
}

메모리 : 14252KB, 시간 : 104ms
```

3. BufferedReader(IOEception 구현)

```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class Main{
      public static void main(String[] args) throws IOException{
          BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

          String str = br.readLine();
          StringTokenizer st = new StringTokenizer(str, " ");
          int a = Integer.parseInt(st.nextToken());
          int b = Integer.parseInt(st.nextToken());

          System.out.println(a+b);
    }
}

메모리 : 14160KB, 시간 : 104ms.
```


메모
```
간결하게 작성하는 현대 JAVA에서는 3번을 주로사용하지만
복잡한 구현을 할때는 세밀한 코드인 2번을 주로 사용.
io패키지는 필수로 IOException 체크를 해주어야함(try-catch, throws 등으로)
Scanner나 System.out.print는 자체적으로 예외처리를 해줘서 해줄필요는 없다.
```
