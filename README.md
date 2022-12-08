# Intel® oneAPI Hackathon for Open Innovation
## Environment set up for various run:
Step 1: Open the condaenvsetup.ipynb and activate Python 3(Intel oneAPI 2022.3) kernel<br />
Step 2: Run through the cells one by one. "qsub" submits the job to do all the setup and "qstat" shows the job status. (all details related to devcloud job submission is in the Welcome.ipyb file)<br />
Step 3: Once the job is finished, the setup should be completed.<br />
Step 4: Now you will have stock-tensorflow as well as intel-tensorflow in the jupyter kernels to run the benchmark code.<br />
Step 5: You will also have stock-XGBoost(xgb0.81) and intel-modin kernel to run the benchmark code.<br />

## Running the notebooks:

### Exercise 1: Intel® extension for Pytorch

Step 1: Open terminal and clone oneAPI samples<br />
git clone https://github.com/oneapi-src/oneAPI-samples.git<br />
step 2: Browse oneAPI-samples/AI-and-Analytics/Features-and-Functionality/IntelPyTorch_Extensions_Inference_Optimization/<br />
step 3: Open the optimize_pytorch_models_with_ipex.ipynb<br />
step 4: Activate the Pytorch(AI kit) kernel.<br />
step 5: Run all the cells for to see comparision between baseline pytorch and IPEX optimization features for inference.<br />

### Exercise 2: Intel® Tensorflow and Stock Tensorflow Performance Comparison 

Step 1: Open terminal, and clone oneAPI samples<br />
git clone https://github.com/oneapi-src/oneAPI-samples.git<br />
Step 2: Browse the oneAPI-samples/AI-and-Analytics/Features-and-Functionality/IntelTensorFlow_ModelZoo_Inference_with_FP32_Int8/<br />
Step 3: Open the ResNet50_Inference.ipynb<br />
Step 4: First select stock-tensorflow kernel with onednn off  and run through every cell of the notebook and note the average time and throughput.<br />
Step 5: Follow step 5 but now with onednn off by adding the following env variable [os.environ["TF_ENABLE_ONEDNN_OPTS"]='0'] and note the performance<br />
Step 6: Repeat step 5 but with intel-tensorflow kernel to add further openmp optimizations and compare the average time and throughput<br />

### Exercise 3: Intel® Extension for Scikit-learn 

Step 1: Browse the oneAPI-samples/AI-and-Analytics/Features-and-Functionality/Intel_Extension_For_SKLearn_Performance_SVC_Adult/<br />
Step 2: Open the Intel_Extension_for_SKLearn_Performance_SVC_Adult.ipynb<br />
Step 3: Activate the python3(Intel oneAPI 2022.3) kernel. Run through all the cells. This compares both the Intel extension SKLearn with the Unoptimized SKLearn and compares the performance optimization.<br />

### Exercise 4: Intel® Distribution for Modin

Step 1: Browse /oneAPI-samples/AI-and-Analytics/Getting-Started-Samples/IntelModin_GettingStarted/<br />
Step 2: Open IntelModin_GettingStarted.ipynb and activate the intel-modin kernel.<br />
Step 3: Run all the cells which has modin and pandas comparision.<br />

### Exercise 5: XGBoost Optimized for Intel®

Step 1: Browse oneAPI-samples/AI-and-Analytics/Features-and-Functionality/IntelPython_XGBoost_Performance/<br />
Step 2: Open IntelPython_XGBoost_Performance.ipynb<br />
Step 3: First activate Python 3(Intel oneAPI 2022.3) kernel and run till 8th cell.<br />
Step 4: Check if perf_numbers.csv file has been created.<br />
Step 5: Change the kernel to xgb0.81 to check results with stock XGBoost.<br />
Step 6: Run all the cell again to see performace comparision.<br />

## Documentation Links:

Intel® Devcloud for oneAPI documentation
https://devcloud.intel.com/oneapi/get_started/

Intel® oneapi AI Analytics toolkit - Documentation
https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit.html#gs.kgt57v

Intel® extension for Pytorch*
https://intel.github.io/intel-extension-for-pytorch/cpu/latest/

Intel® Extension for TensorFlow*
https://github.com/intel/intel-extension-for-tensorflow

Intel® Extension for Scikit-learn*
https://www.intel.com/content/www/us/en/developer/tools/oneapi/scikit-learn.html#gs.ki3i07

Intel® Distribution of Modin*
https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-of-modin.html#gs.ki3gje

XGBoost Optimized for Intel®
https://www.intel.com/content/www/us/en/developer/articles/technical/xgboost-optimized-architecture-getting-started.html
