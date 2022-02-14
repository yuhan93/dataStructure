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

---

#### **함수를 추가하여 swap을 할 수 없다.**

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
					// swap data[j] and data[j+1]
					/*
					 * swap 메서드를 호출하는 순간 data[j]와 data[j+1]의 값이 각각 a,b에 복사된다. 그 뿐이다.
					 * 즉 완전히 별개의 변수이다.
					 * 따라서 a와 b의 값을 변경하여도 data[j]와 data[j+1]의 값에는 변화가 없다.
					 * */
					swap(data[j], data[j+1]);
//					int tmp = data[j];
//					data[j] = data[j+1];
//					data[j+1] = tmp;
				}
			}
		}
	}
	/*
	 * 프리미티브 타입의 매개변수는 호출된 메서드에서 값을 변경하더라도 호출한 쪽에 영향을 주지 못한다.
	 * 이것은 '값에 의한 호출' 이기 때문이다.
	 * 배열의 값은 호출된 메서드에서 변경하면 호출한 쪽에서도 변경된다.
	 * */
	static void swap(int a, int b) {
		int tmp = a;
		a = b;
		b = tmp;
	}

}
```