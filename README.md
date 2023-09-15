# Orderbook

A low latency C++ order book.

Goal: The goal is to create a highly efficient order book model simulating the matching of buy and sell orders. 
- Throughout vs latency: what are we optimizing for and why? There will be trade-offs.
- Cache friendly binary search
- Instruction cache — call code, a dummy runm, so it stays hot in the instruction cache (ready to be called)
- hot path
- Libraries in c++23
- microseconds (µs) vs nanoseconds (ns)

-----
# Design and Data Structure 
- heaps, trees
- Is concurrency necessary?

-----

# Hardware

-----
# Measuring
- Benchmarking

-----
#  Edge Cases and Error Handling

-----
# Resources  

- [What is Low Latency C++ Timur Doumler](https://www.youtube.com/watch?v=jjDolw1PIsM)
- [When a Microsecond Is an Eternity: High Performance Trading Systems in C++](https://www.youtube.com/watch?v=NH1Tta7purM&t=1562s)
