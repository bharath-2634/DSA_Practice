Template for lowerBound:
public static int lowerBound(int[] nums,int target) {
        int left=0,right=nums.length;

  while(left<right) {
            int mid = left+(right-left)/2;
            if(nums[mid]>=target) right = mid;
            else left = mid+1;
        }

  return left;
  }

  Note: 
  nums[0->right] = numbers < target
  nums[left->n-1] = numbers >= target

  Template for upperBound:
  public static int upperBound(int[] nums,int target) {
        int left=0,right=nums.length;

  while(left<right) {
            int mid = left+(right-left)/2;
            if(nums[mid]>target) right = mid;
            else left = mid+1;
  }

  return left;
  }

  Note:
  arr[0 ... right] <= target
  arr[left ... n-1] > target
