## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:7186e74fa2a18e10762254207b4af1f0779cf54b03db8f94ac02392a0a715e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0a5777d8a12a1445c5e5e822c7b29ca21b429f959156970b567dc6cd9ef4bb24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39958548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808114ce39c2c8ac4fcf5c18bfd1cd0e8cf5902309833788c976f173eb883422`
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

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5db0458077d942d6744e9319bc57db365a93b36f1483364a288241f9a68ade1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33940311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f38f1e458dbc3104109b48488ba6c34f46b7d98c6dd010a7843b326d754d96`
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

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1f49dd9ae94ac486a8203db83c52bad708d0f165baeb56c686dbda7a25be2620
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38189936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6623beec524176ef0a47bb171506df574dc78a496c3840ab19ddbc3645668ead`
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

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:02202f4e038a37e76c6125e3bf5244104f3aa9a0d3c249f4a810f89498e13768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46468215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bff8e6ebea2a2c556cb678b10daa660b532ad3afccb2810640adf9f9c790dfd`
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

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:572f3d04e424d4ad8b57fd84ef81c99826c91e02a9283662820b5fe9d1d07921
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34119219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1113cb0f69a6e4623e1744d72a498740be45ebdde82870af09f9ee6fc8ff58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:14:32 GMT
ADD file:da9b6ecab27e35ebae8f492705795f99e0f2cc85731b5df9d5d3219de9931283 in / 
# Thu, 21 Apr 2022 23:14:34 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 00:07:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b8029d8dece6b7c2484f3de2deabcc27fb90a113378736b4dc2177c2d0f2aaf9`  
		Last Modified: Tue, 19 Apr 2022 13:15:55 GMT  
		Size: 24.2 MB (24228118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b4e672c9f8fe26957fdb418ac8a515a3cadb41d7d287e5b23ef72bd3450440`  
		Last Modified: Fri, 22 Apr 2022 00:50:34 GMT  
		Size: 6.7 MB (6746409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0c9187320e6be3859e97d2c6516161a9bdc3abacc5d6d4f071ee6f14ce535f`  
		Last Modified: Fri, 22 Apr 2022 00:50:30 GMT  
		Size: 3.1 MB (3144692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0fefd9a3f6d8215ddbbbfabcc5caf09ef516a36a0c0b92cfd7188ae4f84e5f57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38030581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c34b0ab29c98acd68a5ebd28f7db655ba5f3eec3bc0cd4c361df1e7a4263ef8`
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
