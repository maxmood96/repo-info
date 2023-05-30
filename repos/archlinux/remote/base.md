## `archlinux:base`

```console
$ docker pull archlinux@sha256:1b020d5df52c08550f9808060a5f8989fba361035030d819e0cccab98b7442e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a64dbdb732c68c3b31a108c3ff8ccf3e0dffbbacc79e1a17c59a293910bbfaea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145896619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047cf0fc607fefedb26cf0f80cc3306289615feaa97fc47104bc613aeb3ebda7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 20:19:54 GMT
COPY dir:ffe8a6e8f872325c0fef70c7d55ad0673fb3ae79f2b6f44f750a44fe355580ef in / 
# Tue, 30 May 2023 20:19:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 30 May 2023 20:19:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 May 2023 20:19:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:50bd11ca3ec46966b625c906b04e443c79a476ce57789397ec9854115d212fa8`  
		Last Modified: Tue, 30 May 2023 20:21:25 GMT  
		Size: 145.9 MB (145888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f90b1ce8df6e05fddfa1cc973429a3d7320339f7ffcad16e5c1b89f117394bc`  
		Last Modified: Tue, 30 May 2023 20:21:05 GMT  
		Size: 8.0 KB (8040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
