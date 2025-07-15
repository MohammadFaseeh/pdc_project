🕵️‍♂️ Steganography-Based Information Security
This project implements information security using steganography, where sensitive data is hidden within digital images. It combines image processing, encryption, and data hiding techniques to securely embed and retrieve secret messages without altering the visible content of the image.

🔒 What is Steganography?
Steganography is the art and science of hiding information in plain sight — in this case, within images. Unlike cryptography, which hides the content, steganography hides the existence of the message itself.

🎯 Objective
To develop a system that:

Hides secret data (text/files) inside images using LSB (Least Significant Bit) technique.

Extracts hidden data from the stego-image.

Ensures confidentiality and data integrity during transmission or storage.

🧠 Features
Image-based data hiding (using .png, .jpg)

LSB encoding/decoding method

Simple, user-friendly interface (CLI or GUI)

Support for CUDA/OpenMP/MPI for parallel processing

📁 Project Structure
bash
Copy
Edit
├── encode_mpi.cu         # CUDA-based encoding source code
├── decode_mpi.cu         # CUDA-based decoding source code
├── image_io.jpg/image_io.png     # OpenCV functions for image handling
├── README.md         # Project documentation
├── samples/          # Sample input/output images
└── utils/            # Helper functions for string/image operations
🛠️ How It Works
Encoding:

Convert secret message to binary.

Embed bits into the least significant bits of image pixels.

Save as a new "stego-image".

Decoding:

Extract the LSBs from the image pixels.

Reconstruct the original message from the binary sequence.

🚀 Technologies Used
CUDA C

OpenCV for image handling

MPI_ranks for parallelism

CMake / Makefile for building the project

📷 Example
Original Image: landscape.png

Secret Message: "MyPassword123"

Output Image: output.png

Decoded Output: "MyPassword123"

🔐 Use Cases
Secure communication

Watermarking

Digital rights management

Covert data storage

📌 Limitations
Limited data capacity (depends on image size)

Vulnerable to lossy compression (e.g., JPEG artifacts)

Can be detected by steganalysis tools if not carefully done

✅ Future Work
Add encryption before embedding

Use audio or video carriers

Deep learning-based adaptive steganography

Robustness against image editing
