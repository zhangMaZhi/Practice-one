package three;
import java.util.*;

public class Three {
	

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner in = new Scanner(System.in );
		String str ,s2 = "",s4="";
		int cak = 0,UTC=0,B=0,C=0;
		while(true){
			str = in.nextLine();
			s2 = s2 + str;
			if(str.equals("END"))
				break;
		}
		s2 = s2.replaceAll("END", "");
		if(s2.indexOf("$GPRMC")==0){
			for(int i = 1; i<s2.indexOf("*");i++){
				cak ^= s2.charAt(i);
			}
		}
		cak%=65536;
		if(cak == Integer.parseInt(s2.substring(s2.indexOf("*")+1),16 )&&s2.indexOf(",A,") != -1){
			B = Integer.parseInt( s2.substring(7, 13));
			B = B/10000;
			C = B + 8;
			if(C >= 24){
				 s4 = "0"+String.valueOf(C-24);
			}
			if(C <10){
				 s4 = "0"+String.valueOf(C);
			}
			else if(C<24&&C>=10){
				s4 = String.valueOf(C);
			}
			
		}
//		String s3 = String.valueOf(UTC);
//		s3 = String.format("%08d", s3);
		System.out.println(s4+":"+s2.substring(9, 11)+":"+s2.substring(11, 13));
	}
}
