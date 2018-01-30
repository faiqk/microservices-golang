build:
	GOOS=linux GOARCH=amd64		# no 'go build' here, building in container
	docker build -t user-cli .

run:
	docker run -e MICRO_REGISTRY=mdns user-cli
