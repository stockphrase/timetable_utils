# timetable_utils
==================


Command-line utility for query Dartmouth's Timetable. Borrows heavily from 
student-authored code (https://github.com/katzdaniel/course_finder/) to parse 
oddly formatted HTML.

Requires:
------------
+ lxml


Sample usage:
-------------


<code>
[jed@parergon timetable_utils ]$ bin/get_enrollments -d COLT
COLT-07.17      Michael McGillen               2   16  16 
COLT-07.22      Kristin O'Rourke               12  16  16 
COLT-10.28      Jessica Smolin                 10  20  18 
COLT-19.01      Michael Wyatt                  11  15  15 
COLT-40.01      Jessica Beckman                2A  16  16 
COLT-52.09      Marie Larose                   2   20  5  
COLT-54.01      Lada Kolomiyets                2   30  4  
COLT-62.10      Eman Morsi                     2A  20  17 
COLT-70.05      Matteo Gilebbi                 10  25  26 
COLT-72.01      Ayo Coly                       2A  20  2  
COLT-73.05      Andrew McCann                  10A 20  14 
COLT-079        James Dorsey                   ARR NaN 1  
COLT-085        Veronika Fuechtner             3B  8   5  
COLT-101        Eman Morsi                     3B  11  11 
COLT-103        Rebecca Biron                  3A  11  11 
COLT-110        Rebecca Biron                  ARR 12  1  
</code>

<code>
[jed@parergon timetable_utils ]$ bin/get_enrollments -d WRIT -s 005 -e 
WRIT-005        John Barger                    12  16  16  0  
WRIT-005        John Barger                    2   16  16  0  
...
WRIT-005        Leigh York                     2A  16  16  0  
WRIT-005        Rosetta Young                  11  16  16  0  
</code>


<code>
[jed@parergon timetable_utils ]$ bin/get_enrollments -d GOVT -s 005 -e --sum
GOVT-005        Kathleen Powers                11  40  31  9  
GOVT-005        Kathleen Powers                2   40  30  10 

Total empty seats: 19
</code>
