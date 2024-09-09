# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.
----------------------------------------------------
Like the proof for the insertion sort exercise we mostly ignore any constant values which, while small, do have an impact on the complexity; like from the slides we mention $10^{-10}n^2 \in \Theta{n^2}$ while this is true the leading coefficent has a massive impact on that graph which I will get to in a second.
The Big-O and Big- $\Theta$ bounds are very loose, in the above point I mention how the functions $10^{-10}n^2$ and $n^2$ are compared, but if we were to graph these two equations we would see that while $n^2$ starts increase almost immediately the function $10^{-10}n^2$ doesn't perceptively increase until almost $n$ = $1*10^8$.
Lastly the analysis doesn't factor in hardware, since it's only theoretical we can still get wildly different results from two different machines, for instance if we had a machine from the 60s it would run an algorithm a decent amount slower than a modern machine just because of the ability of the hardware.











