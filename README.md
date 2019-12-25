# LeetCode question number 15.
import java.util.ArrayList;
import java.util.List;

public class Solutio15 {

	public static List<List<Integer>> threeSum(int[] nums) {

		List<List<Integer>> outlist= new ArrayList<List<Integer>>();

		for (int i = 0; i<nums.length; i++) {

			for ( int j =i+1 ; j<nums.length; j++) {

				for ( int k =j+1; k<nums.length; k++) {

					List<Integer> inlist= new ArrayList<Integer>();

					if (nums[i]+nums[j]+nums[k]==0) {
						inlist.add(nums[i]);
						inlist.add(nums[j]);
						inlist.add(nums[k]);
						outlist.add(inlist);		
					}		
				}	
			}	
		}


		return outlist;

	}

	public static void main(String[] args) {

		int [] nums = {-1, 0, 1, 2, -1, -4};
		System.out.println(threeSum(nums));

	}

}
