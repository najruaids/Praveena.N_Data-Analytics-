class Solution(object):
    def isUgly(self, n):
        for i in [2,3,5]:
            while(n>1):
                 if n%i==0:
                    n=n//i
                 else:
                    break
        if n==1:
            return True
        return False
                
        