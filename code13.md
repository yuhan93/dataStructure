문제 : n개의 음이 아닌 한 자리 정수를 입력 받아 배열에 저장한다.

이들 중에서 1개 이상의 연속된 정수들을 합하여 얻을 수 있는 소수들 중에서 최대값을 구하여

출력하는 프로그램을 작성하라.

ex ) \[ 1 , 9, 4 ,0 ,**7 ,1 ,3** ,6 ,2 ,3 \]

                    **713 으로 해석**

```java
public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int [] data = new int [n];
		
		for(int i = 0; i < n; i ++) {
			data[i] = sc.nextInt();
		}
		sc.close();
		
		int max = 0;
		for (int i =0; i < n; i++) {
			for(int j = i; j < n; j++) {
				
				int val = 0;
				for (int k = i; k <= j; k++) {
					val = val * 10 + data[k];
				}
				boolean isPrime = true;
				for(int k = 2; k * k <= val && isPrime; k++) {
					if (val % k == 0) {
						isPrime = false;
					}
				}
				if(isPrime && val > 1 && val > max) {
					max = val;
				}
			}
		}
		if(max > 0) {
			System.out.println("max");
		} else {
			System.out.println("No prime number");
		}
		
	}

}
```

![캡처](https://user-images.githubusercontent.com/56163121/150909692-c3d854d8-f218-4fd7-b7b9-326d39a07a85.PNG)
