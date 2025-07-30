TARGET_PLATFORMS=linux/amd64
REPO ?= thomasferrandiz
TAG ?= v0.0.1
IMAGE = $(REPO)/iperf3:$(TAG)

BUILD_OPTS = \
	--platform=$(TARGET_PLATFORMS) \
	--tag "$(IMAGE)"

.PHONY: image-build
image-build:
	docker build \
		$(BUILD_OPTS) \
		--pull \
		.

.PHONY: push-image
image-push:
	docker buildx build \
		$(BUILD_OPTS) \
		--push \
		.

