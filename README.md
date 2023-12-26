# BinarySearch
package DS;

public class BinarySearch1 {

	public static void main(String[] args) {
		int[] arr= {2,4,6,9,11,12,14,36,48};
		int target=36;
		System.out.println(binarySearchAlgorithm(arr, target));
		
	}
	static int binarySearchAlgorithm(int[] array,int target) {
		int startIndex=0;
		int endIndex=array.length-1;
		while(startIndex<endIndex) {
			int middleElementIndex=(startIndex+endIndex)/2;
			if(target>array[middleElementIndex]) {
				startIndex=middleElementIndex+1;
				
			}
			else if(target==array[middleElementIndex]) {
				return middleElementIndex ;
			}
			else {
				endIndex=middleElementIndex-1;
			}
			
		}
		return -1;
	}

}
