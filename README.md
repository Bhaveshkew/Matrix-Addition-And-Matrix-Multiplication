# Matrix-Addition-And-Matrix-Multiplication

//CODE FOR MATRIX ADDITION

import java.util.Scanner;

public class MatrixAddition {
public static void main(String[] args) {
	int r1,r2,c1,c2,i,j;
	Scanner n=new Scanner(System.in);
	System.out.println("Enter the number of rows and columns for first matrix :");
	r1=n.nextInt();
	c1=n.nextInt();
	System.out.println("Enter the number of rows and columns for second matrix :");
	r2=n.nextInt();
	c2=n.nextInt();
	int arr1[][]=new int[r1][c1];
	int arr2[][]=new int[r2][c2];
	if(r1==r2&&c1==c2) {
		int sum[][]=new int[r1][c1];
		System.out.println("Enter the elements of first matix :");
		for(i=0;i<r1;i++) {
			for(j=0;j<c1;j++) {
				arr1[i][j]=n.nextInt();
			}
		}
		System.out.println("Enter the elements for second matrix :");
		for(i=0;i<r1;i++) {
			for(j=0;j<c1;j++) {
				arr2[i][j]=n.nextInt();
			}
		}
		for(i=0;i<r1;i++) {
			for(j=0;j<c1;j++) {
				sum[i][j]=arr1[i][j]+arr2[i][j];
			}
		}
		System.out.println("Sum of two matrices is :");
		for(i=0;i<r1;i++) {
			for(j=0;j<c1;j++) {
				System.out.print(+sum[i][j]+" ");
			}
			System.out.println();
		}
	}
	else {
		System.out.println("Sum cannot be found as number of rows and columns of two matrices are different");
	}
	
}
}




//CODE FOR MATRIX MULTIPLICATION



import java.util.Scanner;

public class MatixMultiplication {
public static void main(String[] args) {
	Scanner n1=new Scanner(System.in);
	int r3,r4,c3,c4,i,j,k;
	System.out.println("Enter number of rows and columns of first matrix :");
	r3=n1.nextInt();
	c3=n1.nextInt();
	System.out.println("Enter number of rows and columns of second matrix :");
	r4=n1.nextInt();
	c4=n1.nextInt();
	if(c3==r4) {
		int arr3[][]=new int[r3][c3];
		int arr4[][]=new int[r4][c4];
		int product[][]=new int[r3][c4];
		System.out.println("Enter the elements of first matrix :");
		for(i=0;i<r3;i++) {
			for(j=0;j<c3;j++) {
				arr3[i][j]=n1.nextInt();
			}
		}
		System.out.println("Enter the elements of second matrix :");
		for(i=0;i<r4;i++) {
			for(j=0;j<c4;j++) {
				arr4[i][j]=n1.nextInt();
			}
		}
		for(i=0;i<r3;i++) {
			for(j=0;j<c4;j++) {
				for(k=0;k<r4;k++) {
					product[i][j]=arr3[i][k]*arr4[k][j];
				}
			}
		}
		System.out.println("Product of two matrices are :");
		for(i=0;i<r3;i++) {
			for(j=0;j<c4;j++) {
				System.out.print(+product[i][j]+" ");
			}
			System.out.println();
		}
	}
	else {
		System.out.println("Product of two matrices cannot be found");
	}
}
}
