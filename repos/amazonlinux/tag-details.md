<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220805.0`](#amazonlinux20202208050)
-	[`amazonlinux:2.0.20220805.0-with-sources`](#amazonlinux20202208050-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220802.0`](#amazonlinux2018030202208020)
-	[`amazonlinux:2018.03.0.20220802.0-with-sources`](#amazonlinux2018030202208020-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20220817.0`](#amazonlinux20220202208170)
-	[`amazonlinux:2022.0.20220817.0-with-sources`](#amazonlinux20220202208170-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:cd47c5b30a6fd6442767a00db594704d7220ccd29beb49e5667c25d6c84fb9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:586ecf7413d0d53c0983872be242c371d8da2ee7a57d5cbdad7761b5824a74f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62316216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341032df1f72651e5af72fefbc21a1d6859f825a8455bb890470b959d759faa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ab12022e1a7cd318058af138291d638b1024dcb9844799e8014e6e37d0b35831
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63938765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c59c262be8ebd1b4918c0709fa529587d5205204a85c86be6c30b2ac224d19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:21b5c144b6663ea5ef5d3a1961a85ca271969754f8b9edb236a93de867163df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c91344e903d6bea0fb98c8df86886491a013958ab957eb55a08e4a898727543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487998330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a9a6ede56b90857d5d422629dfecd2d2153eb3bf752bb71ae038541217232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 00:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-44ee790ea60c4090ba6e215c0d148c239e7806623b75f6f14930ce7e2f6b07f8.tar.gz"     && echo "8b5abb84b1d279d3c26a9c2721b1daa1317ca4109f56f84b032d756c3fab7368  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd6532db54d15f6c38e8c6535dea038b0e4354712e588e1424d2f035a863896`  
		Last Modified: Fri, 26 Aug 2022 00:41:14 GMT  
		Size: 424.1 MB (424059565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220805.0`

```console
$ docker pull amazonlinux@sha256:85a36a4ba91751d096563b3c5a8a8f0285c230b60fe2a5379f24d8d3e3349349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220805.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ab12022e1a7cd318058af138291d638b1024dcb9844799e8014e6e37d0b35831
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63938765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c59c262be8ebd1b4918c0709fa529587d5205204a85c86be6c30b2ac224d19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220805.0-with-sources`

```console
$ docker pull amazonlinux@sha256:5ec0b6e4116e4e9db1fa39ceeb9d548c202145d498668c1523cc7a95ef9ffc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220805.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c91344e903d6bea0fb98c8df86886491a013958ab957eb55a08e4a898727543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487998330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a9a6ede56b90857d5d422629dfecd2d2153eb3bf752bb71ae038541217232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 00:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-44ee790ea60c4090ba6e215c0d148c239e7806623b75f6f14930ce7e2f6b07f8.tar.gz"     && echo "8b5abb84b1d279d3c26a9c2721b1daa1317ca4109f56f84b032d756c3fab7368  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd6532db54d15f6c38e8c6535dea038b0e4354712e588e1424d2f035a863896`  
		Last Modified: Fri, 26 Aug 2022 00:41:14 GMT  
		Size: 424.1 MB (424059565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:496028061202e8a8c2cfce3be1569b67af168a583ddf5e5a6fc9937007042216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:feac713bf3db85be05ec483a37afd2f5953c1782a221416e30d01ab1912ff68a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56652515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89652aced48a645218387173eb8ea38224d8086241aa656c9b807c9c6e813a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:760d81932d5706133e31f2f83456e19dcd43c0ec0023c6fbb9f41a4c370258ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6d34d82cfc93e13ff3092c803ec471c6df2189ac77c7def89340908e180a717d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391435816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db54d4aae5846c92569752a868b2de5ebece60aa6b29d9bcb6a45dd704ed1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 02:31:55 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0bd20a60b455dd23e6d5a415477a24bc08ceed6abb15fc56778a27f1aa45`  
		Last Modified: Thu, 25 Aug 2022 02:33:11 GMT  
		Size: 334.8 MB (334783301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220817.0`

```console
$ docker pull amazonlinux@sha256:496028061202e8a8c2cfce3be1569b67af168a583ddf5e5a6fc9937007042216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220817.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220817.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:feac713bf3db85be05ec483a37afd2f5953c1782a221416e30d01ab1912ff68a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56652515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89652aced48a645218387173eb8ea38224d8086241aa656c9b807c9c6e813a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220817.0-with-sources`

```console
$ docker pull amazonlinux@sha256:760d81932d5706133e31f2f83456e19dcd43c0ec0023c6fbb9f41a4c370258ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220817.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220817.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6d34d82cfc93e13ff3092c803ec471c6df2189ac77c7def89340908e180a717d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391435816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db54d4aae5846c92569752a868b2de5ebece60aa6b29d9bcb6a45dd704ed1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 02:31:55 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0bd20a60b455dd23e6d5a415477a24bc08ceed6abb15fc56778a27f1aa45`  
		Last Modified: Thu, 25 Aug 2022 02:33:11 GMT  
		Size: 334.8 MB (334783301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:496028061202e8a8c2cfce3be1569b67af168a583ddf5e5a6fc9937007042216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:feac713bf3db85be05ec483a37afd2f5953c1782a221416e30d01ab1912ff68a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56652515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89652aced48a645218387173eb8ea38224d8086241aa656c9b807c9c6e813a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:760d81932d5706133e31f2f83456e19dcd43c0ec0023c6fbb9f41a4c370258ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6d34d82cfc93e13ff3092c803ec471c6df2189ac77c7def89340908e180a717d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391435816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db54d4aae5846c92569752a868b2de5ebece60aa6b29d9bcb6a45dd704ed1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 02:31:55 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0bd20a60b455dd23e6d5a415477a24bc08ceed6abb15fc56778a27f1aa45`  
		Last Modified: Thu, 25 Aug 2022 02:33:11 GMT  
		Size: 334.8 MB (334783301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:cd47c5b30a6fd6442767a00db594704d7220ccd29beb49e5667c25d6c84fb9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:586ecf7413d0d53c0983872be242c371d8da2ee7a57d5cbdad7761b5824a74f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62316216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341032df1f72651e5af72fefbc21a1d6859f825a8455bb890470b959d759faa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ab12022e1a7cd318058af138291d638b1024dcb9844799e8014e6e37d0b35831
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63938765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c59c262be8ebd1b4918c0709fa529587d5205204a85c86be6c30b2ac224d19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:21b5c144b6663ea5ef5d3a1961a85ca271969754f8b9edb236a93de867163df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c91344e903d6bea0fb98c8df86886491a013958ab957eb55a08e4a898727543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487998330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a9a6ede56b90857d5d422629dfecd2d2153eb3bf752bb71ae038541217232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 00:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-44ee790ea60c4090ba6e215c0d148c239e7806623b75f6f14930ce7e2f6b07f8.tar.gz"     && echo "8b5abb84b1d279d3c26a9c2721b1daa1317ca4109f56f84b032d756c3fab7368  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd6532db54d15f6c38e8c6535dea038b0e4354712e588e1424d2f035a863896`  
		Last Modified: Fri, 26 Aug 2022 00:41:14 GMT  
		Size: 424.1 MB (424059565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
