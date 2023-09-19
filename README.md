# Orderbook

A low latency C++ order book.

Goal: The goal is to create a highly efficient order book model simulating the matching of buy and sell orders. 
- Throughout vs latency: what are we optimizing for and why? There will be trade-offs.
- Cache friendly binary search
- Instruction cache — call code, a dummy run, so it stays hot in the instruction cache (ready to be called)
- Hotpath [only exercised .01% of the time
- jitter is unacceptable; meaning bad trades
- Libraries in c++23
- microseconds (µs) vs nanoseconds (ns)
- a lot can go wrong in a few microseconds
- placement `new` can be slightly inefficient (will perform a null pointer check on memory passed in)
- What about partial order executions where an order can be filled by multiple orders?

-----
# Design and Data Structure 
- heaps, trees
- Is concurrency necessary?

-----
# Order Class
- orderID
- datetime timestamp (microseconds? How to be extremely precise?)
- BuyOrSell (perhaps vectors)
- price (limit up, limit down; perhaps a pointer)
- volume
- client

-----
# Interface
- `Place order` find order to fill or place it in limit book
- `Cancel order` cancels order if not filled
- `Get volume` open orders for either buying or selling

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
