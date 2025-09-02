## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:0a38180eec511746ef2669f30c3fc54cc374efff64bdd65c7371800713cc3180
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
$ docker pull buildpack-deps@sha256:24712486bf0cdccd370abad54f5c2c90ab82deed7ef8ec4b566c6309a9922abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43347718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb398d15b2dad30e011f1b5f171b00fac531f8e2065170fd06b41aa73bae9e59`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599a0863b5086726ce474510df419769c90aac8856f7b6cd5b4f7b7a3e1d9cdd`  
		Last Modified: Mon, 01 Sep 2025 23:07:59 GMT  
		Size: 13.6 MB (13624654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:710c4fee510282ebdd45f5c89fee2e1775c619e57cf1a4bffc316161f40e757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc02a625170068f06ae6e818d7e70f0ff1c0e28407f20ef302e8a6555d0ce86`

```dockerfile
```

-	Layers:
	-	`sha256:699f2ee56b25b3d50dbdf0f916e6add934ecaa31213d9d6d9246703442f44e18`  
		Last Modified: Tue, 02 Sep 2025 01:19:45 GMT  
		Size: 2.6 MB (2607809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd46f39a7a189d64f89ec93f0fc98edbbfbc795d1d29ee029a6dd547e4b8518`  
		Last Modified: Tue, 02 Sep 2025 01:19:46 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d559c84ac4d69f6797a97d69c7dd2a65ef0a91ee669a8bf4dab00332731f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39634666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c835a9f7fff43c505fd6ca70359cff2793ec8d8de550aad176b2cfbf3fdf6b0d`
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
ADD file:cd43b2c2117454679b981355ba71c009d527d1ebe0a6c3fc69420af222fd6ee7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e823e9332188e662391782d0d87ba101759880efca7a17d9a5a20e8906cc8d7`  
		Last Modified: Tue, 19 Aug 2025 17:59:44 GMT  
		Size: 26.9 MB (26851104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24dc111693a8e008a75ddf6e402f76fa1dd1ed82cc4ed2c81d12708c71667b`  
		Last Modified: Tue, 02 Sep 2025 01:20:18 GMT  
		Size: 12.8 MB (12783562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9f8ff6b6ee7a6883fc9eacb46b8348a5861bef23e85d0147beb85a47be926b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d01e7f72ff7a7bd2164850f15ccc5723f4b13fdf789dca7eec1e023cfb1b0f`

```dockerfile
```

-	Layers:
	-	`sha256:7158fa8eafd7f3faa995d7db966ac0ff8780a7ca1a074c74e748a0ecef5dc54d`  
		Last Modified: Tue, 02 Sep 2025 01:19:51 GMT  
		Size: 2.6 MB (2610113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd528fcf5f5855e9b4f7b514685dafce59168cb138f72e77c3b7d42ac59eec03`  
		Last Modified: Tue, 02 Sep 2025 01:19:52 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b743f2dfe67080edaa9d4bbf1217b76d28a5ecd3371ae95b7893d101c6d1c47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42320255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0a677eb39f885c2445a37eae11659f77c196e6401b79394d194b96363840e5`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255c14692196785d756fa7bf53272e96460c2d3bafaf78c78a9d7f9dcbcff0d`  
		Last Modified: Tue, 02 Sep 2025 00:13:14 GMT  
		Size: 13.5 MB (13460015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11d872ecf1914955d6d801c0ee62037e2db45027cb084a3175f776dddda7c02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f5228a1ed4803a23b76ba44ce472f6aa17c32bf873f5f8a0aaca9025c5fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:df2a5b8fb33d7a187db2427d77fef9e0df08ac36973afc367740777bc7bcaf03`  
		Last Modified: Tue, 02 Sep 2025 01:19:56 GMT  
		Size: 2.6 MB (2608867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b083a19b689d18f5c5dd718cc0b4fbad0c1bc96006cf6be3f0f7ed399a1ad71b`  
		Last Modified: Tue, 02 Sep 2025 01:19:57 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7e850f11746c544c8d7f33e053f9afd46ab617bec3eb960b93135ac48d09b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50282495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84e3ff549a325c83ba3c386780fe5c91edf5a72c7350c0fb2640a4974f9ef66`
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
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b4abc25d3f06856cb737c6e84248ab748d0581d68478303f47c2db588a544`  
		Last Modified: Tue, 02 Sep 2025 00:12:27 GMT  
		Size: 16.0 MB (15952962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b20e37b1b5182bcc704e4ad51881161fb11c1fe9154c5fc744d61a3e82cb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fa604362027c754dde5344121353202272e092ecba674c26e2b176055d6964`

```dockerfile
```

-	Layers:
	-	`sha256:516bb02e3bec350aaa32d1d0cccdfa96a0e2d6cdc42f4d198eb73a38cab33477`  
		Last Modified: Tue, 02 Sep 2025 01:20:05 GMT  
		Size: 2.6 MB (2612428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081564ddf7c29f5ce8c672c42b593d07743a48f46ce2209758ccb36ca1a90d6f`  
		Last Modified: Tue, 02 Sep 2025 01:20:06 GMT  
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
$ docker pull buildpack-deps@sha256:6e7d8b364903c5a40b9b8b8a8e6b3c79cb354bc0c3a27d10744d1dd4d7614c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44870835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606c420f5df3c7445e3a99997d8c35483a5657fd8a8ed7b921e60f67f46afa2`
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
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95860c69be03c0607c5a656672f106f8fbd3a718d0939e6bec1a0f150972126f`  
		Last Modified: Mon, 01 Sep 2025 23:09:05 GMT  
		Size: 14.9 MB (14937826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c00e1eb25754567276408dc685d41565a744e4eb78ced18cbb753031afd1c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5370618b7b61b2d30abb534af39a614fb9aa30f095580d9b8eee23fe47377c3c`

```dockerfile
```

-	Layers:
	-	`sha256:7730849b05e3a0c67a9794b79216008237e2cc6a7e25170a5070ab85f2cdcf99`  
		Last Modified: Tue, 02 Sep 2025 01:20:14 GMT  
		Size: 2.6 MB (2610634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65188c55a22d930cc6904e08f72fbedbe956a584682df8b43911f24b313393ea`  
		Last Modified: Tue, 02 Sep 2025 01:20:14 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
