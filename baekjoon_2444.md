## BAEKJOON 2004_별찍기-7

- My Source

  ```java
  import java.util.Scanner;

  public class Main {
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
      int input = sc.nextInt();
      
      for(int i=0; i<input; i++) {
        for(int j=input-1; j>i; j--) {
          System.out.print(" ");
        }
        for(int k=0; k<2*1+1; k++) {
          System.out.print("*");
        }
        System.out.println();
      }
      for(int i=1; i<input; i++) {
        for(int j=0 j<i; j++) {
          System.out.print(" ");
        }
        for(int k=0; k<2*input-1-2*i; k++) {
          System.out.print("*");
        }
        System.out.println();
      }
    }
  }
  ```

  ​

- Source from "ruikg4858"

  ```java
  import java.util.Scanner;

  /**
   * Created by homr on 2017. 5. 25..
   */
  public class Main {
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
      int num = sc.nextInt();
      String footer = "";
      
      for(int i = 1; i<=num; i++) {
        String str = "";
        for(int j=0; j<num-1; j++) {
          str += " ";
        }
        for(int j = 0; j<i*2-1; j++) {
          str += "*";
        }
        
        System.out.println(str);
        
        if(i!=num) {
          footer = str + "\n" + footer;
        }
      }
      
      System.out.print(footer);
    }
  }
  ```

  ​

 나의 소스는 너무 단순하게 올라가는 for문 한 번, 내려오는 for문 한 번 이렇게 따로따로 찍어냈는데, 올라가는 for문 찍을 때 차례로 아예 한 줄 전체를 문자열로 역순으로 저장해 놓은 다음 나중에 한 번에 찍어주는 생각이 기발했다. 