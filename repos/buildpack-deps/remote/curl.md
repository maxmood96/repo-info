## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:140dce11e57c0c18c80c199b215138f7225a79f1ff343ca4cb92c885d948dfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ce7e846f60727efea42b5abdfd8673e13a94e288c6a5d7c37da1973ce7c5d78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73582025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c399a665f317215e5dd18dcf72a1723bc891edc5df1e57bf176d1c65f757cd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd206bea61ff3e3b54be1c20b58d8475ddd6f89df176146ddb7a2fd2c747ea2`  
		Last Modified: Tue, 04 Jul 2023 03:51:23 GMT  
		Size: 24.0 MB (24030593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cd79b4dbc7daadcec5980ed2d535ce9340c36adea17ccf7dbb0c0d2712ca57e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70111719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea85fcb87a6435ababbbc09b75d697c82c737049086f3d59690dca803e1758d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:22 GMT
ADD file:09001854dc5081f907ac2a66d301e4b3d6b4bf2c2483aad5395a535bf068698d in / 
# Tue, 04 Jul 2023 00:48:22 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e0a1f476b42bcc214197ec9c5ef753ddf2ab36a314416a6ac96cd921ff0d41d`  
		Last Modified: Tue, 04 Jul 2023 00:51:29 GMT  
		Size: 47.4 MB (47402786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68311cc5ff511aa59283fdd7f1e25bc33dfc3ad9ae87e5c94447f36c3f7c4817`  
		Last Modified: Tue, 04 Jul 2023 04:28:32 GMT  
		Size: 22.7 MB (22708933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ee52b93b57b097abb318a077905af9d187e98a1feb6c49f47ad7368f254dac9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67172647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7745cabe6a186fe38c73aa2d5384961dc430b541f6f0ccee40bb24c7865441c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:57:42 GMT
ADD file:279ef7213d41f1f7ae76bd76293a5107fd1f8caf557f837cab9c834d2841e031 in / 
# Tue, 04 Jul 2023 00:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:49:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9bdcf1a9a6361f231594c76a75bfb4c2fef5f9745b9713bbd50efaf37ca11b8`  
		Last Modified: Tue, 04 Jul 2023 01:02:26 GMT  
		Size: 45.2 MB (45236201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ee33ea63b2391e912423c14b2f1e789137ffb03659568cb361a2fa2b4efbd`  
		Last Modified: Tue, 04 Jul 2023 06:18:41 GMT  
		Size: 21.9 MB (21936446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6b1b12d88f18474b52830b7189f2d54b534002ee9b00dbe7a5947684dbbef4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73142327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccf74d87c178f322cc3cc0e5b79bb62adfcb518a1c78943c8a7d7241427f748`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0518ec57568a70561f7c04650f9554c88dada973f54d88e36f65b0796d35de`  
		Last Modified: Tue, 04 Jul 2023 06:21:03 GMT  
		Size: 23.6 MB (23569546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abb0cf0f3dc36c7e284598893d32388fe2b09b68e02ef75869a6ddce988d6624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75432135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce569bff52f1ef304acf004cee953e9829211468502cb021457f297c7f8d098d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:25 GMT
ADD file:e0a25fe261e09183ec383698ab2c800f93c5b0805564d7104ad5119db52cccb7 in / 
# Tue, 04 Jul 2023 01:38:25 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:381263dab43af8bfb8e85c7a9a32f35492cbdcc3a046b35f947cf3bf3a55f4c1`  
		Last Modified: Tue, 04 Jul 2023 01:43:02 GMT  
		Size: 50.6 MB (50562388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af522778d6fcd5f4b85dafb1f21b89441dedee6ce875890b15ad8c454bbb9fe6`  
		Last Modified: Tue, 04 Jul 2023 05:38:10 GMT  
		Size: 24.9 MB (24869747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:42c022c724478620aab86e25894ad7ed4983628338234841643275c750cf7eb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73153276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7440c8f98ae3b5ed63c6e5c21ade2218dcc623c7b24bcc429ae5b03fcec14d49`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:08:08 GMT
ADD file:fbe506fea544eae98a8a13d6b55d001b4327c933053d898d5a19bf9ffd7470f8 in / 
# Tue, 13 Jun 2023 00:08:13 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb5fba29e113a7ea4313a026e3a37cd5bc1425850dfd19a63973d48c89e0f266`  
		Last Modified: Tue, 13 Jun 2023 00:21:46 GMT  
		Size: 49.5 MB (49541536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d455436c8b88038e08b0000c9ee013619617a7c7820a0bf065a54b80a660d`  
		Last Modified: Tue, 13 Jun 2023 02:19:52 GMT  
		Size: 23.6 MB (23611740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dd742426422d9d9c53b1f294d91895bd56b7748b0a559826babb53cec399ddef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79218037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4572b0656e7dfc6731b3f7dd64ee5baeb3421d7762079b77c60f1226bfa152f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:17:23 GMT
ADD file:5aaa642008df5a97014e76042a767f06bbfda91db1d5f336a1b3f98e9b11c7a1 in / 
# Tue, 04 Jul 2023 01:17:26 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e039cf6634cf83a31e97e2a56b4db40a8c38a62d6857c77e687d5edb3eb0dfde`  
		Last Modified: Tue, 04 Jul 2023 01:23:59 GMT  
		Size: 53.5 MB (53536740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fff62f5ff539ace95f1581096d57b95ca024b9d5cc7c85bb4a2bf159ad845f`  
		Last Modified: Tue, 04 Jul 2023 04:36:20 GMT  
		Size: 25.7 MB (25681297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a798ecf011d711b31bea6acffa8e271e0dd369826fd2813a2472fbca9be8eae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71950258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cd125487e510aac59f7d8dd47244374ae0ba8c9e1ad6fc49b0a5bcf2cd2162`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 04:29:22 GMT
ADD file:249060834694c2236703705d65a79827f5e97ac9cf82b79a6941cf0f47134556 in / 
# Tue, 13 Jun 2023 04:29:25 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:568dd23e2b461377b9cc9f517f959ed366ef5f337dcef4396672fcf62e6cdc68`  
		Last Modified: Tue, 13 Jun 2023 04:34:06 GMT  
		Size: 47.9 MB (47921596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddffd93669165e140e3013df0db3388c86878eea11b756f8926635d0f203ff48`  
		Last Modified: Tue, 13 Jun 2023 18:37:41 GMT  
		Size: 24.0 MB (24028662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
