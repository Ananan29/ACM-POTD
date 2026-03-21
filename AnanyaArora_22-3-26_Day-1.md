<img width="1452" height="648" alt="Screenshot 2026-03-22 at 3 42 48 AM" src="https://github.com/user-attachments/assets/756d9353-6736-453c-9faf-d89d7a68488f" />class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int j=0;
        for(int i=1;i<nums.size();i++){
            if(nums[i]!=nums[i-1]){
                j++;
                nums[j]=nums[i];
            }
        }
        return j+1;
    }
};

