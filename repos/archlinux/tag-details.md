<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20221120.0.103865`](#archlinuxbase-202211200103865)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20221120.0.103865`](#archlinuxbase-devel-202211200103865)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:353e92f6b8bcd32ae55780feda22ae68cce47c2f41f0c41c2ee596a2e969c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:21f87bccb97e84c5366caec636c91b0044117bd7120e10bc2e5fce9940b184d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141825444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5247f2e8791059f956689350f390e9a9fe2857dbe76b88ed7f43392658ea97e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:21:42 GMT
COPY dir:e6a6f7d20c2c15d3c136a01db74e687bd96b9e7217fca969d89be9378b7748cd in / 
# Mon, 21 Nov 2022 19:21:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:21:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:21:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d1706afb11ef76505bce444478fb027cce429b13f7111429bb69ae89fe771e8`  
		Last Modified: Mon, 21 Nov 2022 19:23:25 GMT  
		Size: 141.8 MB (141817489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d81aaeee7fafb87979c2de72766ed156d0e669f00513197d769c535ac95fc0f`  
		Last Modified: Mon, 21 Nov 2022 19:23:04 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20221120.0.103865`

```console
$ docker pull archlinux@sha256:353e92f6b8bcd32ae55780feda22ae68cce47c2f41f0c41c2ee596a2e969c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20221120.0.103865` - linux; amd64

```console
$ docker pull archlinux@sha256:21f87bccb97e84c5366caec636c91b0044117bd7120e10bc2e5fce9940b184d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141825444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5247f2e8791059f956689350f390e9a9fe2857dbe76b88ed7f43392658ea97e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:21:42 GMT
COPY dir:e6a6f7d20c2c15d3c136a01db74e687bd96b9e7217fca969d89be9378b7748cd in / 
# Mon, 21 Nov 2022 19:21:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:21:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:21:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d1706afb11ef76505bce444478fb027cce429b13f7111429bb69ae89fe771e8`  
		Last Modified: Mon, 21 Nov 2022 19:23:25 GMT  
		Size: 141.8 MB (141817489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d81aaeee7fafb87979c2de72766ed156d0e669f00513197d769c535ac95fc0f`  
		Last Modified: Mon, 21 Nov 2022 19:23:04 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:edc85ab8aca021f10e4c1cde0c7e8fee1cf5ba06f1c35e95548951734fa9e8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d8b519a56143e1effcc578ec70f4aa8fffd299f8ed3b30ec9c44854d1c0fb72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243038466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8081dcb4ed80b08ba4840fd8a01d8aa5474b80907bec01120bb40dff751796d8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:22:41 GMT
COPY dir:98fb3009f9c7f9a83ff303ebfdc4cf40b4ebafdbea31741327bd4b8fbf93629c in / 
# Mon, 21 Nov 2022 19:22:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:22:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:22:45 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2949cabf88761e050f296e873f3dc3220b14f3119ab2de5578ce220e93b3d0ff`  
		Last Modified: Mon, 21 Nov 2022 19:24:10 GMT  
		Size: 243.0 MB (243029833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a4d6c177105fc09d8a72f786c0bbbdcbdb2a0ba4debc2733246dc6beb6ea8f`  
		Last Modified: Mon, 21 Nov 2022 19:23:37 GMT  
		Size: 8.6 KB (8633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20221120.0.103865`

```console
$ docker pull archlinux@sha256:edc85ab8aca021f10e4c1cde0c7e8fee1cf5ba06f1c35e95548951734fa9e8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221120.0.103865` - linux; amd64

```console
$ docker pull archlinux@sha256:d8b519a56143e1effcc578ec70f4aa8fffd299f8ed3b30ec9c44854d1c0fb72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243038466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8081dcb4ed80b08ba4840fd8a01d8aa5474b80907bec01120bb40dff751796d8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:22:41 GMT
COPY dir:98fb3009f9c7f9a83ff303ebfdc4cf40b4ebafdbea31741327bd4b8fbf93629c in / 
# Mon, 21 Nov 2022 19:22:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:22:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:22:45 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2949cabf88761e050f296e873f3dc3220b14f3119ab2de5578ce220e93b3d0ff`  
		Last Modified: Mon, 21 Nov 2022 19:24:10 GMT  
		Size: 243.0 MB (243029833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a4d6c177105fc09d8a72f786c0bbbdcbdb2a0ba4debc2733246dc6beb6ea8f`  
		Last Modified: Mon, 21 Nov 2022 19:23:37 GMT  
		Size: 8.6 KB (8633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:353e92f6b8bcd32ae55780feda22ae68cce47c2f41f0c41c2ee596a2e969c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:21f87bccb97e84c5366caec636c91b0044117bd7120e10bc2e5fce9940b184d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141825444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5247f2e8791059f956689350f390e9a9fe2857dbe76b88ed7f43392658ea97e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 21 Nov 2022 19:21:42 GMT
COPY dir:e6a6f7d20c2c15d3c136a01db74e687bd96b9e7217fca969d89be9378b7748cd in / 
# Mon, 21 Nov 2022 19:21:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 21 Nov 2022 19:21:44 GMT
ENV LANG=C.UTF-8
# Mon, 21 Nov 2022 19:21:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d1706afb11ef76505bce444478fb027cce429b13f7111429bb69ae89fe771e8`  
		Last Modified: Mon, 21 Nov 2022 19:23:25 GMT  
		Size: 141.8 MB (141817489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d81aaeee7fafb87979c2de72766ed156d0e669f00513197d769c535ac95fc0f`  
		Last Modified: Mon, 21 Nov 2022 19:23:04 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
