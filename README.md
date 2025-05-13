# cs29003-lab-6-greedy-algorithm-solved
**TO GET THIS SOLUTION VISIT:** [CS29003 Lab 6-Greedy Algorithm Solved](https://www.ankitcodinghub.com/product/cs29003-lab-6-greedy-algorithm-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92908&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS29003 Lab 6-Greedy Algorithm Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
. Problem Statement

In your city, there is a grocery store that is quite popular. People can order the items online on a given day and collect the parcel next day. On a given day, assume that 2 ≤ n ≤ 8 people have given their orders. With the order, they also mention the time window on the next day, when they can collect the parcel. This time window is specified by two integers ai, bi, which give the beginning and end of a closed interval [ai, bi] during which the person can visit the shop. The numbers ai and bi are specified in minutes and satisfy 0 ≤ ai ≤ bi ≤ 1440. Assume that the time taken to collect the parcel is negligible. Further, a constraint due to Covid-19 scenario is that the visiting times should be stretched out as much as possible so that the minimum achievable time gap between successive visits is as large as possible. For example, if three people visit the shop at 10:00 am, 10:05 am, and 10:15 am, then the smallest gap is five minutes, which occurs between the first two people. Not all gaps have to be the same, but the smallest gap should be as large as possible!

See Figure 1 for an illustration. Each line denotes the interval specified by a person. In the leftmost example, there are three people with time windows of [0,10], [5,15] and [10,15], respectively. To maximize the minimum achievable gap, their visits need to be scheduled at times [0 : 00,7 : 30,15 : 00] as denoted by the stars, which gives a minimum gap of 7 : 30 minutes (read 7 minutes 30 seconds). You can verify that you cannot get a larger gap.

Figure 1: Example Scenarios (answers are given in mins:secs format).

Write a schedule visits() function to implement the greedy algorithm. Note that the inputs are not sorted in

anyway and if you need to sort you should only use an O(n log n) algorithm.

<ol>
<li>Compute an order for the visits that respects these time windows given the constraint of maximising the
minimum achievable time gap.
</li>
<li>Print the answer split into minutes and seconds, rounded to the closest second.</li>
</ol>
<ol>
<li>Hint 1: Try to draw parallels with the activity scheduling problem.</li>
<li>Hint 2: For each specific visit order, we want to know the largest possible visit window. Suppose we use a certain window length L. We can greedily check whether this L is feasible by forcing the first person to visit as soon as possible and the subsequent persons to visit in max(a[that person], previous person’s arrival time + L).</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Read the input file as follows

<ol>
<li>The first line contains the number of persons n (assume 2≤ n ≤ 8)</li>
<li>Read ai, bi respectively for each person. n
a1

b1

a2

b2

…so on
</li>
</ol>
Sample 1: input file

File: input1.txt

4 0 8 2 4 3 9 10 20

Sample 2: input file

File: input2.txt

3 0 12 0 2 13 50

You have to print the followings exactly in the same way as shown in the sample output file 1. The first line contains the time gap split into minutes and seconds.

2. The second line prints the order for the visit of the persons.

Sample 1: output file

File: output1.txt 4:00

0123

Sample 2: output file

File: output2.txt

12:00 102

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Notes

1. Make sure to read inputs from a file named “input1.txt”. At the time of evaluation, the input data might be different from the one given here.

2. You need not to submit “output1.txt”, but your code should write the output in the given format in a file named “output1.txt”.

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
