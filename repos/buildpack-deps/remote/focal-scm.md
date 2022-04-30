## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:ccbaf75657a96b6a6cece8706d69c795801c1811de831028ecde678d63d01674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bf0a5c9b7ea9d606441a5d54858ea2037022c777c2c10cf5c8abc341e79078ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100687935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9c4684e8a222735ef8b723f01229322f32b3318f6cb27d132811f7b9accc1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:47:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:47:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b802a9f71706fa309700ea1fd5d986b885729b323ffdb716d290a98e6dfe0706`  
		Last Modified: Sat, 30 Apr 2022 00:01:21 GMT  
		Size: 7.8 MB (7768179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da477514e5fd4aae7503079d6eec1a60d6210d0717abfae57581636ebf69b690`  
		Last Modified: Sat, 30 Apr 2022 00:01:20 GMT  
		Size: 3.6 MB (3624139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f807692b16fa0ebcd5870262328798a2fbe3e75987d50f1794e1fbdcaa34c2`  
		Last Modified: Sat, 30 Apr 2022 00:01:40 GMT  
		Size: 60.7 MB (60729387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f0a40882a2e7fda131cf855b58f17748c4c2209b29b833c44a9fae9c4496b9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89387301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e939222556781f115fa3e71a72021581a12faa85c1d9deb4cd9faf135d8466`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:27:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1563a0a8b5e832769a2de291e460a7fcacd9bee37ad7a2d8a73b14a0f0ddfc`  
		Last Modified: Fri, 29 Apr 2022 23:46:30 GMT  
		Size: 6.8 MB (6762469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493cef317c1c6766357569ceb016cc5074fdef707c8caf5a67a543cd3f49f167`  
		Last Modified: Fri, 29 Apr 2022 23:46:27 GMT  
		Size: 3.1 MB (3104192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaaed45380a5a8e10619db9bee81a02afc8c18a5b05750eb6b438db9b180461`  
		Last Modified: Fri, 29 Apr 2022 23:47:21 GMT  
		Size: 55.4 MB (55446990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee95a180abdfe1c01ba91cb2cb617cbc2b498f56c45d71e9cb45f05c278480bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98964496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e2d891bb1ef1b7a5198201e9b0407cf08a37c74698cb0fdd825961879adb96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:16:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:16:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:16:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7feebf8b53c2ab8397b63406bbd6ed34bc670367c3fa74c734bf99c6a2e8ec4`  
		Last Modified: Fri, 29 Apr 2022 23:24:40 GMT  
		Size: 7.6 MB (7634266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8adbae9f42bff04c79875d37944fa1587613ef0de5f7bca85a0b429d4e8d83b`  
		Last Modified: Fri, 29 Apr 2022 23:24:39 GMT  
		Size: 3.4 MB (3386282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b7412064586b1ab2a3ac7b334961d6862b1ce933411b8fd3b75cda3f82b02b`  
		Last Modified: Fri, 29 Apr 2022 23:25:01 GMT  
		Size: 60.8 MB (60774560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4c6d4a4771246bb9715200985c9b0de126573ae0522bae5c82bf25e964ba510
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115887384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a471680dedc8c35122838f4920c858d2551eac6f1c84438f0b7ca6aca0889270`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Apr 2022 08:08:14 GMT
ADD file:f1c44e93e7a6c0fb06800e11460dc680e252dff4a20297ab2eed86e559398616 in / 
# Fri, 22 Apr 2022 08:08:17 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 09:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:16:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Apr 2022 09:19:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30c729c4ac9a0cf192e6c3e5618b0e930ca2ecdd73c01d9c5fed5b0707eb8836`  
		Last Modified: Tue, 19 Apr 2022 13:15:19 GMT  
		Size: 33.3 MB (33290375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201e69fef602ecd9c604dbc526e412a7f9f53da3d9073dcf9b13e90174bdc39e`  
		Last Modified: Fri, 22 Apr 2022 09:41:50 GMT  
		Size: 8.7 MB (8721811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2269d321fbb9bc5909b0f64e4bd17d6910613bd979b25648123ea6ada12e8fcc`  
		Last Modified: Fri, 22 Apr 2022 09:41:49 GMT  
		Size: 4.5 MB (4456029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16173b57d4ef7ed2d38f9b4db91f53dc363095ca8362df80de0e936beefe33e`  
		Last Modified: Fri, 22 Apr 2022 09:42:17 GMT  
		Size: 69.4 MB (69419169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:779dcdb5ce1162017b00ade6d7ce8c8a97e5708fa248b3f551404b96c93ea86a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98041364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381a7ca102f71ebdc9111ca844dfaf2ae1337aeeb0260fe45c9370be60034e7c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:50:05 GMT
ADD file:fdc1835c7f7eae641bd78a4c938c3d94746b95a0c151498d332a2b9878fd99d8 in / 
# Fri, 29 Apr 2022 22:50:07 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:11:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e0f1090807e81093e3637ffe3d350f58816de907201055908c3506a30c68993`  
		Last Modified: Fri, 29 Apr 2022 22:52:01 GMT  
		Size: 27.1 MB (27065417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad05d33c3457ff71f921fd9c69734064bb89a93c55c748e7c2b83b0aa4b6237`  
		Last Modified: Fri, 29 Apr 2022 23:19:20 GMT  
		Size: 7.4 MB (7422981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa203495428900214c5ff3ea85c5b6134947347f9c1dfda07e1576ab83bf1f9`  
		Last Modified: Fri, 29 Apr 2022 23:19:19 GMT  
		Size: 3.5 MB (3542183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f815ebe8abf75b277a16ac4bc87b6aa8e7db92f1993dbbe8240dcc3d1359c14c`  
		Last Modified: Fri, 29 Apr 2022 23:19:36 GMT  
		Size: 60.0 MB (60010783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
