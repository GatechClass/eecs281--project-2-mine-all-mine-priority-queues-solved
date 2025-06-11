# eecs281--project-2-mine-all-mine-priority-queues-solved
**TO GET THIS SOLUTION VISIT:** [EECS281- Project 2 Mine All Mine (Priority Queues) Solved](https://mantutor.com/product/eecs281-project-2-mine-all-mine-priority-queues-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;69217&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EECS281- Project 2 Mine All Mine (Priority Queues) Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
This project is broken into two parts (A and B). Part A is your main()​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;,​ using the STL std::priority_queue&lt;&gt;; part B is you implementing several different versions of a priority queue.​

Project Goals

● &nbsp; &nbsp; &nbsp; Understand and implement several kinds of priority queues.

● &nbsp; &nbsp; &nbsp; Be able to independently read, learn about, and implement an unfamiliar data structure.

● &nbsp; &nbsp; &nbsp; Be able to develop efficient data structures and algorithms.

● &nbsp; &nbsp; &nbsp; Implement an interface that uses templated “generic” code.

● &nbsp; &nbsp; &nbsp; Implement an interface that uses inheritance and basic dynamic polymorphism.

● &nbsp; &nbsp; &nbsp; Become more proficient at testing and debugging your code.

Part A: Gold Mining

For Part A, you should always use std::priority_queue&lt;&gt;​ &nbsp;, not your templates from Part B.​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;In Part A you probably do not need or want to use pointers; in Part B you will have to (for the Pairing Heap).

Overview

You are an adventurous gold miner. &nbsp;However, in your avarice you’ve ignored several safe-tunneling practices, and a recent earthquake has left you trapped! &nbsp;Luckily, out of paranoia, you always carry ridiculous quantities of dynamite sticks with you. &nbsp;You need to blast your way out and make the most of each dynamite stick by blasting the piles of rubble which take the fewest sticks to destroy.

Breaking Out of the Mine

The mine you are trapped in can be represented with a 2-dimensional grid. &nbsp;There are 2 types of tiles:

● &nbsp; &nbsp; &nbsp; Tiles containing rubble.

○ &nbsp; &nbsp;Think of cleared tiles as containing 0 rubble. &nbsp;A tile in the mine could contain 0 before you clear it, that means that it never contained rubble.

● &nbsp; &nbsp; &nbsp; Tiles containing TNT.

You (the miner) start on a specified tile. &nbsp;At every iteration, you will attempt to blast away the “easiest” tile you can “access”, until you escape!

Definition of Discovered

The mine is very dark and you cannot see very far. When standing on a clear tile there are only four tiles that you can discover from your current tile: up, down, left and right (except for edge-of-map conditions). This is true in every case except for the start of the simulation, when you can only discover the starting tile. Adding tiles to the primary priority queue counts as “discovering” them. &nbsp;They can never be discovered (added to the primary PQ) twice.

Definition of Investigating

The priority queue will always tell you what your “next” tile will be. &nbsp;Investigating is taking the “next” tile from the priority queue and making it your “current” location. When you investigate a tile, you must clear it if it contains rubble or TNT. &nbsp;After clearing the tile, you can then discover any of the four tiles visible from your current location, add them to the priority queue, etc. &nbsp;You use the priority queue to remember tiles that you have discovered, but have not yet investigated.

Definition of Easiest Tile

The easiest tile you can reach is defined as follows, in the stated order:

1. &nbsp; &nbsp; Any TNT tile you can reach.

2. &nbsp; &nbsp; The lowest rubble-value tile you can reach.

Tie-breaking

In the event of ties (two TNT tiles or two rubble tiles with the same rubble-value):

1. &nbsp; &nbsp; Investigate the tile with the lower column coordinate first.

2. &nbsp; &nbsp; If the tiles have the same column coordinate, investigate the tile with the lower row coordinate.

Clearing Tiles

When clearing away rubble tiles, the tile turns into a cleared tile.

When clearing away TNT tiles, the following happens:

● &nbsp; &nbsp; &nbsp; The TNT tile becomes a cleared tile.

● &nbsp; &nbsp; &nbsp; All tiles touching the TNT tile are also “cleared”

○ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;If a TNT tile is touching another TNT tile, this will cause a chain explosion.

○ &nbsp; &nbsp;Diagonals are not considered for TNT explosions.

Definition of Escape

The miner escapes when their current tile has been cleared and is at the edge of the grid.

Example

In the following example, you start at position​ [1,2]​ (row 1, column 2). &nbsp;The tiles that the miner has investigated are ​red​ and the tiles that the miner has discovered are ​blue​. The tile that the miner just cleared is ​red and underlined​. Note: all cleared tiles will be 0, because you must clear a tile as part of investigating it. Positive integers signify rubble tiles (0 is a clear tile) and the value -1 signifies a TNT tile.

Please note: ​This example mine is for illustrative purposes and is not the same as the input file described in the ​Full I/O Example​ section​.​ To make things clearer, there are ​bold ​indices on the edges that refer to row and column number – they are not a part of the actual input file.

0 &nbsp; 1 &nbsp; 2 &nbsp; 3 &nbsp; 4 0​ &nbsp;20 &nbsp;20 &nbsp;20 &nbsp;20 &nbsp;20 1​ &nbsp;20 100 &nbsp;​10​ &nbsp;20 &nbsp;15 2 ​ 20 &nbsp;15 &nbsp; 5 &nbsp; 0 &nbsp;20

3​ &nbsp;20 &nbsp;20 &nbsp; 0 &nbsp;-1 100

4​ 100 &nbsp;-1 &nbsp;-1 &nbsp;20 &nbsp;20

At the first iteration, the only tile that can be discovered is the starting location, ​[1,2]​. The miner clears this tile and then can discover other tiles.

0 &nbsp; 1 &nbsp; 2 &nbsp; 3 &nbsp; 4 0​ &nbsp;20 &nbsp;20 &nbsp;​20​ &nbsp;​20 &nbsp;20 1​ &nbsp;20 ​100 &nbsp; ​0​ &nbsp;20​ &nbsp;15 2​ &nbsp;20 &nbsp;15 &nbsp;​ ​5​ &nbsp; 0 &nbsp;20 3​ &nbsp;20 &nbsp;20 &nbsp; 0 &nbsp;-1 100

4​ 100 &nbsp;-1 &nbsp;-1 &nbsp;20 &nbsp;20

Next, the miner will investigate and clear tile ​[2,2]​ because there are no TNT tiles in view and it has the lowest rubble-value. &nbsp;Clearing that tile allows us to discover more tiles!

0 &nbsp; 1 &nbsp; 2 &nbsp; 3 &nbsp; 4

0​ &nbsp;20 &nbsp;20 &nbsp;​20​ &nbsp;20 &nbsp;20 1​ &nbsp;20 ​ ​100 &nbsp;​0​ &nbsp;20​ &nbsp;15 2​ &nbsp;20 &nbsp;​15​ &nbsp;​ ​0​ &nbsp; ​0​ &nbsp;​20 3​ &nbsp;20 &nbsp;20​ &nbsp; 0 &nbsp;​-1 100 4​ 100 &nbsp;-1 &nbsp;-1 &nbsp;20 &nbsp;20

The tiles [2,1], [2, 3], and [3,2] are now discoverable (but still uninvestigated). The miner then investigates tile ​[3,2]​. Both this tile and tile ​[2,3]​ have an equally low level of difficulty. The tile ​[3,2] is chosen because its lower column value of ​2​ breaks the tie.

0 &nbsp; 1 &nbsp; 2 &nbsp; 3 &nbsp; 4

0​ &nbsp;20 &nbsp;20 &nbsp;​20​ &nbsp;20 &nbsp;20 1​ &nbsp;20 ​ ​100 &nbsp;​0​ &nbsp;20​ &nbsp;15 2​ &nbsp;20 &nbsp;​15​ &nbsp;​ ​0​ &nbsp; ​0​ &nbsp;​20 3​ &nbsp;20 &nbsp;​20 &nbsp; ​0​ &nbsp;-1​ 100 4​ 100 &nbsp;-1 &nbsp;​-1​ &nbsp;20 &nbsp;20

At this point, there are two TNT tiles which could be investigated next! &nbsp;However, due to the tie-breaking rules, the miner will choose to blow up the TNT at ​[4,2]​ instead of [3​ ,3]​ (this choice is made because it is at the top of the priority queue). &nbsp;Blowing up the TNT tile at ​[4,2]​ clears all the tiles touching it, creating a chain reaction with the TNT tile at ​[4,1]​. &nbsp;After all the TNT explosions have been resolved, the grid looks like the following:

0 &nbsp; 1 &nbsp; 2 &nbsp; 3 &nbsp; 4

0​ &nbsp;20 &nbsp;20 &nbsp;​20​ &nbsp;20 &nbsp;20 1​ &nbsp;20 ​ ​100 &nbsp;​0​ &nbsp;20​ &nbsp;15 2​ &nbsp;20 &nbsp;​15​ &nbsp;​ ​0​ &nbsp; ​0​ &nbsp;​20 3​ &nbsp;20​ &nbsp;​ ​0 &nbsp; ​0​ &nbsp;-1​ 100

4​ &nbsp; ​0​ &nbsp; ​0​ &nbsp; ​0​ &nbsp;​ 0​ &nbsp;​20

An explosion makes tiles ​discovered​ but does not ​investigate​ the tile (or discover around it). So, for example, [3, 1] was blown up by TNT and thus discovered. &nbsp;Therefore it is a candidate to be

investigated next, but [3, 0] (adjacent to it) is not. Since the current location is ​[4,2]​, and this tile is now cleared and on the edge of the map, we have escaped!

TNT Explosions

As you will see in the ​Output​ section, you need to keep track of the order in which tiles are cleared.

When a TNT tile detonates, all tiles ​ &nbsp;that are cleared as a result of the TNT detonation (including chain​ &nbsp; &nbsp; &nbsp; reactions) are cleared in order from “easiest” to “hardest” (as defined in Breaking Out of the Mine​ &nbsp; ,​ including tie-breaker rules). &nbsp;These tiles should also be discovered. &nbsp;As stated in Breaking Out of the​

Mine, do ​ NOT​ &nbsp;consider diagonals; even TNT only destroys rubble piles up, down, left and right of it.​

When a TNT detonation occurs, you should use a priority queue to determine detonation order. &nbsp;Push all the detonated tiles into a separate TNT priority queue, and then pop them out in priority order. &nbsp;You need to use some type of priority queue, because TNT blows up other TNT first, followed by smaller piles of rubble, etc.

Notice that, as you progress through your TNT priority queue, you may blow up a tile that is already waiting in your primary priority queue. &nbsp;If this happens, you have to make sure that the new rubble value of 0 comes out of the primary PQ sooner than the old, non-0 value. &nbsp;Think about how it will be possible for the primary PQ to actually know that a tile has changed! What if there were two entries for the same tile, and you ignore the second one? &nbsp;See the Full I/O Example​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;for more details.​

Command Line

Your program MineEscape​ &nbsp; &nbsp; &nbsp; should take the following case-sensitive command-line options:​ &nbsp; &nbsp; &nbsp; &nbsp;● &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;-​ h, –help

○ &nbsp; &nbsp;Print a description of your executable and exit(0)​ .​

● &nbsp; &nbsp; &nbsp; -s, –stats N

○ &nbsp; &nbsp; &nbsp; An optional flag that tells the program it should print extra summarization statistics upon termination. &nbsp;This optional flag has a required argument N. &nbsp;Details are covered in the Output section.​

● &nbsp; &nbsp; &nbsp; -m, –median

○ &nbsp; &nbsp; &nbsp; An optional flag that tells the program it should print the median difficulty of clearing a rubble tile that the miner has seen. Details are covered in the Output​ &nbsp;section.​

● &nbsp; &nbsp; &nbsp; -v, –verbose

○ &nbsp; &nbsp; &nbsp; An optional flag that tells the program it should print out every rubble value (or TNT) as a tile is being cleared. &nbsp;Details are covered in the Output​ &nbsp;section.​

Examples of legal command lines:

● &nbsp; &nbsp; &nbsp; ./MineEscape -v &lt; infile.txt

● &nbsp; &nbsp; &nbsp; ./MineEscape –stats 15 &lt; infile.txt &gt; outfile.txt

We will not be error checking your command-line handling, but we expect your program to accept any valid combination of input parameters.

Input and Output Redirection

In order to read an input file, you will use input redirection, just like you did in project 1. If you want to send your output to a file, you can also use output redirection, as seen in one of the command line examples above. The &lt; redirects​ ​the file specified by the next command line argument to be the standard input (​stdin/cin​) for the program. The &gt; redirects the standard output (​stdout/cout​) of the program to be printed to the file specified by the next command line argument.

Input

Settings will be given from an input file, ​‘MINEFILE’​ (this input file will not necessarily be named ‘MINEFILE’​). There will be two different types of input: map (M) and pseudo-random (R). &nbsp;Map input is for your personal debugging, but pseudorandom allows easier testing of large grids.

Map input mode (M)

Input will be formatted as follows:

● &nbsp; &nbsp; &nbsp; ‘​M​’ – A single character indicating that this file is in map format.

● &nbsp; &nbsp; &nbsp; ‘​Size​’ – Positive integer number that specifies the size of the square grid &nbsp;(20 means a grid with 20 rows and 20 columns).

● &nbsp; &nbsp; &nbsp; ‘​Start​’ – Coordinate indicating the starting location, row followed by column (two integers).

Map input consists of a map of all the tiles in the mine. &nbsp;Each tile will be separated from other tiles on the same line with whitespace (any number of spaces or tabs). There are 2 types of tiles:

● &nbsp; &nbsp; &nbsp; Rubble tiles which are signified by an integer between 0 and 999 (0 means the tile is already clear of rubble).

● &nbsp; &nbsp; &nbsp; TNT tiles, which are represented by the integer -1.

Tiles are indexed as follows:

● &nbsp; &nbsp; &nbsp; The tile in the top left corner is at location [0,0].

● &nbsp; &nbsp; &nbsp; The tile in the bottom right corner is at location [Size-1,Size-1].

Example of M input (starting location is at [1,2], or row 1 column 2, underlined):

M

Size: 5

Start: 1 2

9 &nbsp; &nbsp;0 &nbsp; &nbsp;9 &nbsp; &nbsp;3 &nbsp; &nbsp;3 &nbsp; &nbsp; 6 &nbsp; &nbsp;9 &nbsp; &nbsp;6​ &nbsp; &nbsp;8 &nbsp; &nbsp;3​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;9 &nbsp; &nbsp;4 &nbsp; &nbsp;1 &nbsp; &nbsp;9 &nbsp; &nbsp;0

2 &nbsp; &nbsp;0 &nbsp; -1 &nbsp; -1 &nbsp; &nbsp;9

8 &nbsp; &nbsp;3 &nbsp; &nbsp;9 &nbsp; &nbsp;7 &nbsp; &nbsp;5

Pseudorandom Mode (R)

Input will be formatted as follows:

● &nbsp; &nbsp; &nbsp; ‘R’​ – character indicating that this file is in pseudorandom format.

● &nbsp; &nbsp; &nbsp; ‘Size’​ – Number that specifies the size of the square grid (unsigned integer)

● &nbsp; &nbsp; &nbsp; ‘Start’ – ​Coordinate indicating the starting location (two unsigned integers, row first).

● &nbsp; &nbsp; &nbsp; ‘Seed’​ – Number used to seed the random number generator (unsigned integer)

● &nbsp; &nbsp; &nbsp; ‘Max_Rubble’ ​- &nbsp;The max rubble value a tile can have (unsigned integer)

● &nbsp; &nbsp; &nbsp; ‘TNT’ ​- &nbsp;Chance that a generated tile will be a TNT tile (20 = 1 in 20 chance of a given tile being a TNT tile, 0 = no chance of TNT; also an unsigned integer)

Example of R input:

R

Size: 5

Start: 1 2

Seed: 0

Max_Rubble: 10

TNT: 5

Generating your grid in R mode:

Included in Canvas with the project spec are the files ​P2random.h​ and ​P2random.cpp​ that​ ​contain definitions for the following function:

void P2random::PR_init(std::stringstream&amp; ss, unsigned int floor_size, &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; unsigned int seed, unsigned int max_rubble, &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;unsigned int tnt_chance);

The function ​P2random::PR_init(…)​ will set the contents of the stringstream argument (​ss​) so that you can use it just like you would ​cin​ for M input mode. &nbsp;You may find the following (incomplete) C++ code helpful in reducing code duplication. &nbsp;Remember, ​DO NOT​ copy/paste from a PDF file, retype the code by hand!

​stringstream ss; &nbsp; &nbsp; if (mode == “R”) {

// Read some variables from cin

P2random::PR_init(ss, floor_size, seed, max_rubble, tnt_chance);

} // if

// If map mode is on, read from cin; &nbsp; &nbsp; // otherwise read from the stringstream &nbsp; &nbsp; istream &amp;inputStream = (mode == “M”) ? cin : ss;

From this point on, read from ​inputStream​; it doesn’t matter whether the mode is M or R!

The example R and M input files given above are equivalent. ​ That is, ​both​ should generate the exact same map!

Errors you must check for

You must make sure that the input file describes a valid mine by checking for each of the following:

● &nbsp; &nbsp; &nbsp; The character on the first line of the file is either a ‘​M​’ or an ‘​R​’

● &nbsp; &nbsp; &nbsp; The coordinate specifying the ‘​Start’​ is a valid location given the ‘​Size​’ of the grid

If you detect invalid input at any time during the program, print a helpful message to ​cerr​ and exit(1)​. &nbsp;​You do not need to check for input errors not explicitly mentioned here.

Look in the Part A samples file, ​Error_messages.txt​: if your program performs an ​exit(1)​ and produces one of those error messages for a valid test case, we’ll show you your error output (to help you debug).

Output

Default Output

After completing the escape, your program should ​always​ print a summary line:

Cleared ​&lt;NUM&gt;​ tiles containing ​&lt;AMOUNT&gt;​ rubble and escaped.

&lt;NUM&gt; &nbsp; &nbsp; the number of tiles cleared. &nbsp;This number ​does ​include tiles cleared by TNT, but does not include the TNT tile itself.

&lt;AMOUNT&gt; the total rubble cleared. &nbsp;This number ​does ​include rubble cleared by TNT, but clearing (detonating) the TNT tile itself counts as 0 rubble cleared.

Verbose Output

During the program execution, if the ​-v or​ &nbsp; &nbsp; ​ –verbose​ switch is present, each time you clear a tile whose rubble amount is greater than 0, you should print:

Cleared: ​&lt;RUBBLE&gt;​ at [​&lt;ROW&gt;​,​&lt;COL&gt;​]

&lt;RUBBLE&gt; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;the amount of rubble being cleared

&lt;ROW&gt; &lt;COL&gt; &nbsp; &nbsp; &nbsp; the coordinates of the tile being cleared

Any TNT tiles blown up should display:

TNT explosion at ​[&lt;ROW&gt;,&lt;COL&gt;]​!

Any rubble tiles cleared by TNT should add the words “by TNT” to the cleared line; the general format is:

Cleared by TNT: ​&lt;RUBBLE&gt;​ at [​&lt;ROW&gt;​,​&lt;COL&gt;​]

The verbose mode output is produced as tiles are cleared, before the summary line. &nbsp;Consider getting verbose mode working early: it involves very little code, and will help you debug if you have any incorrect output.

Median Output

During the program execution, if the ​-m or​ ​ –median​ switch is present, each time you clear a tile, you should print:

Median difficulty of clearing rubble is: ​&lt;MEDIAN&gt;

&lt;MEDIAN&gt; The median value of rubble cleared so far. This includes rubble tiles cleared

by TNT, but does not include TNT tiles (-1 values should not be included in this calculation). &nbsp;Tiles that start out clear (rubble value 0) are not included here.

Median output must display 2 decimal digits. You can use:

cout &lt;&lt; std::fixed &lt;&lt; std::setprecision(2); at the beginning of your program to guarantee this.

Stats Output

After printing the summary line, if the ​-s​ or ​–stats ​option is specified print the following output (where ​N​ is the argument given to the -s flag on the command line):

A. &nbsp; &nbsp;The line, ​“First tiles cleared:”​ (without quotes) followed by the first ​N​ tiles cleared in the following format:

&lt;TILE_TYPE&gt;​ at [​&lt;ROW&gt;​,​&lt;COL&gt;​]

&lt;TILE_TYPE&gt; &nbsp;the type of the tile being cleared. &nbsp;If it is a rubble &nbsp;tile, this is the

rubble amount. &nbsp;If this is a TNT tile, print ​“TNT”​ without the quotes

&lt;ROW&gt;,&lt;COL&gt; the coordinates of the tile being cleared.

Remember​: when a TNT tile detonates or when there is a chain reaction, all the tiles are cleared from easiest to hardest. &nbsp;Refer back to ​TNT Explosions​ for more details.

B. &nbsp; &nbsp;The line, ​“Last tiles cleared:”​ (without quotes) followed by the last ​N tiles cleared in the​ &nbsp; &nbsp; &nbsp; &nbsp; same format as part ​A​. &nbsp;The ​last​ tile cleared should be printed first, followed by the second last, etc.

C. &nbsp; &nbsp;The line, ​“Easiest tiles cleared:”​ (without quotes) followed by the ​N​ easiest tiles you blew up in the same format as part ​A ​in ​descending order ​(easiest tile followed by next easiest tile)

D. &nbsp; &nbsp;The line, ​“Hardest tiles cleared:”​ (without quotes)’ followed by the​ N​ hardest tiles you blew up in the same format as part ​A. in ​ ​ascending order​ (hardest tile followed by next hardest tile)

If you have cleared less than N tiles, then simply print as many as you can. &nbsp;Tiles that start out clear (rubble value 0) are not included here.

Full I/O Example

Input (spec-M.txt​ &nbsp;and ​ spec-R.txt​ ):​

Equivalent input files (the R input file will generate a grid that looks just like the M input file):

M &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;R

Size: 5 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Size: 5

Start: 1 2 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Start: 1 2

9 &nbsp; &nbsp;0 &nbsp; &nbsp;9 &nbsp; &nbsp;3 &nbsp; &nbsp;3 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Seed: 0

6 &nbsp; &nbsp;9 &nbsp; &nbsp;6 &nbsp; &nbsp;8 &nbsp; &nbsp;3 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Max_Rubble: 10

9 &nbsp; &nbsp;4 &nbsp; &nbsp;1 &nbsp; &nbsp;9 &nbsp; &nbsp;0 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;TNT: 5

2 &nbsp; &nbsp;0 &nbsp; -1 &nbsp; -1 &nbsp; &nbsp;9

8 &nbsp; &nbsp;3 &nbsp; &nbsp;9 &nbsp; &nbsp;7 &nbsp; &nbsp;5

Output:

We ran the program with this command line: &nbsp;./MineEscape -v -m -s 10 &lt; spec-M.txt​ &nbsp; &nbsp; &nbsp;The output is shown below, with the verbose mode​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;highlighted in blue. &nbsp;The median mode output is​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;easy to identify, and statistics come after the “Cleared 6 tiles” summary line.

Cleared: 6 at [1,2]

Median difficulty of clearing rubble is: 6.00 Cleared: 1 at [2,2]

Median difficulty of clearing rubble is: 3.50

TNT explosion at [3,2]!

TNT explosion at [3,3]!

Cleared by TNT: 7 at [4,3]

Median difficulty of clearing rubble is: 6.00 Cleared by TNT: 9 at [4,2]

Median difficulty of clearing rubble is: 6.50

Cleared by TNT: 9 at [2,3]

Median difficulty of clearing rubble is: 7.00 Cleared by TNT: 9 at [3,4]

Median difficulty of clearing rubble is: 8.00 Cleared 6 tiles containing 41 rubble and escaped.

First tiles cleared:

6 at [1,2]

1 at [2,2]

TNT at [3,2]

TNT at [3,3]

7 at [4,3]

9 at [4,2]

9 at [2,3]

9 at [3,4] Last tiles cleared:

9 at [3,4]

9 at [2,3]

9 at [4,2]

7 at [4,3]

TNT at [3,3]

TNT at [3,2]

1 at [2,2]

6 at [1,2]

Easiest tiles cleared:

TNT at [3,2]

TNT at [3,3]

1 at [2,2]

6 &nbsp;at [1,2]

7 &nbsp;at [4,3]

9 at [4,2]

9 at [2,3]

9 at [3,4]

Hardest tiles cleared:

9 at [3,4]

9 at [2,3]

9 at [4,2]

7 at [4,3]

6 at [1,2]

1 at [2,2]

TNT at [3,3]

TNT at [3,2]

PART B: Priority Queue Implementation

For this project, you are required to implement and use your own priority queue containers. &nbsp;You will implement a​ “sorted array priority queue”​, a ​“binary heap priority queue”​, and a ​“pairing heap priority queue”​ which implement the interface defined in ​Eecs281PQ.h​.

To implement these priority queues, you will need to fill in separate header files, ​SortedPQ.h​,

BinaryPQ.h​, and ​PairingPQ.h​, containing all the definitions for the functions declared in

Eecs281PQ.h​. &nbsp;We have provided these files with empty function definitions for you to fill in. You may also add any additional functions needed to maintain the priority queue.

We provide a very bad priority queue implementation called the “​Unordered priority queue​” in

UnorderedPQ.h​, which does a linear search for the most extreme element each time it is requested. You can look at the code in this priority queue to see the use of ​this-&gt;compare()​ (more on that below), how to write your constructors, etc. &nbsp;There’s also an ​UnorderedFastPQ.h​ that is faster; look at how it uses ​mutable​ to accomplish that.. You can also use this priority queue to ensure that your other priority queues are returning elements in the correct order. &nbsp;All priority queues should return elements in the same (priority) order no matter which implementation is being used.

These files specify more information about each priority queue type, including runtime requirements for each member function and a general description of the container.

You are not allowed to modify ​Eecs281PQ.h​ in any way. &nbsp;Nor are you allowed to change the interface (names, parameters, return types) that we give you in any of the provided headers. &nbsp;You are allowed to add your own private helper functions and variables to the other header files as needed, so long as you still follow the requirements outlined in both the spec and the comments in the provided files.

These priority queues can take in an optional comparison functor type, ​COMP_FUNCTOR​. Inside the classes, you can access an instance of ​COMP_FUNCTOR​ with ​this-&gt;compare()​. All of your priority queues must default to be MAX priority queues. &nbsp;This means that if you use the default comparison functor with an integer PQ, ​std::less&lt;int&gt;​, the PQ will return the ​largest​ integer when you call top()​. Here, the definition of max (aka most extreme) is entirely dependent on the comparison functor.

For example, if you use ​std::greater&lt;int&gt;​, it will become a min-PQ. The definition is as follows:

If A is an arbitrary element in the priority queue, and ​top()​ returns the “most extreme” element. this-&gt;compare(top(), A)​ should always return false (A is “less extreme” than ​top()​).

It might seem counterintuitive that ​std::less&lt;&gt;​ yields a max-PQ, but this is consistent with the way that the STL ​std::priority_queue&lt;&gt;​ works (and other STL functions that take custom comparators, like ​sort()​).

We will compile your priority queue implementations with our own code to ensure that you have correctly and fully implemented them. To ensure that this is possible (and that you do not lose credit for these tests), do not define a main function in one of the PQ headers, or any header file for that matter.

Eecs281PQ&lt;&gt; interface​

Functions:

push(const TYPE&amp; val) //inserts a new element into the priority //queue

top() &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; //returns the highest priority element in the

//priority_queue

pop() &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; //removes the highest priority element from

//the priority queue

size() &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; //returns the size of the priority queue

empty() &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; //returns true if the priority queue is

//empty, false otherwise

Unordered Priority Queue

The ​unordered priority queue​ implements the priority queue interface by maintaining a vector. &nbsp;This has already been implemented for you, and you can use the code to help you understand how to use the comparison functor, etc. &nbsp;Complexities and details are in ​UnorderedPQ.h​ and UnorderedFastPQ.h​ &nbsp; &nbsp; &nbsp;​.

Sorted Priority Queue

The ​sorted priority queue​ implements the priority queue interface by maintaining a ​sorted ​vector. Complexities and details are in ​SortedPQ.h​. &nbsp;This should be written almost entirely using the STL. &nbsp;The number of lines of code needed to get this working is fairly low, generally &lt;= 10.

Binary Heap Priority Queue

Binary heaps will be covered in lecture. &nbsp;We also highly recommend reviewing Chapter 6 of the CLRS book. Complexities and details are in ​BinaryPQ.h​. &nbsp;One issue that you may encounter is that the examples and code in the slides use 1-based indexing, but your code must store the values in a vector (where indexing starts at 0). &nbsp;There are three possible solutions to this problem:

1) &nbsp; &nbsp; Add a “dummy” element at index 0, make sure you never let them access it, and make sure that size()​ and ​empty()​ work properly.

