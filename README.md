# Usage Guide

## Environment & Dataset Setup
1. Prepare the environment and dataset according to the official repo: ![NTIRE2025_ESR](https://github.com/Amazingren/NTIRE2025_ESR.git)

## Validate on DIV2K_LSDIR_valid Dataset
1. Uncomment the following line in `test_demo.py` to generate Super-Resolution (SR) results of the validation dataset:
    ```python
    # --- Save Restored Images ---
    util.imsave(img_sr, os.path.join(save_path, img_name+ext))
    ```

2. Generate SR results and statistical information of NanoSR:
    ```bash
    cd /path/to/NTIRE2025_ESR_NanoSR
    CUDA_VISIBLE_DEVICES=0 python test_demo.py --model_id 7 --ssim
    ```

## Generate SR Results of DIV2K_LSDIR_test Dataset
1. To generate SR results of the test dataset, run the following command:
    ```bash
    cd /path/to/NTIRE2025_ESR_NanoSR
    CUDA_VISIBLE_DEVICES=0 python generate_test_results.py --model_id 7 --include_test
    ```

## License and Acknowledgement
This code repository is release under [MIT License](LICENSE). 