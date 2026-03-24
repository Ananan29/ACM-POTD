75. Sort Colors

class Solution {
public:
    void sortColors(vector<int>& nums) {
        int z=-1,o=-1,t=nums.size();
        while(o<t-1&&o<int(nums.size())){
            o++;
            if(nums[o]==0){
                z++;
                if(z<o){
                    nums[z]=0;
                    nums[o]=1;
                }
            }else if(nums[o]==2){
                t--;
                int x=nums[t];
                nums[t]=nums[o];
                nums[o]=x;
                o--;
            }
        }
    }
};

<img width="1443" height="651" alt="day 3" src="https://github.com/user-attachments/assets/cb39bf4d-6340-49a5-af28-8167f617d578" />
