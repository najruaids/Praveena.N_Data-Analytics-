class Solution(object):
    def findCenter(self, edges):
        degree = {}
        for i in edges:
            for j in i:
                if j not in degree:
                    degree[j] = 1
                else:
                    degree[j] += 1
        return  max(degree, key=degree.get)