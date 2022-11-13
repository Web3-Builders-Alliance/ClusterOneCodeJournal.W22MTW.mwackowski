# Cluster 1 Code Journal

Please find my notes listed in contract.rs file within /* */ block comments. 
I focused primarly on instantiate and execute methods as they required getting familiar with most of the contract file.

* What are the concepts/organization/mechanism?
Comments are provided in the code - both methods use either structs or enums. 
Borrowing and ownership are dictated by underlying methods but what I found most interesting was that instantiate() dependencies need to be mutable
as they are changed at the end of the method:

&nbsp;&nbsp;&nbsp;&nbsp;CONFIG.save(deps.storage, &config)?;
&nbsp;&nbsp;&nbsp;&nbsp;TOTAL.save(deps.storage, &0)?;
