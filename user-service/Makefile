build:
	# protoc -I. --go_out=plugins=grpc:./ proto/user/user.proto # standard gRPC
	protoc -I. --go_out=plugins=micro:./ proto/user/user.proto   # using go micro plugin
	# GOOS=linux GOARCH=amd64 go build
	GOOS=linux GOARCH=amd64
	docker build -t user-service .

run:
	docker run -p 50052:50051 \
		-e MICRO_SERVER_ADDRESS=:50051 \
		-e MICRO_REGISTRY=mdns user-service
