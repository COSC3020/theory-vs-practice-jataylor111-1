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


First we need to determine how many search attempts it took to find the value we were looking for, using the average case $O(log(n))$ $^{[1]}$ we can get log(1000) = 3 search attempts.  We can do the same for a tree of 10,000 elements and build an equation for how long it took.  Using the same average case we can get log(10,000) = 5.  Now for our equation:

$\frac{5s}{3attempts}$ * $4attempts$ $\approx$ 6.7 seconds for the tree of 10,000 elements.


The first reason I would think of is that the hardware is different, like my third point above maybe the first search was run on a powerful machine and the second one, while using the same code, was run on a machine with significantly slower internals.
The average case is something I found online and as such maybe the search function is poorly written and while it does its job it has in reality a much worse asymptotic complexity for larger trees.
The original tree might have been all one data type while the second might have been a mixture of them which can take much longer to search through.


$^{[1]}$ I got this average case from wikipedia at; https://en.wikipedia.org/wiki/Binary_search_tree
I also had to google a little bit of markdown code for the approximatley equals sign here; https://stackoverflow.com/questions/43025450/how-can-i-type-approximate-equal-sign-in-markdown-jupyter

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice






