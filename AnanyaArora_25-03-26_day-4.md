// 167. Two Sum II - Input Array Is Sorted

class Solution {
public:
    vector<int> twoSum(vector<int>& numbers, int target) {
        int i=0,j=numbers.size()-1;
        while(i<j){
            if(numbers[i]+numbers[j]>target)j--;
            else if(numbers[i]+numbers[j]<target)i++;
            else return {i+1,j+1};
        }
        return {-1,-1};
    }
};

<img width="1444" height="646" alt="day 4" src="https://github.com/user-attachments/assets/25a29912-592e-4211-9f3d-666209786524" />
