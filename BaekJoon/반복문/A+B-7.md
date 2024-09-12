**출처** : <a href="https://www.acmicpc.net/problem/11021" style="color: blue; text-decoration: underline;">BackJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** :두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.<br>

**입력** : 첫째 줄에 테스트 케이스의 개수 T가 주어진다. <br>

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)<br>

**출력** : 각 테스트 케이스마다 "Case #x: "를 출력한 다음, A+B를 출력한다. 테스트 케이스 번호는 1부터 시작한다.<br>

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
