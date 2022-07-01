# myleetcode
##88. 合并两个有序数组  
先合并再排序    
class Solution {  
&ensp; &ensp; public void merge(int[] nums1, int m, int[] nums2, int n) {  
&ensp; &ensp; &ensp; &ensp; //合并nums2到nums1  
&ensp; &ensp; &ensp; &ensp; //nums1排序  
&ensp; &ensp; &ensp; &ensp; System.arraycopy(nums2,0,nums1,m,n);  
&ensp; &ensp; &ensp; &ensp; Arrays.sort(nums1);  
&ensp; &ensp; }  
}  


##169. 多数元素  
class Solution {  
&ensp; &ensp;public int majorityElement(int[] nums) {  
&ensp; &ensp; &ensp; &ensp;//遍历每个元素，记录个数  
&ensp; &ensp; &ensp; &ensp;//找出元素个数大于n/2的元素   
&ensp; &ensp; &ensp; &ensp;Map<Integer, Integer> countNum = new HashMap<>();  
&ensp; &ensp; &ensp; &ensp;for(int i:nums){  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp;if (countNum.containsKey(i)) {  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp;int v=  countNum.get(i)+1;  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp;countNum.put(i,v);  
&ensp; &ensp; &ensp; &ensp;}else {  
&ensp; &ensp; &ensp; &ensp;&ensp;&ensp;countNum.put(i,1);  
&ensp; &ensp; &ensp; &ensp;}  
&ensp; &ensp;}  
&ensp; &ensp;&ensp;&ensp;for(Map.Entry entry:countNum.entrySet()) {  
&ensp; &ensp;&ensp;&ensp;&ensp;&ensp;&ensp;if((int)entry.getValue()>nums.length/2){  
&ensp; &ensp;&ensp;&ensp;&ensp;&ensp;&ensp;return (int)entry.getKey();  
&ensp; &ensp;&ensp;&ensp;&ensp;&ensp;&ensp;}  
&ensp; &ensp;&ensp;}  
&ensp; &ensp;&ensp;&ensp;return 0;  
&ensp;}   
}
