# Container-With-Most-Water
leetcode incomplete code

class Solution {
public:
    int maxArea(vector<int>& height) {
         int j,i;
    i=0;
    int maxi = INT_MIN;
    j=height.size()-1;
    
    while(i<j)
    {
       int area;
        if(height[i] < height[j])
        {
            area = (j-i) * height[i];
            if(area>maxi)
                maxi=area;
            else
                i++;
        }
        
        else{
            
            area = (j-i) * height[j];
            if(area>maxi)
                maxi=area;
            else
                j--;
        }
        
    
    }
    
    return maxi;
}
};
