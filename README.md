# lab-7-benchmark
## OUTPUT

// * Summary *

BenchmarkDotNet=v0.13.1, OS=Windows 10.0.19042.421 (20H2/October2020Update)
AMD Ryzen 7 PRO 2700, 1 CPU, 16 logical and 8 physical cores
.NET SDK=5.0.202
  [Host]     : .NET Core 3.1.13 (CoreCLR 4.700.21.11102, CoreFX 4.700.21.11602), X64 RyuJIT
  DefaultJob : .NET Core 3.1.13 (CoreCLR 4.700.21.11102, CoreFX 4.700.21.11602), X64 RyuJIT


|                  Method |        Mean |     Error |    StdDev |     Gen 0 | Allocated |
|------------------------ |------------:|----------:|----------:|----------:|----------:|
|    Benchmark_BubbleSort |  1,383.6 us |  26.97 us |  45.80 us |    1.9531 |      8 KB |
|  Benchmark_CocktailSort |    771.9 us |  10.74 us |   8.97 us |    1.9531 |      8 KB |
| Benchmark_InsertionSort |    293.1 us |   5.59 us |   6.65 us |    1.9531 |      8 KB |
|     Benchmark_QuickSort | 14,556.3 us | 109.10 us | 102.05 us | 1031.2500 |  4,258 KB |

// * Hints *
Outliers
  Sorts.Benchmark_CocktailSort: Default -> 2 outliers were removed (815.48 us, 825.08 us)

// * Legends *
  Mean      : Arithmetic mean of all measurements
  Error     : Half of 99.9% confidence interval
  StdDev    : Standard deviation of all measurements
  Gen 0     : GC Generation 0 collects per 1000 operations
  Allocated : Allocated memory per single operation (managed only, inclusive, 1KB = 1024B)
  1 us      : 1 Microsecond (0.000001 sec)

// * Diagnostic Output - MemoryDiagnoser *


// ***** BenchmarkRunner: End *****
// ** Remained 0 benchmark(s) to run **
Run time: 00:01:38 (98.25 sec), executed benchmarks: 4

Global total time: 00:01:42 (102.09 sec), executed benchmarks: 4
