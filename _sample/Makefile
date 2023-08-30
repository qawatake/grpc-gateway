BIN_DIR = $(CURDIR)/bin

install.tools:
	GOBIN=$(BIN_DIR) go install github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-grpc-gateway@latest
	GOBIN=$(BIN_DIR) go install ../protoc-gen-openapiv2

.PHONY: proto.gen
proto.gen:
	PATH=$(PATH):$(BIN_DIR) protoc -I . --openapiv2_out ./gen \
	--openapiv2_opt=output_format=yaml \
  your/service/v1/your_service.proto
