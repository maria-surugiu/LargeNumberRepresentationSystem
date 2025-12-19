# Large Number Representation System

## Overview

This project implements a high-performance large integer (BigInt) arithmetic system with both CPU and CUDA GPU support. It is designed to handle very large numbers efficiently and to explore the trade-offs between latency and throughput when executing big-number operations on modern hardware.

The system combines classic big integer techniques with advanced algorithms and GPU optimizations, making it suitable for research, experimentation, and performance-oriented applications such as cryptography or large-scale numerical computation.

---

## Project Structure

The project is organized into three main modules:

### Module 1 – Big Integer Core and Basic Operations
- Custom BigInt data representation
- Core arithmetic operations:
  - Addition
  - Subtraction
  - Basic multiplication
- CPU implementations
- Initial CUDA kernels for basic arithmetic

### Module 2 – Advanced Algorithms and CUDA Optimizations
- Advanced multiplication algorithms:
  - Karatsuba multiplication
  - Montgomery multiplication (cryptographic-grade)
- Hybrid CPU–GPU execution strategies
- CUDA optimizations for parallel execution
- Analysis of algorithmic choices (e.g., Karatsuba vs. FFT)

### Module 3 – CPU Reference and Testing
- CPU reference implementations for correctness
- Randomized testing framework
- Result validation between CPU and GPU implementations
- Performance comparisons

---

## Implemented Algorithms

- **Big integer addition**
- **Big integer subtraction**
- **Schoolbook (naive) multiplication**
- **Karatsuba multiplication**
- **Montgomery multiplication** for modular arithmetic

---

## CUDA Design Considerations

- GPU kernels are optimized for **batch processing** rather than single operations
- Emphasis on **throughput** over single-operation latency
- **Hybrid execution model** where the CPU coordinates complex control flow and the GPU handles parallel arithmetic
- Careful memory layout to reduce global memory access overhead

---

## Performance Notes

- Single big-number operations may not benefit significantly from GPU acceleration due to kernel launch overhead
- **Batch processing** of many operations shows substantial performance gains on the GPU
- The project highlights the difference between **theoretical algorithmic efficiency** and **real-world hardware performance**

---

## Use Cases

- Experimental research in big integer arithmetic
- Performance studies of CPU versus GPU numerical computation
- Foundations for cryptographic systems requiring large integer operations
- Educational reference for CUDA-accelerated arithmetic algorithms

---

## Getting Started

- Upload the LargeNumberRepresentationSystem.ipynb file in Google Colab and run it

---

## Acknowledgments

- Course: Computer Architecture 
