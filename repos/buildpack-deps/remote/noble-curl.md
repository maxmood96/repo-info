## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:8693aea4cdad1dd3a30cc105434f7ba25d1711c976a18f80626c606f892794d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6aba59310a17a36bc3217e81410fa6d32860bbb79993a99d769d8d6debfc6d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43348130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cd46a7b89e2f8f80a0812fe95de8316d33c574330dee0d8be5fe589d3ca907`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e7b3a08fae7407ef8f950501569fa3360f18e39d873ac1921a71da14d6b9b`  
		Last Modified: Tue, 12 Aug 2025 17:23:50 GMT  
		Size: 13.6 MB (13624915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c14a7ec8227ef478ddc7bb143a0e0ac4e85e5282de4f68fb20a0436667f9d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c10a827b3bf3568bbb3cf238e3919abf46443a9407dce6f9bf5bfc2bf646b9c`

```dockerfile
```

-	Layers:
	-	`sha256:dee5e4b16ddfea50298d9fd532f43dabe1258292fe3071d7731536711fc63702`  
		Last Modified: Tue, 12 Aug 2025 18:02:55 GMT  
		Size: 2.6 MB (2607809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c450fc0990cecea288b091eb13c41822023e11c4f57ed6be90502a304d4e404a`  
		Last Modified: Tue, 12 Aug 2025 18:02:55 GMT  
		Size: 7.0 KB (6958 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:62e7431c2e0c7568bfb247c558a57c41200bcb4410052873362a2831e580887f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39634813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688ba55b02263019f9ddbf9b6b4e6f8ce4d46f4e71f768dd148e63c4b90add0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:3d0bcbe19ab589b9febc888a3f1e7d731d2ffc32ab216f5a65461d73e6542ece in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5775aaee0b6caf578e138eda76ce3385180e0796b81e02b9edf4909084017d62`  
		Last Modified: Wed, 30 Jul 2025 10:35:13 GMT  
		Size: 26.9 MB (26851072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c1e6e8d6e49b6a21d80ed5f0be8e0d1a70f1b210b7897fc9211050ac4c5c8`  
		Last Modified: Tue, 12 Aug 2025 17:23:42 GMT  
		Size: 12.8 MB (12783741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:027fced1059dfa14f53900137ca1ef1845d18db5e5638c4adee9c4146ea215bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2667c1cebd334665422fa5b7e1b18c51279f0791c3e2c9fce2076793dbaddc5e`

```dockerfile
```

-	Layers:
	-	`sha256:1ff70e8834c72dab40da734ab89c9357869f446943637f4c8ec32da9a6679275`  
		Last Modified: Tue, 12 Aug 2025 18:02:58 GMT  
		Size: 2.6 MB (2610113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e917a13aa1cb303aaef6f54c7593659c8df72cda19a2fd18ef02de6b0930418b`  
		Last Modified: Tue, 12 Aug 2025 18:02:56 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:996e41cc678d3ba6696c71933d1062cc1a201a29017a5e7aa7e9cef2a15385b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42320620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf73478a0d2f88d13ef59f13a1c7e641da0218b25e592f0bff16de4b80ca0df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62336d0e960694fc4c54a90b27a6f2b9c96cb37051a77fbecbb178ecc98f5e`  
		Last Modified: Tue, 12 Aug 2025 17:25:03 GMT  
		Size: 13.5 MB (13460243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cddd15840760dd4bf65ec681f7eceafcba5dc0338d00a969d5d42db64dc2d698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd62c1e605564a22d5e69a52e63f2c673fa68a91eee7919e810ac2c763a1cbe`

```dockerfile
```

-	Layers:
	-	`sha256:9522ed4cc8404a660c53d67e4039aa30fd47f211ab6232cb228c656be0999618`  
		Last Modified: Tue, 12 Aug 2025 18:02:54 GMT  
		Size: 2.6 MB (2608867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6357f4f87c4868c3e647500e2a44dabafcbff19b0e4630d9a0cc8d82f93fec89`  
		Last Modified: Tue, 12 Aug 2025 18:02:53 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2af7960d5deb94a2bb0a63276b708c801111c785908ae438e9e651993621bc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50282548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de58fd3de3b234f3dc7b2ef59d7a0139b192428501305c5e3659ef3e1e8c8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b91bea16983599d5d56d392195728b21b204304ef105b59dafe3b14bc2e91a`  
		Last Modified: Wed, 13 Aug 2025 01:33:53 GMT  
		Size: 16.0 MB (15952898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1838e01f1130b88b5c68defd4d063ec053e7658d81d6a1b96aec35a3569354c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92861c90cd0aa3e5af78df4a119c4453bc094ef8433a1c5fe7c14f8920570273`

```dockerfile
```

-	Layers:
	-	`sha256:91af742fe140d63de54991dfcadaf4a8e27f296ccb2770e6da48cfbc1c3e1b1c`  
		Last Modified: Tue, 12 Aug 2025 19:20:30 GMT  
		Size: 2.6 MB (2612428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3821f1b35aa1eb977cd28b9c45a16bd8ab7d4523ed94e09c9ab4b7f1069ba5`  
		Last Modified: Tue, 12 Aug 2025 19:20:31 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:674f873371034e3746b8247b7e2249dbd688d69a2cb599e99ec25bab28a9a9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45282098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4eaa43f8fc8d02434c35514a9aa521b985536bc32f339d2721b78765b5d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c92de88b6f5d1841d526c8e8cec306e3c3db1b6e524a3c75f65fcb249b90a`  
		Last Modified: Tue, 12 Aug 2025 17:28:45 GMT  
		Size: 14.3 MB (14330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d4c6f1a2d95b6c83e155bd3205992bfb0d863aa25c75f8728fe19cfa65cc345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8390323100b3caedc5d9ed3acce0dd591c65fad37912982e262b5877b8a994`

```dockerfile
```

-	Layers:
	-	`sha256:e4cc8ec5b6ef839d4e88858ef7af72a8304408925239dd0a1f1d4094830f35e0`  
		Last Modified: Tue, 12 Aug 2025 19:20:35 GMT  
		Size: 2.6 MB (2601708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30385eb35717b5720bda20cccf6a290095921a8133c3b02ec2db0b1d7188a4b`  
		Last Modified: Tue, 12 Aug 2025 19:20:36 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8999ac12837c69066d68a3eb497421a05e5520666fe296c697a3cad904c2230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44870744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d7cd2b84e13fa8959c83a40df98dd243aa2dee42e6ccf9056652754ac516bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84400ce3eef4778a70239f864f38527e70fcb56dce37d1f0c2653c9024fbac19`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 14.9 MB (14938064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1245aba6dcb3b1846c955a403132b24423b0c9089046b9682e9a8635737fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095e9a71f99f659b3a63485b3be54aec5031297720af4bf28ccad16f16a63d5d`

```dockerfile
```

-	Layers:
	-	`sha256:fc7ad93c073238e549642aae8416be0c804f99ec6a4d7768c4584719f9dc178d`  
		Last Modified: Tue, 12 Aug 2025 19:20:40 GMT  
		Size: 2.6 MB (2610634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b86dc30b7e036f64d790f03e669e7e45656947988200b4e47705ccf8aa5422`  
		Last Modified: Tue, 12 Aug 2025 19:20:41 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
