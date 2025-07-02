## Problems Solved
- Largest Element in an Array
- Second Largest Element in an Array without Sorting
- Check if Array is Sorted
- Remove Duplicates from Sorted Array
- Left Rotate Array by one place
- Left Rotate Array by D place
- Move Zeros to End


### Rotate by K Elements

```cpp
class Solution {
public:
    void rotate(vector<int>& nums, int k) {
        int n=nums.size();
        if(n==1) return;
        k = k % n;
     
        vector<int> temp;

        for(int i=n-k;i<n;i++){
            temp.push_back(nums[i]);
        }

        for(int i=n-k-1;i>=0;i--){
            nums[i+k] = nums[i];
        }

        for(int i=0;i<k;i++){
            nums[i] = temp[i];
        }
    }    
};
```

### Move Zeros

```cpp
class Solution {
public:
    void moveZeroes(vector<int>& nums) {

        vector<int> temp;

        for(int i=0;i<nums.size();i++) {
            if(nums[i] != 0)
            {
                 temp.push_back(nums[i]);
            }
        }

        int nz=temp.size();
        for(int i=0;i<nz;i++){
            nums[i] = temp[i];
        }

        for(int i=nz;i<nums.size();i++){
            nums[i] = 0;
        }

        for(int i=0;i<nums.size();i++){
           cout<<nums[i]<<",";
        }
    }
};
```
```
