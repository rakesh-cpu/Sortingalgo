import java.util.*;
public class SortingAlgo{
  //********************bubble sort method********************************
    public void bubbleSort(int array[]){
    for(int i=0;i<array.length;i++)
    {
        for(int j=i+1;j<array.length;j++)
        {
            if(array[j]<array[i])
            {
                int temp=array[i];
                array[i]=array[j];
                array[j]=temp;
            }
        }
        for(int k=0;k<array.length;k++)
        {
        System.out.print(array[k]+" ");
        }
        System.out.println();
        
    }
    }
    //*******************selection sort method*******************************
    public void selectionSort(int array[])
    {
     for(int i=0;i<array.length-1;i++)
       {
        int indx=i;
        for(int j=i+1;j<array.length;j++)
        {
            if(array[j]<array[indx])
            {
                indx=j;
            }
        }
        int temp=array[i];
         array[i]=array[indx];
         array[indx]=temp;
        for(int k=0;k<array.length;k++)
        {
        System.out.print(array[k]+" ");
        }
        System.out.println();
        }
    }   
    public void insertionSort(int array[])
    {
        for(int i=1;i<array.length;i++)
        {
            int key=array[i];
            int j=i-1;
            
            while(j>=0 && key<array[j])
            {
                
                array[j+1]=array[j];
                j--;
                
                
            }
            array[j+1]=key;
            for(int k=0;k<array.length;k++)
            {
             System.out.print(array[k]+" ");
            }
            System.out.println();
          }
    }
    // code driver start here
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
        int size=sc.nextInt(); // it takes array size
        System.out.println("size: "+size);
        
        int array[]=new int[size];
        //array initialization 
        for(int i=0;i<size;i++){
            array[i]=sc.nextInt();
        }
        //****************display unsorted array***********************************
        System.out.print("\n your array before sort:");
        for(int i=0;i<size;i++){
            System.out.print(array[i]+" ");
            
        }
        System.out.println();
        // ***************************calling methods throw based on the choice ***************************************
        switch(choice){
            case 1:
                sa.bubbleSort(array);  //it invoke bubbleSort() method
                break;
            case 2:
                sa.selectionSort(array); //it invoke selectionSort() method 
                break;
            case 3:
                sa.insertionSort(array);  //it invoke insertionSort() method
                break;
           /* case 4:
                sa.quickSort(array);      //it invoke quickSort() method 
                break;
            case 5:
                sa.mergeSort(array);      //it invoke mergeSort() method
                break;  */
            default:
                System.out.println("you haven't selected any sorting algo ");
                break;
        }
        //print sorted array
        System.out.print("\n array after sort: ");
        for(int i=0;i<size;i++)
        {
            System.out.print(array[i]+" ");
        }
    }
}
