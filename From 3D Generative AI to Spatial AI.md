Spatial AI -- enhance our ability to perceive and interact with the physical world, reflecting how humans think and understand.

#### Part I -- Next-gen 3D tech: advanced projects
Five projects:
1. 3D generative AI
2. 3D deep point cloud registration
3. 3D semantic modelling
4. Efficient semantic extraction
5. 3D Gaussian splatting

##### **3D Generative AI**
###### Text to 3D
1. NLP breaks down the text input into individual words or tokens 
2. Represents them as a numerical vector (capture the semantic meaning and relationships between words)
3. Model learns a latent, high-dimensional mathematical space where complex relationships between text and 3D objects can be represented
4. Text embedding are mapped to points in this latent space
5. A generative model, such as variational autoencoder (VAE) or a generative adversarial network (GAN), decodes the latent representation into 3D coordinates
6. Model iteratively refines the generated 3D structure based on feedback from a discriminator network or reconstruction loss

Diffusion -- Process of deliberately destroying an image with static (noise) and then teaching an AI how to reverse that destruction to create something new. 

Latent diffusion -- Instead of generating an image pixel-by-pixel, the AI compresses the data into smaller mathematical representation called latent space -> does the heavy computational work there -> uncompresses it back into a visible image. 

(Three-step pipeline)
1. Encoder (Compression):
   - Neural Network called Variational Autoencoder (VAE) compresses the high-resolution training image into smaller, denser matrix. 
   - E.g., a 512 x 512 image might be squished down to 64 x 64 latent map -> this loses the literal pixels but retains the semantic meaning - the shapes, textures, and spatial relationships. 

2. Diffusion Process (U-Net):
   (Actual generative AI work happens here)
   - System adds random mathematical noise to the latent map
   - Specialized network (usually a U-Net) is trained to predict and iteratively remove that noise step-by-step
   - (The conditioning happens here) If your text prompt asks for a specific style or object, that text is embedded into the U-Net via 'cross-attention', guiding the AI on exactly how to denoise the data to match your prompt

3. Decoder (Uncompression):
   - After U-Net is fully denoised the latent map into a brand new concept -> latent map is passed to the Decoder
   - Decoder translates that dense mathematical matrix back into high-resolution pixels that humans can see

###### Image to 3D



#### Part II -- Spatial AI: the future of 3D experiences