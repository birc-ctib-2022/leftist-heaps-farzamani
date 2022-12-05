[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=9552250&assignment_repo_type=AssignmentRepo)
# Leftist heap

As you recall, a *leftist heap* is one where we assign a `rank` to each node such that `n.rank` is zero if `n` is an empty heap and otherwise `n.rank = n.right.rank + 1`. To make the operations run in `O(log n)`, we always merge to the left and we always ensure that `n.rank.left >= n.rank.right`, i.e., when we merge we merge the smallest of the sub-heaps.

In `src/heap.py` I've written a heap, and I've added a `rank` to all the nodes, but I haven't made it a leftist heap yet. You need to ensure that the `merge()` operation always return leftist heaps, and you can do that by first creating nodes the way we do it now, but then restore the leftist property, `n.rank.left >= n.rank.right`, before you return.

Implement that.
