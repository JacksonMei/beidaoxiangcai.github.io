DFS template

```c++
    bool findTarget(TreeNode* root) {
        stack<TreeNode*> stack;
        
        stack.emplace(root); // root could be null
        while(!stack.empty()) {
            auto node = stack.top();
            stack.pop();
                        
            if (node) {
                stack.emplace(node->left);
                stack.emplace(node->right);
            }
        }
        
        return false;
    }
```

+ 变种1 【leetcode653】， 当为BST时，找两个节点值的和为指定K值时， 通过边dfs边记录节点值的方式，实现O(n) 找到两个目标节点