``` ini

BenchmarkDotNet=v0.13.5, OS=Windows 11 (10.0.22621.1778/22H2/2022Update/SunValley2)
Intel Core i7-10750H CPU 2.60GHz, 1 CPU, 12 logical and 6 physical cores
.NET SDK=7.0.203
  [Host]     : .NET 7.0.5 (7.0.523.17405), X64 RyuJIT AVX2
  DefaultJob : .NET 7.0.5 (7.0.523.17405), X64 RyuJIT AVX2


```
|                 Method |      Mean |     Error |    StdDev |    Median |   Gen0 | Allocated |
|----------------------- |----------:|----------:|----------:|----------:|-------:|----------:|
|         ExtractNumbers | 6.0086 ns | 0.1498 ns | 0.4346 ns | 5.8938 ns | 0.0051 |      32 B |
| ExtractNumbersWithSpan | 0.0105 ns | 0.0156 ns | 0.0130 ns | 0.0000 ns |      - |         - |
