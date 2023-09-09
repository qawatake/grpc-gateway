BIN_DIR = $(CURDIR)/bin

install.tools:
	# GOBIN=$(BIN_DIR) go install ../protoc-gen-grpc-gateway
	GOBIN=$(BIN_DIR) go install ../protoc-gen-openapiv2

.PHONY: proto.gen
proto.gen:
	PATH=$(BIN_DIR):$(PATH) protoc -I . --openapiv2_out ./gen \
	--openapiv2_opt=output_format=yaml \
  your/service/v1/your_service.proto
# proto.gen:
# 	cd ..; \
# 	PATH=$(PATH):$(BIN_DIR) protoc -I . --openapiv2_out ./gen \
# 	--openapiv2_opt=output_format=yaml \
#   examples/internal/proto/examplepb/echo_service.proto

dump:
	PATH=$(BIN_DIR):$(PATH) protoc -I . --reqdump_out ./gen \
  your/service/v1/your_service.proto

hoge:
	PATH=$(BIN_DIR):$(PATH) protoc -I . --openapiv2_out ./gen \
	--openapiv2_opt=output_format=yaml \
  your/service/v1/your_service.proto
