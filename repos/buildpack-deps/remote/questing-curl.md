## `buildpack-deps:questing-curl`

```console
$ docker pull buildpack-deps@sha256:78fcabaa4b88c1bc85df0ac3cf3169a66accf4960b59a92dc977d2e8f163de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3f83043370553840afdc7acd82bae5d29f305187bd7ef9dc0974fba0a403108a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48603303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648d441843b93fe895502d86d47fdd34a8359ec3691c2be36b54d4f46787e97c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:a74a840d4eedf15a85cf6d55ff2e2efce2562bb735481008b7b05feab3e31a41 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17bdd67b6aa5856e02c1b36cec4ec29df1dacb071c5f6279c9aea0a311ee1058`  
		Last Modified: Sat, 16 Aug 2025 00:41:51 GMT  
		Size: 29.7 MB (29740502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79c5851a446b3b5b175c8d0ac3f08bbee9078a0b4863c6e57fefddd86b32c0`  
		Last Modified: Sat, 16 Aug 2025 00:49:30 GMT  
		Size: 18.9 MB (18862801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13aeae6aab6d509dbe5cd951f31b2efc51acca20041024db06ce0f43be833b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f4d64f078d71293922385d003633acc6580d254a0cd972ccdc32e5fa7fa50e`

```dockerfile
```

-	Layers:
	-	`sha256:ea5affe8a719c47d12412d55b912f3c5eabfa03f98b95dd020adf6369218466f`  
		Last Modified: Sat, 16 Aug 2025 01:19:32 GMT  
		Size: 2.6 MB (2628771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:519da3330386e87d2b4f17a5015748c23973bd73538fc1b94ca3779db3f7c1ad`  
		Last Modified: Sat, 16 Aug 2025 01:19:33 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:07a14ac7ad0318474c2f38b1c2a9f0cf7c12f7179674a7250d080be697315a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45025681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61615fdcf297b44bbddb150c4e35b415a9e9864691f6d1834630fee5ee8ccf8b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:6cceeaa1e4c04b40ea2fa59915877179d13dfe75963b2bf5af2d179b7651fcab in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5fdf70baf2d69a62d712c5290da1eadd264d65ac840f33b44cab7084448ac925`  
		Last Modified: Sat, 16 Aug 2025 01:48:56 GMT  
		Size: 27.8 MB (27766578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f5f8859e7c63a9c160d8e856742d21c1c5cd88e9979620c98d02e7400a78d1`  
		Last Modified: Sat, 16 Aug 2025 02:09:43 GMT  
		Size: 17.3 MB (17259103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c09f16611d430ea367c52b560869e871ed1a2e8f272030b896a2877f798bd410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd7f6a1c42fa023a0c7aeebae2322ada322ff2375ae46c73fbab364216667f8`

```dockerfile
```

-	Layers:
	-	`sha256:1f0dbaae2082f32b09d5cb66207ec887c2b5072fb29b11fbe2aee08df5595ac3`  
		Last Modified: Sat, 16 Aug 2025 04:20:00 GMT  
		Size: 2.6 MB (2630276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e8c76d22ec71117662583134bc837ffc892a8f07f3a4130aef8c657d4c6b94`  
		Last Modified: Sat, 16 Aug 2025 04:20:01 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7491a591ffbe213ea4ff94320056d2a465471b7948c10db450ff2fa4fc01d759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47695086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505c5138f79f9100c92c4d2a9855d5cd7a9dd6dcb948e5fc97df8442577293a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:b572189ec957414802fcdd31718df41b6aa37b1788b72c0b4276113a05ca3847 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1303c7d3dea2855daef53d0a8f3ec020cf348b429dc95ae8653a86d0d8b8ed`  
		Last Modified: Sat, 16 Aug 2025 01:38:38 GMT  
		Size: 29.3 MB (29310925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97eb8f278e435c853098d1ffa029d384d7ea69f796411aa8cddffc825cdaae`  
		Last Modified: Sat, 16 Aug 2025 02:09:42 GMT  
		Size: 18.4 MB (18384161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0685e87338ec4638cee4587a5f005ca1722d3a4c4b17203df4ef40b4860f8108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbab29600018fb5d6f80b949fc71cc9cea4e37526b86f5594dcdea526990813`

```dockerfile
```

-	Layers:
	-	`sha256:50e438bca21c7a0190fb92e85d3a9427423c1664c450ca3f4e96e7971eead38c`  
		Last Modified: Sat, 16 Aug 2025 04:20:05 GMT  
		Size: 2.6 MB (2629030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b93c682a2b15fe3702d6cce96e2183ff3ef6b18143b2cacf305f5e1d31183c`  
		Last Modified: Sat, 16 Aug 2025 04:20:05 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:30e940dc7ba984be95f657d28719df44cddf435c5a185fa1c52b3fd522f48625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54917289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be9e11a8f04f4f671daca41384cd6fa98b4f002db6324459ac5fe3a52c4a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:9ee944b262d08273ebeed7c7e10331931448ce12dbbf68a399e8c06bef0d9b1b in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c17919b40786dbdd1b0e57e5e0f6254429096c2a4edd2c2d1abb619a9860b100`  
		Last Modified: Sat, 16 Aug 2025 01:52:43 GMT  
		Size: 34.2 MB (34171496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cee2a7f9203ea1c35edf02b23466082a11ceb072dbbb218de698867c4cd518`  
		Last Modified: Sat, 16 Aug 2025 02:14:52 GMT  
		Size: 20.7 MB (20745793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecd0a007faae6baa170252847b9595b0bf352066ce5bcea9efa25c4e89405922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf8a2f9c9569c075858753c5f6a7e95933378c203c803dd2908c78348eb1837`

```dockerfile
```

-	Layers:
	-	`sha256:7304bf7f9f92d1c6a85ab31b384aa383a980ad899d78842e8e7cc9498bd5bc38`  
		Last Modified: Sat, 16 Aug 2025 04:20:09 GMT  
		Size: 2.6 MB (2632599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa31152d203dd2c98d073a6a1fa743e8e7baf885c1317fcb2fb489b2bb57f9f8`  
		Last Modified: Sat, 16 Aug 2025 04:20:10 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:219e1fccba82e26bb799d7a10e7e7677f73b8c1e0b9376607838ab8b00d75b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50567938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e5175a07050ec5fa0d19d161dc31e17c9b211db8d4c8934d7225c875b4b6f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:2ad5f91fe5edd35a8a0cb6ec99904a35771f2b8a0819b888cca27bd2b8edc998 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c765da7735337fafbed911e71485d7f0505e50d1941beb7fa962494422b6b9be`  
		Last Modified: Tue, 12 Aug 2025 17:03:53 GMT  
		Size: 29.6 MB (29618719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c981ca1715af0d0448a048d0a4642c6a7becf08354f007f4e1da1b9569b0`  
		Last Modified: Tue, 12 Aug 2025 20:19:20 GMT  
		Size: 20.9 MB (20949219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d054b12fee6ae53954cf2ebfbc9c691353f603821fe1157f6c1bebb4f3b06283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c72e6a6c5ba8dfe91b31a4967b94ce9e3a718ea37a6e293f006f56519e9dc2`

```dockerfile
```

-	Layers:
	-	`sha256:8dcc0107bfd41ce734fcaeff14c46b13ab75b7a83898fe4477e8bb0a845e5c74`  
		Last Modified: Tue, 12 Aug 2025 19:21:21 GMT  
		Size: 2.6 MB (2629964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c70d3cc8428211b8a4c533c3af9e2f94e705d1d9dcb7ae9f8f7f80a1c26a54`  
		Last Modified: Tue, 12 Aug 2025 19:21:22 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
