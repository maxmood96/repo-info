## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:920b01c6f16e0b4e281b97277ee192cf06d471da6242c9ab6639ba7777cd4f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ec8a6bd2a2877a009a9e59778bc626f974ef251fd5a3167b8332f6da0eeb824
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e015d485fa0e676e79f1a5c345e35f6b1016d25dde9caf17af492152184a918`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:09 GMT
ADD file:e5210ca55e6714aec9564543eeb4b4a748c57e62c0ae0c741dd0f3eb75ab72de in / 
# Tue, 17 Nov 2020 20:23:09 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:39:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:40:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:648de6ce4c8700aa65bb00de61082bc80448ba5410d2558ccd0f8c5e5616dbdf`  
		Last Modified: Tue, 17 Nov 2020 20:29:13 GMT  
		Size: 56.0 MB (55978493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a58a1358b2808071560abfa71693ca944d1732a1543c107859d521b29bd65`  
		Last Modified: Wed, 18 Nov 2020 00:52:36 GMT  
		Size: 5.1 MB (5063542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e6e253f47148f777fe41db1237b0eba7f14df71ec26f973f35c05182b4173`  
		Last Modified: Wed, 18 Nov 2020 00:52:36 GMT  
		Size: 10.6 MB (10646140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:106550b1b20cc4e0110a1b1c80799046c4ca426001b123e5c49fd15e8b190e5f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69087855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19cf9f06699812ebfb364662009b82d8d88649326436d41d70425f2b5111097`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:43 GMT
ADD file:a57353f597051225232a9e7abed847b86e4c6dddd2072732b4625acbac7128fd in / 
# Fri, 11 Dec 2020 02:07:47 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:50:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 02:50:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:af6b8b544b162386c7b3c6d5c131158e341ff3b454198faf077cc6c1427321df`  
		Last Modified: Fri, 11 Dec 2020 02:17:13 GMT  
		Size: 51.3 MB (51288429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e601c83f1a1756a052d156762b6629539a7e67063cb8852d73fb18958f7726`  
		Last Modified: Fri, 11 Dec 2020 03:08:38 GMT  
		Size: 7.5 MB (7464314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6a25346e41f4aa7fbe4f2fbf817bc776305935298bbe8403d2b5fd5ebec3a8`  
		Last Modified: Fri, 11 Dec 2020 03:08:38 GMT  
		Size: 10.3 MB (10335112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8b9e972ac8d6cab2a4cb1a2b6886d9c6422925d87fc56d9e22357f2268f5f733
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66164834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d50083c44ef17916636b824ed497f960c5988aa5b2098f3add93ba1356be76`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:26:33 GMT
ADD file:fa1941c40adf31f1de7cad83033e24d208bc560e0818d6c0977fe2e74ef87e0d in / 
# Fri, 11 Dec 2020 02:26:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:29:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:29:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:54bf394474a2aad8c49632d0f0974854752ca4ff40354a996cb0806ea65d7253`  
		Last Modified: Fri, 11 Dec 2020 02:35:33 GMT  
		Size: 49.0 MB (48987318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d959969d53555f2806838ef7825603115e52bc31662dcb17623ba77bf941b1a`  
		Last Modified: Fri, 11 Dec 2020 16:45:13 GMT  
		Size: 7.2 MB (7203302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f104a599ccc89fa932a5c9977f3f9e107d9364f7c408f3d954dd2fc7475cd05c`  
		Last Modified: Fri, 11 Dec 2020 16:45:14 GMT  
		Size: 10.0 MB (9974214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e8c2cce2bfde8d72637411595755e7b3dfe68f91987ee7d77d62310b1d186e44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70639559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a53f795f74fe7ce980405b63e09e411b3d9002a68386a28ba184c1713059c1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:46:54 GMT
ADD file:f2ae922bdd400314a7bdccb54b19fed4d2441eabfa76c14f4656754f4639c9f2 in / 
# Fri, 11 Dec 2020 02:46:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:56:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 18:56:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:56da081f64fe82857d727ffa4501fbe0725d416c8b8062202081a62f97fd37f6`  
		Last Modified: Fri, 11 Dec 2020 02:54:16 GMT  
		Size: 52.2 MB (52214368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ea5ffc1beeb347c710279a3ac88b6b0e4edebb2feaf5c372e9118d8bf5c0b`  
		Last Modified: Fri, 11 Dec 2020 19:09:03 GMT  
		Size: 7.8 MB (7771425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fa408149a9595cea659967e65fc21816e34d52435f6850a7cbd24c27554905`  
		Last Modified: Fri, 11 Dec 2020 19:09:03 GMT  
		Size: 10.7 MB (10653766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8c9f792df88c924d883281936dd7ae7e4a3b7328537eca3b8080bc4d044f1fd6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73308219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88329186fa891b9f9fa60ba923532e1c54ad8595d6bbf2a6986435c553ed2f82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:59 GMT
ADD file:6d6afa8490ae5ac639c8369b0f5d9f8e49c675672ebd5348a955a3c9656453f5 in / 
# Tue, 17 Nov 2020 20:22:00 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:17:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be81561500ea27b67d364b1567d73e6fbfac19e1739e5b1e5674dbea758abedd`  
		Last Modified: Tue, 17 Nov 2020 20:28:52 GMT  
		Size: 57.1 MB (57102236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc436cb880e1d23236f4f748fe380b16b0e16955049a2c0c1ab65456f67c2a49`  
		Last Modified: Tue, 17 Nov 2020 21:26:18 GMT  
		Size: 5.2 MB (5183137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca3e53afca84ddbe3333e0b6c779a68bb454199b167cfb74eda23f74fbea675`  
		Last Modified: Tue, 17 Nov 2020 21:26:19 GMT  
		Size: 11.0 MB (11022846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b20c27c4b5d424f699dafdb40897c11674231c2f4c406ef97135b52e30ae4514
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70157304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736fd42e2728894d1a8f81e87838dddf049f5998fb4060065c628322bd8e256c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:55 GMT
ADD file:144f263fbf8197586830814ff675d3c7d3ac8e3df7debe6633a1e91f84ff845b in / 
# Fri, 11 Dec 2020 02:03:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:54:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 02:55:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9b60fb1f705939e8d3e124cd99cb825ac48613619a7a75de5656f0bde8bb1f05`  
		Last Modified: Fri, 11 Dec 2020 02:11:04 GMT  
		Size: 52.1 MB (52069726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc2b81267c2dccbb94aa4a39fbd561e967b04505581d2d37c94c116454be253`  
		Last Modified: Fri, 11 Dec 2020 03:05:44 GMT  
		Size: 7.4 MB (7430898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d8b7d4e3509bc9ab5283dda924581973c2fe390d34bf794abb077b094d9c66`  
		Last Modified: Fri, 11 Dec 2020 03:05:44 GMT  
		Size: 10.7 MB (10656680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:62092e9b95736875c9bb5a3f6e1faba71a7e13222afc69048b49d09967a8f68a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77098891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c216dd799f70798cdbaf81e4ee75e36f6db03f57e60d10a39750f1aef844f7c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:34 GMT
ADD file:d6769e024c4c1bf3ac50de798e3b70ddbae5e8dc6c4edc64cbf31ef39fba2896 in / 
# Fri, 11 Dec 2020 03:34:40 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:37:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:38:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:897184b44dea4f1c1b646278a369b1024dac0562097178b81b92da84665fd760`  
		Last Modified: Fri, 11 Dec 2020 03:42:05 GMT  
		Size: 57.3 MB (57314487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee2620ff3e328f5bc3688195568d3b5b1cef135eedf50ed4cfc28b1a10e1f5`  
		Last Modified: Fri, 11 Dec 2020 19:54:04 GMT  
		Size: 8.4 MB (8363461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c218c75d39db360d7134c468b34f1237b347888e09366545db43481f8e2a50`  
		Last Modified: Fri, 11 Dec 2020 19:54:04 GMT  
		Size: 11.4 MB (11420943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:28062642fe805ca40945b789b2627545fb1c2768846a10734c29f290b520066f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70005469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c64383f15a9734f25674f81029d565cb597833a756e1cc55aea5f240a75f30e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:29 GMT
ADD file:81f25bd988cd2db6809416e7139b279a1a04ce8e2b864c71e35768d7211232db in / 
# Fri, 11 Dec 2020 02:12:36 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:07:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:07:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d882124dbf8a54501109f018ee08c93cb805beed092d3bf2e6979740fad5f861`  
		Last Modified: Fri, 11 Dec 2020 02:17:27 GMT  
		Size: 51.9 MB (51894888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf6b2001d1a8b91d37dd19d21d1f31ce0dfcc83648225746fdc024ebfa8f686`  
		Last Modified: Fri, 11 Dec 2020 16:16:50 GMT  
		Size: 7.6 MB (7585246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c42824152b87e26d9c06509c0a9035c25ec1a1740793c472931585f433c904`  
		Last Modified: Fri, 11 Dec 2020 16:16:50 GMT  
		Size: 10.5 MB (10525335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
