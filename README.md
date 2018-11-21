# COMS 311 PA2 WGraph & ImageProcessor
For my Computer Science 311 Programming Assignment 2 I was tasked with completing two classes: WGraph and ImageProcessor. The main goal of this assignment was to implement different variations of the shortest path problem for graphs. I chose to use Dijkstra's.

## WGraph
![wgraph](https://user-images.githubusercontent.com/40704571/48816945-ca572f00-ed09-11e8-87f8-dfa43b191fda.PNG)

The goal of this class is to take as input a string, containing the filename from which to pull information from. This information is what will be used to build a directed graph. After building the graph the goal is to implement 3 variations of the shortest path problem: V2V, V2S, & S2S.
- V2V:

![wgraphv2v](https://user-images.githubusercontent.com/40704571/48817349-ad236000-ed0b-11e8-94a2-d21a9e430bce.PNG)

- V2S:

![wgraphv2s](https://user-images.githubusercontent.com/40704571/48817476-45214980-ed0c-11e8-8073-368373534dee.PNG)

- S2S:

![wgraphs2s](https://user-images.githubusercontent.com/40704571/48817531-7d288c80-ed0c-11e8-92f9-39789fe2a53d.PNG)

## ImageProcessor
![imageprocessor](https://user-images.githubusercontent.com/40704571/48817009-14d8ab80-ed0a-11e8-975d-7a1e361406b0.PNG)
The goal of this class is to take as input a string, containing the filename from which to pull information from. This information is what will be used to build an image of pixels, containg the RGB values. After building the image the goal is to be able to reduce the image width by a value of k (such that W-k > 1). When reducing the image width by 1 just removing vertical line of pixels won't do. So in order to know which pixels to remove we must calculate the importance for every given pixel in the image. From this point starting at the top row (0th row) we will use the importance values to calcuate the shortest path from the top row to the last row. Once we have calculated the shortest path from top to bottom we must remove these pixels, reorder the pixels and repeat. We do this until we have done it k times. After the last interation we will write the end value to a file. In order to two this I must implement two methods: getImportance & writeReduced.
- getImportance: Calculates the importance for every pixel by following these steps.
