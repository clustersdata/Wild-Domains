# Wild-Domains

Wild Domains

Description

Consider a search engine that knows a number of sites. A site is described by a well-formed domain name which consists of two or more domain parts separated by dots such as www.sharif.edu. A domain part is a string of upper-case and lower-case alphabetic characters. For the rest of this description, we use the term domain name for well-formed domain name.

To restrict a search to some specific sites, a user is allowed to use domain patterns in a search query. A domain pattern is similar to a domain name, except that it may contain arbitrary number of the following wildcards:


    Asterisk character (*) that matches a sequence of one or more domain parts separated by dots,
    Question mark character (?) that matches at least one and at most three domain parts separated by dots,
    Exclamation mark character (!) that matches at least three domain parts separated by dots.


Note that if a wildcard character appears in a domain pattern, it should be separated from its surrounding domain parts (if any) by dots. For example www.?.edu, or *.edu are both valid domain patterns matching domain name www.sharif.edu.

Two domain patterns match if at least one domain name can be constructed matching both domain patterns. For example, the domain patterns www.?.edu and *.edu match, since both match the domain name www.xyz.edu. Note that the constructed domain name may be an arbitrary (yet not necessarily an existing) site. You are to write a program that given two domain patterns, determines whether the patterns match.

Input

The first line of the input file contains a single integer t (1 <= t <= 10), the number of test cases, followed by the input data for each test case. Each test case consists of two lines, each containing a domain pattern. Each domain pattern is at most 255 characters long, and does not include any leading or trailing blank characters.

Output

There should be one line per test case in the output file containing a single word YES or NO, depending on whether the two domain patterns in the test case match or not.

Sample Input

2
www.?.edu
?.edu
*.edu
yahoo.com

Sample Output

YES
NO
