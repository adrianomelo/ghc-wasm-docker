
Docker images for the GHC WebAssembly backend


```bash
# Create a Hello World example
echo 'main = putStrLn "hello world"' > hello.hs

# Build the project
docker run -it --platform linux/amd64 -w /app -v `pwd`:/app adrianomelo/ghc-wasm:latest /usr/local/bin/wasm32-wasi-ghc/bin/wasm32-wasi-ghc ./hello.hs

# Execute the generated code using `wasmtime`
wasmtime ./hello.wasm
```