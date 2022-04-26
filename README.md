# GRPCStream

A sample to demonstrate the use of GRPC Stream.

Setup go.mod
```
go mod init 
```
Create the routeguide.proto

Generate the protobuf code

```
protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    routeguide/route_guide.proto 
```

Implement the client

Implement the server 

Add GRPC mod
```
go get google.golang.org/grpc
```

Run server

```
cd server
go run server.go
```

Run client

```
cd client
go run client.go
```

Client output should be
```
start client
2022/04/26 20:55:05 Looking for features within lo:{latitude:400000000  longitude:-750000000}  hi:{latitude:420000000  longitude:-730000000}
end client
```
