// **출처** : <a href="https://www.acmicpc.net/problem/10871" style="color: blue; text-decoration: underline;">BackJoon</a><br>
// **언어 : <mark>JAVA**</mark><br>
// **문제** :정수 N개로 이루어진 수열 A와 정수 X가 주어진다. 이때, A에서 X보다 작은 수를 모두 출력하는 프로그램을 작성하시오.

// **입력** : 첫째 줄에 N과 X가 주어진다. (1 ≤ N, X ≤ 10,000)

둘째 줄에 수열 A를 이루는 정수 N개가 주어진다. 주어지는 정수는 모두 1보다 크거나 같고, 10,000보다 작거나 같은 정수이다.

// **출력** : X보다 작은 수를 입력받은 순서대로 공백으로 구분해 출력한다. X보다 작은 수는 적어도 하나 존재한다.
```
1. Scanner 사용

import java.util.Scanner;

public class App {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // N과 X를 입력받음
        int N = sc.nextInt();
        int X = sc.nextInt();

        // 수열 A를 입력받음
        int[] A = new int[N];
        for (int i = 0; i < N; i++) {
            A[i] = sc.nextInt();
        }

        // X보다 작은 수를 출력
        for (int i = 0; i < N; i++) {
            if (A[i] < X) {
                System.out.print(A[i] + " ");
            }
        }

        // 종료
        sc.close();


    }
}





```

메모리 : 30616kb , 시간 : 496ms
