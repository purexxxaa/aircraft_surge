# aircraft_surge
For stall prediction and detection of aircraft engine compressors, the deployment of temporal dependency model algorithms iTransformer and PatchTST onto FPGA for acceleration, using the Zynq MPSoC development board,


# Four-Channel Three-Band Experiment: Project Overview 
## 1. Project Objectives This project is designed for the three-class early warning task of compressor surge in aviation, based on 80 Hz data, completing the full process from data preparation, model training and testing to FPGA/HLS deployment export. Three-class labels: - `NORMAL` - `PRE_EVENT` - `SURGE` The current experiment focuses on: - Four-channel input: `sensor38, sensor19, sensor24, sensor37` - Three-band input: `0.5-2 Hz, 2-5 Hz, 5-10 Hz` - Comparison between native iTransformer and compressed iTransformer - Export FP32/FP16 weight versions to Vitis HLS --- 

## 2. Directory Structure (Core) Project root directory: `ds80hz_model_tests/no_clear_precursor_stress_test/four_channel_three_band_experiment` Key subdirectories: - `dataset/`: Training/validation/test window data and metadata for each sample - `model_save/`: Model weights obtained from training - `test_results/`: Test results, confusion matrices, stage_overview plots - `vitis_hls_package_latest/`: Latest HLS package results (FP32/FP16/PS reference code)
