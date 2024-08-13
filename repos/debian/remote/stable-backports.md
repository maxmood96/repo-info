## `debian:stable-backports`

```console
$ docker pull debian@sha256:ce45c3031fa7b8e3c9604e7058d9fdb72d6c813c1c9c9c33639c08448d157ac5
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
$ docker pull debian@sha256:9b75a2c65c0a558df890506bb7d7273cf6db306cce3b9cd9b540cfe0dac0c7a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47320344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78679ec3f9680a657cc93dc13a8a004709b44ffc7c2978ca9a755b68081554a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:24 GMT
ADD file:82ad0813e50805e3408179c867cfb1b41c0aa4ff3989c0ed243162146a7ac0fe in / 
# Tue, 13 Aug 2024 00:56:25 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:56:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c72fe4118577745401176777484a4d5573019e79e85e9c1a50589c3ef15f7449`  
		Last Modified: Tue, 13 Aug 2024 01:00:35 GMT  
		Size: 47.3 MB (47320122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77026ed7354ac065731d24d12d9f44d5623c3031f7936d74b71fb550cae2295`  
		Last Modified: Tue, 13 Aug 2024 01:00:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:50c74810f9b878d6e3f5524fc107a5961ced72f753aabff9d6d9c95a70d93607
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdf704e1e7629de898a8452e3cf1e48ab0f8a8a3cf41fc1b1a61a6e9558510f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:39 GMT
ADD file:8ce547e2e0fc0f1db059c2ab76ae3a7ecf0c82faa73a35c6ee69169003a723d9 in / 
# Tue, 13 Aug 2024 00:58:39 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:58:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6e19b9a41452f444ef9919a2ba312d02b9821fe245596eb76f61493ed565679`  
		Last Modified: Tue, 13 Aug 2024 01:02:55 GMT  
		Size: 45.1 MB (45148235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a830d8c6fd4de3d45600dbd71b194549b33fc74a3424480668d869fc7f5f3a`  
		Last Modified: Tue, 13 Aug 2024 01:03:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4eb01a5c2a309c4c7dae1658bc2503c50cbf4de77d6f54fe1a037fa1daaca131
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49588840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98afdd026868042d5ecf192c950cda0a69e45097b13b3e2ff0754d42fbeae84`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:41 GMT
ADD file:f0cd237823c9aba91d71a785dd79e38fb76dc55b24c6512e1a30213938536218 in / 
# Tue, 13 Aug 2024 00:40:41 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:982959712424d5377e742653cc7235fd1bdf091821477ce8b0acc2fd5e48dba0`  
		Last Modified: Tue, 13 Aug 2024 00:44:39 GMT  
		Size: 49.6 MB (49588618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65e6df85ce6885a8867e4c78998c346b3411910a95b601e6d86f43a7566922b`  
		Last Modified: Tue, 13 Aug 2024 00:44:46 GMT  
		Size: 222.0 B  
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
$ docker pull debian@sha256:3a5fd210cb08e7e3e53090581e9820c1e0cf8d43f65ebaf8d3f3914146069706
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47931594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f92f63f0921aa5a1adacf16c6aa3fd4a3f5d5766391f434e7e0dae0a490b82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:44:22 GMT
ADD file:9907632aed6914bafc36e4c2f01681f1d33a68bafff9ec5579d87619fbd11a3c in / 
# Tue, 13 Aug 2024 00:44:24 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:44:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:98f101323faf6c329718e45a1d3e003fc15a02571d2c741bb274315aeea851ed`  
		Last Modified: Tue, 13 Aug 2024 00:48:53 GMT  
		Size: 47.9 MB (47931373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4149f7ba8093229cb2a7e604ab342bc9f204f7f2733f86d194fa98ffa407fd99`  
		Last Modified: Tue, 13 Aug 2024 00:48:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
