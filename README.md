# Set-Intersection-Size-at-Least-Two


n efficient Python solution to the "Set Intersection Size at Least Two" problem using a greedy algorithm approach.

## Problem Statement

Given a list of intervals `[a, b]`, find the size of the smallest set `S` such that for every interval in the list, the intersection of `S` with the interval has at least two elements.

## Solution Approach

### Key Insights
- **Greedy Algorithm**: Selects elements in a way that maximizes future overlaps
- **Optimal Sorting**: Intervals are sorted by end points to enable efficient processing
- **Minimal Set Construction**: Maintains only necessary elements to satisfy intersection conditions

### Algorithm
1. Sort intervals by end point (ascending), then by start point (descending)
2. Initialize an empty result set
3. For each interval:
   - If no overlap with current set, add two largest elements from interval
   - If one overlap, add largest element from interval
   - If two overlaps, do nothing

### Complexity
- **Time Complexity**: O(n log n) due to sorting
- **Space Complexity**: O(n) for storing the result set
