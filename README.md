# csc361-assignment-2-tcp-traffic-analysis-solved
**TO GET THIS SOLUTION VISIT:** [CSC361 Assignment 2-TCP Traffic Analysis Solved](https://www.ankitcodinghub.com/product/csc361-assignment-1-tcp-traffic-analysis-4-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;62793&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC361 Assignment 2-TCP Traffic Analysis Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 138px;">
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
            5/5 - (1 vote)    </div>
    </div>
The purpose of this project is to understand the details of state management in Transmission 7 Control Protocol (TCP). You are required to write a python program to analyze the TCP protocol 8 behavior.

<h2>9 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Requirements</h2>
10 You will be given a <em>sample </em>TCP trace file (sample-capture-file.cap). During the period traced, a 11 single web client accesses different web sites on the Internet. This trace is to be used for your own 12 test. TA might use a different trace file to test your code.

13 You need to write a python program for parsing and processing the trace file, and tracking TCP 14 state information. In this assignment, your code will be tested on the server <em>linux.csc.uvic.ca</em>. As 15 such, you are allowed to use <strong>only the Python packages of python3 currently installed </strong>on 16 <em>linux.csc.uvic.ca</em>. You are not allowed to install/use other third-party python packages.

17 Your program should process the trace file and compute summary information about TCP 18 connections. Note that a TCP connection is identified by a 4-tuple (IP source address, source port, 19 IP destination address, destination port), and packets can flow in both directions on a connection 20 (i.e., duplex). Also note that the packets from different connections can be arbitrarily interleaved 21 with each other in time, so your program will need to extract packets and associate them with the 22 correct connection.

<ul>
<li>The summary information to be computed for each TCP connection includes:</li>
</ul>
<table width="53">
<tbody>
<tr>
<td width="53">25

26

27

28

29

30

31

32

33

34&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; •
</td>
</tr>
</tbody>
</table>
<ul>
<li>the state of the connection. Possible states are: S0F0 (no SYN and no FIN), S1F0 (one SYN and no FIN), S2F0 (two SYN and no FIN), S1F1 (one SYN and one FIN), S2F1 (two SYN and one FIN), S2F2 (two SYN and two FIN), S0F1 (no SYN and one FIN), S0F2 (no SYN and two FIN), and so on, as well as R (connection reset due to protocol error). For consistence, we count a SYN+ACK segment (i.e., a segment with both SYN bit and ACK bit set to 1) as a SYN message. (Of course, a SYN segment is also counted as a SYN segment). Getting this state information correct is the most important part of your program. We are especially interested in the complete TCP connections for which we see at least one SYN and at least one FIN. For these complete connections, you can report additional information, as indicated in the following. the starting time, ending time, and duration of each complete connection</li>
</ul>
1

<ul>
<li>the number of packets sent in each direction on each complete connection, as well as the total</li>
<li>packets</li>
<li>the number of data bytes sent in each direction on each complete connection, as well as 38 the total bytes. This byte count is for data bytes (i.e., excluding the TCP and IP protocol 39 headers).</li>
</ul>
40 Besides the above information for each TCP connection, your program needs to provide the 41 following statistical results for the whole trace data:

<ul>
<li>the number of reset TCP connections observed in the trace</li>
<li>the number of TCP connections that were still open when the trace capture ended</li>
<li>the number of complete TCP connections observed in the trace</li>
<li>Regarding the complete TCP connections you observed:</li>
<li><strong>– </strong>the minimum, mean, and maximum time durations of the complete TCP connections</li>
<li><strong>– </strong>the minimum, mean, and maximum RTT (Round Trip Time) values of the complete 48 TCP connections</li>
</ul>
49 <strong>– </strong>the minimum, mean, and maximum number of packets (both directions) sent on the 50 complete TCP connections

51&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>– </strong>the minimum, mean, and maximum receive window sizes (both sides) of the complete 52&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TCP connections.

53 As a guideline for output format, please follow the output format of this project shown in 54 outputformat.pdf.
