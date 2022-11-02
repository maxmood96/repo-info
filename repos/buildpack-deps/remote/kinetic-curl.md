## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:d95a7c84585ca7d415c76ba58f3c14d933fac1e80daf3f6d6e04c5ac7493d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:628343781ded2c94ad5718697c35e308a5f311e55d0cdfa5683a3212ef1228b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37871048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5734d54baebbd154ff8e126a96d0562dc73c32d57f5533596ca492663f206b57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:42:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00919c8a5cf1930144d6fd110c137244137a98d7a72e6a12685a879091389d23`  
		Last Modified: Tue, 25 Oct 2022 09:53:54 GMT  
		Size: 6.8 MB (6779535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895cb5b3ae5f27255eda4cb39e4ed45bad1d38cab7a215c9e80ea9d4fcb23d67`  
		Last Modified: Tue, 25 Oct 2022 09:53:53 GMT  
		Size: 3.6 MB (3633931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8aca6427cecb7148d83318aef5f511ae84cdd8636c4d109acc14fd1a186aa3b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35627130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef90be293f9f664b6bffd166899798396c391304c0804dc7150ad8fb96cb6de3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 17:59:05 GMT
ADD file:75349a3eb1b6088d6273239255c38f1b06092238dc4f33150465f79c3dfb0d2a in / 
# Wed, 02 Nov 2022 17:59:06 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:24:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ceab7032a4972ceafece338b0f5e3ebbc81d48d712647ff011a102e03e71d244`  
		Last Modified: Wed, 02 Nov 2022 18:00:51 GMT  
		Size: 25.9 MB (25871361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5cde5881687bfd0f5c7814e306e45ba740d0b7a55578dedc1cf6e332748645`  
		Last Modified: Wed, 02 Nov 2022 18:32:30 GMT  
		Size: 6.0 MB (5954638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbbfc114f5fb1e6d3ab4d8d42d3252c89f60f18670e7e7047271d69bcb04024`  
		Last Modified: Wed, 02 Nov 2022 18:32:30 GMT  
		Size: 3.8 MB (3801131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:373a282293140d34f364cb32917ccbfbb1b5657135e1d5b77becf7ec26d57437
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0532ca7c686b7c5989d673e4c097b51d9fa7759a3b351e18ab993f11252e5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:06 GMT
ADD file:30361063c284df6e20a85ff95b9c7b93648fe9e04ac935c9ff888e5c5f3af7ea in / 
# Tue, 25 Oct 2022 05:55:06 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:19:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a2e58a4bc1e52e3ab8904706a68a79146364ec32d8caf1bd106c3c9966a38fc`  
		Last Modified: Tue, 25 Oct 2022 05:56:30 GMT  
		Size: 26.7 MB (26676995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c8913a9c66f64a1f5ca1349c8a8b9923f9eb9c8aed25bf3ec160a33e5a796`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 6.6 MB (6607031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491d7cc7a42af61771e26652e91532db813e380fa19339f7279420206df0290`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 3.6 MB (3602476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3bc1adbecb0a3a041cd571aa13c6e57ea14259dfb9b72b23c0c77cb48c575822
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44214283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461faf967c1aea30f00dedd094b28774cfc501b03119f483e9504e67f8aac9e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:47 GMT
ADD file:02ef6cd7544bbd78972e9193da5adf058ae660c0dfbdba6a01c6dd53ca0dd4dd in / 
# Wed, 02 Nov 2022 18:17:49 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:44:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:345382392ac82767fe9071a0db9ec45e49ca5810d51499caf1f2e1f9a5219733`  
		Last Modified: Wed, 02 Nov 2022 18:19:26 GMT  
		Size: 32.1 MB (32099850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a66230aa93af28fd2ae7105d7436076c43a6e62ef4e40dfbd05bad90cd6d6b2`  
		Last Modified: Wed, 02 Nov 2022 18:53:26 GMT  
		Size: 7.8 MB (7752358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d5e0c03ca131a3450680ae21ae96995663400861d73240ceb2a708f69c803`  
		Last Modified: Wed, 02 Nov 2022 18:53:25 GMT  
		Size: 4.4 MB (4362075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8a15a4dc4e2bed4e6c918c30e78a154640305642174809cd2068ea57b92475fc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35438670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbd0430fb0003ea049701c4e4f48c263db2fd0b465b629c023af10128ceac8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:25:56 GMT
ADD file:8b523a4459cfcef333ade98289072a047a1f716565672fbba2b99fa0b7595bff in / 
# Tue, 25 Oct 2022 04:25:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:59:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f4447a9c12287b9486384fdda13ff5d2394a84fa81f944b1df82a6c65cacc889`  
		Last Modified: Tue, 25 Oct 2022 04:42:49 GMT  
		Size: 25.6 MB (25621218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc55b17f01e8499ec0532021df7869d72331bb1a3894bd93e3d212b1498e245`  
		Last Modified: Tue, 25 Oct 2022 10:37:50 GMT  
		Size: 5.9 MB (5936166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edee1f55b908e16aef18d4f96c19a0fa263eb259b672dc0e87b32f06e8d90562`  
		Last Modified: Tue, 25 Oct 2022 10:37:46 GMT  
		Size: 3.9 MB (3881286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:213c078da2e3330a3c24bb5ac58b5554ddb27165bcdb98acbfc84c955f2b6e87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36121437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c8da9d449fb485f6b6e48c4e4fc3579f503e3537394393bb4fb2d8ecfca4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:49 GMT
ADD file:09ee4d9832dd5806eff549d8fa985f38ec5204ca80ef0fe5c5e614802cfa064b in / 
# Wed, 02 Nov 2022 18:42:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:06:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:06:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b34514224fe768d909b05dcd6ac27c44f4e63bef04be0728f33433ca9a7798ab`  
		Last Modified: Wed, 02 Nov 2022 18:44:17 GMT  
		Size: 26.0 MB (26022224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d108ef6171fca3acbbf9623da81c6b8d324702f4cc40d243121893096d6041`  
		Last Modified: Wed, 02 Nov 2022 19:14:38 GMT  
		Size: 6.5 MB (6474315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c2b98692a0e66d0c62cd87407d4b34cdea4894b835f55ecad111c89a807a5`  
		Last Modified: Wed, 02 Nov 2022 19:14:38 GMT  
		Size: 3.6 MB (3624898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
