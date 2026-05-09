## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:a2ef37767737497d29f3aaf4ee7bdca70d80a40d3af6670fccf389efbf7346e8
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
$ docker pull buildpack-deps@sha256:9c4bcb19f3b18348937640316eaf80b038d82a132ae0f3fc63e4df6b4b8664a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69554038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d605bf1ea3c6464dcd265246f5d852aa7f6ee2b0c0738a2bb2b569e915dfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9888e096307133d2fbd60bcb00b491486db0aecbd10ad65207abf37059a9af`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 15.8 MB (15790695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd5060b6b0f434a2ca6cc31afbfbc93011edea5271179cd7f1a8bca19537296c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86366218b5921b4b870c867d6e08a7117c21e3e6f3150a39798ed73fd64c58ca`

```dockerfile
```

-	Layers:
	-	`sha256:3a95f844ee4f4bd303c404be345ac5077091a1bd1091f0e4b584626d5a6e409e`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77dcf59e13b0cbcaa1aa14e5f48eab9632197bb1a2607f81e6c38c9ef31369a1`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3cbaea61f13ef1c978dc5e3523d25873e1b70958393fa1b9591d948b3a83ce15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63960176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44228415dd1e883f837e10a0e76114394ba2283d29cdd3f79fc02907cb415aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4cb33fa51e00f2c5cad3e12a59f701c1cb73526295425e2f64b4cb13b9375c4f`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 49.1 MB (49055106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba52e9af1266c17416a17c315f698fb07fc71701dcf95b70a57e9d0f65c70ea`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 14.9 MB (14905070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eae36042625ff7470cd9e195c87427e56ee16b4ef9a5fb97e7333756786de1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae19f06cc82c5ad35ea6d86dd66ab7d31ca97bbb7cfe7d9eea0982e2d1b01624`

```dockerfile
```

-	Layers:
	-	`sha256:c53e9065a4dc2b158fa14997169fcfeed70cb588008119f30f38167eea833b11`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 4.6 MB (4639155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974b0c4f067ef868f0b565704e87b95cd4ffce50c9acecf84db4dd16eb870ad7`  
		Last Modified: Fri, 08 May 2026 19:44:46 GMT  
		Size: 6.8 KB (6827 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8c226d8482cd4116684fc284172431affb779c2c645dc27f28e29a650f8cccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68028044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce33f7d8e6aa3719c56930b119851055b9f54200e68626b3ccb76ff8fe45ca1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d20a72a3ae72af0f6239652b45dcc6f5eda87bb797e4c05972c586c32afca3f`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 15.8 MB (15774834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:992b3d6330dcd43af0ef3b5c351de937dd4b704d3d4f87f05d6150f5d37d2798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c129b228dd57bbb5f0fa98b9093e66e28661020d73a47ad60a7601cced03a18c`

```dockerfile
```

-	Layers:
	-	`sha256:aa73aea84017ee42d0521e2e41899558f5e43b9e0ae5b3ae5ae1af28fc0af7ad`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d341aab8e205eafc8124bb4a0eb76602588e4e5fbc839b5a36292dba05233e`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 6.8 KB (6843 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:576c0b696b6422ffc11fff24f4af087e116740b350383e480c7cc438b023dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71000940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87c331c023550bd1a52496922164899f7a84050d7247e5776970d5a52232a42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bebb3bb20b05d30c1a5354688795bd554c50c12bfa7e9190aa4a54c7dce2a8`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 16.3 MB (16295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60e8fd768f37bc2081ae6b32085725bdcdeb38a7aa6415b7c6382365281e898e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73ad575011483f91e980534a8ba54d6fc25f99b1dcda4118914a29711823c66`

```dockerfile
```

-	Layers:
	-	`sha256:312a964991b4d2502d1ffd4c7bbec549ad2d85a27889bf444178c7ec98c60104`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9a9f56fbe225cf4c2622aa62a5ee43d7aa8b8d0ad2b63adb789eda52669a05`  
		Last Modified: Fri, 08 May 2026 19:43:40 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
