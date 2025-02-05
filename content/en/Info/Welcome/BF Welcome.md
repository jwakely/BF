---
weight: 2
bookCollapseSection: false
title: "BF Welcome"
url: /
---
<!-- <l style="color: #7D3368; font-size:32px">xxx</> -->
<!-- <div style="text-indent: 40px"> </div>-->
# Bugs Framework: <l style="color: #0428AE">Formalizing Software Security Weaknesses and Vulnerabilities</l><br/>_`Irena Bojanova, PI & Lead, NIST Bugs Framework (BF), 2014 – ~~~~`_
<!-- ## <l style="color: #0428AE">Formalizing Software Security Bugs, Weaknesses, and Vulnerabilities</l><l style="color: black">!<l/><br/>_`Irena Bojanova, PI & Lead, NIST Bugs Framework (BF), 2014 – ~~~~`_</l> -->
<!-- Software Developers 'Best Friend' -->
Bugs Framework (BF) is being created as a structured classification system of software security bugs, faults, and weaknesses that allows unambiguous formal specification of the software security vulnerabilities. It comprises:

<div style="text-indent: 40px">

➢ Software security _[concepts definitions](/BF/info/vulnerability-model/bf-concepts/)_

➢ A _Bugs model_ with possible flow of operations

➢ A structured, complete, orthogonal, language and domain independent weakness _[taxonomy](/BF/info/bf-classes)_

➢ A  _[vulnerability model](/BF/info/vulnerability-model/bf-vulnerability-model/)_ of weakness chains leading to failures

➢ An _LL(1) formal language_ for specification of weaknesses and vulnerabilities

➢ A _database_ for querying weakness and vulnerability repositories and scoring systems towards BF

➢ _Tools_ for generation of BF CWE  and BF CVE formal specifications and  visualization of BF classes and BF specifications. 

</div>

_Structured_ means a weakness is described via one _cause_, one _operation_, one _consequence_, and _attributes_ from the lists defining a BF class (see [BF concepts](/BF/info/vulnerability-model/bf-concepts/)).This assures precise causal descriptions as _(bug, operation, error)_ and _(fault, operation, error)_ triples. _Complete_ means BF has the expressive power to describe precisely any software security bug and weakness. This assures the BF weakness types have no gaps in coverage. _Orthogonal_ means the sets of operations of any two BF classes do not overlap. This assures the BF weakness types do not overlap,  as there is no operation with different meanings. _Language and domain independent_ means BF is applicable for source code in any programming language for any platform, operating environment, or application technology. This assures BF is context-free, as an operation cannot have different meanings depending on the context.

The BF _bug model_ combines the _bug models_ of particular BF cluster of classes that reveal possible chains of weaknesses within a particular BF cluster of classes.

The BF _vulnerability model_ defines how software security weaknesses chain via cause–consequence–cause transitions to form a vulnerability that ends with a software security failure. This assures back-tracking from the failure through the errors to the bug. 

The BF _formal language_ is generated by the BF LL(1) context-free formal grammar with lexicon defined by the [BF Taxonomy](/BF/info/bf-classes) and syntax defined by the BF [Vulnerability Model](/BF/info/vulnerability-model/bf-vulnerability-model/). This assures the BF specifications are unambiguous!

<l style="font-size: 15px; color: #0428AE">_BF CITATION: Irena Bojanova, NIST Bugs Framework (BF), Accessed: <span id="currentDate"></span>. [Online]. Available: [https://usnistgov.github.io/BF](https://usnistgov.github.io/BF)._</l>

<l style="font-size: 15px; color: #7D3368">Note: Any BF-application publication that lists classes not featured on this website is a misrepresentation of BF. If in doubt, please [seek guidance from the BF PI](/BF/info/contact/bf-contact). 

## BF Intro Presentations

<br/>
{{< rawhtml >}} 
BF Terminology and Existing Repositories:
<br/><br/>
<div class="row">
<div class="col-9">
{{< youtube TYoJAfo3Mu0 >}}
</div>
</div>

<div class="row">
<div class="col-9">
<br/><br/>
BF Goals, Features, and Taxonomy <br/>
(contuniation of the previous presentation):
<br/><br/>
{{< youtube QnCPXHLi7JQ >}}
</div>
</div>

<div class="row">
<div class="col-9">
<br/><br/>
BF Hands On and Potential Impacts <br/>
(contuniation of the previous presentation):
<br/><br/>
{{< youtube XfAuRp5GcrE >}}
</div>
</div>

{{< /rawhtml >}}

<br/><br/>


<script>
    document.addEventListener('DOMContentLoaded', function() {
        const currentDateElement = document.getElementById('currentDate');
        const currentDate = new Date().toLocaleString('en-US', {
            year: 'numeric', 
            month: '2-digit', 
            day: '2-digit'
        });
        currentDateElement.textContent = currentDate;
    });
</script>