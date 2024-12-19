java c
Faculty of Arts  Science 
Fall 2024 Quiz 5 
CSC 110 Y1F
Question 1. Tabular Data [6   marks]Here   is   a   sample   list   similar   to   the   data   we   saw   in   the   lecture.   Each   column   represents   an   ID,   a   civic   centre name,   the   number   of   marriage   licenses   issued,   and   the   month   and   year   when   they   were   issued   (YYYY,   MM,   DD).
import datetime
marriage_data =   [
[1657,   '   ET   '   , 80, datetime.date(2011,   1,   1)],
[1658,   '   NY   '   ,   136, datetime.date(2011,   1,   1)],
[1659,   '   SC   '   ,   159, datetime.date(2011,   1,   1)],
[1660,   '   TO   '   , 367, datetime.date(2011,   1,   1)],
[1662,   '   NY   '   ,   150, datetime.date(2011, 2,   1)],
[1664,   '   TO   '   , 383, datetime.date(2011,   2,   1)]
]
a)   What   would   the   following   expressions   evaluate   to?   Write   your   answers   in   the   space   provided   below   each   statement.
>>> len(marriage_data)
>>> marriage_data[5][2]
>>> len(marriage_data[-1])
>>> min([row[2] for   row   in   marriage_data])b)   Fill   in   a   plain   English   docstring   description   for   the   function   below,   based   on   the   provided   function   body.   The preconditions are provided for   you.   You do not need   to   provide   any   doctests   or   further   preconditions.
def do_something(data: list[list], year: int)   ->   float:
"""
Preconditions:
- year   is a   positive   integer
- data satisfies all of the properties   described   in   the beginning   of   this   question
"""
counts   =   [row[2] for   row   in   data   if   row[3]   .year   == year]
num_months   = len({row[3]   .month   for   row   in   data   if   row[3]   .year   ==   year})
return sum(counts)   / num_months
Question 2. Dataclasses [3   marks]
Recall   this   dataclass   we   discussed   in   lecture:
@dataclass
class MarriageData:
"""A record of the number of marriage   licenses   issued   in   a   civic   centre
in a   given   month   .
Instance Attributes:
- id: a   unique   identifier   for   the   record代 写CSC 110 Y1F Fall 2024 Quiz 5C/C++
代做程序编程语言
- civic_centre: the name   of   the   civic   centre
- num_licenses: the number of   licenses   issued
- date_issued: the month and year these   licenses were   issued
"""
id:   int
civic_centre:   str
num_licenses:   int
date_issued: datetime   .date
Rewrite   the   function   body   from   the   do_something   function   from   the   previous   question   so   that   it   now   deals   with   a   list   of MarriageData   instances.   Fill   this   in   below:
def do_something_v2(data: list[MarriageData], year: int)   -> float:
"""
Docstring omitted   . The code should   do   the   same   thing   that   it   does   in   Question   1   .   """
counts   =
num_months =
return sum(counts)   / num_months
Question 3. Debugging / Index-Based For Loops [3   marks]The   function   below   is   an   incorrect   attempt   to   return   True if   a   string   s is   a   palindrome.    Your   friend   Bob   believes   the   function   is   correct   because   he   tried   calling   the   function   with   some   string   arguments   which   the   code   did   work   correctly   for.   Answer   the   questions   below.
def   is_palindrome(s:   str)   -> bool:
"""Return whether s   is   a palindrome   .
A palindrome is a   string that reads   the   same   backward   as   forward   .
>>>   is_palindrome(   '   davad   '   )   True
>>>   is_palindrome(   '   david   '   )
False   """
n   =   len(s)
for   i   in   range(n   //   2):
if   s[i]   !=   s[n   -   1   -   i]:
return False
else:
return True
Part (a) [1   mark]
Give   an   example   of a   valid   argument   for   s   where   this   function   will   return   the   correct   expected   value   (according   to   the   docstring):
Part (b) [1   mark]
Give   an   example   of a   valid   argument   for   s   where   this   function   will   NOT   return   the   correct   expected   value:
Part (c) [1   mark]
Brieﬂy   explain   (in   1–2   sentences)   why   this   function   is   incorrect   (identify   the   issue   in   the   code):



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
