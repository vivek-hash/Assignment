# Assignment
#pairSum

import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Scanner;

public class PairSumExisted {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int num =input.nextInt();
        int targetSum =input.nextInt();
        int arr[] = new int[num];

        for(int i=0;i<num;i++)
        {

            arr[i]=input.nextInt();
        }
        HashSet<Integer> set = new HashSet<>();
        int count=0;
        for(int i=0;i<num;i++)
        {
            int delta =targetSum -arr[i] ;

            if(set.contains(delta))
            {
                System.out.println("1 ");
                count++;
                break;
            }
            else
                set.add(arr[i]);
        }
        if(count == 0)
        System.out.println("0 ");
    }

}
