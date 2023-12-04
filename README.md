<div align="center" id="top"> 
</div>

<h1 align="center">Reto_05</h1>

## :dart: About ##

Sam and Kelly are programming buddies. Kelly resolves to practice more as Sam isa head initially.
They each solve a number of problems daily. Find the mínimum number or days for Kelly to have
solved more problems than Sam. If Kelly cannot surpass retum -1.
Example
SamDaily = 3
KellyDaily = 5
Difference = 5
Initially, Sam has solved difference problems more than Kelly. Each day, they solve samDaily and
kellyDaily problems each.
Day 1: samSolved = difference + samDaily = 5 + 3 = 8
kellySolved = kellyDaily = 5
Day 2: samSolved = 8 + 3 = 11
kellySolved = 5 + 5 = 10
Day 3: samSolved = 11 + 3 = 14
kellySolved = 10 + 5 = 15
Sam is 5 problems ahead of Kelly and they solve 3 and 5 problems a day. Sam will be ahead by only
3 after the first day, 1 after the second, and Kelly will pass Sam on day 3.
Function Description
Complete the function minNum in the editor below.
MinNum has the following parameter(s):
SamDaily: Number of problems Sam solves in a day
KellyDaily: Number of problems Kelly solves in a day
Difference: Number of problems Sam isa head to begin
Return
Int: the minimum number of days needed by Kelly to exceed Samm, or -1 if it is imposible
Constraints
• 1 ≤ samDaily, kellyDaily ≤ 100
• 0 ≤ difference ≤ 100
Input format for Custom Testing
Input from stdin will be processed as follows and passed to the fuction.
The first line contains an integer samDaily.
The second line contains an integer kellyDaily.
The third line contains an integer ahead.
Sample Case 0
Sample Output 0
1
Sample Case 1
Sample Output 1
2
QUESTION DESCRIPTION
Consider every susequence of an array of integers.
• Sort the subsequence in increasing order.
• Determine the sum of differences of elements in the subsequence.
• Return the length of the longest subsequence where this sum is even.
We can see that the máximum posible length of a valid subsequence is 4.
Function Description
Complete the function findLongestSubsequence in the editor below.
FindLongestSubsequence has the following parameter(s):
Int arr[n]: an array of integers
Returns
Int: the length of the longest subsquence as describe
Constraints
• 3 ≤ n ≤ 105
• 0 ≤ arr[i] ≤ 109
Input Format For Custom Testing
The first line contains an integer, n, the number of elements in arr.
Each line i of the n subsequent lines ((where 0 ≤ i < n) contaisn an integer, arr[i]

## :rocket: Technologies ##

The following tools were used in this project:

- [Node.js](https://nodejs.org/en/)

## :white_check_mark: Requirements ##

Before starting :checkered_flag:, you need to have [Git](https://git-scm.com) and [Node](https://nodejs.org/en/) installed.

## :checkered_flag: Starting ##

```bash
# Clone this project
$ git clone https://github.com/daniel12082/push_up_Reto_05

# Access
$ cd reto_05

#Open Terminal

# Run the project
$ run code start

function minNum(samDaily, kellyDaily, difference) {
    if (samDaily >= kellyDaily) {
        return -1;
    }

    let days = 0;
    let samSolved = difference;
    let kellySolved = 0;

    while (samSolved >= kellySolved) {
        samSolved += samDaily;
        kellySolved += kellyDaily;
        days++;
    }

    return days;
}
```

## :open_book: Explain ##
  
-----------------------------------------------------------------------

| Nr.  | Step                                                         |
| ---- | ------------------------------------------------------------ |
| 1    | The minNum function is defined with three parameters: samDaily, kellyDaily, and difference. These parameters represent the number of problems Sam solves daily, the number of problems Kelly solves daily, and the initial difference in the number of problems solved by Sam and Kelly, respectively.|
| 2    | Inside the function, there is an if statement that checks if samDaily is greater than or equal to kellyDaily. If this condition is true, it means that Sam is already solving more problems than Kelly, so the function returns -1. |
| 3    | Three variables are declared and initialized: days is set to 0, samSolved is set to the initial difference, and kellySolved is set to 0.|
| 4    | The code then enters a while loop. The loop continues as long as samSolved is greater than or equal to kellySolved.|
| 5    | Inside the loop, the values of samSolved and kellySolved are updated by adding the respective daily amounts (samDaily and kellyDaily). |
| 6    | The days variable is incremented by 1 in each iteration of the loop. |
| 7    | Once the condition in the while loop is no longer true (i.e., samSolved becomes less than kellySolved), the loop exits.|
| 8    | Finally, the function returns the value of the days variable, which represents the number of days it takes for Sam to solve more problems than Kelly. |
| 9    | The console.log statement at the end of the code calls the minNum function with the arguments 7, 8, and 6, and logs the result to the console. |
  
## :memo: License ##

Made with :heart: by <a href="https://github.com/{YOUR_GITHUB_USERNAME}" target="_blank">{Daniel Felipe Diaz}</a>

