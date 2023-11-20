﻿---
weight: 3
title: "DVR"
---
## BF Data Verification (DVR) Bugs Class <br/>_`Irena Bojanova, Inventor, Creator, PI Bugs Framework (BF)`_

#### Definition
{{< definition >}}Data are verified (semantics check) or corrected (assign, remove) improperly.{{< /definition >}}

####  Taxonomy


{{< img src="images/BF Classes/_INP/DVR.png" >}}

<table>
<tr>
<td>
<button class="btn btn-primary " type="button" data-bs-toggle="collapse" data-bs-target="#collapseTable" aria-expanded="false" aria-controls="collapseTable">Show/Hide Definitions</button>
</td>
</tr>
</table>
	
{{< rawhtml >}}
<div class="collapse" id="collapseTable">
<table>
<tr>
			<td><strong>Operations</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Verify </td>
	<td>Check data semantics (proper value/meaning) in order to accept (and possibly correct) or reject it.</td>
	</tr>
	<tr>
			<td>Correct </td>
	<td>Modify data (assign new value, remove) to make it accurate.</td>
	</tr>
	<tr>
			<td><strong>Operands</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Data </td>
	<td>The data value of an object -- stored in object's memory.</td>
	</tr>
	<tr>
			<td><strong>Causes</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Code Defect Bug</td>
	<td>The operation has a bug, which is the first cause for the chain of weaknesses underlying a software security vulnerability. The bug must be fixed to resolve the vulnerability.</td>
	</tr>
	<tr>
			<td>   Missing Code </td>
	<td>The entire operation implementation or a part of its specification is absent.</td>
	</tr>
	<tr>
			<td>   Erroneous Code </td>
	<td>The operation implementation has a bug.</td>
	</tr>
	<tr>
			<td>Specification Defect Bug</td>
	<td>A specification (algorithm, protocol) of an operation an error or a rule (policy, keying material) used by the operation has an error, which when implemented becomes the bug causing the chain of weaknesses underlying a software security vulnerability. It must be fixed to fix the bug and to resolve the vulnerability.</td>
	</tr>
	<tr>
			<td>   Under-Restrictive Policy </td>
	<td>Accepts bad data.</td>
	</tr>
	<tr>
			<td>   Over-Restrictive Policy </td>
	<td>Rejects good data.</td>
	</tr>
	<tr>
			<td>Data Fault</td>
	<td>The object data has harmed semantics or inconsistent or wrong value</td>
	</tr>
	<tr>
			<td>   Invalid Data </td>
	<td>Data with harmed syntax due to sanitization errors.</td>
	</tr>
	<tr>
			<td><strong>Consequences</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Data Error</td>
	<td>The object data has harmed semantics or inconsistent or wrong value</td>
	</tr>
	<tr>
			<td>   Wrong Value </td>
	<td>Data value is not accurate value (e.g., outside of a range).</td>
	</tr>
	<tr>
			<td>   Inconsistent Value </td>
	<td>Data value does not correspond to the value of a related data (e.g., inconstancy between the value of a size variable and the actual buffer size).</td>
	</tr>
	<tr>
			<td>Type Error</td>
	<td>The set or range of allowed values is wrong or the operations allowed on them are wrong.</td>
	</tr>
	<tr>
			<td>   Wrong Type </td>
	<td>A data type range or structure is not correct.</td>
	</tr>
	<tr>
			<td><strong>Operations Attributes</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Mechanism </td>
	<td>Shows how the buggy/faulty operation code is performed.</td>
	</tr>
	<tr>
			<td>   Value </td>
	<td>Checking data for a specific value (incl. NULL or list of values).</td>
	</tr>
	<tr>
			<td>   Quantity </td>
	<td>Checking data for a specific measurable value (e.g., size, time, rate, frequency).</td>
	</tr>
	<tr>
			<td>   Range </td>
	<td>Checking data are within a (min, max) interval.</td>
	</tr>
	<tr>
			<td>   Data Type </td>
	<td>A set of allowed values and the operations allowed over them.</td>
	</tr>
	<tr>
			<td>   Other Rules </td>
	<td>Check data against other business logic.</td>
	</tr>
	<tr>
			<td>Source Code </td>
	<td>Shows where the buggy/faulty operation code is in the program -- in what kind of software.</td>
	</tr>
	<tr>
			<td>   Codebase </td>
	<td>The operation is in the programmer's code - in the application itself.</td>
	</tr>
	<tr>
			<td>   Third-Party </td>
	<td>The operation is in a third-party software.</td>
	</tr>
	<tr>
			<td>   Standard Library </td>
	<td>The operation is in the standard library for a particular programming language.</td>
	</tr>
	<tr>
			<td>   Compiler/Interpreter </td>
	<td>The operation is in the language processor that allows execution or creates executables (compiler, assembler, interpreter).</td>
	</tr>
	<tr>
			<td>Execution Space </td>
	<td>Shows where the buggy/faulty operation code is running or with what privilege level).</td>
	</tr>
	<tr>
			<td>   Local </td>
	<td>The bugged code runs in an environment with access control policy with limited (local user) permission.</td>
	</tr>
	<tr>
			<td>   Admin </td>
	<td>The bugged code runs in an environment with access control policy with unlimited (admin user) permission.</td>
	</tr>
	<tr>
			<td>   Bare-Metal </td>
	<td>The bugged code runs in an environment without privilege control. Usually, the program is the only software running and has total access to the hardware.</td>
	</tr>
	<tr>
			<td><strong>Operands Attributes</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>         Data State </td>
	<td>Shows where the data come from.</td>
	</tr>
	<tr>
			<td>            Entered </td>
	<td>The data are from a user via a user interface (e.g., text field).</td>
	</tr>
	<tr>
			<td>            Stored </td>
	<td>The data are from a permanent storage (e.g., file, database on a storage device).</td>
	</tr>
	<tr>
			<td>            In Use </td>
	<td>The data are from a volatile storage (e.g., RAM, cache memory).</td>
	</tr>
	<tr>
			<td>            Transferred </td>
	<td>The data are from another device via a network (e.g., connecting analog device or another computer).</td>
	</tr>
	
</table>
</div>
{{< /rawhtml >}}

