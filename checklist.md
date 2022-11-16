# Good Laboratory Practice for Optimization Research - GLP4OPT
In this section we present the recommendations that should be adopted by the optimization research community. Many of these have been suggested in other works, including many of those referred to in Section 3.1. However, to our knowledge, there has been very little take up on many of the proposals made and many of the bad practices that were highlighted still exist. We hope that providing an explicit set of recommendations will focus the minds of researchers as to the areas that need to be addressed when proposing a hypothesis and then designing and running simulations to investigate that hypothesis. The recommendations have been split into a number of key areas.

## Guiding Principles
There are certain guiding principles that underpin all the other recommendations. This is similar to the guidelines set out by the Committee on Publication Ethics $([COPE][3])$, which is aimed at journal editors and publishers.

In some sense, they are obvious, but we believe that it is worth stating them explicitly, so that there is no confusion.

### Recommendations for GLP4OPT

- [ ] R.1 Researchers should adopt the highest ethical standards in conducting their research.

- [ ] R.2 Researchers should ensure that the work of others is properly cited.

## Benchmark Datasets

Some of the papers we reviewed in Section $3.1$ were critical of the way that benchmark instances were either introduced into the scientific literature, were biased towards certain algorithms or that randomly generated instances were not a true representation of the problem being considered or that the randomness was biased in some way. Moreover, instances are not always available for other researchers to use and, when randomly generated instances were used the algorithm is not reproducible, meaning that other researchers cannot generate a representative set of instances. Indeed, any generated instance, or its generator, should either be made available to other researchers or the algorithm (including any random number generation) should be defined to enable another researcher to create the same instance.

There are many datasets that have been introduced into the scientific literature. There should be some control as to how a dataset is introduced into the scientific literature, and ultimately utilized.

### Recommendations for GLP4OPT

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

Not every researcher will want to register a benchmark dataset, as defined in Section 4.2. For example, they may not want to wait for a separate paper to be peer reviewed enabling them to claim that they are using a registered dataset. Indeed, they may not be convinced that their dataset will stand up to the scientific review process but they still believe that the dataset is important in the context of their work.

### Recommendations for GLP4OPT

- [ ] R.15 If a researcher decides not to register a dataset that they use, they should still make the dataset available to the scientific community and should seek to respect recommendations R.6 to R.13. 

## Presentation of Solutions