2) &nbsp; &nbsp; Translate the code from 1-based to 0-based. &nbsp;This is the best solution but the hardest.

3) &nbsp; &nbsp; Use a function to translate indices for you. &nbsp;Instead of accessing ​data[i]​, use getElement(i)​. &nbsp;The code for ​getElement()​ is given below (both versions are needed).

// Translate 1-based indexing into a 0-based vector​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;TYPE &amp;getElement(std::size_t i) { &nbsp; &nbsp; &nbsp; &nbsp; return data[i – 1];

} // getElement()

const TYPE &amp;getElement(std::size_t i) const { &nbsp; &nbsp; &nbsp; &nbsp; return data[i – 1];

} // getElement()

Pairing Priority Queue

Pairing heaps are an advanced heap data structure that can be quite fast. In order to implement the pairing priority queue, read the two papers we provide you describing the data structure. Complexity details can be found in PairingPQ.h​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; . We have also included a couple of diagrams that may help you​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; understand the tree structure of the pairing heap.

Below is the pairing heap modeled as a tree, in which each node is greater than each of its children:

To implement this structure, the pairing heap will use child and sibling pointers to have a structure like this:

Implementing the Priority Queues

Look through the included header files: you need to add code in ​SortedPQ.h​, ​BinaryPQ.h​, and

