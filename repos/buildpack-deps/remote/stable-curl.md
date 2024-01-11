## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:7a06079135b92770afadef5c953864488b1b6ac259af344556c4b01a2fd2393e
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4dd8db7c989ab704518359c5193bc0300e385e70cc22cc196839b987ee5c5aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73607984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a5822960447c9e7259a31f057f09fc8c27e01b7da993a202d030320958730`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:390f50a032923f246d5a5df336203e186a8e7172b92d0aa8eae7b7929a7dd369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70043879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8fc90fd2b8868771734a3c47d342dda49fa8df68657aa64e0482b50cdd3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3c6d70a61861b29ae9fb0496e45e73d9c6ad089e09c5b09515a756ce97530e13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67106583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a7e305942d46d87f6238a7b8a8aec42f6e4f5768f75a20db9bc5731b148fa7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08234a7fda165f1f2cc19d1327c94f96cea2af0d0c09ca8bba8529c957a8ffb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73174530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d766d8fb19e2b942e22e45bf09333640c72b15999aa01a5b9d99bdefc11cdd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1f9923e304299d2474f842f8d4baf9d587d276bd686e12b78dbbd79735eb1d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6d5564246daff8d2e8c4df5a5863cb8cca8ea4cd1bbb7e495b3d9f30df8519`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:28 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Thu, 11 Jan 2024 02:38:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abfb5cb040b6af10cb1e9ac26bb34229604ca8c2cd52ef5bf19c4b933dd6600`  
		Last Modified: Thu, 11 Jan 2024 04:41:29 GMT  
		Size: 24.9 MB (24884306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:306e0f48708a4b3e61a51b422bfcf4b9f98cb6750c2bfce46813fe613fce766a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0564a093b4b0480e75d0a6505e99350608f55777394e80a5b96037150fe5023`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:06 GMT
ADD file:e632734e8c2b1e7594b8a79fefe3b2790d6e662e647019a7daa2713f4b1aa7be in / 
# Thu, 11 Jan 2024 02:11:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:48:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32de429a78b4633d08d4ddf9cb62b7ff44ee9ed79fafe52b6d33ec4e772c2beb`  
		Last Modified: Thu, 11 Jan 2024 02:21:59 GMT  
		Size: 49.5 MB (49548641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdc39b4d6447f4b14a9d2668a4ec5e5cf44bb6dd0d7958fc882ba5d7297cd1c`  
		Last Modified: Thu, 11 Jan 2024 03:24:15 GMT  
		Size: 23.6 MB (23630453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c7fe3373d84a62f8cc34f8ae62c92bc2211b446bd0dfd36734417f5f37c2414
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79253899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b50142e354daac39a02610d6a59a3d4eff397c98c12095d0a18f46e2311e682`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:31 GMT
ADD file:1728d055717ccd4f036c355a84deb6451942dd6e2c7998ee9d9d4edb3c02f7f4 in / 
# Tue, 19 Dec 2023 01:21:34 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:43:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5382b02d02e48b7676d14a370941b889916302c0c0a4ce6eed6a87ddd65e5a3`  
		Last Modified: Tue, 19 Dec 2023 01:25:50 GMT  
		Size: 53.6 MB (53557744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bef292d6dca0f2e01dadfb6697f50846fd2abe37345bd28c4b40d155bd3efb`  
		Last Modified: Tue, 19 Dec 2023 12:22:47 GMT  
		Size: 25.7 MB (25696155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dbce2e1b781ebe884e9784fa983049e99abc15b2bd33ccea7c62d347cec72ec1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71961129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83fde389b074fbf56bf7cf9ec00e69acae4c5b5f72996047d1cbd409e511162`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:44:46 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Thu, 11 Jan 2024 01:44:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcda5a31401318d38b94cd36426844d1953c0561252561b5205f9b95c442bac`  
		Last Modified: Thu, 11 Jan 2024 02:21:00 GMT  
		Size: 24.0 MB (24043257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
