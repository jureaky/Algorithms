## BAEKJOON_2748 피보나치 수 2

- My source

  ```java
  import java.util.Scanner;

  public class Main {
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
      int n = sc.nextInt();
      long fib = 0;
      long fib0 = 0;
      long fib1 = 1;
      
      if(n==0) {
        fib = fib0;
        System.out.println(fib);
      }
      if(n==1) {
        fib = fib1;
        System.out.println(fib);
      }
      if(n>1) {
        for(int i=2; i<=n; i++) {
          fib = fib0 + fib1;
          fib0 = fib1;
          fib1 = fib;
        }
        System.out.println(fib);
      }
    }
  }
  ```

  변수의 scope에 대한 개념이 잘 안잡혀서 쓸데없이 고생했던 문제...



- Source from "kjlkggg"

  ```java
  import java.io.BufferedReader;
  import java.io.BufferedWriter;
  import java.io.IOException;
  import java.io.InputStreamReader;
  import java.io.OutputStreamWriter;

  public class Main {
    
    private BufferedReader br;
    private BufferedWriter bw;
    private int n;
    private long dp[];
    public static void main(String[] args) throws IOException {
      new Main().start();
    }
    
    void start() throws IOException {
      
      br = new BufferedReader(new InputStreamReader(System.in));
      bw = new BufferedWriter(new OutputStreamWriter(System.out));
      n = Integer.parseInt(br.readLine());
      dp = new long[n+1];
      dp[1] = 1;
      
      for(int i=2; i<=n; i++) {
        dp[i]=dp[i-1]+dp[i-2];
      }
      bw.write(dp[n]+"");
      bw.flush();
      br.close();
      bw.close();
    }
  }
  ```

  ​

