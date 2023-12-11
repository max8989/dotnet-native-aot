<p align="center"><img src="https://socialify.git.ci/max8989/dotnet-native-aot/image?font=Inter&language=1&name=1&owner=1&pattern=Solid&stargazers=1&theme=Light" alt="dotnet-native-aot" width="640" height="320" /></p>

<p id="description">This repository contains a demo project for benchmarking the .NET Native Ahead-of-Time (AOT) compilation. The project can be built and run using Docker or the .NET SDK directly.</p>

<h2>🚀 Demo</h2>

<h2>🛠️ Installation Steps:</h2>

<p>1. Build</p>

```
docker build -t native-aot:latest ./nativeAot
```

<p>2. Run</p>

```
docker run -d -p 8080:8080 -p 8081:8081 native-aot
```

<p>3. Get endpoint</p>

```
http://localhost:8080/todos
```
