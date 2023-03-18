# overemployed
This is a repo for the code and technology needed to search for work when you already have a job.
Purposed tech stack:

API - SprintBoot

DB - MySQL

Mobile - Xamerin

Web - React

Problem Statement - When searching for OverEmployment on the current search engines there is a lack of NOT or NOR functionality to the query.  What is lacking is a way to filter out by Company, Recruiting firm, type of work, etc.  Currently the focus is to bring in more rather than less.

Solution - This solution is an effort to narrow the focus and find a small group of results that fit the criteria better so that time is not wasted hunting for the wrong opportunity.

Approach - In order to filter you first need something to filter.  In this case the solution will, in real time, search all major Job Boards for the typical criteria, then it will filter for the specific.  For example:  Job searches typically take, Where, What type of job, keywords, salary, company, etc.  This solution will do this as the only thing really being done is a DB query build with joins and unions.  However, next is to remove postings that are done by the same type of criteria.  So a SQL statement may look like this: 
SELECT post FROM indeeddb.table WHERE date=last30 AND salary >= 100,000 AND location = remote ANDNOT company= AMAZON ANDNOR keyword contains selenium;  

This will allow the user to do what all the search engines do but then filter down to a better focused result.
