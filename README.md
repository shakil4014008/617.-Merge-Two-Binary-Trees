# 617.-Merge-Two-Binary-Trees

```c#
public class Solution {
    public TreeNode MergeTrees(TreeNode t1, TreeNode t2) {
       
        if(t1 == null){
            return t2;
        }
        if(t2 == null){
            return t1;
        }
        
        TreeNode t = new TreeNode(t1.val + t2.val);
        t.left = MergeTrees(t1.left, t2.left);
        t.right = MergeTrees(t1.right, t2.right);
        
        return t;       
        
    }
}

```
