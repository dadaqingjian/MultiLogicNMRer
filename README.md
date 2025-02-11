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

"**Facts_number**": 11, 

"**Defalut_Rules**": "-octagonal(X):-talkative(X),-drab(X), not -combative(X), not educational(X).strong(X):--busy(X),-persistent(X), not -hollow(X), not graceful(X).-educational(X):-fat(X),strong(X), not -poor(X).-poor(X):--octagonal(X), not -educational(X).-hollow(X):--octagonal(X), not strong(X), not beautiful(X).-combative(X):--amused(X), not -educational(X), not gleaming(X).significant(X):-faithful(X),energetic(X), not -poor(X).-old(X):--laugh(X,Y), not sudden(X).-amused(X):-love(X,Y),-average(X), not -crowded(X).aggressive(X):-mock(X,Y),-old(X), not -educational(X).", 

"**NL_Origin_Facts**": "Morgan is talkative.Morgan love Orson.Morgan is energetic.Morgan is not drab.Morgan is not persistent.Morgan is faithful.Morgan mock Orson.Morgan does not laugh Orson.Morgan is fat.Morgan is not busy.Morgan is not average.",

"**NL_Defalut_Rules**": "If someoneA is talkative and not drab then he is not octagonal,unless he is not combative or he is educational.If someoneA is not busy and not persistent then he is strong,unless he is not hollow or he is graceful.If someoneA is fat and strong then he is not educational ,unless he is not poor.If someoneA is not octagonal then he is not poor ,unless he is not educational.If someoneA is not octagonal then he is not hollow,unless he is strong or he is beautiful.If someoneA is not amused then he is not combative,unless he is not educational or he is gleaming.If someoneA is faithful and energetic then he is significant ,unless he is not poor.If someoneA does not laugh someoneB then he is not old ,unless he is sudden.If someoneA love someoneB and someoneA is not average then he is not amused ,unless he is not crowded.If someoneA mock someoneB and someoneA is not old then he is aggressive ,unless he is not educational.", 

"**Origin_ASP_extension_number**": 1, 

"**Origin_Question_Text_Lists**": ["-octagonal(morgan).", "-strong(morgan).", "-poor(morgan)."], 

"**NL_Origin_Question_Text**": ["Morgan is not octagonal.", "Morgan is not strong.", "Morgan is not poor."], 

"**Origin_Question_Label_Lists**": [["T"], ["F"], ["M"]], 

}


