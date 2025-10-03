# Папка с сгенерированным Go-кодом
GEN_DIR := ./gen/go

# Пути до proto файлов
PROTO_FILES := proto/route/route.proto

# Команда protoc
PROTOC := protoc
PROTOC_FLAGS := -I proto $(PROTO_FILES) \
	--go_out=$(GEN_DIR) --go_opt=paths=source_relative \
	--go-grpc_out=$(GEN_DIR) --go-grpc_opt=paths=source_relative

# Цель по умолчанию
.PHONY: generate
generate:
	@echo "Generating Go code from proto files..."
	$(PROTOC) $(PROTOC_FLAGS)
	@echo "Done!"
