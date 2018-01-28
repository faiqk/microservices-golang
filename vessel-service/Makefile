build:
	# protoc -I. --go_out=plugins=grpc:./ proto/vessel/vessel.proto # standard gRPC
	protoc -I. --go_out=plugins=micro:./ proto/vessel/vessel.proto   # using go micro plugin
	# GOOS=linux GOARCH=amd64 go build
	GOOS=linux GOARCH=amd64
	docker build -t vessel-service .

run:
	docker run -p 50052:50051 \
		-e MICRO_SERVER_ADDRESS=:50051 \
		-e MICRO_REGISTRY=mdns vessel-service
