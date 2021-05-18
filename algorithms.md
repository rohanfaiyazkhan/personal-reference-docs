# Algorithms

## N-Ary tree get max depth

Given a N-Ary (non-binary) tree sometimes we need to find the maximum depth of the tree.

The recursive approach is:
1. Check current children. If no children return 0.
2. Set depth to 0. Loop through children and calculate their depth. If new depth is greater than previous depth, set depth to new depth.
3. Return depth + 1

```

	function getMaxDepth(tree){

		const children = tree.children

    		if (!children?.length) {
    		    return 0;
    		}

    		let depthTree = 0;
    		for (const child of children) {
    		    if (!!child?.children?.length) {
    		        depthTree = Math.max(depthTree, getMaxDepth(child.children));
    		    }
    		}

    		return depthTree + 1;
	}
	
```