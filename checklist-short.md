# Good Laboratory Practice for Optimization Research - GLP4OPT
## Guiding Principles
- [ ] R.1 Researchers should adopt the highest ethical standards in conducting their research.
- [ ] R.2 Researchers should ensure that the work of others is properly cited.

## Benchmark Datasets
- [ ] R.3 Where possible, data should come from the real world, for example, from biological experiments.
- [ ] R.4 Any benchmark dataset that is accepted into the scientific community should be stored in one central location (see Section 4.16) so that all the datasets are available to all researchers in one place.

Associated with each instance will be the paper (see R.5) that introduced the benchmark, along with all published results.

- [ ] R.5 Any dataset that a researcher wants to become a recognized dataset should be subject to the same peer review process as any other scientific paper. Furthermore, where possible, a dataset should be introduced via a stand-alone paper so that the peer review process can focus on the proposed benchmark instances, rather than on an algorithm that is being proposed. The paper should introduce the datasets, and provide all the elements that are set out in R.6 to R.14.
- [ ] R.6 A benchmark instance should be presented in a standard format, that is specified in such a way that new instances can be presented in the same way. We recognize that this may not be possible for existing datasets, as they may have different formats, but when a new dataset is introduced, the authors should define how future instances should be represented.
- [ ] R.7 The format in which solutions should be presented should be defined. The format should be amenable to parsing by a computer. We recognize that this may not be possible for existing datasets, as they may have different formats, but when a new dataset is introduced, the authors should define how future instances should be represented.
- [ ] R.8 When a benchmark instance is proposed, the researcher should provide the necessary means to evaluate each instance. As a minimum a class should be provided in as many languages as possible (e.g. Java, C++, C\#, PHP, Python) which the researcher can utilize to validate the validity and solution quality of any instance that they create. Several examples should be given, to show the evaluation of a number of solutions to help researchers verify that they are evaluating the solutions they produce in the correct way (see R.18).
- [ ] R.9 When a benchmark instance is proposed, a statistical test should also be suggested that can be used by future researchers to compare against other instances from the benchmark set. This should provide a way to compare different algorithms in a robust way. There are many sources of reference for defining suitable statistical tests. Recent examples include (Derrac et al., 2011) and (García et al., 2010).
- [ ] R.10 When a benchmark instance is proposed, the researcher should state the recommended computational times used for each instance. Two main timing measures could be adopted. Firstly, the number of times that the evaluation function can be called. Secondly, how long the algorithm can run using the same time as returned by recommendation $\mathbf{R} .28$.
- [ ] R.11 Researchers are encouraged to present a range of different benchmark instances, covering different sizes and complexity. Some of the instances may be solvable to optimality (for example using mathematical programming) so that stochastic methods are able to provide some indication how close they are to optimality. Other instances might be challenging to the methodologies available today and others might be considered to provide challenges for the foreseeable future.
- [ ] R.12 At the same location (see Section 4.16), where the benchmark instances are located, a history of best known solutions should be available. This, by definition, means that the best known solution is always available.
- [ ] R.13 Any paper that is published (not just under review) that utilizes one of the standard benchmark datasets must provide ALL the solutions that are referred to in the paper that the authors have published. As an example, if the paper produces 30 solutions for statistical analysis then all those 30 solutions should be available so that other researchers are able to perform comparisons against the set of solutions rather than just the best, mean, median and average (also see R.41). Note, we not suggesting that all the instances in a given dataset have to be reported. A researcher might decide not to use all instances. But, if any instance is used, then ALL the solutions should be made available to the community.
- [ ] R.14 It is recognized that there are some datasets that have been in the scientific literature for so long that they have become a defacto standard. We cannot simply ignore these and the international advisory board (see Section 6) will define those datasets that should form the basis for this proposed initiative.

## Non-registered Datasets
- [ ] R.15 If a researcher decides not to register a dataset that they use, they should still make the dataset available to the scientific community and should seek to respect recommendations R.6 to R.13. 

## Presentation of Solutions
- [ ] R.16 When presenting the result of a simulation, any solution that is presented must be accompanied by the actual solution in the format that can be validated by R.8. The solutions that are presented (both the solution and its evaluation) should include all those referred to in the paper. For example, any solutions that are used in statistical analysis, or when tuning parameters (see R.41).

## Evidence of Hybridized Approaches
- [ ] R.17 If a hybridized algorithm is being presented then, unless previously reported in other work, the researchers should provide results from each non-hybridized element, using statistical analysis so that there is evidence that the hybridization is actually effective.

## Evaluation Function
- [ ] R.18 The evaluation function must be described in a way that can be understood and implemented by other researchers.
- [ ] R.19 Referring to recommendation R.8 it should be possible for another researcher to test their implementation of an evaluation function to check that they have implemented it correctly and that it produces the same values as R.8.


## Algorithm Presentation
- [ ] R.20 Any algorithm that is presented must be reproducible. This is one of the underpinning tenets of scientific research but some details are often missing, or vague. The optimization research community needs to ensure that all algorithms (and results) are reproducible.
- [ ] R.21 An algorithm should be presented in pseudo code, rather than a specific programming language. This is to stop any assumptions being made about another researchers' understanding on any given programming language.
- [ ] R.22 Attention should be given to areas such as variable initialization, how many iterations of certain lines are carried out, all (sub)operations are defined etc.

## Computational Times
- [ ] R.23 The researcher should adopt the recommended computational times as provided in R. 10, stating which method they are using.
- [ ] R.24 A researcher is at liberty to use a different computational time, but it must be done in such a way that other researchers are able to use the same timings in future research (see recommendation R.28)

## Statistics
- [ ] R.25 The necessary statistical test, as defined by R.9, should be applied to the relevant results (e.g. the best known solution and the solutions produced from the current study). 

## Experimental Conditions
- [ ] R.26 The full specification of the machine that was used for the experiments should be given. This should include the type of computer, the operating system and version number, the programming language that was used together with the compiler, the amount of memory available to the program, whether parallel processing was employed, if GPUs were utilized etc. Increasingly, researchers are using cloud services. These should also be reported in appropriate detail.
- [ ] R.27 The date(s) that the experiments were run should be given. This provides another point of reference for future researchers. This is important as the time between running experiments and the paper appearing in print could be a matter of years.
- [ ] R.28 For each main operating system the community will provide a test program ((Dongarra, 1992) might provide some inspiration for how this can be done) that can be run on a researcher's target machine. This will record the speed of the researcher's machine against some known baseline, informing the researcher how long they should run their algorithm to give a fair comparison with other researchers, particularly the original benchmark. See (McCollum et al., 2010) for an example of this method being used for an international competition.

The benchmark program will also provide a data file that can be stored as part of the paper that is subsequently published which future researchers can refer to in order to compare their algorithm's performance against previous algorithms.

## Laboratory Notebooks
- [ ] R.29 Optimization researchers should maintain a laboratory notebook. These can be used by the researcher to record their thoughts, ideas and successes/failures and they also provide an important historic record for future researchers to refer to. 
- [ ] R.30 Researchers are encouraged to make available, via a supplementary file, the relevant parts of their notebooks, once a paper has been published.
- [ ] R.31 Other researchers should not be critical of notebooks, but should accept them for what they are. A notepad that provides a historic document of the research ideas, thoughts and timeline associated with a given piece of research.

## Software
- [ ] R.32 It is beholden on the individual researcher(s) to keep a copy of the software that led to the contribution claimed in a given paper. Researcher(s) should retain an exact copy of the source code, the compiled code and any other environmental factors that are required to reproduce their results. If necessary, they should be able to re-run their algorithm and produce exactly the same results (see R.33), even years later.
- [ ] R.33 In the case of any dispute, authors can be asked to demonstrate their software to show that it produces the results claimed in the paper. This request can only come from the editor-in-chief (or their nominated representative) of the journal to which a paper has been submitted to, or published in.
- [ ] R.34 The source code for a given paper should be made available, under one of four categories:
    1. The source code is made freely available to other researchers
    2. The source code is not available to other researchers, but is available to the reviewers who can access the code using the accepted confidentially that is associated with reviewing scientific papers
    3. The source code is supplied, but is not made available to either researchers or the reviewers
    4. The source code is not made available at all
- [ ] R.35 Supplying source code does imply that any support will be given to other researchers who later use, or access, the source code.
- [ ] R.36 The complete environment must be described so that anybody using the source code is able to replicate the computational conditions. As an example, the experimental setup might utilize Matlab, R or mathematical software. These elements need to be described in a manner that enables reproducibility.
- [ ] R.37 Source code associated with a published paper should be held in a repository that does not allow updates (any corrections should be done via an erratum) and which can be accessed via a permalink, in the same way that scientific papers are generally available via a DOI. This is to ensure that, like scientific papers, scientific researchers are accessing the same version of the source code as supplied by the authors.

In order to protect the scientific archive, the repository (or repositories) should be maintained by the scientific community, rather than an Open Source repository. 

- [ ] R.38 Only in exceptional circumstances will access be given to the code without the author's permission, and then only the editor-in-chief of the relevant journal can authorize this. Exceptional circumstances might include accusations of plagiarism, or suspicions of incorrect results being claimed.
- [ ] R.39 If all the authors have passed away, the software will be available to anybody that requests it, unless other arrangements have been made. This is to allow future researchers to access the code without any hindrance. There is no expectation of support of any kind from colleagues, or institutions.

## Parameter Selection and Values
- [ ] R.40 Be specific on how the parameter values were set, detailing the simulations that were carried out, to the point that these should be as reproducible as any other simulations reported in the paper.
- [ ] R.41 All the solutions that are used to compare the parameters should be made available to other researchers in the same way that the main solutions are also reported (see R.16).
- [ ] R.42 When making claims that one set of parameter values is better than another, a statistical analysis should support this claim.
- [ ] R.43 If no evidence is provided to the contrary, no claims should be made that the parameter values that were used for the main simulations presented in the paper are in any way robust, optimal or can be relied upon in other simulations to provide any level of solution quality. 

## Random Number Generation
- [ ] R.44 The random number generator that was used should be explicitly stated. The coding lines that are used to generate each random variable should be presented, along with any preparatory steps (e.g. setting starting values, seeding the sequence).
- [ ] R.45 It should be possible for any researcher to generate the same sequence of random numbers, so that the simulation can be reproduced.

## Termination Criteria
- [ ] R.46 Researchers should precisely define the termination criteria for any algorithm that is presented.

## GLP4OPT Adherence and Support
- [ ] R.47 Any benchmarks that are introduced (see R.5 to R.14) into the scientific literature must be recorded in the journal's supplementary repository (see R.54).
- [ ] R.48 The GLP4OPT supplementary file must define which version of the standard has been used. As mentioned in the Introduction, the version introduced here is GLP4OPT version 1.00.
- [ ] R.49 If a journal or publisher has subscribed to GLP4OPT then it should insist on a supplementary file that reviewers can access to check against compliance with the standard. It should also be made available to those readers that are enable to access the main paper.
- [ ] R.50 Once (and if) established, the GLP4OPT web site will maintain the best known solutions for each registered dataset, along with a history of best known solutions (see R.12).
- [ ] R.51 ALL solutions that are referred to in a given paper must be uploaded to the journal as a supplementary file(s) (see R.13). This includes any solutions used to establish parameter settings (see R.41)
- [ ] R.52 Once (and if) established, the GLP4OPT web site will contain a repository of all the papers that have used a given registered benchmark dataset.
- [ ] R.53 Once (and if) established, the GLP4OPT web site will maintain the set of historical datasets (see (R.14), including best known solutions and all papers that have used those datasets.
- [ ] R.54 It is recognized that many of the data specified in this section might be held as a supplementary file on the journal's we site. In this case, the GLP4OPT web site will contain the necessary links to the supplementary data.
