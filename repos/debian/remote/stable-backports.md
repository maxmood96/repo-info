## `debian:stable-backports`

```console
$ docker pull debian@sha256:54d30353ae1e0bb234cc5cd98e1a06ea432139b11ca9f00444390f6dd1951d30
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d4d1ecb83eebcc3d1cd971421d013699a6f20b4aa12cfae7cd1fbd2dfa8c4721
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49554309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb831641822743079b68d4e6060ee52efaacec12766f90c7de720f14dfeaf1f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:30 GMT
ADD file:4a5ae376c911453be04ce5612fdeff5e401f6572dc2b5c8bff1b983a303bedf2 in / 
# Tue, 13 Aug 2024 00:21:30 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:21:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d2735c4dcbfe4497fefddfca90937ab24f30adfba9f41e35d636398e66e81bf`  
		Last Modified: Tue, 13 Aug 2024 00:25:37 GMT  
		Size: 49.6 MB (49554087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0168c2772470cf41792595020d90ecff66709d415d3bc5ef44951e267e4b3a38`  
		Last Modified: Tue, 13 Aug 2024 00:25:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd59f81dd27b7fa7e3a09001ccd9dcb37bb2517a02aff033fe3d0c2eb10116ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47333397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9b58ef70d2a509d1ff1f932f59a430ef6781725c33ca1e26d1790f2edbf667`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:27 GMT
ADD file:ec0bb44b5d3805a2e5db9b8066a2b84d5937d406125c67f97cb850d7524fc743 in / 
# Wed, 04 Sep 2024 21:49:28 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:49:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d8aa53e0f7995da98c9cfdad1f9d8f965a5a84786e4b1ccecb6c758c3525301`  
		Last Modified: Wed, 04 Sep 2024 21:53:33 GMT  
		Size: 47.3 MB (47333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d18b07c3a71895a5306627f272eb5d896e76746f558841ecfaa54e11190efdb`  
		Last Modified: Wed, 04 Sep 2024 21:53:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:87ee647ae2881679879d7e3976544c373e1d5a08c20a98fe3cd66444e146f9fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4227a2edeb112d651cb4dcab8e46296a2b305375012f5b30f09431f1bdd0b15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:17 GMT
ADD file:6d69eee4be8d3dc69096ba6d0ae6083cd08d608e0f6d4bf4c63d87574dda52f6 in / 
# Wed, 04 Sep 2024 21:59:18 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:59:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1aacfd79a22fc6f8b7d0a3e28ed5a6a60a17b6a06be91a14ecf3b0de0ba02bed`  
		Last Modified: Wed, 04 Sep 2024 22:03:46 GMT  
		Size: 45.1 MB (45148451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6ee6d15dd758e70dfdd88d0913801e11eea7a8b8876367f658a8892b5b4522`  
		Last Modified: Wed, 04 Sep 2024 22:03:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f9a40a2b133255bee3de7ba6c7924d216df1ee96033ccd3c2aae7341d44d7cae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9df31f9582b0582b4e791dbf2df41f7ba3501dd1587eae3b0012588438715`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:42 GMT
ADD file:aefd88d90b7065f1ebd802cd2ce02290bd918d612ccd1e72ed134583a85b87a1 in / 
# Wed, 04 Sep 2024 21:40:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:40:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8763adf53582aae4539130df0a79824468a12d27cb0f988a82aa6c3403901e7`  
		Last Modified: Wed, 04 Sep 2024 21:44:18 GMT  
		Size: 49.6 MB (49585594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a1b5652abee13ae1a7e9751fc89adeba1bc70d3542d1144691a4decf6f75d`  
		Last Modified: Wed, 04 Sep 2024 21:44:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:b6896dd777520b9af3f799c06614d8f8ed19b0f62ae7e4af60c7499303b69c14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50579600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc65142d7d3de7df1629a846068b1ef8906fec147b9f57146635a7d7c44287c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:11 GMT
ADD file:e5d33d83474558010265e3f4709201ae85dd0ceadcbfcee168d911fb87a373a1 in / 
# Tue, 13 Aug 2024 00:40:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:790eedb5a34bafcb63a3b07a770e2c220179e5e3ba6c3c5f1652d89e48d86d18`  
		Last Modified: Tue, 13 Aug 2024 00:44:45 GMT  
		Size: 50.6 MB (50579378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244628e1e3cf96de87fb022aadfcd59a42f1fa727dcd711d4d9f2bf7811ced42`  
		Last Modified: Tue, 13 Aug 2024 00:44:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:40770570cac1756456975d9fa66bc55816e5e02dcf926e52e667684c1e35f4c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7287126d7bf5dc3eb903ed8d040fd7166d1372314404499154c4ce20a3cfd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:15:34 GMT
ADD file:6d1b87941c2b356bc1237dae2b25b558c2910426fe5c20f1680ebe6a1d891795 in / 
# Tue, 13 Aug 2024 00:15:40 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:15:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73d3ff40a2a433b51a1d943cdbfbaa475ba05fcd7997ed1bc9ff63d0e0516a99`  
		Last Modified: Tue, 13 Aug 2024 00:27:03 GMT  
		Size: 49.6 MB (49563205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f24dcef952f79b50198b772fc2cb4487e80581f62ef1661abe1e4ddfae48252`  
		Last Modified: Tue, 13 Aug 2024 00:27:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f533a2757012040477891f4febfc91136539e7bcc64c738efd386193fbd4ec7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4eb2c98caaeb5d39fdb77e04a809ac111ab6ea945d439d8c03688c3bcfe377`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:33 GMT
ADD file:83109252ae4beb7d691c70b4d59da3186481c078cc4d115430a124e735ff2041 in / 
# Tue, 13 Aug 2024 00:23:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:23:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbb9d8563565c410b940b571495aec8c416dce820c3fc5925b89ef33e82cf323`  
		Last Modified: Tue, 13 Aug 2024 00:28:53 GMT  
		Size: 53.6 MB (53556925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb8fc5437dfdad123fe735801a90befe8d3ed2ea153f606fcae92d57fb8d4a`  
		Last Modified: Tue, 13 Aug 2024 00:29:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:351197cf69d4d424994e4d123eb85cbf284c8d3e47e1ecef77384e36c00bee5e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47939467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786c14735873ecd1e0b094bafe019187509440f3c940c6af7fd3cae1fac965af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:34 GMT
ADD file:4b77787828c39ca103962aa8cadf6ce27f696a549ecc4d302e09b14c67e59712 in / 
# Wed, 04 Sep 2024 21:44:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:44:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91a734b2cdf740a10d8113f3dfc48d10b4e0037b5ff88cc5bfc566190c351bc1`  
		Last Modified: Wed, 04 Sep 2024 21:49:06 GMT  
		Size: 47.9 MB (47939245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38edae4cac2814b3400f71ab7bc96f6d7a1ad3492fa15adff9ece1d03abbb975`  
		Last Modified: Wed, 04 Sep 2024 21:49:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
