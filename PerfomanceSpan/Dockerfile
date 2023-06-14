FROM mcr.microsoft.com/dotnet/runtime:7.0 AS base
WORKDIR /app

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["PerfomanceSpan/PerfomanceSpan.csproj", "PerfomanceSpan/"]
RUN dotnet restore "PerfomanceSpan/PerfomanceSpan.csproj"
COPY . .
WORKDIR "/src/PerfomanceSpan"
RUN dotnet build "PerfomanceSpan.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "PerfomanceSpan.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "PerfomanceSpan.dll"]
