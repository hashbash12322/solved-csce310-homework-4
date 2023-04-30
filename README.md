Download Link: https://assignmentchef.com/product/solved-csce310-homework-4
<br>
<h2>Written Assignment</h2>

<strong>Question 1       </strong>

From <em>Introduction to Algorithms </em>ISBN 978 − 0 − 262 − 03293 − 3

Draw the recursion tree for the Merge-Sort procedure presented below on an array of 16 elements. Explain why memoization is ineffective in speeding up a good divide-and-conquer

algorithm such as Merge-Sort.

<strong>if </strong><em>p &lt; r </em><strong>then </strong><em>q </em>←b(<em>p </em>+ <em>r</em>)<em>/</em>2c;

Merge-Sort(A,<em>p</em>,<em>q</em>);

Merge-Sort(A,<em>q </em>+ 1,<em>r</em>);

Merge(A,<em>p</em>,<em>q</em>,<em>r</em>); <strong>end</strong>

<strong>Algorithm 1: </strong>Merge-Sort(A,<em>p</em>,<em>r</em>)

<em>n</em><sub>1 </sub>← <em>q </em>− <em>p </em>+ 1; <em>n</em><sub>2 </sub>← <em>r </em>− <em>q</em>;

create arrays <em>L</em>[1<em>..n</em><sub>1 </sub>+ 1] and <em>R</em>[1<em>..n</em><sub>2 </sub>+ 1]; <strong>for </strong><em>i </em>← 1 <strong>to </strong><em>n</em><sub>1 </sub><strong>do</strong>

<em>L</em>[<em>i</em>] ← <em>A</em>[<em>p </em>+ <em>i </em>− 1]; <strong>end for </strong><em>j </em>← 1 <strong>to </strong><em>n</em><sub>2 </sub><strong>do</strong>

<em>R</em>[<em>j</em>] ← <em>A</em>[<em>q </em>+ <em>j</em>]; <strong>end</strong>

<em>L</em>[<em>n</em><sub>1 </sub>+ 1] ←∞; <em>R</em>[<em>n</em><sub>2 </sub>+ 1] ←∞; <em>i </em>← 1; <em>j </em>← 1; <strong>for </strong><em>k </em>← <em>p </em><strong>to </strong><em>r </em><strong>do</strong>

<strong>if </strong><em>L</em>[<em>i</em>] ≤ <em>R</em>[<em>j</em>] <strong>then </strong><em>A</em>[<em>k</em>] ← <em>L</em>[<em>i</em>]; <em>i </em>← <em>i </em>+ 1;

<strong>end else</strong>

<em>A</em>[<em>k</em>] ← <em>R</em>[<em>j</em>]; <em>j </em>← <em>j </em>+ 1; <strong>end end</strong>

<strong>Algorithm 2: </strong>Merge(A,<em>p</em>,<em>q</em>,<em>r</em>)

<strong>Question 2       </strong>

Question 8<em>.</em>1<em>.</em>3 in <em>The Design and Analysis of Algorithms</em>

<strong>Question 3      </strong>

From <em>Algorithm Design and Applications </em>ISBN: 9781118335918

Binomial coefficients are a family of positive integers that have a number of useful properties and they can be defined in several ways. One way to define them is as an indexed recursive function, <em>C </em>(<em>n,k</em>), where the <em>C </em>stands for “choices” or “combinations”. In this case, the definition is as follows:

<em>C </em>(<em>n,</em>0) = 1<em>,</em>

<em>C </em>(<em>n,n</em>) = 1<em>,</em>

and, for 0 <em>&lt; k &lt; n</em>,

<em>C </em>(<em>n,k</em>) = <em>C </em>(<em>n </em>− 1<em>,k </em>− 1) + <em>C </em>(<em>n </em>− 1<em>,k</em>)

<ul>

 <li>Show that, if we don’t use memoization, and <em>n </em>is even, then the running time for computing is at least 2</li>

 <li>Describe a scheme for computing <em>C </em>(<em>n,k</em>) using memoization. Give a big-oh characterization of the number of arithmetic operations needed for computing in this case.</li>

</ul>

<strong>Question 4       </strong>

From <em>Algorithms </em>ISBN: 9780073523408

Given two strings <em>x </em>= <em>x</em><sub>1</sub><em>,x</em><sub>2 </sub><em>…x<sub>n </sub></em>and <em>y </em>= <em>y</em><sub>1</sub><em>,y</em><sub>2 </sub><em>…y<sub>m</sub></em>, we wish to find the length of their <em>longest common substring</em>, that is, the largest <em>k </em>for which there are indices <em>i </em>and <em>j </em>with <em>x<sub>i</sub>x<sub>i</sub></em><sub>+1 </sub><em>…x<sub>i</sub></em><sub>+<em>k</em></sub>−<sub>1 </sub>= <em>y<sub>j</sub>y<sub>j</sub></em><sub>+1 </sub><em>…y<sub>j</sub></em><sub>+<em>k</em></sub>−<sub>1</sub>. Show how to do this in time <em>O </em>(<em>mn</em>).

<strong>Question 5     </strong>

From <em>Algorithms </em>ISBN: 9780073523408

<em>Counting Heads</em>. Given integers <em>n </em>and <em>k</em>, along with <em>p</em><sub>1</sub><em>,…,p<sub>n </sub></em>∈ [0<em>,</em>1], you want to determine the probability of obtaining exactly <em>k </em>heads when <em>n </em>biased coins are tossed independently at random, where <em>p<sub>i </sub></em>is the probability that the <em>i</em>th coin comes up heads. Give an for this task. Assume you can multiply and add two numbers in [0<em>,</em>1] in <em>O </em>(1) time. A <em>O</em>(<em>n</em>log<em>n</em>) time algorithm is possible.