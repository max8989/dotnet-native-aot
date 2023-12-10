#Build Stage
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /sourcek
COPY . .

# Install the required tools
RUN apt-get update && \
    apt-get install -y clang gcc zlib1g-dev

ARG BUILD_CONFIGURATION=Release
ARG RUNTIME=linux-x64
RUN dotnet restore "nativeAot.csproj"
RUN dotnet publish "nativeAot.csproj" -c $BUILD_CONFIGURATION -r $RUNTIME -o /app --no-restore

#Serve State
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS serve
WORKDIR /app
COPY --from=build /app ./

EXPOSE 8080
EXPOSE 8081

ENTRYPOINT ["dotnet", "./bin/Release/net8.0/linux-x64/nativeAot"]

#docker build -t native-aot:latest ./nativeAot
#docker run -d -p 8080:8080 -p 8081:8081 native-aot