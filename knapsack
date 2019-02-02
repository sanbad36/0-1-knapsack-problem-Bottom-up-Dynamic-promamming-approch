
/*	Author- sanket Badjate.
	0/1 knapsack---(By Dynamic programming - Bottom up approch)
	In  0/1 knapsack we are not suppose to take the frackion of the element .
	There are two possibities --Either to take the object fully or not to take it.
	The time complexity is O(size*capacity)
*/

#include<iostream>
#include<stdio.h>
#include<stdlib.h>
using namespace std;

int findmax(int a,int b){  //to find the max between two

	return (a>b)?a:b;
}

int calArraylength(int wt[],int profit[]){	//calculate the size of array
	
	int size_wt=sizeof(wt)/sizeof(wt[0]);
	int size_profit=sizeof(profit)/sizeof(profit[0]);

		if(size_wt==size_profit)
					return size_profit+1;
			
		else {
					cout<<"Both the array has different count of element\n";
					exit(1);
		}		

}

int knapsack(int wt[],int profit[],int capacity,int n){   // Bottom up approch

	int T[n][capacity];	// forming the table only for the unique subproblems (funtion_calls) .

		 for (int i = 0;i <=n; i++) 
   { 
       for (int j=0; j <=capacity;j++) 
       { 
           if (i==0 || j==0) 
               T[i][j] = 0; 
           else if (wt[i-1] <= j) 
                 T[i][j] = findmax(profit[i-1]+T [i-1] [j-wt[i-1]], T[i-1][j]); 
           else
                 T[i][j] = T[i-1][j]; 
       } 
   } 
  
   return T [n][capacity]; //returning the last value of the table which is the total profit
} 

int main(){
	int Total_profit=0;
	int wt[]={1,2,4}; 
	int profit[]={10,12,28};
	int capacity=6;
	int size=calArraylength(wt,profit);
	Total_profit=knapsack(wt,profit,capacity,size);
	cout<<"Total_profit in the knapsack is : "<<Total_profit<<endl;
}
