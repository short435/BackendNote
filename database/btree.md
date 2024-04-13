# B-Tree and B+Tree

Auto Scaling structure

## Let's talk about How we need BTree

### Disk
- Tracks/Sectors/Blocks

### Main Memory
- Ram
- Which Directly use by program
    
        
## M-way search tree

### What's M-way search tree

Advance strucutre of the binary tree.

M-way tree cloud could have ```M``` children under each node, instead of the binary tree only have 2 children under each node.

M-way tree have ```M``` children under the node and ```M-1``` key in the node.

#### Structure for the M-way tree

**Example**
- 4-way search tree
  - Members
    - Child ptr (cp)
    - Memory ptr (mp)
    - Key (ky)
      - ```cp ky mp cp ky mp cp ky mp cp```


#### Cons

Without the guideline. If construct the M-way tree in the wrong way. It would take almost the same time-complex as linear search.

## B-tree

- Define the rules!
  - [m/2] children
  - Root can have min 2 children
  - All leaf at same level
  - Creation way >> **Bottom up** 

## B+tree

- How’s B+Tree
  - Multiple level indexing
  - Key are only saving in leaf
  - Leaf would connect as linked-list

<!-- 
- Advance from these structure
    - Binary Search Tree
        - 1 Key 2 childeren
            - Multiple key more than 2 children in each node and
                - Example
                    - 2keys would get 3 children > 3 way search tree
            - M-way search tree M-1 keys
            - Memory structure
                - 4-way search tree
                    - Members
                        - Child ptr (cp)
                        - Memory ptr (mp)
                        - Key (ky)
                    - cp ky mp cp ky mp cp ky mp cp
            - Cons
                - 缺乏使用gulidline，建制方式錯誤，與M數選擇不好的話有可能會使得搜尋時間和linear search不相上下
        - Improve from m-way search tree
            - Define the rules!
                - [m/2] children
                - Root can have min 2 children
                - All leaf at same level
                - Creation way >> Bottom up 
        - How’s B+Tree
            - Multiple level indexing
            - Key are only saving in leaf
            - Leaf would connect as linked-list -->

## Reference

- [Youtube Course](https://www.youtube.com/watch?v=aZjYr87r1b8&ab_channel=AbdulBari)