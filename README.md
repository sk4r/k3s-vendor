# k3s-vendor

Pre-built Go vendor tarballs for k3s.

## Why?

Building k3s requires downloading hundreds of Go modules. Sandboxed or offline build environments don't have network access during the build phase. These tarballs contain all dependencies pre-vendored.

## Usage

Download the tarball for your k3s version from [Releases](../../releases), then extract it in the k3s source directory:

```bash
cd k3s
tar -xzf k3s-1.34.1-k3s1-vendor.tar.gz
go build -mod=vendor ./...
```

## Automation

New vendor tarballs are automatically created when upstream k3s releases a new version.

To manually trigger a build for a specific version, use the "Run workflow" button in Actions.
