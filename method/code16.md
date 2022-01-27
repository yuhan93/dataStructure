문제 : 입력으로 두 정수 a 와 b 를 받아 a 의 b승을 계산한다.

```java
public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		
		int a = sc.nextInt();
		int b = sc.nextInt();
		
		/*
		 * result : 메서드 power가 return 문으로 넘겨준 값을 받아서 변수 result에 저장한다.
		 * power : 메서드 power를 호출하면서 매개변수로 정수 a와 b의 값을 건낸다. 
		 * */
		int result = power( a , b);
		System.out.println("Hte result is : " + result);
		sc.close();
	}
	
	/*
	 * power : 메서드 power는 매개변수로 두 개의 정수를 건내 받으며 각각을 m과 n이라고 이름 짓는다.
	 * return result : 메서드 power는 계산 결과, 즉 변수 result의 값을 return 문을 이용해 자신을 호출한 이에게 넘겨준다.
	 * */
	public static int power( int n , int m ) {
		int result = 1;
		for (int i = 0; i < m; i++) {
			result *= n;
		}
		return result;
	}

}
```