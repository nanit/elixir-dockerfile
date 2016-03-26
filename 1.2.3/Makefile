VERSION=1.2.3
IMAGE_NAME=nanit/elixir

build: base onbuild

base:
	docker build -t $(IMAGE_NAME):$(VERSION) . && docker push $(IMAGE_NAME):$(VERSION)
	docker tag -f $(IMAGE_NAME):$(VERSION) $(IMAGE_NAME):latest && docker push $(IMAGE_NAME):latest

onbuild:
	docker build -t $(IMAGE_NAME):$(VERSION)-onbuild ./onbuild && docker push $(IMAGE_NAME):$(VERSION)-onbuild 
	docker tag -f $(IMAGE_NAME):$(VERSION)-onbuild $(IMAGE_NAME):latest-onbuild && docker push $(IMAGE_NAME):latest-onbuild

