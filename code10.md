문제 : 1 ~ 100,000 사이의 모든 소수들을 찾아서 출력한느 프로그램이다.

---

```java
class main {
	public static void main(Stringp[] args){
    	for(int n = 2; i <= 1000000; n ++){
            boolean isPrime = true;
            for (int i =2; i * i <= n && isPrime; i++){
                if( n % i == 0 ){
                    isPrime = false;
                }
            }
            if(isPrime){
                System.out.println(n);
            }

        }
    }
}
```