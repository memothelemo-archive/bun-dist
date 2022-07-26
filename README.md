# bun-dist

I compiled [Bun](https://github.com/oven-sh/bun) (A JavaScript runtime) on x86-64 Linux from [equal-l2's PR repository](https://github.com/equal-l2/bun)
for pushing support for non-AVX2 CPUs in purpose of publishing bun on [some package managers](https://github.com/Homebrew/homebrew-core/pull/105263#issuecomment-1185819052).

## Notes
- AVX2 is disabled in compile-time on purpose. If you're running on AVX2 compatible CPU,
you may want to download the official binary of bun instead.
- These are precompiled binaries provided from me. If you're not confident on running these executables from unknown source,
you may want to compile from [equal-l2's repository](https://github.com/equal-l2/bun). (This will take around 30 minutes to 2 hours to compile)
- This binaries are not verified if bun is stable enough to use non-AVX2 instructions. Do it at your own risk.
- I have non-AVX2 machine but I don't know if it can be compiled on that machine because I compiled it on a cloud server.
*Let me know if you managed to compile this thing! :)*

## Issues
- Managing packages will give an `Instruction Error`. (I'm going to figure out why is that so)

## What is the purpose of this repository?
This repository is for distributing compiled binaries of Bun designed for older CPUs that
do not have AVX2 capability.
