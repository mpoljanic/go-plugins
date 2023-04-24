## go plugins sample
Example that showcases go plugin dynamic loading.

See:

- https://pkg.go.dev/plugin@go1.20.3

## Build instructions

```
cd plugin
go mod init plugin-example
go mod tidy
go build -buildmode=plugin
```

Should produce plugin-example.so

```
cd ..
cd consumer
go mod init plugin-consumer
go mod tidy
go build
```

Run consumer:

```
./plugin-consumer
```

Should print:

Hello, number 7