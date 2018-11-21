# COMS 311 PA2 WGraph & ImageProcessor
For my Computer Science 311 Programming Assignment 2 I was tasked with completing two classes: WGraph and ImageProcessor. The main goal of this assignment was to implement different variations of the shortest path problem for graphs. I chose to use Dijkstra's.

## WGraph
![wgraph](https://user-images.githubusercontent.com/40704571/48816945-ca572f00-ed09-11e8-87f8-dfa43b191fda.PNG)
As the requirements state the goal of this class is to take as input a string, containing the filename from which to pull information from. This information is what will be used to build a directed graph. After building the graph the goal is to implement 3 variations of the shortest path problem: V2V, V2S, & S2S.
- V2V: takes as input ux, uy, vx, & vy. Finds the shortest path from the vertex at (ux, uy) to -(vx, vy). The output will be an array list of integers w/the index 0 = ux, 1 = uy, 2 = next x coordinate in the path, 3 = next y coordinate in the path. Up until you reach vx and vy.
- V2S: takes as input ux, uy, & S (a set of vertices). Finds the shortest path from vertex at (ux, uy) to ALL vertices inside the set S. The output will be the array list of the shortest path from vertex (ux, uy) to a vertex in set S.
- S2S: takes as input S1 & S2. Finds the shortest path between all vertices in S1 to all vertices in S2. And returns whichever path is the shortest.

## ImageProcessor
![imageprocessor](https://user-images.githubusercontent.com/40704571/48817009-14d8ab80-ed0a-11e8-975d-7a1e361406b0.PNG)

As the requirements state the goal of this class is to take as input a string, containing the filenam from which to pull information from. This information is what will be used to build an image of pixels, containg the RGB values. After building the image the goal is to be able to reduce the image width by a value of k (such that W-k > 1). When reducing the image width by 1 just removing vertical line of pixels won't do. So in order to know which pixels to remove we must calculate the importance for every given pixel in the image. From this point starting at the top row (0th row) we will use the importance values to calcuate the shortest path from the top row to the last row.
