```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int[] data = new int [n];
		for( int i = 0 ; i < n; i ++) {
			data[i] = sc.nextInt();
		}
		
		sc.close();
		
        // 함수를 사용해 오름차순으로 정렬 
		bubbleSort( n,data );
		
		System.out.println("Sorted data : ");
		for( int i = 0 ; i < n; i ++) {
			System.out.println(data[i]);
		}
	}
	 // void : return 값이 없다.
	static void bubbleSort(int n , int[] data) {
		for( int i = n-1; i > 0; i --) {
			for( int j = 0; j < i; j++) {
				if (data[j] > data[j+1]) {
					int tmp = data[j];
					data[j] = data[j+1];
					data[j+1] = tmp;
				}
			}
		}
		
	}

}
```
