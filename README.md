# BinarySearch
package DS;

package DS;

public class DescendingOrderBinarySearch {

	public static void main(String[] args) {
		int[] array= {1,10,11,12,13,14,15};
		int target=11;
		System.out.println(binarySearch1(array,target));

	}
	static int binarySearch1(int[] array, int target) {
		if(array[0]>array[array.length-1]) {
		int startIndex=0;//1
		int endIndex=array.length-1;//5
		while(startIndex<=endIndex) {
			int middleElementIndex=startIndex+(endIndex-startIndex)/2;
			if(target>array[middleElementIndex]) {
				endIndex=middleElementIndex-1;
			}
			else if(target<array[middleElementIndex]) {//4<5
				startIndex=middleElementIndex+1;
			}
			else {
				return middleElementIndex;
			}
		}
		return -1;
	}
		else if(array[0]>array[array.length-1]){
			int startIndex=0;//1
			int endIndex=array.length-1;//5
			while(startIndex<=endIndex) {
				int middleElementIndex=startIndex+(endIndex-startIndex)/2;
				if(target>array[middleElementIndex]) {
					startIndex=middleElementIndex+1;
					
				}
				else if(target<array[middleElementIndex]) {//4<5
					endIndex=middleElementIndex-1;
				}
				else {
					return middleElementIndex;
				}
			}
			return -1;
		}
		else {
			return -1;
		}
		}
}
