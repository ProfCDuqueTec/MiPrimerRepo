# Computational Complexity
- Let N=WH be the total number of pixels. The algorithm proceeds in the following principal steps:
	Integral‐Image Construction: Two passes over the image (one to compute S, another for S2), each of cost per pixel O(N), thus the integrals time is
T_integrals=O(N),         (15) 
	Per‐Pixel Local‐Variance and Thresholding: The set Ω_valid of “valid” pixels for which W_k (x,y) ⊆ Ω is denoted:
Ω_valid={(x,y)ϵ Ω:  m+1≤x≤W-m,m+1≤y≤H-m},(15)
- Where the number of elements in Ω_valid is:
 N_valid=(W-2m)(H-2m),         (16) 
	For each valid (x,y): Compute μ(x,y) and σ2(x,y) in O(1) via four accesses to S and four to S2, plus O(1) arithmetic (approximately 10 floating‐point operations), and evaluate the condition I(x,y)≥μ(x,y)+κσ(x,y) in O(1), therefore, let Cvar be the cost per pixel as:
C_var≈8 (memory reads)+10 (flops)+1 (comparation),         (17) 
- And, if the condition holds, perform the Sobel convolution in 3×3 (nine reads of I and about 16 flops), otherwise assign zero and skip the convolution. Then, let CSobel be the cost per pixel 
