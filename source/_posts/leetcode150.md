title: LeetCode面试150题
date: 2023-4-29 23:44
tags:
- 算法
- 研究生
---



# LeetCode面试150题

## 88.合并两个有序数组

```c++
class Solution {
public:
    void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
        int i = m-1,j = n-1;
        for(int k = nums1.size()-1; k >= 0;k --){
            if(i>=0 && j>=0){
                if(nums1[i] >= nums2[j]){
                    nums1[k] = nums1[i];
                    i--;
                }else{
                    nums1[k] = nums2[j];
                    j--;
                }
            }else if(i>=0){
                nums1[k] = nums1[i];
                i--;
            }else{
                nums1[k] = nums2[j];
                j--;
            }

        }
           

    }
};

//解法：从后往前依次合并
```

## 27.移除元素

```c++
class Solution {
public:
    int removeElement(vector<int>& nums, int val) {
        int p = 0;
        for(int i = 0;i < nums.size(); i++){
            if(nums[i] != val){
                nums[p++] =nums[i]; 
            }
        }
        return p;
    }
};

//解法：双指针
```



## 26. 删除有序数组中的重复项

```c++
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if(nums.size() ==0 ) return 0;
        int p = 0, q = 1;
        while(q < nums.size()) {
            if(nums[p] != nums[q] ){
                nums[p+1] = nums[q];
                p++;
            }
            q++;
        }
        return p + 1;
    }
};

// 解法：双指针
```

## 80.删除有序数组的重复项

```c++
class Solution {
public:

    int removeDuplicates(vector<int>& nums) {
        if(nums.size() == 1 || nums.size() == 0) return nums.size();
        int p = 2, q = 2;
        while( p < nums.size()){
            if(nums[p] != nums[q-2]){
                nums[q] = nums[p];
                q++;
            }
            p++;
        }
        return q;
    }
};

//双指针
```

## 189.轮转数组

```c++
class Solution {
public:
    void reverse(vector<int>& nums,int i, int j){
        for(int k = i; k< (j + i)/2+1; k++){
            int temp = nums[k];
            nums[k] = nums[j-k+i];
            nums[j-k+i] = temp;
        }
    }

    void rotate(vector<int>& nums, int k) {
        k = k%nums.size();
        if(nums.size() == 1 || nums.size() ==0 || k==0) return ;
        reverse(nums,0,nums.size() - 1);
        reverse(nums,0,k-1);
        reverse(nums,k,nums.size()-1);
    }
};

//数组翻转
```

## 121.买卖股票的最佳时机

```c++
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int n = prices.size(),minprice = prices[0];
        vector<int> dp(n, 0);
        for(int i = 1;i < n; i++){
            minprice = min(minprice, prices[i]);
            dp[i] = max(dp[i - 1], prices[i] - minprice);
        }
        return dp[n-1];
    }
};

//解法： 一维动态规划
```

## 122.买卖股票的最佳时机~贰

```c++
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int n = prices.size();
        vector<int> dp(n, 0);
        for(int i = 1; i < n; i ++){
            // dp[i][0] 为第i天最大利润 ，
        }
    }
};
```

abitur orci libero, mollis sed semper vitae, adipiscing in lectus. Aenean non egestas odio. Donec sollicitudin nisi quis lorem gravida, in pharetra mauris fringilla. Duis sit amet faucibus dolor, id aliquam neque. In egestas, odio gravida tempor dictum, mauris felis faucibus purus, sit amet commodo lacus diam vitae est. Ut ut quam eget massa semper sodales. Aenean non ipsum cursus, blandit lectus in, ornare odio. Curabitur ultrices porttitor vulputate.