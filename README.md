Wikiracing Candidate Brief
==========================

This problem is designed to test your abilities to do the kind of systems programming we do at Segment, with a focus on **concurrency**, **networking**, **performance** and some **algorithmic optimizations**. 

Problem
=======

There's an online form of racing called [Wikiracing](https://en.wikipedia.org/wiki/Wikiracing).  The goal is to traverse your way from one Wikipedia page to another, using only links. For this particular problem, we're trying to traverse from "**Tennessee**" to "**Printer**". 

Here's an example path from "Mike Tyson" to "Segment" which can be found in about a second in four hops:

-   Mike Tyson → Alexander the Great

-   Alexander the Great → Greek language

-   Greek language → Fruit anatomy

-   Fruit anatomy → Segment

We want to complete a Wikirace *as quickly as possible* without requiring a complete graph of Wikipedia because Wikipedia pages are changing all the time. Feel free to take this as an opportunity to showcase your knowledge of network programming and concurrent/parallel programming. You can scrape HTML pages, but we'd suggest taking a peek at what the MediaWiki API has to offer. Or do both, and benchmark the approaches against each other.

Your Wikiracer should take a starting page and an end page (as either a URL or a page title) and successfully figure out how to traverse from one to the other (or tell the user if there isn't a path). The output should be a list of pages on the path, as well as the total elapsed time to run. Watch out for pathological edge cases and handle them gracefully.

Your Wikiracer gets points for having a low wall-clock time, **not** for the lowest number of hops. You'll want to optimize for the wall-clock time speed of navigating from one page to the other.

There are many ways to build a Wikiracer, but we'd especially like it if yours had a REST API.

We love all kinds of programming languages at Segment. We're currently building all our services in Go and Node, and we're excited to work with you if you know these languages or think you could pick them up reasonably quickly. For this exercise, it would be great if you could use either Go or Node to implement it, since that gives us the best opportunity to have a deeply technical conversation with you. If you're currently more comfortable with Java, C/C++, Python, Ruby or other languages in those families, we're happy to make it work --- Segment has many fans of all of the above on the team. Wherever possible we want you to use the right tool for the job, including the programming language you're most comfortable with.

Feel free to use any libraries that you think might aid your cause. Be ready to walk us through why you chose your specific implementation language and libraries --- we'd love to understand the decisions you made here.

**Key Requirements**

-   We should be able to read and understand your code. It should be clean and well-formatted and the techniques and algorithms that you are using should be clear.
-   We love unit tests. Please write some.
-   A reasonable amount of code comments are always appreciated!
-   Please include a README file with:

-   High-level architecture overview
-   What the code does
-   Instructions for how to run your Wikiracer
-   Strategies you tried
-   How long you spent on each part of the project

-   Bonus points for additional infrastructure like a docker-compose file that makes it really easy to test your solution.
-   Take as long as you need to build a good piece of software that showcases your skills.
-   Have fun!
-   If you have any questions about this assignment, feel free to reach out to your recruiter. We're always happy to discuss.

**Ideas for Extra Credit**

-   Build your Wikiracer to scale out as multiple instances for extra parallelization. A docker-compose file might make it easy for us to spin up multiple instances of your Wikiracer.
-   If you want to use an extra service (ZooKeeper, etcd, Redis, etc.) for coordinating between your instances, drop it in a container and let's do this thing.
-   Build this like you'd build a real production service. Give us beautiful logs! Give us useful metrics! Give us tracing. Go wild. We live for this stuff.
-   Modify your tool to run on any site, not just Wikipedia.
-   Come up with your own ideas. Be sure to write about it in the README. Sell us on how awesome your Wikiracer is. The more effort you put in here, the more excited we're going to be to meet you when you come on-site at Segment. 

**Evaluation**

When we receive your submission, the first thing we'll do is to unpack the code archive (or git clone it, if appropriate), enter the directory and run make test. We'll do this on a modern Linux or Mac OS distribution with a recent version of docker and docker-compose installed. The expectation is that, by following the steps above, the code would build itself and run all relevant tests. We expect it to, at least, contain an end-to-end test for each requirement you claim to implement. After successfully running the tests, we'll review the code and design.

For example, this is expected to "just work":

`tar -xzvf assignment.tar.gz`

`cd assignment`

`make test`\
Please submit here:\
<https://app.greenhouse.io/tests/756bcc0707906dbc9d666dee4db8fe17>
