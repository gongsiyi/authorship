# Incremental Learning of Code Authors Over Time
## Project summary

Identifying code authors is important in many research topics, and various approaches have been proposed. Recent studies show that the temporal effect can significantly affect existing approaches: they rapidly become outdated and ineffective due to the evolution of code authors’ coding style over time. To our knowledge, only one approach[1] was proposed to alleviate the temporal effect. This approach treats the temporal effect problem as a cross-domain problem and uses transfer learning method to reduce it. In their case, the domain refers to the time at which the programmer is coding the source code. Although this approach achieves promising results on their datasets, the evaluation of this approach shows that the effectiveness of transferred models decreases with the increasing intervals between the source and the target domains.

In this paper, we propose new methods to combat the temporal effect problem of code authorship attribution. Since source files of code authors are accumulated in real development and attribution models need to be continuously updated with continuous data, we use chunk-based incremental learning: we treat the accumulated source files as data streams, and each incoming batch of data is treated as a chunk, we utilize an ensemble framework to maintain an ensemble of base classifiers that are incrementally trained (with no access to previous data) on incoming chunks of data, and the base classifiers are dynamically weighted according to their performance on the current data chunk, then these classifiers are combined using a dynamically weighted voting. We evaluate the effectiveness of our approach using two datasets of programs written in C++ and Java. Our evaluation shows that our incremental learning-based approach leads to significant improvements, compared to the previously published transfer learning-based approach. Our approach improves the prediction accuracy from 0.7343 to 0.9017 on the Java dataset and the prediction accuracy from 0.8016 to 0.9022 on the C++ dataset. Also, our approach maintains more consistent performance across a seven-year time period than the past approach. The results show that our approach can incrementally learn the evolving coding style of code authors over time.

Here is the list of our [dataset](https://github.com/gongsiyi/authorship).

Here is the list of our [models](https://github.com/gongsiyi/authorship).

## Our evaluation results

The evaluation results of three research questions are as follows: 
[cpp](https://github.com/gongsiyi/authorship/blob/main/cpp.xlsx), [java](https://github.com/gongsiyi/authorship/blob/main/java.xlsx)

## Our motivating example results

To illustrate how the code styles evolve over time, we calculate the code metrics of source files written by eatmore* from 2012 to 2015. The results are as follows: 
[style_2012](https://github.com/gongsiyi/authorship/blob/main/style_2012.xlsx), [style_2013](https://github.com/gongsiyi/authorship/blob/main/style_2013.xlsx), [style_2014](https://github.com/gongsiyi/authorship/blob/main/style_2014.xlsx), and [style_2015](https://github.com/gongsiyi/authorship/blob/main/style_2015.xlsx)

## Reference
[1] Z. Li, S. Zhao, C. Chen, and Q. Chen. Reducing the impact of time evolution on source code authorship attribution via domain adaptation. ACM Transactions on Software Engineering and Methodology, 2024.
