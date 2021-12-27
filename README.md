# selection-sort

package com.company;

import java.util.Arrays;
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        int a = input.nextInt();
        int[] arr = new int[a];
        for (int i=0;i<a;i++){
            arr[i] = input.nextInt();
        }
        System.out.println(Arrays.toString(arr));
    //    int[] arr = {2,4,3,1};
        selection(arr);
        System.out.println(Arrays.toString(arr));
    }
    public static void selection(int[] arr){
        for(int i = 0;i<arr.length;i++){
            int last = arr.length -i -1;
            int maxIndex = max(arr,0,last);
            swap(arr,maxIndex,last);

        }
    }
    public static  void swap(int[] arr,int first,int sec){
        int temp = arr[first];
        arr[first] = arr[sec];
        arr[sec] = temp;
    }
    public static int max(int[] arr,int start,int end){
        int max = 0;
        for(int i=start;i<=end;i++) {
            if (arr[max] < arr[i]){
                max = i;
            }
        }
        return max;
    }
}
