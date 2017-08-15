public class Fenjiezhiyinshu {
	public static void sum(int a,int b)
	{
		int sum=0;
		int count =0;
//		boolean =true;
		for(int i =a;i>=a&&i<=b;i++){
			for(int h =1;h<i;h++){
				if(i%h == 0){
					sum = sum + h;
					}
				}
			if(sum == i){
				count++;
				if(count==1)
				{
					System.out.print(i);
				}
				else{
					System.out.print(" "+i);
				}
			}
						
			sum = 0;	
		}
		if(count == 0){
			System.out.print("\n"+"NIL");
		}
		
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		sum(5,50);
//		sum(3,5);

	}

}
}
