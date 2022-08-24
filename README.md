### Stable Diffusion AI - https://github.com/CompVis/stable-diffusion
### Using fork for GPUs with less then 12GB of VRAM  - https://github.com/basujindal/stable-diffusion

* System Requirments:
    * GPU with 6GB VRAM +
    * 5 GB Free space

* Install `python 3.10` from the `Microsoft Store` 
    * Note: Unsure if this is needed but good idea to install anyways 

* Download and install Anaconda
    * https://www.anaconda.com/products/distribution

* Download and install GIT
    * https://git-scm.com/download/win

* Using `Powershell` Clone The repo to your `Documents` 
   * `git clone https://github.com/basujindal/stable-diffusion`

* Get the dataset from `Hugging Face` at 
    *  `https://huggingface.co/CompVis/stable-diffusion-v-1-4-original`
    * Note: You will need to sign up and agree to the TOS to gain access to this data

* Copy the `.ckpt` file from the download file into `models/ldm/stable-diffusion-v1/` in the `models\ldm\stable-diffusion-v1/` folder
	* Name it `model.ckpt`

* Launch `Anaconda Navigator` and open `CMD.exe Prompt`
	* Note: Change to powershell by typing in `powershell`
    * Launch the Anaconda environment
		* Navigate to `stable-diffusion`
		* `conda env create -f environment.yaml`
		* `conda activate ldm`

* Test if everything is working by entering the following command
	* `python optimizedSD/optimized_txt2img.py --prompt "Cyberpunk style image of a Telsa car reflection in rain" --H 512 --W 512 --seed 27 --n_iter 2 --n_samples 10 --ddim_steps 50` 

To create more images just change the writting in the prompt section of the command. Also look at the instructions in https://github.com/CompVis/stable-diffusion to view and understand different command options.


When finished shut down the Anaconda container with `conda deactivate ldm`
