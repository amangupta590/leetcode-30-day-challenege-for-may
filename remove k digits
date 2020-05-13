class Solution {
public:
    string removeKdigits(string num, int k) {
        int n = num.length();
        
        if(n <= k)
            return "0";
        if(k == 0)
            return num;
        
        while(k > 0)
        {
            int flag = 0;
            for(int i = 0; i < num.length() - 1; i++)
            {
                if(num[i] > num[i + 1])
                {
                    num.erase(num.begin() + i);
                    flag = 1;
                    break;
                }
            }
            
            if(flag == 0)
                num.pop_back();
            
            while(num.size() > 0 && num[0] == '0')     
                num.erase(0, 1);
            
            k--;
        }
        
        if(num.size() == 0)
            return "0";
        return num;
    }
};
