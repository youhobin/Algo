### Day 12

---

#### 70. Climbing Stairs `java`

```java
class Solution {
    public int climbStairs(int n) {
        if(n==1) return 1;
        if(n==2) return 2;

        int[] a =  new int[n];
        a[0]=1;
        a[1]=2;

        for(int i=2;i<n;i++){
            a[i]=a[i-1]+a[i-2];
        }
        return a[n-1];
    }
}
```

---


#### 120. Triangle

```java
class Solution {
    public int minimumTotal(List<List<Integer>> triangle) {
        for(int i=triangle.size()-2;i>=0;i--){
            for(int j=0;j<triangle.get(i).size();j++){
                int min=Math.min(triangle.get(i+1).get(j),triangle.get(i+1).get(j+1));
                int sum=min+triangle.get(i).get(j);
                triangle.get(i).set(j,sum);
            }
        }
        return triangle.get(0).get(0);
    }
}
```

---

#### 198. House Robber

```java
class Solution {
    public int rob(int[] nums) {
        int n = nums.length;

        if (n == 0) return 0;
        if (n == 1) return nums[0];
        if (n == 2) return nums[1];

        int[] dp = new int[n];

        dp[0] = nums[0];
        dp[1] = nums[1];


        for(int i = 2; i < n; i++) {
            dp[i] = Math.max(nums[i] + dp[i - 2], dp[i - 1]);
        }

        return dp[n-1];
    }
}
```
