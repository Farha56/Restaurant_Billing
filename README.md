# Restaurant_Billing
import java.util.ArrayList;
import java.util.Date;
import java.util.Iterator;
import java.util.Scanner;

public class MultiThread  {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
	Scanner sc=new Scanner(System.in);
	
	Date date=new Date();
	System.out.println("Enter userName");
	String userName=sc.nextLine();
	System.out.println(" ");
	System.out.println();
	System.out.println("Hotel Name\t\t"+"Paradise Veg & Non Veg Restaurant"+"\t\t\t"+date.toString());
			
	int a,b,c,d,e,f,l,i;
	int eachCost=0;
			int cost=0;
			int price=0;
	int y=0,v=0;
	String items=" ";
	System.out.println("");
	System.out.println("our menu card");
	System.out.println("");
	System.out.println("Item Name\t\t"+" Amount"+"\t\t\t\t\t"+"press to order");
	System.out.println("");
	System.out.println("Rice\t\t\t"+60+"\t\t\t\t\t"+1);
	System.out.println("chinese\t\t\t"+80+"\t\t\t\t\t"+2);
	System.out.println("fish\t\t\t"+90+"\t\t\t\t\t"+3);
	System.out.println("Mutton\t\t\t"+260+"\t\t\t\t\t"+4);
	System.out.println("chicken\t\t\t"+160+"\t\t\t\t\t"+5);
	System.out.println("paneer\t\t\t"+130+"\t\t\t\t\t"+6);
	System.out.println("");
	System.out.println("");
	ArrayList order=new ArrayList();
	ArrayList<Integer> pric=new ArrayList<>();
	ArrayList plate=new ArrayList();
	do
	{
		System.out.println("press to order");
		a=sc.nextInt();
		int press[]=new int[] {a};
		
		System.out.println("Enter no of plates");
		b=sc.nextInt();
		System.out.println("");
		
		
		if(a==1)
		{
			items="Rice and dal";
			price=60;
			eachCost=price*b;
			cost+=eachCost;
			
			boolean of=order.contains(items);
			if(of)
			{
				order.add("");
				pric.add(eachCost);
				plate.add(b);
			}
			else
			{
				pric.add(eachCost);
				plate.add(b);
				order.add(items);
			}
		}
		if(a==2)
		{
			items="chinese";
			price=80;
			eachCost=price*b;
			cost+=eachCost;
			order.add(items);
			
			
				pric.add(eachCost);
				plate.add(b);
			}
		if(a==3)
		{
			items="fish";
			price=90;
			eachCost=price*b;
			cost+=eachCost;
			order.add(items);
			
			
				pric.add(eachCost);
				plate.add(b);
			}
		if(a==4)
		{
			items="Mutton";
			price=260;
			eachCost=price*b;
			cost+=eachCost;
			order.add(items);
			
			
				pric.add(eachCost);
				plate.add(b);
			}
		if(a==5)
		{
			items="chicken";
			price=160;
			eachCost=price*b;
			cost+=eachCost;
			order.add(items);
			
			
				pric.add(eachCost);
				plate.add(b);
			}
		if(a==6)
		{
			items="paneer";
			price=120;
			eachCost=price*b;
			cost+=eachCost;
			order.add(items);
			
			
				pric.add(eachCost);
				plate.add(b);
			}
		for(int k=0;k<press.length;k++)
		{
			String fetchitemname=" ";
			if(press[k]==1)
			{
				fetchitemname=" Rice";	
			}
			if(press[k]==2)
			{
				fetchitemname="Chinese";	
			}
			if(press[k]==3)
			{
				fetchitemname=" fish";	
			}
			if(press[k]==4)
			{
				fetchitemname="Mutton";	
			}
			if(press[k]==5)
			{
				fetchitemname=" chicken";	
			}
			if(press[k]==6)
			{
				fetchitemname=" paneer";	
			}
		}
			System.out.println("do u want to continue the order(press 1 for continue /or press0)");
			
			y=sc.nextInt();
			System.out.println(" ");
		}
		while(y!=0);
		System.out.println(" ");
		System.out.println(" ");
		System.out.println("Items Names\t\t\t"+"no of plates\t\t\t"+"sub total");
				System.out.println(" ");
		Iterator itr=order.iterator();
		Iterator<Integer>itr1=pric.iterator();
		
		Iterator itr2=plate.iterator();
		while(itr.hasNext() && itr2.hasNext())
		{
			System.out.println(itr.next()+"\t\t"+itr2.next()+"\t\t\t"+itr1.next());
		    System.out.println(" ");
		}
		  System.out.println(" ");
		  System.out.println("Total Bill:"+"\t\t\t\t\t"+cost);
		  System.out.println(" ");
		  System.out.println("do u want to delete the order(press 1 for continue /or press0)");;
	l=sc.nextInt();
	System.out.println(" ");
	if(l==1)
	{
		do
		{
			if(order.isEmpty())
			{
				System.out.println("your cart is empty");
				break;
				
				
			}
			else
			{
				System.out.println("press to delete");
				f=sc.nextInt();
				int delete[]=new int[] {f};
				
				if(f==1) {
					items="dal and rice";
					boolean of=order.contains(items);
					int of1=order.indexOf(items);
					if(of)
					{
						order.remove(items);
						cost=cost-pric.remove(of1);
						plate.remove(of1);
					}
					
				}
				if(f==2) {
					items="chinese";
					boolean of=order.contains(items);
					int of1=order.indexOf(items);
					if(of)
					{
						order.remove(items);
						cost=cost-pric.remove(of1);
						plate.remove(of1);
					}
				}
				if(f==3) {
					items="fish";
					boolean of=order.contains(items);
					int of1=order.indexOf(items);
					if(of)
					{
						order.remove(items);
						cost=cost-pric.remove(of1);
						plate.remove(of1);
					}
				}
				if(f==4) {
					items="Mutton";
					boolean of=order.contains(items);
					int of1=order.indexOf(items);
					if(of)
					{
						order.remove(items);
						cost=cost-pric.remove(of1);
						plate.remove(of1);
					}
				}
				if(f==5) {
					items="chicken";
					boolean of=order.contains(items);
					int of1=order.indexOf(items);
					if(of)
					{
						order.remove(items);
						cost=cost-pric.remove(of1);
						plate.remove(of1);
					}
				}
					if(f==6) {
						items="paneer";
						boolean of=order.contains(items);
						int of1=order.indexOf(items);
						if(of)
						{
							order.remove(items);
							cost=cost-pric.remove(of1);
							plate.remove(of1);
						}
				}
				 System.out.println("continue to delete the order(press 1 for continue /or press0)");;
				y=sc.nextInt();	
			}
			
		}
		while(v!=0);
System.out.println(" ");
System.out.println("Items Names\t\t\t"+" no of plates\t\t\t"+"sub total");
	itr=order.iterator();
itr1=pric.iterator();
itr2=plate.iterator();
int scost=0;
while(itr.hasNext() && itr1.hasNext() && itr2.hasNext())
{
	System.out.println(itr.next()+"\t\t"+itr2.next()+"\t\t"+itr1.next());
			System.out.println(" ");

	System.out.println(" ");

}
System.out.println(" Total bill : "+"\t\t"+" " +"\t\t"+cost);
	}
	System.out.println(" Thank you for visiting"+" "+"paradise"+"\t\t\t"+"signature(farha)");
	
	}

	}

	
		
		
	
        
	
