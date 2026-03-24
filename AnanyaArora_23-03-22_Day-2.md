// 560. Subarray Sum Equals K

class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        unordered_map<int,int> m;
        int res=0,s=0;
        for(int i:nums){
            s+=i;
            if(m.find(s-k)!=m.end())res+=m.find(s-k)->second;
            m[s]++;
            if(s==k)res++;
        }
        return res;
    }
};
<img width="1446" height="651" alt="Screenshot 2026-03-24 at 3 51 03 PM" src="https://github.com/user-attachments/assets/193cbd02-b75d-40d0-acf7-8a5bd279a058" />
