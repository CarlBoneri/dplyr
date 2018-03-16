# unknown

## mudata2 (introduced in 68d90b4d)

- `library(mudata2); example(ns_climate)`
- https://github.com/paleolimbot/mudata/issues/26

Version: 1.0.0

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    
    > ns_climate %>% 
    +   select_locations(sable_island = starts_with("SABLE"),
    +                    nappan = starts_with("NAPPAN"), 
    +                    baddeck = starts_with("BADDECK")) %>% 
    +   select_params(ends_with("temp")) %>%
    +   filter_data(month(date) == 6) %>% 
    +   autoplot()
    Warning: Unknown or uninitialised column: 'param'.
    Warning: Unknown or uninitialised column: 'location'.
    Warning: Unknown or uninitialised column: 'dataset'.
    Not all values were found: SABLE ISLAND 6454, NAPPAN CDA 6414, BADDECK 6297
    Warning: Unknown or uninitialised column: 'param'.
    Warning: Unknown or uninitialised column: 'location'.
    Warning: Unknown or uninitialised column: 'dataset'.
    Warning: Unknown or uninitialised column: 'param'.
    Warning: Unknown or uninitialised column: 'location'.
    Warning: Unknown or uninitialised column: 'dataset'.
    Error in long_plot_base(.data, ...) : .data contains no data
    Calls: %>% ... autoplot -> autoplot.mudata -> long_ggplot -> long_plot_base
    Execution halted
    ```

*   checking tests ...
    ```
     ERROR
    Running the tests in ‘tests/test-all.R’ failed.
    Last 13 lines of output:
      OGR: Unsupported geometry type
      ══ testthat results  ═══════════════════════════════════════════════════════════
      OK: 836 SKIPPED: 0 FAILED: 9
      1. Error: read/write JSON functions work (@test_mudata.io.R#141) 
      2. Error: read/write directory functions work (@test_mudata.io.R#435) 
      3. Failure: mudata objects subset properly (@test_mudata_subset.R#14) 
      4. Failure: mudata objects subset properly (@test_mudata_subset.R#23) 
      5. Failure: mudata objects subset properly (@test_mudata_subset.R#28) 
      6. Failure: mudata objects subset properly (@test_mudata_subset.R#30) 
      7. Error: recombined subsetted objects are the same as the original (@test_mudata_subset.R#72) 
      8. Error: filter_* functions work as expected (@test_mudata_subset.R#79) 
      9. Error: rename works when some values are factors (@test_rename.R#68) 
      
      Error: testthat unit tests failed
      Execution halted
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    Warning: Removed 85 rows containing missing values (geom_path).
    Quitting from lines 176-184 (mudata.Rmd) 
    Error: processing vignette 'mudata.Rmd' failed with diagnostics:
    object 'mean_temp' not found
    Execution halted
    ```

## nonmemica

- `library(nonmemica); example(nonmemica)`
- reason unclear
- e-mail sent
- maintainer will take a look

Version: 0.7.9

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    > ### ** Examples
    > 
    > library(magrittr)
    > library(fold)
    
    Attaching package: ‘fold’
    
    The following object is masked from ‘package:stats’:
    
        filter
    
    > options(project = system.file('project/model',package='nonmemica'))
    > 1001 %>% fold(ID,TIME,subset='MDV==0') %>% head
    Warning in as.folded.data.frame(y) :
      removing unique values where keys are duplicated
    Warning in as.folded.data.frame(y) :
      removing unique values where keys are duplicated
    Error in `[.data.frame`(res, , c("VARIABLE", "META")) : 
      undefined columns selected
    Calls: %>% ... fold.character -> <Anonymous> -> meta.character -> [ -> [.data.frame
    Execution halted
    ```

## PPforest

- reason unclear
- e-mail sent

Version: 0.1.0

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Warning in PPclassify2(Tree.result = x[[1]], test.data = xnew, Rule = 1) :
      restarting interrupted promise evaluation
    Error in do.ply(i) : task 1 failed - "object 'Type' not found"
    Calls: PPforest ... trees_pred -> <Anonymous> -> llply -> <Anonymous> -> <Anonymous>
    Execution halted
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    ...
        nasa
    
    Loading required package: gridExtra
    
    Attaching package: 'gridExtra'
    
    The following object is masked from 'package:dplyr':
    
        combine
    
    Loading required package: PPtreeViz
    Loading required package: ggplot2
    Loading required package: partykit
    Loading required package: grid
    Loading required package: libcoin
    Loading required package: mvtnorm
    Loading required package: rpart
    Quitting from lines 155-160 (PPforest-vignette.Rmd) 
    Error: processing vignette 'PPforest-vignette.Rmd' failed with diagnostics:
    object 'Type' not found
    Execution halted
    ```

# dimensions

## pRoloc

- reason unclear
- e-mail sent

Version: 1.16.1

### Newly broken

*   checking re-building of vignette outputs ... WARNING
    ```
    ...
    
    This is pRoloc version 1.16.1 
      Read '?pRoloc' and references therein for information
      about the package and how to get started.
    
    
    This is pRolocdata version 1.14.0.
    Use 'pRolocdata()' to list available data sets.
    Loading required namespace: GO.db
    
    Loading required package: GO.db
    Retaining 85 out of 530 in GOAnnotations
    Retaining 80 out of 85 in GOAnnotations
    Warning in lapply(X = X, FUN = FUN, ...) :
      NaNs found in 'precision' with hyperparameters cost:8 sigma:0.1.
    Warning in lapply(X = X, FUN = FUN, ...) :
      NaNs found in 'precision' with hyperparameters cost:8 sigma:1.
    Quitting from lines 220-223 (pRoloc-transfer-learning.Rnw) 
    Error: processing vignette 'pRoloc-transfer-learning.Rnw' failed with diagnostics:
    incorrect number of dimensions
    Execution halted
    ```

## TPP

- reason unclear
- e-mail sent

Version: 3.4.3

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    Removing duplicate identifiers using quality column 'qupm'...
    261 out of 261 rows kept for further analysis.
    Reformating data for input into function 'analyzeTPPCCR' ...
    Done.
    No output directory specified. No result files or plots will be produced.
    Looking for intensity column prefix: 'sumionarea_protein_'
    Computing fold changes...
    Done.
    Found the following column name in attr(data, 'importSettings')$proteinIdCol: 'representative'
    Found the following column name in attr(data, 'importSettings')$fcStr: 'rel_fc_protein_'
    Performing median normalization per temperature...
    Done.
    Looking for unique ID column: 'unique_ID'
    Looking for nonZeroCols: 'qusm'
    Checking which columns in the data table contain the fold change values for fitting and plotting...
    Normalized data columns detected with prefix 'norm_rel_fc_protein_'. Analysis will be based on these values.
    This information was found in the attributes of the input data (access with attr(dataTable, 'importSettings'))
    Performing TPP-CCR dose response curve fitting and generating result table...
    Error in foldChanges[, refCol] : incorrect number of dimensions
    Calls: analyze2DTPP ... withCallingHandlers -> analyzeTPPCCR -> tppccrNormalizeToReference
    Execution halted
    ```

*   checking tests ...
    ```
     ERROR
    Running the tests in ‘tests/testthat.R’ failed.
    Last 13 lines of output:
      ══ testthat results  ═══════════════════════════════════════════════════════════
      OK: 381 SKIPPED: 0 FAILED: 35
      1. Error: allOK (@test_analyze2DTPP.R#14) 
      2. Error: allOK_scientific_drug_concentration_format (@test_analyze2DTPP.R#37) 
      3. Error: warning_deprecated_fct_arg (@test_analyze2DTPP.R#62) 
      4. Error: NPARC_allok (@test_analyzeTPPTR.R#14) 
      5. Error: NPARC_allok_output (@test_analyzeTPPTR.R#34) 
      6. Error: NPARC_allok_plot (@test_analyzeTPPTR.R#61) 
      7. Error: NPARC_allok_files (@test_analyzeTPPTR.R#94) 
      8. Error: meltCurves_allOK_no_conditions (@test_analyzeTPPTR.R#153) 
      9. Error: testApplyCoeffs (@test_applyCoeffs.R#9) 
      1. ...
      
      Error: testthat unit tests failed
      Execution halted
    ```

*   checking whether package ‘TPP’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: replacing previous import ‘Biobase::exprs’ by ‘dplyr::exprs’ when loading ‘TPP’
    See ‘/home/muelleki/tmp/Rtmp8tFe4G/file182cc725e0494/TPP.Rcheck/00install.out’ for details.
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    ...
    
    Filtering by annotation column(s) 'qssm' in treatment group: Panobinostat_1
      Column qssm between 4 and Inf-> 333 out of 508 proteins passed.
    
    333 out of 508 proteins passed in total.
    
    Filtering by annotation column(s) 'qssm' in treatment group: Panobinostat_2
      Column qssm between 4 and Inf-> 364 out of 509 proteins passed.
    
    364 out of 509 proteins passed in total.
    
    	2. Find jointP:
    Detecting intersect between treatment groups (jointP).
    -> JointP contains 261 proteins.
    
    	3. Filtering fold changes:
    Filtering fold changes in treatment group: Vehicle_1
    Quitting from lines 73-76 (NPARC_analysis_of_TPP_TR_data.Rnw) 
    Error: processing vignette 'NPARC_analysis_of_TPP_TR_data.Rnw' failed with diagnostics:
    incorrect number of dimensions
    Execution halted
    ```

# tidyselect problems

## desctable

- `example(desctable)`
- Use of `eval()` a `select()` statement in `desctable:::subTable`
- https://github.com/MaximeWack/desctable/issues/8

Version: 0.1.1

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    +                                 mpg = "Miles per gallon"))
                         N      Mean        sd     Med       IQR
    1  Miles per gallon 32 20.090625 6.0269481      NA        NA
    2         Cylinders 32        NA        NA   6.000   4.00000
    3              disp 32        NA        NA 196.300 205.17500
    4       Horse Power 32        NA        NA 123.000  83.50000
    5              drat 32  3.596563 0.5346787      NA        NA
    6                wt 32        NA        NA   3.325   1.02875
    7              qsec 32 17.848750 1.7869432      NA        NA
    8                vs 32        NA        NA   0.000   1.00000
    9                am 32        NA        NA   0.000   1.00000
    10             gear 32        NA        NA   4.000   1.00000
    11             carb 32        NA        NA   2.000   2.00000
    > 
    > # With grouping on a factor
    > iris %>%
    +   group_by(Species) %>%
    +   desctable(stats = stats_default)
    Error in eval(grps[[1]]) : object 'Species' not found
    Calls: %>% ... vars_select_eval -> map_if -> map -> .Call -> .f -> eval -> eval
    Execution halted
    ```

*   checking re-building of vignette outputs ... WARNING
    ```
    Error in re-building vignettes:
      ...
    
    Attaching package: 'desctable'
    
    The following object is masked from 'package:DT':
    
        datatable
    
    The following objects are masked from 'package:stats':
    
        IQR, chisq.test, fisher.test
    
    Quitting from lines 217-222 (desctable.Rmd) 
    Error: processing vignette 'desctable.Rmd' failed with diagnostics:
    object 'Species' not found
    Execution halted
    ```

# list

## fold

- likely responsible for *nonmemica* failures
- `example("fold.data.frame")`

Version: 0.2.5

### Newly broken

*   checking examples ... ERROR
    ```
    ...
    1   VARIABLE   META   ID   TIME
    > 
    > # another example
    > x <- Theoph
    > x %<>% mutate(
    +   conc_LABEL = 'theophylline concentration',
    +   conc_GUIDE = 'mg/L',
    +   Time_LABEL = 'time since drug administration',
    +   Time_GUIDE = 'hr',
    +   Time_HALF = Time / 2 # to demonstrate variant attribute of key column
    + )
    > x %<>% fold(Subject, Time)
    Warning in as.folded.data.frame(d, sort = sort, ...) :
      removing unique values where keys are duplicated
    > x %>% unfold %>% head
    Warning in is.na(x$META) :
      is.na() applied to non-(list or vector) of type 'NULL'
    Error in y[sapply(y, function(i) nrow(i) > 0)] : 
      invalid subscript type 'list'
    Calls: %>% ... _fseq -> freduce -> <Anonymous> -> unfold -> unfold.folded
    Execution halted
    ```

# exprs

## biobroom

Version: 1.8.0

### Newly broken

*   checking whether package ‘biobroom’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: replacing previous import ‘dplyr::exprs’ by ‘Biobase::exprs’ when loading ‘biobroom’
    See ‘/home/muelleki/tmp/Rtmp8tFe4G/file182cf70acbf91/biobroom.Rcheck/00install.out’ for details.
    ```

## switchde

Version: 1.2.0

### Newly broken

*   checking whether package ‘switchde’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: replacing previous import ‘dplyr::exprs’ by ‘Biobase::exprs’ when loading ‘switchde’
    See ‘/home/muelleki/tmp/Rtmp8tFe4G/file182cb467e9ca/switchde.Rcheck/00install.out’ for details.
    ```

## IHWpaper

Version: 1.4.0

### Newly broken

*   checking whether package ‘IHWpaper’ can be installed ... WARNING
    ```
    Found the following significant warnings:
      Warning: replacing previous import ‘dplyr::exprs’ by ‘Biobase::exprs’ when loading ‘IHWpaper’
    See ‘/home/muelleki/tmp/Rtmp8tFe4G/file182ca33b1d350/IHWpaper.Rcheck/00install.out’ for details.
    ```
