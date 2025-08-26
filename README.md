# LMCache External Log Backend

This project provides an external logging backend implementation for LMCache.

## Features
- Implements the `StorageBackendInterface` from LMCache
- Logs all backend operations (put, get, prefetch, pin, etc.)
- Easy to integrate with existing LMCache systems

## Installation

```bash
pip install lmc_external_log_backend
```

## Usage

To use this backend in your LMCache,

Add the following to your LMCache Configuration:
```yaml
chunk_size: 64
local_cpu: False
max_local_cpu_size: 5
external_backends: "log_external_backend"
extra_config:
  external_backend.log_external_backend.module_path: lmc_external_log_backend.lmc_external_log_backend
  external_backend.log_external_backend.class_name: ExternalLogBackend

```


## Development

To build the package:
```bash
python setup.py sdist bdist_wheel
```

To install locally:
```bash
pip install -e .
```

## License
Apache-2.0 License