Too often in the optimization research literature, when presenting the results of a simulation the researcher simply reports the value of the evaluation function. If another researcher wants to view the solution, to either verify that the evaluation is correct, or to simply inspect it to give insights for further research, the solution is often impossible to access. Occasionally, results are verified. A good example of this is the Traveling Tournament Problem (TTP) instances, introduced in (Easton et al., 2001). Before a result can be recognized on the [web site[4], the solution has to be sent to Michael Trick, one of the authors who established the benchmarks in (Easton et al., 2001), who will validate that it is correct.

### Recommendations for GLP4OPT

- [ ] R.16 When presenting the result of a simulation, any solution that is presented must be accompanied by the actual solution in the format that can be validated by R.8. The solutions that are presented (both the solution and its evaluation) should include all those referred to in the paper. For example, any solutions that are used in statistical analysis, or when tuning parameters (see R.41).

## Evidence of Hybridized Approaches

Many researchers are now using hybridized approaches to develop effective algorithms. It is important to provide evidence that the hybridized approach is actually effective.

### Recommendations for GLP4OPT

- [ ] R.17 If a hybridized algorithm is being presented then, unless previously reported in other work, the researchers should provide results from each non-hybridized element, using statistical analysis so that there is evidence that the hybridization is actually effective.

## Evaluation Function

The evaluation function is often the most important part of the paper and it is important to get this aspect of the paper correct.

### Recommendations for GLP4OPT

- [ ] R.18 The evaluation function must be described in a way that can be understood and implemented by other researchers.

- [ ] R.19 Referring to recommendation R.8 it should be possible for another researcher to test their implementation of an evaluation function to check that they have implemented it correctly and that it produces the same values as R.8.


## Algorithm Presentation

It is important that an algorithm is presented in a way that another researcher could reproduce it.

### Recommendations for GLP4OPT

- [ ] R.20 Any algorithm that is presented must be reproducible. This is one of the underpinning tenets of scientific research but some details are often missing, or vague. The optimization research community needs to ensure that all algorithms (and results) are reproducible.

- [ ] R.21 An algorithm should be presented in pseudo code, rather than a specific programming language. This is to stop any assumptions being made about another researchers' understanding on any given programming language.

- [ ] R.22 Attention should be given to areas such as variable initialization, how many iterations of certain lines are carried out, all (sub)operations are defined etc.

## Computational Times

Computational times have been an issue for a long time, and will remain so for the foreseeable future. The recommendations in this section, we hope, will resolve many of the issues.

### Recommendations for GLP4OPT

- [ ] R.23 The researcher should adopt the recommended computational times as provided in R. 10, stating which method they are using.

- [ ] R.24 A researcher is at liberty to use a different computational time, but it must be done in such a way that other researchers are able to use the same timings in future research (see recommendation R.28)

## Statistics

The question of which statistics to use is often problematical. However, if recommendation R.9 is adopted then each registered benchmark will come with a set of recommendations as to how different algorithms can be compared. Moreover, this recommendation would have undergone a peer review process so the community will have acknowledged that this statistical test is sufficient. In addition, recommendation R.16 will ensure that there is a sufficient number of solutions available (rather than just the best solution) so that the relevant statistical test has the correct data in order to be applied.

### Recommendations for GLP4OPT

- [ ] R.25 The necessary statistical test, as defined by R.9, should be applied to the relevant results (e.g. the best known solution and the solutions produced from the current study). 

## Experimental Conditions

One of the issues in comparing different algorithms is the environment on which those simulations were run. Whilst we can never account for different programming styles/skills there is a lot we can do to, at least, record the differences in the environment that other researchers will use in the future.

### Recommendations for GLP4OPT

- [ ] R.26 The full specification of the machine that was used for the experiments should be given. This should include the type of computer, the operating system and version number, the programming language that was used together with the compiler, the amount of memory available to the program, whether parallel processing was employed, if GPUs were utilized etc. Increasingly, researchers are using cloud services. These should also be reported in appropriate detail.

- [ ] R.27 The date(s) that the experiments were run should be given. This provides another point of reference for future researchers. This is important as the time between running experiments and the paper appearing in print could be a matter of years.

- [ ] R.28 For each main operating system the community will provide a test program ((Dongarra, 1992) might provide some inspiration for how this can be done) that can be run on a researcher's target machine. This will record the speed of the researcher's machine against some known baseline, informing the researcher how long they should run their algorithm to give a fair comparison with other researchers, particularly the original benchmark. See (McCollum et al., 2010) for an example of this method being used for an international competition.

The benchmark program will also provide a data file that can be stored as part of the paper that is subsequently published which future researchers can refer to in order to compare their algorithm's performance against previous algorithms.

## Laboratory Notebooks

As is the case with other scientific disciplines, optimization researchers should be encouraged to maintain a laboratory notebook and make these available to interested parties. Like some of the other recommendations, this is good scientific practice but is noted here so that there is no confusion.

### Recommendations for GLP4OPT

- [ ] R.29 Optimization researchers should maintain a laboratory notebook. These can be used by the researcher to record their thoughts, ideas and successes/failures and they also provide an important historic record for future researchers to refer to. 

- [ ] R.30 Researchers are encouraged to make available, via a supplementary file, the relevant parts of their notebooks, once a paper has been published.

- [ ] R.31 Other researchers should not be critical of notebooks, but should accept them for what they are. A notepad that provides a historic document of the research ideas, thoughts and timeline associated with a given piece of research.

## Software

Whether software should be provided as part of the peer review process, and subsequently made available to other researchers, is a moot point in optimization research, although we note that Bioinformatics generally insists on software being made available. There have been recent suggestions that software should be provided. Ince et al. (2012) argue that "anything less than the release of source programs is intolerable for results that depend on computation."

Having access to the software of another researcher would save a lot of time as algorithms would not have to be reimplemented. Moreover, it would remove one area where mistakes could be introduced due to errors/misunderstandings in implementation or the algorithm not being explained well enough to ensure that it can be reproduced.

On the other hand, many researchers are reluctant to provide their code as they might be embarrassed about their coding skills/style and they may feel that they might be asked to explain certain parts of the code or, indeed, provide support.

The fact that an algorithm works now, might not be the case when a new environment is used (e.g new operating systems, different compiler versions etc.). There may also be commercially sensitive reasons why the code should not be in the public domain and researchers may not want to make the code available which has been the result of an investment of weeks/months/years in developing the software.

However, we believe that software which underpins a scientific paper should be part of the peer reviewed scientific archive. This not only adds to the integrity of the discipline but also provides a historical reference that can be utilized by future researchers, perhaps for reasons other than algorithm reproducibility. This might include an historical perspective of programming languages, how coding styles have changed and how the implementations of the same algorithms differ.

### Recommendations for GLP4OPT

- [ ] R.32 It is beholden on the individual researcher(s) to keep a copy of the software that led to the contribution claimed in a given paper. Researcher(s) should retain an exact copy of the source code, the compiled code and any other environmental factors that are required to reproduce their results. If necessary, they should be able to re-run their algorithm and produce exactly the same results (see R.33), even years later.

- [ ] R.33 In the case of any dispute, authors can be asked to demonstrate their software to show that it produces the results claimed in the paper. This request can only come from the editor-in-chief (or their nominated representative) of the journal to which a paper has been submitted to, or published in.

- [ ] R.34 The source code for a given paper should be made available, under one of four categories:

    1. The source code is made freely available to other researchers

    2. The source code is not available to other researchers, but is available to the reviewers who can access the code using the accepted confidentially that is associated with reviewing scientific papers

    3. The source code is supplied, but is not made available to either researchers or the reviewers

    4. The source code is not made available at all

Unless the first option is chosen, a statement/justification must be given in the paper as to why the source code is being restricted. This statement will be subject to review and may be reason to recommend that the paper not be published.

- [ ] R.35 Supplying source code does imply that any support will be given to other researchers who later use, or access, the source code.

- [ ] R.36 The complete environment must be described so that anybody using the source code is able to replicate the computational conditions. As an example, the experimental setup might utilize Matlab, R or mathematical software. These elements need to be described in a manner that enables reproducibility.

- [ ] R.37 Source code associated with a published paper should be held in a repository that does not allow updates (any corrections should be done via an erratum) and which can be accessed via a permalink, in the same way that scientific papers are generally available via a DOI. This is to ensure that, like scientific papers, scientific researchers are accessing the same version of the source code as supplied by the authors.

In order to protect the scientific archive, the repository (or repositories) should be maintained by the scientific community, rather than an Open Source repository. 

- [ ] R.38 Only in exceptional circumstances will access be given to the code without the author's permission, and then only the editor-in-chief of the relevant journal can authorize this. Exceptional circumstances might include accusations of plagiarism, or suspicions of incorrect results being claimed.

- [ ] R.39 If all the authors have passed away, the software will be available to anybody that requests it, unless other arrangements have been made. This is to allow future researchers to access the code without any hindrance. There is no expectation of support of any kind from colleagues, or institutions.

## Parameter Selection and Values

All too often, researchers state that parameter values were set by initial experimentation, arriving at the values used in the paper. This misses many points of interest to the scientific community. For example:

- We are often not told what experiments were carried out to arrive at the values that were used

- We are often not informed how many experiments were run, or how long they took to arrive at the final values

- There is often no statistical analysis, comparing one set of parameters against another in order to demonstrate that a given set of parameter values is better than another or indeed whether the parameters are insensitive to change which could indicate a robust algorithm

- There is often no comparison with samples from outside the tested dataset to provide evidence, or not, that the parameters are robust to problem instances outside of those that are the real focus of the study

### Recommendations for GLP4OPT

- [ ] R.40 Be specific on how the parameter values were set, detailing the simulations that were carried out, to the point that these should be as reproducible as any other simulations reported in the paper.

- [ ] R.41 All the solutions that are used to compare the parameters should be made available to other researchers in the same way that the main solutions are also reported (see R.16).

- [ ] R.42 When making claims that one set of parameter values is better than another, a statistical analysis should support this claim.

- [ ] R.43 If no evidence is provided to the contrary, no claims should be made that the parameter values that were used for the main simulations presented in the paper are in any way robust, optimal or can be relied upon in other simulations to provide any level of solution quality. 

## Random Number Generation

Many papers simply state that a random number is generated, being drawn from a given distribution (e.g. normal, uniform etc.). Not only is the random number generator (RNG) key to reproducibility but the RNG that is used may have certain (sometimes undesirable) properties ((Hellekalek, 1998)). It should be noted that random number generation is applicable to both search methodologies, as well as instance generation.

### Recommendations for GLP4OPT

- [ ] R.44 The random number generator that was used should be explicitly stated. The coding lines that are used to generate each random variable should be presented, along with any preparatory steps (e.g. setting starting values, seeding the sequence).

- [ ] R.45 It should be possible for any researcher to generate the same sequence of random numbers, so that the simulation can be reproduced.

## Termination Criteria

In many papers it is often stated to carry out a sequence of algorithmic steps until some termination criteria are met. The exact criteria are often obscure or several choices are given and it is not clear which one has been used. For example, "repeat steps $n$ to $m$ until a certain period of time has passed or $q$ iterations have been performed". It should be possible to precisely ascertain the termination criteria that were used for any simulation that is presented.

### Recommendations for GLP4OPT

- [ ] R.46 Researchers should precisely define the termination criteria for any algorithm that is presented.

## GLP4OPT Adherence and Support

Evidence to demonstrate compliance with GLP4OPT should be provided as a supplementary file(s) to the main article. This enables authors to show compliance, without having to take up valuable space in the main article. In line with current practice, any supplementary files are subject to peer review.

If the recommendations in this paper are embraced by the community, this might lead to a web presence for GLP4OPT, which could reference, and link to, all the papers that have been peer reviewed in-line with the recommendations contained in this paper.

There may also be an opportunity for one of the Operations Research societies to lead on the GLP4OPT standard but we recognise that this is not a decision that is within the scope of this article and would be subject to much more discussion. In the remainder of this section, we provide specific recommendations as to what should constitute a supplementary file(s) and how a web site GLP4OPT might support the community in the future. Section 6 provides more thoughts as to how GLP4OPT might be progressed.

### Recommendations for GLP4OPT

- [ ] R.47 Any benchmarks that are introduced (see R.5 to R.14) into the scientific literature must be recorded in the journal's supplementary repository (see R.54).

- [ ] R.48 The GLP4OPT supplementary file must define which version of the standard has been used. As mentioned in the Introduction, the version introduced here is GLP4OPT version 1.00.

- [ ] R.49 If a journal or publisher has subscribed to GLP4OPT then it should insist on a supplementary file that reviewers can access to check against compliance with the standard. It should also be made available to those readers that are enable to access the main paper.

- [ ] R.50 Once (and if) established, the GLP4OPT web site will maintain the best known solutions for each registered dataset, along with a history of best known solutions (see R.12).

- [ ] R.51 ALL solutions that are referred to in a given paper must be uploaded to the journal as a supplementary file(s) (see R.13). This includes any solutions used to establish parameter settings (see R.41)

- [ ] R.52 Once (and if) established, the GLP4OPT web site will contain a repository of all the papers that have used a given registered benchmark dataset.

- [ ] R.53 Once (and if) established, the GLP4OPT web site will maintain the set of historical datasets (see (R.14), including best known solutions and all papers that have used those datasets.

- [ ] R.54 It is recognized that many of the data specified in this section might be held as a supplementary file on the journal's we site. In this case, the GLP4OPT web site will contain the necessary links to the supplementary data.

[3]: http://publicationethics.org/
[4]: http://mat.gsia.cmu.edu/TOURN/ 
