# myleetcode
88. 合并两个有序数组  
先合并再排序    
class Solution {  
&ensp; &ensp; public void merge(int[] nums1, int m, int[] nums2, int n) {  
&ensp; &ensp; &ensp; &ensp; //合并nums2到nums1  
&ensp; &ensp; &ensp; &ensp; //nums1排序  
&ensp; &ensp; &ensp; &ensp; System.arraycopy(nums2,0,nums1,m,n);  
&ensp; &ensp; &ensp; &ensp; Arrays.sort(nums1);  
&ensp; &ensp; }  
}  
