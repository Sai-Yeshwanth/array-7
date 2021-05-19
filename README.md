import java.util.Scanner;

class Add{
	static int arr[] = new int[100];
	
	static float sum=0;
	static int flag=0;
	static Scanner input = new Scanner(System.in);
	public static void addarr()
	{
		System.out.println("Enter size of array:");
		int n = input.nextInt();
		System.out.println("Enter "+ n +" elements of array");
		for(int i=0;i<n;i++)
		{
			arr[i] = input.nextInt();
		}
		int arr2[] = new int[(arr.length + 1)];
		System.out.println("Enter which element should be added and at what position:");
		int h = input.nextInt();
		int pos = input.nextInt();
		for(int i=0;i<arr2.length;i++)
		{
			if(i<pos)
			{
				arr2[i]=arr[i];
			}
			else if(i==pos)
			{
				arr2[i]=h;
			}
			else
			{
				arr2[i]=arr[i-1];
			}
		}
		
		System.out.println("Elements after adding in array are");
		for(int i=0;i<=n;i++)
		{
			System.out.println(arr2[i]);
		}
	}
}

public class Jala {

	public static void main(String[] args) {
		Add a = new Add();
		a.addarr();
	}
}
