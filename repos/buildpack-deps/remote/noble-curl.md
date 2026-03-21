## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:063c8c84355a91d90b216dea62a6a9b462367ad136158f88a157f6f206364e3c
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
$ docker pull buildpack-deps@sha256:35c90751f8dba4aadeed120cc23298999575c7c301db58b12e7dbf43bdde7209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43363000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c88df4febf06f9ea382955a23e241017b57f448b1dd06c71c25a9ded3cfd0a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37893ef229d11c7b2e7f03e7e2fe577a02b63a79031bbac07a7ef958651051e`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 13.6 MB (13631007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a6650ef4d2c6622197dd10f35702291366c51ddcdb0fdeca7f0fbd9ab365e547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7455dd1db8c07f3faa560560b4e2d8b9535885123fd3ce898462c6b8bcbc9d2`

```dockerfile
```

-	Layers:
	-	`sha256:3ebea8f899248ed695fc04aa35ccaad993b008c50655bad9f131350399431530`  
		Last Modified: Tue, 17 Mar 2026 01:15:31 GMT  
		Size: 2.6 MB (2607837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea8d2b4962c633ea1f40394c567a3ce58fb2cae8435901e78f1256666ff7da95`  
		Last Modified: Tue, 17 Mar 2026 01:15:31 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83c9b40425a117cd7812d6984605e69e5aea5b9df0b2441a8c51683cb90f0efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39647671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f7fd9cb86649d7ea71edac15b85368a351b7b5683510210d3d92e52c575c08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:10 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:14 GMT
ADD file:834191023ea63b612bd409fecc858bd572114f2ce02aca5944385eae5eaf48f8 in / 
# Mon, 23 Feb 2026 17:19:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51c4cbb22341ed2a12c82974973354e1be3db5c9041bb5fbe2640ced2f41020b`  
		Last Modified: Mon, 23 Feb 2026 17:51:31 GMT  
		Size: 26.9 MB (26859311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79a21860b786c32e6868f43825286a9abe5aeca43531e53711cc81e1b02114`  
		Last Modified: Tue, 17 Mar 2026 01:15:19 GMT  
		Size: 12.8 MB (12788360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83e838feb9b20faca1bb8ed75779b81baa04dfd473c635b224bf9c63af461d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c929d7edb46360c97911732861482d03b8100f9c55ad1487ff8cf61251797e0`

```dockerfile
```

-	Layers:
	-	`sha256:c416685102bd20901e9e7b07ba9c22903448da39de6fefb6e3b0cb0dd7c62550`  
		Last Modified: Tue, 17 Mar 2026 01:15:18 GMT  
		Size: 2.6 MB (2610141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd6a18407f0c10f8259e93268398baa05e56f9d00d29f5943d21eac08d8c052`  
		Last Modified: Tue, 17 Mar 2026 01:15:18 GMT  
		Size: 7.0 KB (6980 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ccac5e49f927460f31a22eedf74475fb0a14281861eefdde396ae9acaa3ee5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5383663b9896534754ba5e67010eeb00629530a95deeab5ad3dfd99e743ad6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c14c4233e7d75a38c201e9c5e7f07020dd6f8701769cbea2931551396595d3`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 13.5 MB (13465941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c885a73319206cf00836009800fd79f652acd55a092ceee057c4badca1fe0861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb904dceb90c44d301989d5c4b3c854b683c42874855a31c43b539ef20b3af2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4232983cec16c35be21f5486d54d0be72d36dd081a016da8292816a7e61c59`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 2.6 MB (2608895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8365c904be26aa2f5f1c6bd55c1218b03d3d66e82aafb0f6bfee8ffb68d47d74`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.0 KB (6995 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4cd042bb6ecadef05d5f8da90b32ad4318d9ebc251230f49c5f0e9e01e5b93b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50270320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fe6299b9a7dbf2110aff9ba443f087f805438e98609d8ddcac1fa926eb6892`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e63789dae837b8ef69e9f3d52d1fbec8927249cb62a287e89540342d490b8`  
		Last Modified: Tue, 17 Mar 2026 08:27:28 GMT  
		Size: 16.0 MB (15960269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e9ef5401735ab48ba96ea7f21b601569cbd9563fb83855771d22c5049326213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fc0ff8736a54f52a52bc6ad1e6e1f03eed93634c4e25a7e612b5cee2664db0`

```dockerfile
```

-	Layers:
	-	`sha256:5270bce496cd6eaba98ba5abc4ea84828d00e7806e32999f3ec42d7b09267848`  
		Last Modified: Tue, 17 Mar 2026 08:27:28 GMT  
		Size: 2.6 MB (2612456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181d492a1fcb743f617c457dfc4f022f46c8f7ff9ea32a81a241508552ff9d9b`  
		Last Modified: Tue, 17 Mar 2026 08:27:27 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ae930e2b521063e6400b58ca00d46287bfc6d1a35d1b9b2e3289a36a27b43efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45297023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7878d004c9ac704233c7343cb1a202b742e89464ced8dcf24bc5c4799e95319`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee039942c223db7740f8c7ddba0be9d66f5b268eae6ff09af10e8dfe9568a44b`  
		Last Modified: Sat, 21 Mar 2026 03:07:14 GMT  
		Size: 14.3 MB (14336878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f42d1e3229aee1ae47cfa2acd05315c257a6f709a1ed85b2076f52c437a85bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050c66dfdb1697967ead56a11b17d18fd1d903acd50a1d5f26d283936684d2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d5d9ee3c17495a5b17b26a797f3b10df39374f444602896d3bec8913bd1c923f`  
		Last Modified: Sat, 21 Mar 2026 03:07:12 GMT  
		Size: 2.6 MB (2601736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fddca8c363b3474ad0dffb5ea7b5c0dfb3e9a5572a71512ee21ee9150a90c2`  
		Last Modified: Sat, 21 Mar 2026 03:07:11 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9ec4c4e676ef00fff9453f166d986ff6e250e5dd6f7870d44dd9e9047bf68f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44853513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624f6799f22ef27e5694c2e73ea16fe92fd2f7e2c445256f3bb999144dfebad9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523f4e88b5222cb75f891e4de8500caa034cde5357f00050756cb250567a9997`  
		Last Modified: Tue, 17 Mar 2026 02:20:10 GMT  
		Size: 14.9 MB (14943132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e099c1af09f9cf1d7f7f90bbd5ba3f857f64f9a5a8ade56bdc9173361450171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47acf98e5bf5a728c8382aabd1852f0e16f10dd45ad6d6f5f72da20f650def1e`

```dockerfile
```

-	Layers:
	-	`sha256:b8323feaf2356cef785779160f80788586b9733277a18c0066cd2dacdc1a1fd2`  
		Last Modified: Tue, 17 Mar 2026 02:20:10 GMT  
		Size: 2.6 MB (2610662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd438f6b811cd9978faa1e17b3b1f5de47298efa1a40e88bd58f43cac0596217`  
		Last Modified: Tue, 17 Mar 2026 02:20:10 GMT  
		Size: 6.9 KB (6915 bytes)  
		MIME: application/vnd.in-toto+json
