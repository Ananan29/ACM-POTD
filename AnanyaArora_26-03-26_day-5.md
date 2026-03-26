// Sliding Window Maximum

class Solution {
public:
    vector<int> maxSlidingWindow(vector<int>& nums, int k) {
        k--;
        deque<int> d;
        vector<int> v(nums.size()-k);
        d.push_back(0);
        for(int i=1;i<k;i++){
                while(!d.empty()&&nums[i]>nums[d.back()])d.pop_back();
                d.push_back(i);
        }
        for(int i=k;i<nums.size();i++){
            while(!d.empty()&& nums[i]>=nums[d.back()]){
                d.pop_back();
            }
            d.push_back(i);
            while(d.front()<i-k)d.pop_front();
            v[i-k]=nums[d.front()];
        }
        return v;
    }
};

<img width="1460" height="687" alt="day 5" src="https://github.com/user-attachments/assets/3fa98a7d-cbe3-42fe-8afb-f653565dc949" />
