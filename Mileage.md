import java.util.HashMap;
import java.util.Scanner;

public class Mileage {
		
	public static void main(String[] args) {
		HashMap<String,Integer> map = new HashMap<String,Integer>();
		Scanner in = new Scanner(System.in);
		int cnt = 0;
		int milesge = 0;
		while(true){
			String s = in.next();
			if(s.equals("###"))
				break;
			else
				cnt++;
			map.put(s, cnt);
		}
		int sum[][] = new int [cnt][cnt];
		for(int i = 0;i<cnt;i++){
			for(int j = 0;j<cnt;j++){
				sum[i][j] = in.nextInt();
			}
		}
		String s1 = in.next();
		String s2 = in.next();
		int a = map.get(s1);
		int b = map.get(s2);
		milesge = sum[a-1][b-1];
		System.out.println(milesge);
		

   }
}
