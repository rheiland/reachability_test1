# An exploration of reachability

* based on https://github.com/PhysiCell-Models/grammar_samples/tree/main?tab=readme-ov-file#model-3-base-tumor-immune-example-link
* upgraded to use PhysiCell 1.14.2
* includes `/studio`  (by running `python beta/get_studio.py`)

## Custom output intervals
* add user params to make this possible (`config/PhysiCell_settings.xml` and a simpler `test1.xml`)
* edit main.cpp to use them

After compiling the executable model (with a modified `main.cpp`) and assuming all Studio dependencies are met, you can run it:
  ```
  make
  # run full model
  python studio/bin/studio.py
  # or, run a config file just to test the custom output intervals
  python studio/bin/studio.py -c config/test1.xml
  ```

## Experiment with reproducibility, replicates, permuting ICs
* demonstrate can get bitwise reproducible results with a single thread and same random seed
* make minimal changes to ICs; re-run
* run replicates, multi-threaded, but same model and ICs
