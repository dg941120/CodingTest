**출처** : <a href="https://www.acmicpc.net/problem/2557" style="color: blue; text-decoration: underline;">BaekJoon</a><br>
**언어 : <mark>JAVA**</mark><br>
**문제** : Hello World!를 출력하시오.<br>


1. System.out.print 사용
```
public class Main{
    public static void main(String[] args){
        System.out.print("Hello World!");
    }
}
```

2. BufferedWriter 사용
```
import java.io.BufferedWriter;
import java.io.OutputStreamWriter;
import java.io.IOException;
 
public class Main {
	public static void main(String[] args) throws IOException { //IOException 사용
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));  
 
		bw.write("Hello World!"); // 버퍼에 저장
		bw.flush(); // 출력
		bw.close(); // 닫기 => 성능증가
	}
}
```

3. StringBuilder 사용
```
public class Main {
    public static void main(String[] args){
        StringBuilder sb = new StringBuilder();

        sb.append("Hello World!");
        System.out.println(sb);
    }
}
```

4. StringBuffer 사용
```
// StirngBuilder와 다르게 동기화 지원
// 문자열이 리소스로 활용될 시 StringBuffer 사용해야함

public class Main{
    public static void main(String[] args) {
        StringBuffer sb = new StringBuffer();

        sb.append("Hello World!");
        System.out.println(sb);
    }
}
```
