NAME ?= ns3
NS3_DOCKER_TAG ?= 3.0

all: build start

.PHONY: build start
build:
	docker build \
		--tag="tcc-simulacao-iot/ns3:$(NS3_DOCKER_TAG)" \
		.

start:
	docker run -ti --privileged --network=host -p 5060:5060 --name $(NAME) tcc-simulacao-iot/ns3:$(NS3_DOCKER_TAG)
