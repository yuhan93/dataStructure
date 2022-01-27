문제  n 개의 정수를 입력 받아 순서대로 배열에 저장한다.

그런 다음 모든 정수들을 한 칸씩 오른쪽으로 shift 하라.

마지막 정수는 배열의 첫 칸으로 이동하라.

 8  4  1  7  11  13  5  2 
 ---  ---  ---  ---  ---  ---  ---  --- 

 2  8  4  1  7  11  13  5 
 ---  ---  ---  ---  ---  ---  ---  --- 

---

```java
class main {
	public static void main(Stringp[] args){
    	Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int [] data = new int [n];
        for (int i = 0 ; i  n; i ++){
        	data[i] = sc.nextInt();
        }
        sc.close();
        
        int tmp = data[n-1];
        for (int i = n-2; i = 0; i --){
        	data[i+1] = data[i];
        }
        data[0] = tmp;
        
        for(int i = 0; i  n; i ++){
        	System.out.println(data[i]);
        }
    }
}
```