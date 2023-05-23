Then command, grep, standing for "Global Regular Expression Print," is a tool to search through files for\
patterns or expressions, which bash will return matching lines. Below are four different command-line options\
for grep.


## $ grep -i

The -i option allows you to perform a case-insensitive search, ignoring the distinction between uppercase and lowercase letters.


**Example 1:**
````
$ grep -i "september 11" technical/911report/preface.txt 
````
returns:
````
September 11, 2001, was a day of unprecedented shock and suffering in the history of\
relating to the terrorist attacks of September 11, 2001," including those relating\
most complete account we can of the events of September 11, what happened and why.\
````
The command returns all lines containing the argument, regardless of capitalization.\
Although September isn't capitalized in the prompt, it returned lines where it was capitalized.

**Example 2:** 
````
$ grep -i "frozen" technical/biomed/rr74.txt 
````
returns:
````
flushed with cold PBS. The right lung was frozen for
Frozen lung tissue was homogenized in ice cold 750 μl
Total RNA was extracted from 100 mg of frozen lung
min, and plasma removed and frozen. Later, samples were
````
Here the word, "frozen", was found a total of 4 times, one of which was capitalized.

## $ grep -c

The -c option gives a count of the amount of lines in which the word appeared.

**Example 1:**
````
$ grep -c "frozen" technical/biomed/rr74.txt 
````
returns:
````
3
````
The prompt, "frozen" appeared 3 times, even though the word appeared four.\
This is because the command takes capitalization into account.

**Example 2:**
````
$ grep -ic "frozen" technical/biomed/rr74.txt 
````
returns:
````
4
````
Here the two demonstrated commands are combined, both ignoring capitalization\
AND returning the count of the times the word appeared.

## $ grep -n 
The -n option returns the line, as well as the line number.

**Example 1:**
````
$ grep -n "What" technical/plos/pmed.0020090.txt
````
returns:
````
6:        What is the level of medical evidence that should be used to inform medical practice? At
36:        confounders. What this paper does not do is directly address the question of whether or not
````
The numbers, 6 and 36, correspond to the line the word was found on.

**Example 2:**
````
$ grep -in "it " technical/plos/pmed.0020090.txt
````
returns:
````
12:        been going on for more than 50 years. It started with a paper published in 1951 in the
34:        the risk ratio for prediction of disease was 1.13 (1.07–1.20), but it was only 1.02
37:        serum uric acid is involved in causing CHD through intermediates; however, it does suggest
39:        Where does such a result leave patients? Well, it is likely that improving diet, losing
````
Here, again the lines are printed, and the command ignores capitilization. Note that the command searches for\
"it ", with a space after the "t", meaning words like "with", which don't have a space after the "t" are invalid.
## $ grep -r
The -r option allows grep to search for the given pattern recursively in both directories and subdirectories.

**Example 1:**
````
$ grep -r "the canal" technical/
````
returns:
````
technical/biomed/1471-2091-2-11.txt:        acids. ATP-dependent transporters on the canalicular
technical/biomed/1471-2091-2-11.txt:        other multidrug resistance proteins to the canalicular
technical/biomed/1471-213X-1-3.txt:        veins that connect to the canal. This route is generally
technical/biomed/1471-2202-4-2.txt:          afferent and efferent innervation to the canal crista
technical/biomed/1471-2202-4-2.txt:          innervation to the canal cristae, while reduced, has
technical/biomed/1471-2202-4-2.txt:          neurons to the canal epithelia, in particular the
technical/biomed/1471-2202-4-2.txt:          the canal cristae we expected, and found, only a BDNF
technical/biomed/1471-2202-4-2.txt:          expression of BDNF, as is the case in the canal cristae
````
Here all lines were printed in THE ENTIRE /technical directory that contained "the canal", as well as the specific\
files they were found in.

**Example 2:**
````
$ grep -irn "the reasoning" technical/
````
returns:
````
technical/biomed/1471-2202-3-1.txt:98:        the reasoning and goals underlying our choice of tools.
technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt:101:The reasoning of Regional Management is controlling here. As we
````
Here, in one foul swoop, we are searching ALL DIRECTORIES AND SUBDIRECTORIES under /technical, for the\
term, "the reasoning", ignoring capitalization AND printing the line number of the document the line was found on.
