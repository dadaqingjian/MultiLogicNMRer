# MultiLogicNMRer

This file is a resource library titled "MultiLogicNMR(er): A Benchmark and Neural-Symbolic Framework for Non-monotonic Reasoning Tasks with Multiple Extensions"

## Dataset Description

The Datasets directory contains three sub-datasets (MultiLogicNMR, MultiLogicNMR_OOD, MultiLoigcNMR_NL), each of which contains datasets in credulous reasoning mode and skeptical reasoning mode. MultiLogicNMR is a multi-extended non-monotonic reasoning dataset generated based on a template; MultiLogicNMR_OOD is a non-monotonic reasoning dataset generated based on a template for evaluating the generalization ability of the model in terms of extended quantity; MultiLogicNMR_NL is a multi-extended non-monotonic reasoning dataset rewritten by a large language model.

### The data sample format is as follows:

{

% Sample No.

"**Sample_number**": "1", 

% A set of facts expressed in a formal language

"**Origin_Facts**": "talkative(morgan).love(morgan,orson).energetic(morgan).-drab(morgan).-persistent(morgan).faithful(morgan).mock(morgan,orson).-laugh(morgan,orson).fat(morgan).-busy(morgan).-average(morgan).", 

% The number of facts included in the sample

"**Facts_number**": 11, 

% A set of rules expressed in a formal language (default rules)

"**Defalut_Rules**": "-octagonal(X):-talkative(X),-drab(X), not -combative(X), not educational(X).strong(X):--busy(X),-persistent(X), not -hollow(X), not graceful(X).-educational(X):-fat(X),strong(X), not -poor(X).-poor(X):--octagonal(X), not -educational(X).-hollow(X):--octagonal(X), not strong(X), not beautiful(X).-combative(X):--amused(X), not -educational(X), not gleaming(X).significant(X):-faithful(X),energetic(X), not -poor(X).-old(X):--laugh(X,Y), not sudden(X).-amused(X):-love(X,Y),-average(X), not -crowded(X).aggressive(X):-mock(X,Y),-old(X), not -educational(X).", 

% A collection of factual sentences represented in natural language

"**NL_Origin_Facts**": "Morgan is talkative.Morgan love Orson.Morgan is energetic.Morgan is not drab.Morgan is not persistent.Morgan is faithful.Morgan mock Orson.Morgan does not laugh Orson.Morgan is fat.Morgan is not busy.Morgan is not average.",

% A set of rules for natural language representation

"**NL_Defalut_Rules**": "If someoneA is talkative and not drab then he is not octagonal,unless he is not combative or he is educational.If someoneA is not busy and not persistent then he is strong,unless he is not hollow or he is graceful.If someoneA is fat and strong then he is not educational ,unless he is not poor.If someoneA is not octagonal then he is not poor ,unless he is not educational.If someoneA is not octagonal then he is not hollow,unless he is strong or he is beautiful.If someoneA is not amused then he is not combative,unless he is not educational or he is gleaming.If someoneA is faithful and energetic then he is significant ,unless he is not poor.If someoneA does not laugh someoneB then he is not old ,unless he is sudden.If someoneA love someoneB and someoneA is not average then he is not amused ,unless he is not crowded.If someoneA mock someoneB and someoneA is not old then he is aggressive ,unless he is not educational.", 

% The number of extensions included in this sample

"**Origin_ASP_extension_number**": 1, 

% Questions with formal language representation

"**Origin_Question_Text_Lists**": ["-octagonal(morgan).", "-strong(morgan).", "-poor(morgan)."], 

% Questions with natural language representation

"**NL_Origin_Question_Text**": ["Morgan is not octagonal.", "Morgan is not strong.", "Morgan is not poor."], 

% The Label of the questions

"**Origin_Question_Label_Lists**": [["T"], ["F"], ["M"]], 

}

## Code Description
The Code file contains three sub-files (**Models_on_MultiLogicNMR, Models_on_MultiLogicNMR_OOD, Models_on_MultiLogicNMR_NL**), which respectively represent the execution code of the neural symbolic model (MultiLogicNMRer) proposed in the paper on different datasets. For example, the Iterative_NeSy_NMR_Solver_on_credulous_by_DeepSeek.py file in the Models_on_MultiLogicNMR file refers to the execution code of the neural symbolic framework MultiLogicNMRer proposed with DeepSeek as the basic model on the credulous reasoning subset in the MultiLogicNMR dataset.


