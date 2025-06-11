## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:5b35221bef717e3430beeca5d955c67824c7eb4790baac33acfd6551c1e766af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:515fcf04ba056429ebee62fbcf672d2bde08d5805830b41124968ac08648a121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69519921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86b5eb1a082675a1d80dd116530f6883f4b835bf6cd797cba679170e7dfa3d0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d3a1104916c86ec83a5747c8e633c5e6a390c0dbdd5bc0f94c97267b2a5943f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c3d79ae9421feac66d97d4ddc0adb912b6586a0e7a9cbb561a322df85dc96f`

```dockerfile
```

-	Layers:
	-	`sha256:bc88771a7a79518a75ecd38d86620125a77ea3bfd2047014d8c2cc0727a390ba`  
		Last Modified: Wed, 11 Jun 2025 01:19:53 GMT  
		Size: 4.6 MB (4629093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490e6206df775cb69679892caa2c6ede1b5184d9699ab680489de70e0579637c`  
		Last Modified: Wed, 11 Jun 2025 01:19:54 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9008451d4470a468b67ec19ef2dd4f7cf476eec8a734a2764401ff7e30daff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63924626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e9cc9c03bc387d23923e19cb4ee5df6774a59ceb7e0106beca1dcbda66e170`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 04:58:19 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ea17bd7094a0c2702c4163e2d05ee9f740d03dc9b4b525d4c9a39930b8b78c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9eede969f6f83a3716f751af3d50b0769c48852fe4e1ef10a342c3ded40ee5`

```dockerfile
```

-	Layers:
	-	`sha256:f6c147fb19322348b1521922cae7e1d00eb582c6e9f8b35b8c90e47ce23cf888`  
		Last Modified: Wed, 11 Jun 2025 07:19:50 GMT  
		Size: 4.6 MB (4630729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868e427b47bcb780df552dc621d7cb95f421dcf4897424cbf078b01de94fef0a`  
		Last Modified: Wed, 11 Jun 2025 07:19:51 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b9d0d2045b4e4731f06ce82a7bc992f9cfa3bd789e3557977f63e7b9636f1e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68002867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252a02a9da2ae961e8044b00e8f7a505062f38524f81d4d1f213ac8e7fcf9d74`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d4390d793c46c29a0d236b81bf5d4fbcd71db7d13737c6f280992c6248a558f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb38f54ff64e37b59a85de61cb8d76bfe2bb211a8bf91c771cccd53a27b09bc5`

```dockerfile
```

-	Layers:
	-	`sha256:9ad50f007de9beee8c2d1895736683fc3d4843aa15905abc56d9c7a66c934710`  
		Last Modified: Wed, 11 Jun 2025 04:20:10 GMT  
		Size: 4.6 MB (4628707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0da400629948fe6831148280a42fabf72aed9478fe83315023a553ff11620d`  
		Last Modified: Wed, 11 Jun 2025 04:20:11 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4eb2b7dce67f595c84935c4efc0d19c9e2219f9e98916b18734359c992707872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70958629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a1b2fd3f225b14e162d2febe0afc78240a90a3ca1b203b56780481b392bb49`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18e5f62f541623b085b1ac220a18694c1555eac27e8a78c5a99f3033b5f45f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aa675879b87d355814ac082aef7aa54ecda54f94cc3942bdaf018d76d36f93`

```dockerfile
```

-	Layers:
	-	`sha256:4fba12781b7d1378ef087efc88baf5752a3e7fb7d57ff3f37e275cc5fbf48c16`  
		Last Modified: Wed, 11 Jun 2025 01:20:12 GMT  
		Size: 4.6 MB (4625596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8e32e1d13b9cd655b8f52fd5cee62f6ae2ec79d99a99544c31015763dc0625`  
		Last Modified: Wed, 11 Jun 2025 01:20:13 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.in-toto+json