PairingPQ.h​, and this is the order that we would suggest implementing the different priority queues. Each of these files has TODO comments where you need to make changes. &nbsp;We wanted to provide you with files that would compile when you receive them, so some of the changes involve deleting and/or changing lines that were only placed there to make sure that they compile. &nbsp;For example, if a function was supposed to return an integer, NOT having a return statement that returns an integer would produce a compiler error. &nbsp;Also, functions which accept parameters have had the name of the parameter commented out (otherwise you would get an unused parameter error). &nbsp;Look at UnorderedPQ.h​ as an example, it’s already done.

When you implement each priority queue, you cannot compare ​data​ yourself using the ​&lt;​ operator. &nbsp;You can still use ​&lt;​ for comparisons such as a vector index to the size of the vector, but you must use the provided comparator for comparing the data stored inside your priority queue. &nbsp;Notice that

Eecs281PQ.h​ contains a member variable named ​compare​ of type ​COMP​ (one of the templated class types). &nbsp;Although the other classes inherit from ​Eecs281PQ.h​, you cannot access the ​compare​ member directly, you must always say ​this-&gt;compare()​ (this is due to a template inheriting from a template).

Notice that in ​UnorderedPQ&lt;&gt;​ it uses ​this-&gt;compare()​ by passing it to the ​max_element() algorithm to use for comparisons.

