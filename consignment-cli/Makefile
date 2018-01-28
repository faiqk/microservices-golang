build:
	# GOOS=linux GOARCH=amd64 go build
	GOOS=linux GOARCH=amd64
	docker build -t consignment-cli .

run:
	docker run -e MICRO_REGISTRY=mdns consignment-cli
