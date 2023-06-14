``` ini

BenchmarkDotNet=v0.13.5, OS=Windows 11 (10.0.22621.1778/22H2/2022Update/SunValley2)
Intel Core i7-10750H CPU 2.60GHz, 1 CPU, 12 logical and 6 physical cores
.NET SDK=7.0.203
  [Host]     : .NET 7.0.5 (7.0.523.17405), X64 RyuJIT AVX2
  DefaultJob : .NET 7.0.5 (7.0.523.17405), X64 RyuJIT AVX2


```
|            Method |     Mean |   Error |   StdDev | Allocated |
|------------------ |---------:|--------:|---------:|----------:|
|         FillArray | 507.5 μs | 9.94 μs | 11.45 μs |         - |
| FillArrayWithSpan | 111.3 μs | 2.05 μs |  3.08 μs |         - |