When you write the ​SortedPQ&lt;&gt;​ you cannot use ​binary_search()​ from the STL, but you wouldn’t want to: it only returns a ​bool​ to tell you if something is already in the container or not! &nbsp;Instead use the lower_bound()​ algorithm (which returns an iterator), and you can also use the ​sort()​ algorithm — you don’t have to write your own sorting function. &nbsp;You do however have to pass the ​this-&gt;compare functor to both ​lower_bound()​ and ​sort()​.

The ​BinaryPQ&lt;&gt;​ is harder to write, and requires a more detailed and careful use of the comparison functor, and you have to know how one works to write one in the first place, even for ​UnorderedPQ&lt;&gt; to use. See the ​About Comparators​ section below.

Compiling and Testing Priority Queues

You are provided with a testing file, ​testPQ.cpp​. ​testPQ.cpp​ contains examples of unit tests you can run on your priority queues to ensure that they are correct; however, it is ​not​ a complete test of your priority queues; for example it does not test ​updatePriorities()​. It is especially lacking in testing the ​PairingPQ&lt;&gt;​ class, since it does not have any calls to ​addNode()​ or ​updateElt()​. You should add more tests to this source code file.

Using the 281 ​Makefile​, you can compile ​testPQ.cpp​ by typing in the terminal: ​make testPQ​. You may use your own ​Makefile​, but you will have to make sure it does not try to compile your driver program as well as the test program (i.e., use at your own risk).

