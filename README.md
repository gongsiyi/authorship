# Incremental Learning of Code Authors Over Time
## Project summary

In software development, programmers use issue trackers to manage maintenance issues and record valuable maintenance details in issue reports. Based on these issue reports, programmers have enhanced code comprehension and researchers have mined knowledge from issue reports to assist various programming tasks. Although issue reports are useful, some of them can be obsolete, in that their corresponding commits are overwritten or rolled back, with the evolution of software. The obsolete issue reports can invalidate their references and descriptions and have far-reaching impacts on the approaches built on them.

To deepen the understanding of obsolete issue reports, we conducted the first empirical study to analyze obsolete issue reports. We consider that an issue report is obsolete if its revisions are partially or entirely removed in later commits. To measure how an issue report becomes obsolete, we define an obsolete ratio of an issue report as its deleted lines over all its modified lines. In this paper, we build a tool, ICLINKER, to inspect the obsolete issue reports and calculate the obsolete ratios. With ICLINKER, we analyze 116,106 commits and 72,136 issue reports that are collected from 9 Apache projects. Taking them as our inputs, we explore three research questions, which concern the distributions, the references, and the assignees of obsolete issue reports. Our findings on these research questions enrich the knowledge of obsolete issue reports, and some are even counterintuitive. For example, we find that obsolete issue reports are mixed with other issue reports. As another example, we find that only a small portion of issue reports are mentioned in code comments, but about half of them are obsolete. Furthermore, we analyze how obsolete issue reports affect an issue-recommendation approach. According to our results, we improve this approach by removing 36% of recommendations, which are obsolete.



## Our identified obsolete ratios

We identified the obsolete ratios of the issue reports from five projects. Their obsolete ratios are as follows: 
[aries](https://github.com/gongsiyi/obsolete_issue_reports/blob/main/aries.txt), [calcite](https://github.com/gongsiyi/obsolete_issue_reports/blob/main/calcite.txt), 
