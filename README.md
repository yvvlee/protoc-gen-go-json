# protoc-gen-go-json

This is a protoc plugin that generates code to implement json.Marshaler and json.Unmarshaler using [protojson](google.golang.org/protobuf/encoding/protojson).

## Install

```
go get github.com/yvvlee/protoc-gen-go-json
```

## Usage

```
protoc --go_out=. --go-json_out=. request.proto
```


### Options

- `UseProtoNames={bool}` - uses proto field name instead of lowerCamelCase name in JSON field names
- `UseEnumNumbers={bool}` - emits enum values as numbers.
- `EmitUnpopulated={bool}` - specifies whether to emit unpopulated fields
- `DiscardUnknown={bool}` - unknown fields are ignored.

```sh
protoc --go-json_out=UseEnumNumbers=true,EmitUnpopulated=true:.
```
