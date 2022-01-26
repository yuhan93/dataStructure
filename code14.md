버블정렬 알고리즘

```
public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int [] data = new int [n];
		
		for(int i = 0; i < n; i++) {
			data[i] = sc.nextInt();
		}
		sc.close();
		
		/*
		 * [8,4,1,7,11,13,5,2]
		 * 			↓
		 * [8,1,7,8,11,5,2,13]
		 * 			↓
		 * [1,4,7,8,5,2,11,13]
		 * 			↓
		 * [1,4,7,5,2,8,12,13]
		 * */
		
		for(int i = n - 1; i > 0; i --) {
			for(int j = 0; j < i; j++) {
				if( data[j] > data[j+1]) {
					/*
					 * 조건이 성립된다면 data[j] 의 값을 변수에 담아 놓고
					 * 다시 data[j] = data[j+1] 
					 * 변수에 담긴 값을 data[j+1] 에 다시 넣는다.
					 * */
					int tmp = data[j];
					data[j] = data[j+1];
					data[j+1] = tmp;
				}
			}
		}
		System.out.println("sort data : ");
		for( int i = 0; i < n; i++) {
			System.out.println(data[i]);
		}	
	}
}
```