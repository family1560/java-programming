# java-programming
import java.util.*;

public class Main {

	static long[][] arr = new long[91][2];
	
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		System.out.println(thing(n));
	}
	
	static long thing(int n) {
		arr[1][0] = 0;
		arr[1][1] = 1;  
		for( int i = 2 ; i <=n ; i++) {
			arr[i][0] = arr[i-1][1] + arr[i-1][0];
			arr[i][1] = arr[i-1][0] ; 
		}

		return arr[n][0] + arr[n][1];
	}
}
