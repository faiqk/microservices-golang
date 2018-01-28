build:
	# protoc -I. --go_out=plugins=grpc:./ proto/consignment/consignment.proto # standard gRPC
	protoc -I. --go_out=plugins=micro:./ proto/consignment/consignment.proto   # using go micro plugin
	# GOOS=linux GOARCH=amd64 go build
	GOOS=linux GOARCH=amd64
	docker build -t consignment-service .

run:
	docker run -p 50051:50051 \
		-e MICRO_SERVER_ADDRESS=:50051 \
		-e MICRO_REGISTRY=mdns consignment-service