Logistics

The std::priority_queue&lt;&gt;​

The STL ​std::priority_queue&lt;&gt;​ data structure is basically an efficient implementation of the binary heap which you are also coding in ​BinaryPQ.h​. To declare a ​std::priority_queue&lt;&gt;​ you need to state either one or three types:

1) &nbsp; &nbsp; The data type to be stored in the container. &nbsp;If this type has a natural sort order that meets your needs, this is the only type required.

2) &nbsp; &nbsp; The underlying container to use, usually just a ​std::vector&lt;&gt;​ of the first type. 3) The comparator to use to define what is considered the highest priority element.

If the type that you store in the container has a natural sort order (i.e. it supports ​operator&lt;()​), the std::priority_queue&lt;&gt;​ will be a max-heap of the declared type. For example, if you just want to store integers, and have the largest integer be the highest priority:

std::priority_queue&lt;int&gt; pqMax;

When you declare this, by default the underlying storage type is ​vector&lt;int&gt;​ and the default comparator is ​less&lt;int&gt;​. &nbsp;If you want the smallest integer to be the highest priority:

std::priority_queue&lt;int, vector&lt;int&gt;, greater&lt;int&gt;&gt; pqMin;

If you want to store something other than integers, define a custom comparator as described below.

About Comparators

The functor must accept two of whatever is stored in your priority queue: if your PQ stores integers, the functor would accept two integers. &nbsp;If your PQ stores pointers to units, your functor would accept two pointers to orders (actually two ​const​ pointers, since you don’t have to modify units to compare them).

