# Final_Code_Girish_Kannan


Robust and Secure Audio Watermarking using Chaotic Random Number Generators
This project presents a robust and secure audio watermarking system that utilizes chaotic random number generators, error correction, and spectral domain embedding to conceal watermark data within audio signals. The approach is specifically designed to withstand various audio distortions and is particularly suited for forensic applications where audio authenticity and integrity are critical.

Project Objective
The objective of this project is to develop a watermarking method that ensures:

Inaudibility: The watermark should not degrade the audio quality.

Robustness: The embedded watermark should survive standard audio processing operations such as compression, noise addition, and resampling.

Security: The watermark must be difficult to remove or tamper with, ensuring reliable forensic validation.

This system supports applications where audio content must be verifiable, particularly in digital forensics and legal evidence scenarios.

Tools and Techniques Used
Watermark Processing

Arnold’s Cat Map is used to scramble the watermark image, adding a layer of security against unauthorized detection or modification.

The watermark image is converted into a binary stream for embedding.

Hamming (7,4) encoding is applied to introduce error-correcting capabilities, enabling partial recovery even after audio degradation.

Audio Processing

Short-Time Fourier Transform (STFT) is used to convert the audio signal into the time-frequency domain, where modifications can be made with greater control and resilience.

Chaotic Index Generator combines the Logistic Map and 2D Henon Map to produce pseudo-random embedding positions within the STFT domain, ensuring high unpredictability and resistance to attack.

Embedding and Extraction

Watermark bits are embedded by modifying the magnitudes of selected STFT coefficients.

During extraction, the same chaotic sequences are regenerated to locate embedded bits.

Hamming decoding is applied to correct any bit errors.

Finally, the binary watermark is reconstructed and unscrambled using the inverse Arnold’s Cat Map.

Importance and Applications
This watermarking approach is particularly useful for:

Verifying the authenticity of audio recordings in forensic investigations.

Ensuring integrity of digital evidence presented in legal proceedings.

Supporting secure audio communication and traceability in sensitive environments.

By combining secure scrambling, error correction, and chaotic-based embedding in the time-frequency domain, the system achieves a balance between robustness, imperceptibility, and security.

Required Libraries
The project is implemented in Python using the following libraries:

numpy – for numerical operations

librosa – for audio signal processing

matplotlib – for plotting and visualization

scipy – for signal transformations

soundfile – for audio input and output

