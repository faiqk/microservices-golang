build:
	GOOS=linux GOARCH=amd64		# no 'go build' here, building in container
	docker build -t consignment-cli .

run:
	docker run -e MICRO_REGISTRY=mdns consignment-cli
