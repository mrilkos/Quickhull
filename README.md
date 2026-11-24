# QuickHull
 
An interactive presentation on **QuickHull**, a divide-and-conquer algorithm that computes the convex hull of a set of points.
 
**Live demo:** https://mrilkos.github.io/Quickhull/
 
Made at ENSA Khouribga (Advanced Algorithmics) by Abderrahmane Khayakkoute, Ilyas El Houari and Mossabe Zerradi, supervised by Pr. Ennaji.
 
## The algorithm
 
The convex hull is the smallest convex polygon containing all the points, like a rubber band stretched around nails on a board.
 
1. Take the leftmost point A and the rightmost point B. Both are on the hull. The line AB splits the points into an upper and a lower set.
2. On one side, find the point C farthest from AB. It is also on the hull.
3. Discard every point inside the triangle ABC, since none of them can be on the hull.
4. Repeat on the edges AC and CB with the points left outside.
5. When an edge has no points outside it, it is a hull edge.
6. Do the same for the other side and join the hull points in order.
| Case | Complexity |
| --- | --- |
| Average | O(n log n) |
| Worst | O(n²) |
 
The worst case happens when the farthest point splits the set very unevenly at every step, the same weakness as quicksort with a bad pivot.
 
## What's inside
 
| File | Description |
| --- | --- |
| `index.html` | Main slideshow (18 slides) with draggable 3D models, a goat-and-rope example and a race between algorithms |
| `quickhull_pas_a_pas.html` | Step-by-step walkthrough of the algorithm (French) |
| `quickhull_step_by_step_visualizer.html` | Step-by-step visualizer, also embedded in the slideshow |
| `hull_runner.html` | Small interactive hull demo |
| `img/`, `media/`, `js/` | Images, closing video and a local copy of three.js |
 
## Run locally
 
No build step and no dependencies to install.
 
```bash
git clone https://github.com/mrilkos/Quickhull.git
cd Quickhull
```
 
Then open `index.html` in a browser. An internet connection is needed for the fonts and for Tailwind in the step-by-step visualizer.
 
## Where QuickHull is used
 
- Collision detection in games and robotics
- Computational geometry and GIS, for example the boundary of a point cloud
- Image analysis, such as finding the outline of a shape
- Clustering and outlier detection
## Built with
 
HTML, CSS and vanilla JavaScript, [three.js](https://threejs.org/) for the 3D models, and Tailwind CSS for the visualizer.
 
