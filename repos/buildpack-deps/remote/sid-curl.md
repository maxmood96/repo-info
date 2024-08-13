## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:8185a6222c85c1be83714ce0dd1feb3995a914451e2d80b72384f1a7c06d6815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bb63de05706aa903c44a187423410064757ed4dd7b0fefe8ba2effc0d45f9434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73319093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3647ed5810949bbe8d894a4b2290f0a8af05479d3712f47399cac937258acdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba418b28cb46180ce179bf48a7dfa7135087eefa79b479acfa16fedb4e4a1c2`  
		Last Modified: Tue, 13 Aug 2024 00:51:48 GMT  
		Size: 20.5 MB (20482905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6b5b91dd8563b6c83f9f292f47b4f4dbe9be84f6e6132701121dc0133e988f57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68071420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b80c1c593db8ba05c984a51879cef29a28366f43e1fb6396f1eb08e2ab6422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfa97ce73cde95032209696321352612680db764c680a1b0951f78188c543fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64920297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9f5d5f12b39b29e168914b6f8c8975fdcee316b9e697f402b0b3c5137032b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b6866f17f120014e4e773fa08b076084d73c707be1c6dea2e5f47bc7eb0fbe7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73383467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077f442cd81d6b5adb5fad5659ef31d21aa5f46eeab8b1c900e908547249c10f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:28 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
# Tue, 13 Aug 2024 00:40:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42437a82bf9bbe8487117e25e8d86dc6640c415c01e295d2560ae15db12b5a94`  
		Last Modified: Tue, 13 Aug 2024 01:11:11 GMT  
		Size: 20.2 MB (20228217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cb5e40a7be972b1172bafa92ab71f6a08c143e06b0981336a4bc4d8af23400cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75244435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d80a37e21c9e25d3737094c1c4b40886ed52181492e44fdc9dfbddf970ee8f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e7fa6ef8eb669a3a49a45a66f8cc69d7f09d1b83c63555825932c55ae4e2220
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71416344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfba9f25abc92be9a113bf2def9775d340036cb7b23d08e40a068554fb1d56c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:597bffbfd546b0553a21404706d32d58cb0aff05e5d1c007c50f45820a980671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78023351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e74849ee887deb1ee055850655ecbc96c46bfe4cdabff05dbcb2e34bf9a2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:98648aba4f123076952d703ecae9417a6a3a3a75fc01c6176ea66bd96224e729
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71119009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0b075f1bb889473052aba7b3c18d5e0a28ae1a38b5b378d338f90fd329682`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1fbd779f4eb589e092c27e36df4ce7691bba7800c279e8aa9588ed295da8f17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30203e2370c0857b26cbd63c6d17b0d5cb59f4f69da9eca5b30f41fc7f5143eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
