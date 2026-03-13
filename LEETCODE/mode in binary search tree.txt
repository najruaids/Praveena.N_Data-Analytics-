class Solution:
    def __init__(self):
        self.mod = []
        self.currVal = None
        self.currCount = 0
        self.maxCount = 0

    def inorder(self, root):
        if not root:
            return
        self.inorder(root.left)
        if self.currVal != root.val:
            self.currVal = root.val
            self.currCount = 0
        self.currCount += 1
        if self.currCount == self.maxCount:
            self.mod.append(self.currVal)
        if self.currCount > self.maxCount:
            self.mod = [self.currVal]
            self.maxCount = self.currCount
        self.inorder(root.right)

    def findMode(self, root):
        self.currVal = float('-inf')
        self.inorder(root)
        return self.mod