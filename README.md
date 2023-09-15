# Introduction
This notebook implements the DiffEdit algorithm 

# Dependencies and other code used
* Unet and denoisers with open weights provided by _
* Stable diffusion implementation is based on both the implementation from [the course.fast.ai lesson notebook]() and other bits of code from [_todo name_'s stable diffusion tutorial]()
* My contribution here is inside the denoising loop, implementing the algorithm that was introduced in the DiffEdit paper, to use differential noise predictions to generate a mask for the region of image needing to be edited, and then pasting in the appropriately noised version of the original image *outside* the mask at each step.
* Mask generation code inspired by [_todo huggingface implementation_]()
* Includes support for debugging callbacks and "DiffEdit hyperparameters" to control at which stage of noise the DiffEdit denoising loop will begin, and how aggressively to size the mask.
