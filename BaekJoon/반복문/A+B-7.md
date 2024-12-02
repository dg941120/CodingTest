**출처** : <a href="https://www.acmicpc.net/problem/11021" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** :두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.<br>

**입력** : 첫째 줄에 테스트 케이스의 개수 T가 주어진다. <br>

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)<br>

**출력** : 각 테스트 케이스마다 "Case #x: "를 출력한 다음, A+B를 출력한다. 테스트 케이스 번호는 1부터 시작한다.<br>

**#Case1 . 일반적으로 Scanner 사용법**
```
import java.util.Scanner;
 
public class Main {
	public static void main(String args[]) {
 
		Scanner in = new Scanner(System.in);
 
		int a = in.nextInt();
 
		for (int i = 1; i <= a; i++) {
			int c = in.nextInt();
			int d = in.nextInt();
 
			System.out.println("Case #" + i + ": " + (c + d));
		}
 
		in.close();
	}
}
```

**#Case2 . 배열에 저장해서 구하기**
```
import java.util.Scanner;

public class App {
    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);

        int t = sc.nextInt();

        int[][] testCases = new int[t][2]; 

        for (int i = 0; i < t; i++) {
            testCases[i][0] = sc.nextInt(); 
            testCases[i][1] = sc.nextInt(); 
        }

        for (int i = 0; i < t; i++) {
            int A = testCases[i][0];
            int B = testCases[i][1];
            int C = A + B;
            System.out.println("Case #" + (i + 1) + ": "+ C);
        }

        sc.close(); 
    }
}
```

크게 시간차이는 나지않앗음

**#Case3 . BufferedReader 사용**

```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.StringTokenizer;
import java.io.IOException;
 
public class App {
	public static void main(String args[]) throws IOException {
 
		BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
		
		int a = Integer.parseInt(br.readLine());
 
		StringTokenizer st;
		for (int i = 1; i <= a; i++) {
			st = new StringTokenizer(br.readLine()," ");
			System.out.println("Case #" + i + ": " 
			+(Integer.parseInt(st.nextToken())
			+Integer.parseInt(st.nextToken())));
		}
		br.close();
	}
 
}
```

실행시간이 204 -> 128ms로 줄어듬.
메모리 역시 18000kb -> 16000대로 줄어들었음
