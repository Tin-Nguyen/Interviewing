# WholeWeeks
Calculate the number of whole weeks in a period of time.

John has always dreamed of taking a vacation on Hawaii. He hasdecided to make his dream come true during the next holiday period,and he would like to spend as much time there as possible.

The problem is that there is only one plane per week connecting Hawaiiwith the city where John lives. The plane departs every Monday andarrives every Sunday. There is no other way to get to Hawaii and back. Itmeans that John can spend only whole weeks in Hawaii.

John knows in which month his vacation starts and in which month itends. His vacation period starts on the rst day of the beginning monthand ends on the last day of the ending month. John also knows the yearin which his vacation takes place.

For example, if John's vacation lasts from July to September in 2008,then it starts on 1st July 2008 and ends on 30th September 2008.

Your task is to calculate how many weeks John will spend in Hawaii,given:the month when the vacation begins;the month when the vacation ends;the year when the vacation takes place;the day of the week for 1st January in the vacation year(for convenience).

The names of the days of the week are: Monday, Tuesday,Wednesday, Thursday, Friday, Saturday, Sunday. Thenames of the months are: January, February, March, April,May, June, July, August, September, October,November, December. The lengths of the months are, respectively: 31, 28 (or 29 in a leap year), 31, 30, 31, 30, 31,31, 30, 31, 30, 31 days.

Pay attention to leap years; you should also consider them. The year ofthe vacation will be a number between 2001 and 2099, inclusive, and youcan tell that the year is a leap year if it's divisible by 4.

Write a function:class Solution { public int solution(int Y, StringA, String B, String W); }
Note: the code stype depends on which programming language you will use in the test.

that, given an integer Y and three non-empty strings A, B and W, denotingthe year of the vacation, the beginning month, the ending month and theday of the week for 1st January of that year, returns the maximumnumber of weeks that John can spend in Hawaii.For example, given Y = 2014, A = "April", B = "May" and W ="Wednesday", the function should return 7, since John can leave his cityon April 7th and come back on May 25th, so he will spend 7 weeks onHawaii (the weeks beginning, respectively, on April 7th, 14th, 21st, 28thand May 5th, 12th, 19th).

[Image here]

Assume that:
- Y is an integer within the range [2,001..2,099];
- A and B are valid month names;
- month B does not preceed month A;
- W is a valid weekday name;
- W is the correct weekday for January 1st of year Y in theactual calendar.

In your solution, focus on correctness. The performance of your solutionwill not be the focus of the assessment