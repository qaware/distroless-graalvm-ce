GRAALVM_VERSION=20.1.0-java11

image:
	docker build --build-arg GRAALVM_VERSION=${GRAALVM_VERSION} -t distroless-graalvm-ce:${GRAALVM_VERSION} .
	@echo ""
	@echo "To test the image run:"
	@echo "docker run -it --rm distroless-graalvm-ce:${GRAALVM_VERSION}"

tag: image
	docker tag distroless-graalvm-ce:${GRAALVM_VERSION} qaware/distroless-graalvm-ce:${GRAALVM_VERSION}

push: tag
	docker push qaware/distroless-graalvm-ce:${GRAALVM_VERSION}
