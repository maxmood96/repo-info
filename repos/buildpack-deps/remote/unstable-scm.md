## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:78433f84f9d7d2abdcd3ccb447ce28735514b587ee7f25f1e01352a811c8a0ed
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb28905646673ebf2a4ecfe0e0ce64623a21e39d26fd6dc948724067fd4b7d88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125443500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ec22e747b171d4071bb66d9fef2ff80beb9449dd7f8dda1408c04b1cd1e164`
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
# Wed, 18 Nov 2020 00:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:ae65daff77b5d6ac0619bc955c2b1edd6ad35d46f9ad26b02f3de5bcd0951da7`  
		Last Modified: Wed, 18 Nov 2020 00:52:58 GMT  
		Size: 53.8 MB (53755325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6e5eadd5c7db88dda67c9a8ce6b156508d1e1cba1c7513d27646d96566a75112
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120620088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd0f445fb8cbc98f9ca4f68d1bdaf683b4bea933bfaf6811589ac25baa8de1c`
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
# Fri, 11 Dec 2020 02:51:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:52e79e0e8b81251e6ee4cee77ecbab7ff5bb7a5ab9d1f135cf518b6b99ca6886`  
		Last Modified: Fri, 11 Dec 2020 03:09:05 GMT  
		Size: 51.5 MB (51532233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f7e2deec2a55bb9f43eaa0ea3114e52e04d8bbe8637ea302c164c0e549c63cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115753860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b422d39ee20a117c62b727b95393ddcd0c0b955d4922857e4670eb16e44cfe`
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
# Fri, 11 Dec 2020 16:30:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1bc95b5f2d19ce2f5db34e78db2ba59c101fa341c37c56cee3b9c474bbd05b03`  
		Last Modified: Fri, 11 Dec 2020 16:45:39 GMT  
		Size: 49.6 MB (49589026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7946fc1dcd75182347233bd75a4a4cfef58b67920fb455580be6f8faa551647d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124611009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581def6d05f356597aae0742ee29ec92f6925ae27392f3635265fb5128b853de`
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
# Fri, 11 Dec 2020 18:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:545a3bdfa310b636354f945709a533dc9ceed30a5245b06d29e16d8413b2592c`  
		Last Modified: Fri, 11 Dec 2020 19:09:24 GMT  
		Size: 54.0 MB (53971450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f74a7cd774a9079bdc7a45e46092cf8ded582cc8c1b487dc516f2ff982cf931e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128376510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4526af7986e498c2f897a3baad7d300fa1e59fafcbc6d67e9d3015df16d0060`
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
# Tue, 17 Nov 2020 21:17:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c97dd1237dfa1a40c9c2255e2dcdec27f7d739925bf6b97716b25759ca483baf`  
		Last Modified: Tue, 17 Nov 2020 21:26:43 GMT  
		Size: 55.1 MB (55068291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:829b39ceb3ed0fc4878baa5bad951f4306cadf036e2598c708e92f2b38d402ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122740725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4a1b6d89f58e801de4a83605ea1ef904d19ff6a49d2ca7467a49ac8b592ee1`
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
# Fri, 11 Dec 2020 02:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8630910440ff90347edf0df6f5aa5bbd3ea4e62bc74dcb04c8d9258f587cea26`  
		Last Modified: Fri, 11 Dec 2020 03:06:35 GMT  
		Size: 52.6 MB (52583421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e167489faf43c037aa7476938619dee1b4cd51328e9fd597b82a6bbf8cc9e130
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135220136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5acec05ccd4960593c45bce2317345ce347c49f3cb00f892a55bcee875ed4b3`
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
# Fri, 11 Dec 2020 19:40:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:77815484de78d295d1bb6bed7b78f53e7d6209bae716c033ec4b4c0b13f08572`  
		Last Modified: Fri, 11 Dec 2020 19:54:28 GMT  
		Size: 58.1 MB (58121245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aa319c4e0f2b9fac0a0e916ba8d4ec4433287e904cadffa143c6a2ac5d36d6b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123330404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec19588ca067f2b410ef911a44cb2093bc2464d301cf85f5d0003848b666f31`
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
# Fri, 11 Dec 2020 16:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:aeaadbfa1d0a0ab4d448f235e351c619f71777466221df7ff844225f0a1e6221`  
		Last Modified: Fri, 11 Dec 2020 16:17:11 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
