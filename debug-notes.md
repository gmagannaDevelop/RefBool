# Problems encountered whilst executing the example

1. Hardcoded path, to a file unexistent within the repo.
   
   * I downloaded the appropriate files from [the link](https://webdav-r3lab.uni.lu/public/cbg/RefBool_ReferenceDistributions/) within `example/booleanize_example.m`'s  docstring. However,
     the he name of the hardcoded path does not match any
     file within `example/RefBool_ReferenceDistributions`.
     This path is not included as it is heavy `du -sh -> 357M`,
     and the provided link seems to work. 
     My best guess was that the file `'GeneOrderReference_CoTFCRF.txt'`
     
     should be replaced with `'RefBool_ReferenceDistributions/background_genes.txt'`.

2. Additional ToolBox required
   
   * Running the code yields the following error :
     
     ```{matlab}
      Error using CalculatePValues (line 16)
      Undefined function 'ecdf' for input arguments of type 'double'.
     ```
   
   * Suspecting a problem related to conflicting argument types I
     tried to look up `ecdf`'s documentation, to find that the function
     belongs to a separate toolbox which is not installed on the U-Psud
     server to which I have remote access.
     
     ```{matlab}
      >> help(ecdf)
      'ecdf' requires Statistics and Machine Learning Toolbox.
     ```
     
     I don't know if one must buy the ToolBox or if it can be 
     installed for free, as I am unfamiliar with MATLAB's
     inner workings and MATHWORKS' bussiness model.

   * I tried installing MATLAB on my computer but MATHWORKS refused
     saying that my university had no campus-wide access to licences.
     I tried both specifying Université Paris-Saclay and 
     Université Paris-Sud.

     


