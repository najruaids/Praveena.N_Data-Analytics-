class Solution(object):
    def isPalindrome(self, x):
        a=x
        rev=0
        while(a>0):
            mod=a%10
            rev=(rev*10)+mod
            a//=10
        if(rev==x):
            return True
        
        return False