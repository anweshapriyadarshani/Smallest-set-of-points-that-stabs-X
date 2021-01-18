# Smallest-set-of-points-that-stabs-X
Let X be a set of n intervals on the real line. We say that a set of points P "stabs" X if every interval in X contains at least one point in P. Compute the smallest set of points that stabs X.  For example, given the intervals [(1, 4), (4, 5), (7, 9), (9, 12)], you should return [4, 9].  _____________________

from itertools import combinations
def get_points(intervals);
points=set([element for pair in intervals for element in pair])
subsets=[]
for size in range(1, len(points)):
subsets.extend(list(combinations(points, size)))
for start, end in intervals)):
for subset in subsets:
if all(any(start<= point <=end for point in subset)
for start, end in intervals):
return subset
def get_points(intervals);
intervals.sort(key=lambda x: (x[1], x[0]))
points=[]
latest_endpoint=none
for start, end in intervals:
if start <= latest_endpoint:
continue
else:
points.append(end)
latest_endpoint=end
return points