Your functor receives two parameters, let’s call them ​a​ and ​b​. &nbsp;It must always answer the following question: ​is the priority of ​a​ less than the priority of b​ ​? &nbsp;What does lower priority mean? &nbsp;It depends on your application. &nbsp;For example, refer back to the ​Breaking Out of the Mine​ section: if you have multiple tiles in your priority queue, you determine priority based on smallest rubble value. &nbsp;If rubble value is the same, break ties based on column or row number.

When you would have wanted to write a comparison, such as:

if (data[i] &lt; data[j])

You would instead write:

if (this-&gt;compare(data[i], data[j])

Your priority queues must work ​in general​. In general, a priority queue has no idea what kind of data is inside of it. &nbsp;That’s why it uses ​this-&gt;compare()​ instead of ​&lt;​. &nbsp;What if you wanted to perform the comparison ​if (data[i] &gt; data[j])​? &nbsp;Use the following:

​if (this-&gt;compare(data[j], data[i])

Libraries and Restrictions

For part A, we encourage the use of the STL, with the exception of these prohibited features:

● &nbsp; &nbsp; &nbsp; The thread/atomics libraries (e.g., boost, pthreads, etc) which spoil runtime measurements.

● &nbsp; &nbsp; &nbsp; Smart pointers (both unique and shared).

You ​are​ allowed to use ​std::vector&lt;&gt;​, ​std::priority_queue&lt;&gt;​ and std::deque&lt;&gt;​ &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ​.

You are ​not​ allowed to use other STL containers. Specifically, this means that use of ​std::stack&lt;&gt;​, std::queue&lt;&gt;​, ​std::list&lt;&gt;​, ​std::set&lt;&gt;​, ​std::map&lt;&gt;​, ​std::unordered_set&lt;&gt;​, std::unordered_map&lt;&gt;​, and the ​‘multi’​ variants of the aforementioned containers are forbidden.

For part B,

You ​are​ allowed to use ​std::sort()​.

You ​are​ allowed to use ​std::lower_bound()​.

You are ​not​ allowed to use ​std::partition()​, ​std::partition_copy()​, std::partial_sort()​, ​std::stable_partition()​, ​std::make_heap()​, std::push_heap()​, ​std::pop_heap()​, ​std::sort_heap()​, ​std::qsort()​, or anything that trivializes the implementation of the binary heap.

You are ​not​ allowed to use the C++14 regular expressions library (it is not fully implemented on gcc

6.2) or the thread/atomics libraries (it spoils runtime measurements).

You are ​not​ allowed to use other libraries (eg: boost, pthread, etc).

Furthermore, you may ​not​ use any STL component that trivializes the implementation of your priority queues (if you are not sure about a specific function, ask us).

Your main program (part A) ​must​ use ​std::priority_queue&lt;&gt;​, but your PQ implementations (part B) ​must not​.
