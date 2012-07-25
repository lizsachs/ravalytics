Ravalytics
==========

Analytics performed on a Ravelry user's project data

For this demo, I iterated through the JSON project results examining data for project start and end dates to populate a set of charts that show a user's start and completion trends over time. My mom, LoneStarNeedler, gave me permission to use her project data as well so that I could test my code on multiple datasets.

(After completing this, I went on to build a full webapp loosely based on the ideas here. See my Yarn Store Enabler project for more info: https://github.com/lizsachs/Yarn-Shop-Enabler

I originally planned to use charts that simply bucketed data by month and year and displayed them in order across the bottom of the screen, but found that my project history goes back further than I thought.  Once I saw that the charts would be practically unreadable, I decided to keep the data bucketed by month (bucketing by year is better for the ego, but makes for less interesting charts), but to instead display the months together. This allowed for more concise graph labeling, and also allowed the user to look for annual trends.  (How many projects DO we frantically cast on in the months leading up to Christmas?)  This was especially interesting for my mom's project data.  She's a teacher, so you can see vague spikes during winter break, spring break, and summer break as well as dips during the beginning of the school year.  If I was going to look for significant trends in this data, it would probably be advisable to make sure the axes on all charts match and to not omit the years without project data so that one could compare equally across users and project activity types.

I didn't have any experience with any particular charting libraries, so I poked around a little and decided that Highcharts looked robust, easy to use, and allowed free use of their libraries for non-commercial use. <http://www.highcharts.com/>

I chose to implement this in a single file because the HTML is minimal.  I considered building up a grails app on the back end to take care of data processing because that's where most of my experience lies, but I decided it would be a good test project to get my hands around some basic javascript and it would simplify the overall code sample.

The next thing I'd like to add to this if given infinite time (full time job + baby limits my extracurricular coding time) would be some analysis of project duration. Perhaps a report that shows the average project time, longest project, shortest project, and a chart of number of projects by average duration in days.