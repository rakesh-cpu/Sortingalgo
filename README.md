import java.util.*;
public class SortingAlgo{
    public static void main(String args[]){
        SortingAlgo sa=new SortingAlgo();
        Scanner sc=new Scanner(System.in);
        System.out.print("welcome to sorting world:\n");
        System.out.println("Select below any one sorting algorithm of your choice to sort your array elements in ascending order:\n ");
        System.out.print("\n1.Bubble sort-one \n 2.Selection sort- two \n 3.Insertion sort-three \n 4.Quick sort-four \n 5.Merge sort-five:::\n");
        System.out.println();
        System.out.print("\n your choice: ");
        int choice=sc.nextInt();
        System.out.print("select array size:\n");
        int size=sc.nextInt();
        System.out.println("size: "+size);
        
        int array[]=new int[size];
        for(int i=0;i<=size;i++){
            array[i]=sc.nextInt();
        }
        System.out.println();
        System.out.print("\n your array before sort:");
        for(int i=0;i<size;i++){
            System.out.print(array[i]+" ");
        }
    }
}
