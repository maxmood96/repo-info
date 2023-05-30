<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230528.0.154326`](#archlinuxbase-202305280154326)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230528.0.154326`](#archlinuxbase-devel-202305280154326)
-	[`archlinux:latest`](#archlinuxlatest)

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

## `archlinux:base-20230528.0.154326`

```console
$ docker pull archlinux@sha256:1b020d5df52c08550f9808060a5f8989fba361035030d819e0cccab98b7442e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20230528.0.154326` - linux; amd64

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

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4b5f5c31a5a04caf428c8d9a175a87dbecbb9e3a892ba78abac8126603ce1784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3317d3adc1a1f4b85e81155b46c1e367bb9b085bbaa1ca87e4640cd2e5fd8cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252919851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819b57250da9b69d039a563491c13407eec79cf6d620faab7a1d9c4bd341d781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 20:20:53 GMT
COPY dir:44daec227b53dff21531675eb39198acc99b78db7d8bbad351395eeb4ec096dc in / 
# Tue, 30 May 2023 20:20:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 30 May 2023 20:20:56 GMT
ENV LANG=C.UTF-8
# Tue, 30 May 2023 20:20:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:45ff414ffddb9107ed6633f3e3b38d498f0389de57fb0e9f523624790b937b12`  
		Last Modified: Tue, 30 May 2023 20:22:09 GMT  
		Size: 252.9 MB (252911130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43212488f1a732a4a7904dfc536c8069682e42e2392388c4035620e77d8949d`  
		Last Modified: Tue, 30 May 2023 20:21:36 GMT  
		Size: 8.7 KB (8721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230528.0.154326`

```console
$ docker pull archlinux@sha256:4b5f5c31a5a04caf428c8d9a175a87dbecbb9e3a892ba78abac8126603ce1784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230528.0.154326` - linux; amd64

```console
$ docker pull archlinux@sha256:3317d3adc1a1f4b85e81155b46c1e367bb9b085bbaa1ca87e4640cd2e5fd8cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252919851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819b57250da9b69d039a563491c13407eec79cf6d620faab7a1d9c4bd341d781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 20:20:53 GMT
COPY dir:44daec227b53dff21531675eb39198acc99b78db7d8bbad351395eeb4ec096dc in / 
# Tue, 30 May 2023 20:20:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 30 May 2023 20:20:56 GMT
ENV LANG=C.UTF-8
# Tue, 30 May 2023 20:20:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:45ff414ffddb9107ed6633f3e3b38d498f0389de57fb0e9f523624790b937b12`  
		Last Modified: Tue, 30 May 2023 20:22:09 GMT  
		Size: 252.9 MB (252911130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43212488f1a732a4a7904dfc536c8069682e42e2392388c4035620e77d8949d`  
		Last Modified: Tue, 30 May 2023 20:21:36 GMT  
		Size: 8.7 KB (8721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:1b020d5df52c08550f9808060a5f8989fba361035030d819e0cccab98b7442e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

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
