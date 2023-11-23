﻿---
weight: 3
title: "NRS"
---
## BF Name Resolution (NRS) Bugs Class <br/>_`Irena Bojanova, Inventor, Creator, PI,  Bugs Framework (BF)`_

#### Definition
{{< definition >}}The name of an object, a function, or a type is resolved improperly or bound to an improper type or implementation.{{< /definition >}}

####  Taxonomy


{{< img src="images/BF Classes/_DAT/NRS.png" >}}

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
			<td>Refer </td>
	<td>Use a name in local or remote scopes of source code. The Type System resolves the name and binds a data type to it.</td>
	</tr>
	<tr>
			<td>Call </td>
	<td>Invoke a function implementation. The Type System binds a function implementation to the resolved function name. A polymorphic function implementation is first resolved and then bound.</td>
	</tr>
	<tr>
			<td><strong>Operands</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Name </td>
	<td>The declared identifier for an entity.</td>
	</tr>
	<tr>
			<td>Type </td>
	<td>The data type of an object -- the set of allowed values (e.g., char is within [-128, 127]) and the operations allowed over them (e.g., +, *, mod).</td>
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
			<td>   Erroneous Code </td>
	<td>The operation implementation has a bug.</td>
	</tr>
	<tr>
			<td>Specification Defect Bug</td>
	<td>A specification (algorithm, protocol) of an operation an error or a rule (policy, keying material) used by the operation has an error, which when implemented becomes the bug causing the chain of weaknesses underlying a software security vulnerability. It must be fixed to fix the bug and to resolve the vulnerability.</td>
	</tr>
	<tr>
			<td>   Missing Qualifier </td>
	<td>A namespace include is absent; or a scope is not specified in a fully qualified name.</td>
	</tr>
	<tr>
			<td>   Wrong Qualifier </td>
	<td>A wrong namespace is included, or a wrong scope is specified in a fully qualified name.</td>
	</tr>
	<tr>
			<td>Name Fault</td>
	<td>The resolved name is wrong.</td>
	</tr>
	<tr>
			<td>   Missing Overridden Function </td>
	<td>Function implementation in a particular subclass is absent.</td>
	</tr>
	<tr>
			<td>   Missing Overloaded Function </td>
	<td>Code for particular function parameters' data types is absent.</td>
	</tr>
	<tr>
			<td>Type Fault</td>
	<td>The set or range of allowed values is wrong or the operations allowed on them are wrong.</td>
	</tr>
	<tr>
			<td>   Incomplete Type </td>
	<td>A specific constructor, method, or overloaded function is missing.</td>
	</tr>
	<tr>
			<td>   Wrong Generic Type </td>
	<td>A generic object is instantiated via wrong type argument.</td>
	</tr>
	<tr>
			<td>   Confused Subtype </td>
	<td>The object invoking an overridden function is of wrong subtype data type.</td>
	</tr>
	<tr>
			<td>   Wrong Argument Type </td>
	<td>An argument to an overloaded function is of incorrect data type.</td>
	</tr>
	<tr>
			<td><strong>Consequences</strong></td>
	<td><strong>Definition</strong></td>
	</tr>
	<tr>
			<td>Name Error</td>
	<td>The resolved name is wrong.</td>
	</tr>
	<tr>
			<td>   Wrong Object Resolved </td>
	<td>zzzxxx Object is resolved from wrong scope.</td>
	</tr>
	<tr>
			<td>   Wrong Function Resolved </td>
	<td>Function is resolved from wrong scope.</td>
	</tr>
	<tr>
			<td>   Wrong Generic Function Bound </td>
	<td>Code for a wrong data type is bound due to wrong generic type arguments.</td>
	</tr>
	<tr>
			<td>   Wrong Overridden Function Bound </td>
	<td>Code from wrong subtype is bound due to a wrong invoking subtype object.</td>
	</tr>
	<tr>
			<td>   Wrong Overloaded Function Bound </td>
	<td>Wrong overloaded implementation is bound due to wrong function arguments.</td>
	</tr>
	<tr>
			<td>Type Error</td>
	<td>The set or range of allowed values is wrong or the operations allowed on them are wrong.</td>
	</tr>
	<tr>
			<td>   Wrong Type Resolved </td>
	<td>A data type is resolved from a wrong scope.</td>
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
			<td>   Resolve </td>
	<td>Looking up a name and if needed determining its data type (infer from value, through hierarchy, via generic type attribute).</td>
	</tr>
	<tr>
			<td>   Bind </td>
	<td>Connect object data type, function return type, parameter data type, or simple function implementation.</td>
	</tr>
	<tr>
			<td>   Early Bind </td>
	<td>Resolving subtype and set generic function implementation.</td>
	</tr>
	<tr>
			<td>   Late Bind </td>
	<td>Resolving overridden function via subtype object and set implementation.</td>
	</tr>
	<tr>
			<td>   Ad-hoc Bind </td>
	<td>Resolve overloaded function via signature and set implementation.</td>
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
			<td>         Name Kind </td>
	<td>Shows what the entity with this name is.</td>
	</tr>
	<tr>
			<td>            Object </td>
	<td>A memory region used to store data.</td>
	</tr>
	<tr>
			<td>            Function </td>
	<td>An organized block of code that when called takes in data, processes it, and produces a result(s).</td>
	</tr>
	<tr>
			<td>            Data Type </td>
	<td>A set of allowed values and the operations allowed over them.</td>
	</tr>
	<tr>
			<td>            Namespace </td>
	<td>An organization of entities' names, utilized to avoid names collision.</td>
	</tr>
	<tr>
			<td>         Type Kind </td>
	<td>Shows what the data type composition is.</td>
	</tr>
	<tr>
			<td>            Primitive </td>
	<td>A scalar data type that mimics the hardware units - e.g., int (long, short, signed), float, double, string, Boolean. A primitive data type is only language defined and is not built from other data types.</td>
	</tr>
	<tr>
			<td>            Structure </td>
	<td>A composite data type - e.g., array, list, map, class. A structured data type is built from other data types and has primitive or structured members.</td>
	</tr>
	
</table>
</div>
{{< /rawhtml >}}

