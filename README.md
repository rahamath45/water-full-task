## Water Tank Problem — Interactive Visualization

This project is a simple HTML + CSS + JavaScript visualization tool that demonstrates how the Trapping Rain Water problem works.
It not only calculates the total trapped water but also renders an SVG visualization of buildings (bars) and the water stored between them.

### 🚀 Features

Input any array of heights (e.g., 0,4,0,0,6,0,6,4,0)
Uses Two-Pointer Algorithm to compute:

Total trapped water

Water trapped at each index

Renders an SVG-based visual representation

Yellow bars → building heights

Blue bars → trapped water

#### Example button to auto-load sample input
Clean UI + responsive rendering
Imagine each number in the array represents the height of a block. Water can be trapped only if:
There is a taller block on the left, and
There is a taller block on the right

For each index i, the trapped water is:

min(maxLeft, maxRight) - height[i]


But instead of using extra arrays, we use an optimized two-pointer approach.

##### Two-Pointer Algorithm (Used Here)

We use two pointers:

left starting at index 0

right starting at last index

We maintain:

leftMax → highest block seen so far from the left

rightMax → highest block seen so far from the right

#### Algorithm Logic
If heights[left] <= heights[right]:
    If heights[left] >= leftMax → update leftMax  
    Else → water at left = leftMax - heights[left]
    Move left++
Else:
    If heights[right] >= rightMax → update rightMax  
    Else → water at right = rightMax - heights[right]
    Move right--


This gives us:
Total trapped water

Water stored at every index

### Visualization (SVG Rendering)

The SVG canvas draws:

1. Blocks
Yellow rectangles based on height values.

2. Water
Blue rectangles placed above the blocks based on trapped water units.

3. Height Labels
Small numbers under each column for clarity.

4. Grid Lines
Light grey horizontal lines to make the height difference visually easier.

regrads,
S.rahamathunissa
Email:rahmathsulaiman45@gmail.com