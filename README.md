<div id="header">

<div id="nav" class="container">

-   [FEATURED](index.html){.item}
-   [PUBLICATIONS](pub.html){.item}
-   [SOFTWARES](soft.html){.item}
-   [ABOUT](bio.html){.item}

</div>

</div>

<div class="container container_top">

Software for Factorized Graph Matching
======================================

<div class="down_button">

[DOWNLOAD](http://humansensing.cs.cmu.edu/down_fgm.html){.level3}

</div>

<div class="line_wrap">

<div class="line_content">

Introduction
------------

</div>

</div>

<div class="sec_content">

This page contains software and instructions for [factorized graph
matching
(FGM)](gm.html){.level3}^[<span>\[</span>1<span>\]</span>](#ref1)[<span>\[</span>2<span>\]</span>](#ref2)^.
In addition, we include the following state-of-the-arts methods as
baselines:

-   [spectral
    matching (SM)](https://sites.google.com/site/graphmatchingmethods/){.level3}^[<span>\[</span>3<span>\]</span>](#ref3)^,
-   [spectral matching with affine
    constraints (SMAC)](http://www.timotheecour.com/software/graph_matching/graph_matching.html){.level3}^[<span>\[</span>4<span>\]</span>](#ref4)^,
-   [graduated
    assignment (GA)](http://www.timotheecour.com/software/graph_matching/graph_matching.html){.level3}^[<span>\[</span>5<span>\]</span>](#ref5)^,
-   [probabilistic
    matching (PM)](http://www.cs.huji.ac.il/~zass/gm){.level3}^[<span>\[</span>6<span>\]</span>](#ref6)^,
-   [integer projected fixed point
    method (IPFP)](https://sites.google.com/site/graphmatchingmethods/){.level3}^[<span>\[</span>7<span>\]</span>](#ref7)^,
-   [re-weighted random walk
    matching (RRWM)](http://cv.snu.ac.kr/research/~RRWM/){.level3}^[<span>\[</span>8<span>\]</span>](#ref8)^.

The implementations of the above methods are taken from the authors'
websites (The code of GA was also implemented in the code of SMAC). We
appreciate all the authors for their generosity in sharing codes.

</div>

<div class="line_wrap">

<div class="line_content">

Installation
------------

</div>

</div>

<div class="sec_content">

+--------------------------------------+--------------------------------------+
| <div class="line-numbers">           | <div class="commands">               |
|                                      |                                      |
| <span class="line">1</span> <span    | <span class="line">&gt;&gt; <span    |
| class="line">2</span> <span          | class="nb">cd</span> <span           |
| class="line"> </span> <span          | class="nv">fgm</span></span> <span   |
| class="line"> </span> <span          | class="line">&gt;&gt; <span          |
| class="line">3</span> <span          | class="nb">ls</span></span> <span    |
| class="line">4</span> <span          | class="line">make.m addPath.m        |
| class="line">5</span>                | demoToy.m demoHouse.m testToy.m      |
|                                      | testHouse.m README.md</span> <span   |
| </div>                               | class="line"><span                   |
|                                      | class="nv">data</span> <span         |
|                                      | class="nv">save</span> <span         |
|                                      | class="nv">src</span> <span          |
|                                      | class="nv">lib</span></span> <span   |
|                                      | class="line">&gt;&gt; <span          |
|                                      | class="na">make</span></span> <span  |
|                                      | class="line">&gt;&gt; <span          |
|                                      | class="na">addPath</span></span>     |
|                                      | <span class="line">&gt;&gt; <span    |
|                                      | class="na">demoHouse</span></span>   |
|                                      |                                      |
|                                      | </div>                               |
+--------------------------------------+--------------------------------------+

</div>

<div class="line_wrap">

<div class="line_content">

Package Content
---------------

</div>

</div>

<div class="sec_content">

The package of <span class="key_word">fgm.zip</span> contains following
folders and files:
+--------------------------------------+--------------------------------------+
| <span class="key_word">data</span>:  | This folder contains the [CMU House  |
|                                      | image                                |
|                                      | dataset](http://vasc.ri.cmu.edu/idb/ |
|                                      | html/motion/house/){.level3}.        |
+--------------------------------------+--------------------------------------+
| <span class="key_word">save</span>:  | This folder contains the             |
|                                      | experimental results reported in the |
|                                      | paper.                               |
+--------------------------------------+--------------------------------------+
| <span class="key_word">src</span>:   | This folder contains the main        |
|                                      | implementation of FGM as well as     |
|                                      | other baselines.                     |
+--------------------------------------+--------------------------------------+
| <span class="key_word">lib</span>:   | This folder contains some necessary  |
|                                      | library functions.                   |
+--------------------------------------+--------------------------------------+
| <span                                | Matlab makefile for C++ code.        |
| class="key_word">make.m</span>:      |                                      |
+--------------------------------------+--------------------------------------+
| <span                                | Adds the sub-directories into the    |
| class="key_word">addPath.m</span>:   | path of Matlab.                      |
+--------------------------------------+--------------------------------------+
| <span                                | A demo comparison of different graph |
| class="key_word">demoToy.m</span>:   | matching methods on the synthetic    |
|                                      | dataset.                             |
+--------------------------------------+--------------------------------------+
| <span                                | A demo comparison of different       |
| class="key_word">demoHouse.m</span>: | matching methods on the [CMU House   |
|                                      | image                                |
|                                      | dataset](http://vasc.ri.cmu.edu/idb/ |
|                                      | html/motion/house/){.level3}.        |
+--------------------------------------+--------------------------------------+
| <span                                | Testing the performance of different |
| class="key_word">testToy.m</span>:   | graph matching methods on the        |
|                                      | synthetic dataset.                   |
|                                      | <div class="addition">               |
|                                      |                                      |
|                                      | This is a similar function used for  |
|                                      | reporting (Fig. 4) the first         |
|                                      | experiment (Sec 5.1) in the CVPR     |
|                                      | 2012                                 |
|                                      | paper^[<span>\[</span>2<span>\]</spa |
|                                      | n>](#ref2)^.                         |
|                                      |                                      |
|                                      | </div>                               |
+--------------------------------------+--------------------------------------+
| <span                                | Testing the performance of different |
| class="key_word">testHouse.m</span>: | graph matching methods on the [CMU   |
|                                      | House image                          |
|                                      | dataset](http://vasc.ri.cmu.edu/idb/ |
|                                      | html/motion/house/){.level3}.        |
|                                      | <div class="addition">               |
|                                      |                                      |
|                                      | This is the same function used for   |
|                                      | reporting (Fig. 4) the first         |
|                                      | experiment (Sec 5.1) in the CVPR     |
|                                      | 2013                                 |
|                                      | paper^[<span>\[</span>1<span>\]</spa |
|                                      | n>](#ref1)^.                         |
|                                      |                                      |
|                                      | </div>                               |
+--------------------------------------+--------------------------------------+

</div>

<div class="line_wrap">

<div class="line_content">

FAQs
----

</div>

</div>

<div class="sec_content">

<div class="faq_panel">

Compiler error "Unrecognized switch: -argcheck".
------------------------------------------------

<div class="faq_panelcontent">

This might due to the fact that your Windows c++ compiler cannot
recognize the argument "-argcheck". To fix it, you can modify <span
class="key_word">make.m</span> from line 22 as follows:
<div class="commands">

<span class="line">cd 'src/asg/smac/graph\_matching\_SMAC/cpp';</span>
<span class="line">mex -largeArrayDims
mex\_ICM\_graph\_matching.cpp</span> <span class="line">mex
-largeArrayDims mex\_classes2indexes.cpp</span> <span class="line">mex
-largeArrayDims mex\_computeRowSum.cpp</span> <span class="line">mex
-largeArrayDims mex\_find\_next\_nonzero.cpp</span> <span
class="line">mex -largeArrayDims mex\_ind2rgb8.cpp</span> <span
class="line">mex -largeArrayDims mex\_ind2sub.cpp</span> <span
class="line">mex -largeArrayDims mex\_istril.cpp</span> <span
class="line">mex -largeArrayDims mex\_matchingW2.cpp</span> <span
class="line">mex -largeArrayDims mex\_normalizeColumns.cpp</span> <span
class="line">mex -largeArrayDims mex\_normalizeMatchingW.cpp</span>
<span class="line">mex -largeArrayDims
mex\_projection\_QR\_symmetric.cpp</span> <span class="line">mex
-largeArrayDims mex\_projection\_affine\_symmetric.cpp</span> <span
class="line">mex -largeArrayDims
mex\_w\_times\_x\_symmetric\_tril.cpp</span> <span class="line">mex
-largeArrayDims spmtimesd.cpp</span> <span
class="line">%compileDir;</span> <span class="line">cd(path0);</span>

</div>

<span class="addition">Thanks [Syshiei](){.level1}'s for providing the
solution.</span>

</div>

</div>

</div>

<div class="sec_content">

<div class="faq_panel">

Which functions are implemented in C++?
---------------------------------------

<div class="faq_panelcontent">

We provide several C++ codes under <span
class="key_word">src/asg/fgm/matrix</span> to perform matrix products
between binary matrices in a more efficient way. For instance, the
function <span class="key_word">multiGXH.cpp</span> is used to more
efficiently compute the matrix product, <span class="key_word">G\^T \* X
\* H</span>, where <span class="key_word">G</span> and <span
class="key_word">H</span> are two binary matrices.

</div>

</div>

</div>

<div class="line_wrap">

<div class="line_content">

Change Log
----------

</div>

</div>

<div class="sec_content">

-   <div class="date">

    2013-05-08:

    </div>

    <div class="detail">

    <div class="log_item">

    Add the implementations of the FGM-D, SMAC, PM, GA, IPFP-U, IPFP-S
    and RRWM.

    </div>

    <div class="log_item">

    Update the demo file by including FGM-D and more baselines for
    synthetic data and [CMU House Image
    dataset](http://vasc.ri.cmu.edu/idb/html/motion/house/){.level3}.

    </div>

    <div class="log_item">

    Add a testing file for reproducing the reported experimental result
    on matching 100 pairs of synthetic graphs.

    </div>

    <div class="log_item">

    Add a testing file for reproducing the reported experimental result
    on matching the [CMU House Image
    dataset](http://vasc.ri.cmu.edu/idb/html/motion/house/){.level3}.

    </div>

    </div>

-   <div class="date">

    2012-05-12:

    </div>

    <div class="detail">

    <div class="log_item">

    Add the implementation of FGM-U and SM.

    </div>

    <div class="log_item">

    Add a demo file for synthetic data.

    </div>

    <div class="log_item">

    Add a demo file for [CMU House Image
    dataset](http://vasc.ri.cmu.edu/idb/html/motion/house/){.level3}.

    </div>

    </div>

</div>

<div class="line_wrap">

<div class="line_content">

References
----------

</div>

</div>

<div class="sec_content">

-   <div id="ref1" class="index">

    \[1\]

    </div>

    <div class="detail">

    <span class="pub_info_title">Deformable Graph Matching</span>
    <div class="pub_info_other">

    IEEE Conference on Computer Vision and Pattern Recognition (CVPR),
    2013\
    F. Zhou and [F. De la Torre](http://www.cs.cmu.edu/~ftorre){.level1}

    </div>

    </div>

-   <div id="ref2" class="index">

    \[2\]

    </div>

    <div class="detail">

    <span class="pub_info_title">Factorized Graph Matching</span>
    <div class="pub_info_other">

    IEEE Conference on Computer Vision and Pattern Recognition (CVPR),
    2012\
    F. Zhou and [F. De la Torre](http://www.cs.cmu.edu/~ftorre){.level1}

    </div>

    </div>

-   <div id="ref3" class="index">

    \[3\]

    </div>

    <div class="detail">

    <span class="pub_info_title">A Spectral Technique for Correspondence
    Problems Using Pairwise Constraints</span>
    <div class="pub_info_other">

    International Conference on Computer Vision (ICCV), 2005\
    [M. Leordeanu](http://109.101.234.42/people.php?ID_p=11){.level1}
    and [M. Hebert](http://www.cs.cmu.edu/~hebert/){.level1}

    </div>

    </div>

-   <div id="ref4" class="index">

    \[4\]

    </div>

    <div class="detail">

    <span class="pub_info_title">Balanced Graph Matching</span>
    <div class="pub_info_other">

    Advances in Neural Information Processing Systems (NIPS), 2006\
    [T. Cour](http://www.timotheecour.com/){.level1}, P. Srinivasan and
    [J. Shi](http://www.cis.upenn.edu/~jshi/){.level1}

    </div>

    </div>

-   <div id="ref5" class="index">

    \[5\]

    </div>

    <div class="detail">

    <span class="pub_info_title">A Graduated Assignment Algorithm for
    Graph Matching</span>
    <div class="pub_info_other">

    IEEE Transactions on Pattern Analysis and Machine Intelligence
    (PAMI), 1996\
    S. Gold and [A.
    Rangarajan](http://www.cise.ufl.edu/~anand/){.level1}

    </div>

    </div>

-   <div id="ref6" class="index">

    \[6\]

    </div>

    <div class="detail">

    <span class="pub_info_title">Probabilistic Graph and Hypergraph
    Matching</span>
    <div class="pub_info_other">

    IEEE Conference on Computer Vision and Pattern Recognition (CVPR),
    2008\
    R. Zass and [A.
    Shashua](http://www.cs.huji.ac.il/~shashua/){.level1}

    </div>

    </div>

-   <div id="ref7" class="index">

    \[7\]

    </div>

    <div class="detail">

    <span class="pub_info_title">An Integer Projected Fixed Point Method
    for Graph Matching and MAP Inference</span>
    <div class="pub_info_other">

    Advances in Neural Information Processing Systems (NIPS), 2009\
    [M. Leordeanu](http://109.101.234.42/people.php?ID_p=11){.level1},
    [M. Hebert](http://www.cs.cmu.edu/~hebert/){.level1} and [R.
    Sukthankar](http://www.cs.cmu.edu/~rahuls/){.level1}

    </div>

    </div>

-   <div id="ref8" class="index">

    \[8\]

    </div>

    <div class="detail">

    <span class="pub_info_title">Reweighted Random Walks for Graph
    Matching</span>
    <div class="pub_info_other">

    European Conference on Computer Vision (ECCV), 2010\
    [M. Cho](http://cv.snu.ac.kr/~minsucho/){.level1}, [J.
    Lee](http://cv.snu.ac.kr/~jungminlee/){.level1} and [K.
    Lee](http://cv.snu.ac.kr/kmlee){.level1}

    </div>

    </div>

</div>

<div class="line_wrap">

<div class="line_content">

Copyright
---------

</div>

</div>

<div class="sec_content">

This software is free for use in research projects. If you publish
results obtained using this software, please use this citation:

<span class="line">@article{ZhouD16,</span> <span
class="line">    author = {Feng Zhou and Fernando {De la Torre}},</span>
<span class="line">    title = {Factorized Graph Matching},</span> <span
class="line">    journal = {Transactions on Pattern Analysis and Machine
Intelligence (PAMI)},</span> <span class="line">    year =
{2016},</span> <span class="line">    volume = {38},</span> <span
class="line">    number = {9},</span> <span class="line">    pages =
{1774-1789},</span> <span class="line">}</span>
Contributing back bug fixes and improvements is polite and encouraged.
If you have any question, feel free to contact [Feng
Zhou](http://www.f-zhou.com){.level1}.

</div>

</div>

<div class="footer">

</div>

