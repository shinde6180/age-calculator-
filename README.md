#include &lt;stdio.h&gt;

int main()
{
int birthDay, birthMonth, birthYear;
int currentDay, currentMonth, currentYear;
int ageYears, ageMonths, ageDays;

printf(&quot;Enter your birth date (DD MM YYYY): &quot;);
scanf(&quot;%d %d %d&quot;, &amp;birthDay, &amp;birthMonth, &amp;birthYear);

printf(&quot;Enter the current date (DD MM YYYY): &quot;);
scanf(&quot;%d %d %d&quot;, &amp;currentDay, &amp;currentMonth, &amp;currentYear);

if (currentDay &lt; birthDay)
{
currentDay += 30;
currentMonth--;
}
ageDays = currentDay - birthDay;

if (currentMonth &lt; birthMonth)
{
currentMonth += 12;
currentYear--;
}
ageMonths = currentMonth - birthMonth;
ageYears = currentYear - birthYear;
printf(&quot;Your age is: %d years, %d months, and %d days\n&quot;, ageYears, ageMonths,
ageDays);
return 0;
}
