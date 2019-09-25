# Modularity_Reactions

A number of different biochemical reactions are considered to be treated as modules in a function. 

To start with, a simple reaction ( A ⇋B ) was considered as a segment. The initial assumption is that the user can just import reactions with “one” substance (A) and “one” product (B). 
A ⟶Reaction 1 ⟶B_0  ⟶ Reaction 2 ⟶B_1  ⟶⋯

The substance (A) must be inserted by the user during the function operation but other elements are imported from the CellML file. 

The function catRecognition() asks from the user that which type of reaction is going to be connected. For the above-mentioned type, the answer would be ‘simple reaction (1)’ . The CellML file name, an arbitrary name for the final model, and the desired connections between the reactions are taken as inputs in the "main" function.
The function calls the simpleReactionOne file and the outputs would be initial conditions, bond graph model, and the control variables (rates of the reactions).

If the answer of the user was ‘simple reaction (2)’, the function calls the simpleReactionTwo file and the outputs would be initial conditions, bond graph model, and the control variables (rates of the reactions). In this section, unlike the ‘simple reaction (1)’, the inputs are extracted from a separate component in the CellML file.

Two sets of components are defined in Reactions.cellml file which for considering each set by the function, you need to mark the other sections as comments.
