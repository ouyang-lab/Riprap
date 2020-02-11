# Examples
All sample datasets can be downloaded from the [Downloads](Downloads.md) page.
## Sample input
Riprap requires a table that contain ID, sequence, and SNV information in separated columns by tab.
### 1. Sample input table: sample_input.txt

##### test_sample1    AUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAU    C5U
##### test_sample2    AUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAUAUCGCGAUUAUUGGAAUCGAUCGGGAU    A7U

## Command example
### 1. run Riprap "default" mode
./Riprap_software_1.3.py -i sample_input.txt -o sample_output 
### 2. run Riprap with customized options.
./Riprap_software_1.3.py -i sample_input.txt -o sample_output -t 1 -w 10 -f 0 

where *-t 1* means fold type one (RNAfold), *-w 10 * means minimum window size is 10 nt, and *-f 0* means window type 0, which is the scanning window that covers the SNV site.

The two command lines above should provide the same results.

## Sample output
### 1. Sample output on screen.

One will get information as below and a file called "$output_file_prefix"_riprap_score.tab if Riprap runs successfully.

##### Starting...
##### Finished!
##### --- The running time is 1.98150014877 seconds ---

### 2. Sample output table: sample_output_riprap_score.tab

There will be five columns in the score table: ID, Riprap score, KS-test p-value, start, end
