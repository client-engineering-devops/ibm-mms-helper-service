all: build publish-service

QUAY_REGISTRY:=quay.io/ibmtechgarage

build:
	docker build -t $(QUAY_REGISTRY)/tg-tensorflow-server:1.0.0 .

dev:
	docker run -it $(QUAY_REGISTRY)/tg-tensorflow-server:1.0.0 /bin/sh

push:
	docker push $(QUAY_REGISTRY)/tg-tensorflow-server:1.0.0

publish-service:
	hzn exchange service publish -O -f service.json