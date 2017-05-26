## BAEKJOON_2750 수 정렬하기

- My source

  ```java
  import java.util.Scanner;

  public static void main(String[] args) {
    int temp;
    Scanner sc = new Scanner(System.in);
    int size = sc.nextInt();
    int[] sortArr = new int[size];
    
    for(int i=0; i<size; i++) {
      int a = sc.nextInt();
      sortArr[i] = a;
    }
    
    for(int i=sortArr.length-1; i>=0; i--) {
      for(int j=0; j<i; j++) {
        if(sortArr[j]>sortArr[j+1]) {
          temp = sortArr[j];
          sortArr[j] = sortArr[j+1];
          sortArr[j+1] = temp;
        }
      }
    }
    
    for(int i=0; i<sortArr.length; i++) {
      System.out.println(sortArr[i]);
    }
  }
  ```



- Source from "iluveyou"

  ```java
  import java.io.BufferedReader;
  import java.io.BufferedWriter;
  import java.io.InputStreamReader;
  import java.io.OutputStreamWriter;

  public class Main{
    
    public static void main(String[] args) throws Exception {
      BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
      BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
      
      int n = Integer.parseInt(br.readLine());
      
      int a[] = new int[n];
      
      for(int i=0; i<n; i++) {
        a[i] = Integer.parseInt(br.readLine());
      }
      
      for(int i=0; i<n-1; i++) {
        for(int j=i+1; j<n; j++) {
          if(a[i]>a[j]) {
            int tmp = a[i];
            a[i] = a[j];
            a[j] = tmp;
          }
        }
      }
      
      for(int i=0; i<n; i++) {
        bw.write("" + a[i] + "\n");
      }
      
      bw.flush(); bw.close(); br.close();
    }
  }
  ```

  ​

- Source from "kjlkggg"

  ```java
  import java.io.BufferedReader;
  import java.io.BufferedWriter;
  import java.io.IOException;
  import java.io.InputStreamReader;
  import java.io.OutputStreamWriter;
  import java.util.Arrays;

  public class Main {
    private BufferedReader br;
    private BufferedWriter bw;
    private int n;
    private int arr[];
    
    public static void main(String[] args) throws IOException {
      new Main().start();
    }
    
    void start() throws IOException {
      br = new BufferedReader(new InputStreamReader(System.in));
      bw = new BufferedWriter(new OutputStreamWriter(System.out));
      n = Integer.parseInt(br.readLine());
      arr = new int[n];
      for(int i=0; i<n; i++) {
        arr[i] = Integer.parseInt(br.readLint());
      }
      Arrays.sort(arr);
      for(int i=0; i<n; i++) {
        bw.write(arr[i] + "\n");
      }
      bw.flush();
      br.close();
      bw.close();
    }
  }
  ```

  ​

