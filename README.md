<h1 align="center" id="title">dotnet native aot demo</h1>

<p align="center"><img src="https://socialify.git.ci/max8989/native-aot-demo/image?language=1&amp;owner=1&amp;name=1&amp;stargazers=1&amp;theme=Light" alt="project-image"></p>

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
