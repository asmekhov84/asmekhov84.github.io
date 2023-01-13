In this work I've implemented a simple algorithm to split a polygonal mesh to a number of connected components.

Two faces are in the same connected component if and only if there is a path of adjacent edges between them. Otherwise they are in different connected components.

The pictures below show the result of processing a mesh of about 2 mln vertices and 4 mln triangle and quad faces. The method has separated it to 3 connected components, ordered by decreasing of number of faces.
