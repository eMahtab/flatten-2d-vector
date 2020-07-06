# Flatten 2d vector
## https://leetcode.com/problems/flatten-2d-vector

# Implementation :
```java
class Vector2D {
    List<Integer> nums;
    int pos;
    
    public Vector2D(int[][] v) {
        nums = new ArrayList<Integer>();
        for(int[] arr : v) {
            for(int i : arr) {
                nums.add(i);
            }
        }
    }
    
    public int next() {
        int num = nums.get(pos);
        pos++;
        return num;
    }
    
    public boolean hasNext() {
        if(pos < nums.size())
            return true;
        return false;    
    }
}

/**
 * Your Vector2D object will be instantiated and called as such:
 * Vector2D obj = new Vector2D(v);
 * int param_1 = obj.next();
 * boolean param_2 = obj.hasNext();
 */
```
