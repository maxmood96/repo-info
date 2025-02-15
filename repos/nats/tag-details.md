<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.25`](#nats21025)
-	[`nats:2.10.25-alpine`](#nats21025-alpine)
-	[`nats:2.10.25-alpine3.21`](#nats21025-alpine321)
-	[`nats:2.10.25-linux`](#nats21025-linux)
-	[`nats:2.10.25-nanoserver`](#nats21025-nanoserver)
-	[`nats:2.10.25-nanoserver-1809`](#nats21025-nanoserver-1809)
-	[`nats:2.10.25-scratch`](#nats21025-scratch)
-	[`nats:2.10.25-windowsservercore`](#nats21025-windowsservercore)
-	[`nats:2.10.25-windowsservercore-1809`](#nats21025-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:d3a72168a1fa10ffbe471c2cb4da9485168999964053bf9986d7412477b7e90a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6893; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:d3a72168a1fa10ffbe471c2cb4da9485168999964053bf9986d7412477b7e90a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25`

```console
$ docker pull nats@sha256:d3a72168a1fa10ffbe471c2cb4da9485168999964053bf9986d7412477b7e90a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.25` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25-alpine`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-alpine3.21`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.25-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-linux`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-nanoserver`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.25-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25-nanoserver-1809`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.25-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25-scratch`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-windowsservercore`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.25-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.25-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:3290c829aa05ddd4da12026783ccaff86f3fbc1f0551722908a934c293cd6228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:5f8d6d2f979bdff121151905e04a5e0f7f7beed36fdd94834062cb8bae8731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a760043f694ef7c4db6e6efd98e7cc58747c08427738ed2d1c65e6558d96d5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d217efc4746e011b0991df0e20dde8755ab5267919fc585047fcfea1ca7ee`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 6.4 MB (6371492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ecde6577c288c4e1c77a963452e0ca7913b21c1bd739a2142e6cd2c3b356b`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc88d1dce159dbac9bddaa3826c84e4fb0c396b7fcb645341a94863a1ecf963`  
		Last Modified: Fri, 14 Feb 2025 20:34:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d3295aac35301147ef502c97340d4b7a730cbaacc5e3dcb7781a3ac034578ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6c89a74047251fa610c0207c6fa3c9ce64cd05f098a53117d039991587b23`

```dockerfile
```

-	Layers:
	-	`sha256:4ec7f92ff4b4bea5e29b99e4fe621322a0b8b29bec0b98e515689a9312ed4b04`  
		Last Modified: Fri, 14 Feb 2025 21:56:29 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:0a2ed950c2b26eb823e4a3351bcb24f29e332fadc65a0432679c35d53b24cd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9383395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178bde6de1d19451ec3f5fc4e7891afb21ecd72bafcac9d6d5efa1ef92bdd9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3745c52280c88324b71036fdb9dc2512a3b82a2a984e5c8f78d81cf4145b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:42 GMT  
		Size: 6.0 MB (6017694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315e139f7f1acdee2c16389dec4babfb18da6342f00ef5d0f96bdd3d83475fc`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2160c882f3bd40f5a3f1964e4734a24097b07aadc847b3ae099777b0d6c3c4b4`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e3ff6fb37d5ed2bce971651341ec1b30346993c3eaa240f222fbc0caac94d1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c788ce970e9e1023313860e6716805102f3ebe6fa512db330ea84007acc6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ae273c5e5d4ea9a86d2f298a7bb0c04959dbc3eb643c210139a124b1a6c5f`  
		Last Modified: Fri, 14 Feb 2025 21:56:30 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ef0c29e3adeb3ce1ecfa2caee5086c7c92a9bbbc74c42e9f34d7b03cd4605da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9105254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbec0d3f30febecc59d36d16fc48a0bc073e7ad02416f2bf09cd3787a7f1bb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ade6386145a823a9f231000d97a0bd85fd86c11cf2e5c1d8a6d2a0996ed05`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 6.0 MB (6006162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d399fae77e3122b1c44caca3a01c7b33dcdd3378bb78cefceafe45713a233`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf61a6e8f0cdb4aef6893e9f24930f68d42d59202dedbbecc6fc8093ac28795`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:010de8f076cf13c0d37ccdfeee7df51d79966f2118ad13d8c12928995c849441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086bd850c620e84c4bbdc4c4b8ff96fab9b1853f8ddc9c64edbb233b6d2419e`

```dockerfile
```

-	Layers:
	-	`sha256:9b9eff98d0ece46661517ef6a2d8ce8bbae44774f1d747f95072d65180f5073a`  
		Last Modified: Fri, 14 Feb 2025 21:56:31 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f683cea797981a0f9f6e85e63e5fecaf97e7572ee9070bf470ec4d1cab6e800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61f044d440b75bc651a1e9167509d9362dc6ad06fead74aab7a1b55492a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b4f88eae3b82f37fe13a2f0f3671153134eda05ccfb5b46ae430aa67d2019`  
		Last Modified: Sat, 15 Feb 2025 00:56:31 GMT  
		Size: 5.9 MB (5918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505e69db1de977e2536fdc29d59eda14285b1cc9130501a0d733164ff20bf04`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bd1811de28a84508643aefd22d85597e16a681dfe6f08293720e650b1a5192`  
		Last Modified: Sat, 15 Feb 2025 00:56:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1f5a66e85a07e9e2210e749a679df48a7d1e1376e3f752069a80da5757f3899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938aaf23349820ce3b5ddf1cdf486fc9ad4cf05b435e1852d9c2c9db379257ea`

```dockerfile
```

-	Layers:
	-	`sha256:c918722b3c31e97cea950ccfc17abe233cd2942e3772b080ec5d4fa9bb132373`  
		Last Modified: Sat, 15 Feb 2025 00:56:23 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:578b8adca72ca74ec51fb15debee242820c5e810a004a74f3610dfe7d5fa6075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389c685a2d7238ffc4ae87a3e119695a3f942c48e14d5ab938d5f9098b1b75e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a87e9239fb2f80297f1de7ca000c51c50fdc3d5a369eca9444e6e37455363`  
		Last Modified: Fri, 14 Feb 2025 21:56:41 GMT  
		Size: 5.9 MB (5886325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234b5bf895c51b967e9ccc91e978e12de3601714e77c546dd43f64adaa16a41`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5b7f82c558746c48374f8dd2fff53fbe296a0c244d798b3cd64201faf123b`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c5db3fbaf29c83ead152be1c9a791fcc89db1032052654db57d2f4aa979e9915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e69dbd32d188076aae7d19930d02dd56b5b1bc7b5e6f0edb2a2d0de3048b4c`

```dockerfile
```

-	Layers:
	-	`sha256:cba5595a0a1983029f905bc5acd221eb96d1b9366d8959f2022121593ba1b57f`  
		Last Modified: Fri, 14 Feb 2025 21:56:33 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:9ad7801a21e5859fedc02955d79bf2947b9c9121fb44d25875222d291cddb273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ce953e969e37a26ce42b855ae41547b78b32d6edb1120ea5d57255a74b4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab1c68eace76b6e98e3fae9679e8ac0e95e66a4e111ebce011d6ab938cf59a`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 6.2 MB (6215519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feeb0db4654b15450733f1d1c0dc66ad879299684c899dfe6908b7822aed03`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1968d35d08a72f5bc2af5e17caaf064b211f63d2fb55af3f9bcabbf9bea3aa74`  
		Last Modified: Fri, 14 Feb 2025 21:56:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bca33495da00298c750953bbdcc38e6f4a8000ae22767efbec74f73a5011c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b931343eaee4416fd7c5f6bfde62ea22360680f96df8fc857b6deb2e8fa7f8b`

```dockerfile
```

-	Layers:
	-	`sha256:168e0635a26084d0e182cb1235aa7d9f9db6f6d0f5508969995fa42e2a23b1b7`  
		Last Modified: Fri, 14 Feb 2025 21:56:34 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:d3a72168a1fa10ffbe471c2cb4da9485168999964053bf9986d7412477b7e90a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6893; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:bc0de37758065df1fdee1d3eb9b083525094efda302ac2b97beedd8b0e4277d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:09b474519b02def21c913f3a3d593e0abe2ab316a543289a069840061c7f8d41
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112952027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edf9e0600c446bc3c0a2a074319fb9a6e73ade269fdbef0cf1a7752c64a3895`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 01:14:16 GMT
RUN cmd /S /C #(nop) COPY file:acc152dfee9c5ddc38d24e3c08e54d57b0488af147b7d3bca35c3b0e9cd44184 in C:\nats-server.exe 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 01:14:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 01:14:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b4be985892cbff5859ec15f83fe1e9f9ed395059ed0e19fac5d71580b8ea28`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66cafcad785d7bacc02b7f1a5b4bd5680265969297b75f9c944d55c5bf132f`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 6.0 MB (6030535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec61010dcd23b9212494167cc57412d179fb3808ad619346ff806e8b1122c4b`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6a84b10a4fe9377faf5481f4a4e454e66ee769b9cd93f52d8d41216ccb931`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a33e1efb27f4723e99b6ddba1c07b8f673336f30f347cd7055bcb20e6bb8f8`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f94af37d86ac27dd25a6e4901ef0e0960adcbc3bf6bc840fd5a8bc84a6dad6`  
		Last Modified: Thu, 13 Feb 2025 03:56:28 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:d6f564e72745081b571cdaab80be15e74f393a1887c5b0d28fe1960a3df6abc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:a3cce34063e2171e52961998710abcb68c0af5ce582b4bd261a0e73d991b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adf374ee8949cadaebd08ad86e992523bcb3b988aaeabd23a0f982b42962ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b0ab7b6cbd4f04e3ccfc7e43007f7265c99112ffd21d84d3216eb8066171328c`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.9 MB (5908232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809716529f1b9d64de6f836666c6a4c543cf6e9c48fc283a26ee651aecdb4999`  
		Last Modified: Sat, 15 Feb 2025 00:56:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0633f77705ca0fb4f0c1f0a9365c42b39cd14dc9cbdfce33ffc4c73770652dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dbb8da0c17d4a24f1468741734648fa7e4b817d6f57c94c74a950e25f80f1c`

```dockerfile
```

-	Layers:
	-	`sha256:983b8962d9613c7d12384470fec9ffc9324734f010ef39b6edb64a855226f206`  
		Last Modified: Sat, 15 Feb 2025 00:56:17 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d02ecc3d9f175cd663ebe56beaa81563c2f4b17ceca9eacc47da54a759f72003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c41d72fc64992f463e9bcbdc18b1e6016565a09294191178d5361d15423002`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c739286a1eb26d88eea2bfa99a29b1319b70d05868d157fe40c186fb43158e5`  
		Last Modified: Fri, 24 Jan 2025 01:11:44 GMT  
		Size: 5.6 MB (5558034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30213df472a6d1651b099b6ac4bbe52e7077cea67d18d4d7c2bb08a7a87e8d46`  
		Last Modified: Sat, 15 Feb 2025 12:56:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63a30b41513d0ffe368c0cecdada6ed8ac731b48d555658b13fa758e0efbf604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840705569f07a7624d1080c5092dbc825b94138a91f790c69f8d758c13cb9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8417b632d94321a331fbd411b9a5db838bcb6e36e7b636f177a39d2b372e8ea4`  
		Last Modified: Sat, 15 Feb 2025 12:56:20 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2eef5a5a69b9d11132b4f618d0301b7be54239668d8d7d11acb055ebb205d620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e221e82b38d8852595238ed02caa11f11a6288a70bf51ad4a3edec46261ed5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1399c48aa9c68af4b7de581a13cf0ec1bfbe3133690d03f24371574694d40756`  
		Last Modified: Fri, 24 Jan 2025 01:11:46 GMT  
		Size: 5.5 MB (5545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623db20142a39364ba54388cbfe054300fd0a054a2ad53acb7f1fcda4049931`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9a2f7b38c65c4451719cb061c71692620d774822fad9ce5ee46514f4a4968f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6bae034b4adb172eefd81cb5d5c6921c693e3ce540ba45a1594c8b5ca3f925`

```dockerfile
```

-	Layers:
	-	`sha256:560229b2044e8d01560c6e3c794ac60c66ea653e4f7919d7c7368cd9543cabba`  
		Last Modified: Sat, 15 Feb 2025 12:56:21 GMT  
		Size: 10.6 KB (10599 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1c7f4a1c1c6caddf58ea4c89d1c8c9bc075bbdf63f6011c7cd42ccd6185045e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4a47131f671d2c5fc5e57c059670211cf9dde5d5c327bbc5c516142dc468e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e0a114dd0250b8bf3ba799553b9c1ed6689c907a86d69dc80c2b7c19554f649b`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.5 MB (5458189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc68d42fb8601cb72488a81d57700151f3bae686e833c5106a07c080f1ade74`  
		Last Modified: Sat, 15 Feb 2025 07:11:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63bb1cc1894c0ad8dc0bbdd96272f7e798a855ee3733207975074adf55d7dada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f649b31d0ccfa0086593054e466e7174ae3ad77d92d06f60c75a82becde23`

```dockerfile
```

-	Layers:
	-	`sha256:18f02fc10796c4cc3d156d91fe40a365ea42d9aa81a38f86b0f02190fb413646`  
		Last Modified: Sat, 15 Feb 2025 09:56:22 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:434c658bc44b8b9dcab77f74cfad202c200736a8461f5d265dae43c873adc9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f3ad6ea74c5856e162d25336c70f7a796ec1c80f6eac76353e29aedd0a276`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f24eed68b496d8539fa581425e2e13b88b0c51d26fd4d01b05df701440639f`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 5.4 MB (5422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570ebf2846c1ac3745f0511a216eace0026742ba8ec4daecfc127a0f9662cfc`  
		Last Modified: Sat, 15 Feb 2025 02:30:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:da5b993e04aafc807cd0165c760b94933d34353a2feb454220ac1ca4a44037d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7834ebdcd9c91d3d31870e814669c44adce88e5d6204859c0816a6577673b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:224a4e70cf72f1667da6acadc14554fbf2d958040a351cf7ca1ece7ef8a414d8`  
		Last Modified: Sat, 15 Feb 2025 03:56:22 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:37386852d3f20ef2d3ccb475743f4915e97abdf3a5e3b5a848083cd9b9d18f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb7e65a9c8933a261d86a8957ee8de1ea23651a7c806c68cf295185ff05a6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 23 Jan 2025 18:55:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 23 Jan 2025 18:55:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:89e691e76569a64cd402c4b21acd57d1e4a79c42c6a04faaa925902a0c35cf6b`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 5.8 MB (5751534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6983789c33249592d22ec49cce78643a60a9153a988ffc49c73fab37783267`  
		Last Modified: Sat, 15 Feb 2025 09:56:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4ef7072a3ed44acc75c05593e32daf8d314822bda4881bed0aaef92888aa4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f03a644c0f69fb3e2dc3d9b1c161b4be3da47af51209e9bf16341a8a9e7352`

```dockerfile
```

-	Layers:
	-	`sha256:eacff774eda8fd5ff79e7e5d9bfea7949ded2271906eb7c63585e4be8d4c2dd1`  
		Last Modified: Sat, 15 Feb 2025 09:56:24 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:90f6a9c218e54fca8ddb8f5ef49c6f6ebebb7d89b03b8c5a782e1b66ef645041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:39cb1968945038e1a49d2050366ab438dc18b480e87b5e44619232a9a091d74a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143618063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e340f3813e5c62bb1e880a8b92500255ed31b661ff6b11d0b1af0896b9a598ca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:30:43 GMT
ENV NATS_DOCKERIZED=1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV NATS_SERVER=2.10.25
# Thu, 13 Feb 2025 00:30:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 13 Feb 2025 00:30:46 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 13 Feb 2025 00:31:05 GMT
RUN Set-PSDebug -Trace 2
# Thu, 13 Feb 2025 00:31:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 13 Feb 2025 00:31:22 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 13 Feb 2025 00:31:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Feb 2025 00:31:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Feb 2025 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6bf8fa2712d05ebc326aab9183f1d96892ad97f7899cac56ffc2167dd7dd6`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94310c02275f95397d489002b6985a9c5f753a130c8cf91f17c92aab6c63eb8`  
		Last Modified: Thu, 13 Feb 2025 01:08:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbe9da0a2b25582259cac86013896d1e60d2fdd77b464761a1b13c9b8dee41`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d84ab9a7cce9d71959a0b1ec3046af767c37fa3a03d4cf12c29069ecd1bd93`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6de08f536a814f14692a28bcb492e5c871eb2b54808cd729f95d81f106c6ee`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1affead666dad44febd2844d6a314c236311ade14424d414ea854abfd093cfd`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 330.0 KB (329975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde71a66804b443be4d558b5a4f9b6293313bb94ada1231016939e3aa798f9b2`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 6.4 MB (6367013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c58e512d44c301353256688edcebda6a361be0c1f85d839c93e158f7c461ae7`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cedfacb86bd6297cf6883668655328e219bb4f07447398deaedcc979a70c01`  
		Last Modified: Thu, 13 Feb 2025 01:08:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd56707341ec29eea3c040fd3725f0c12f05232521926f774f7c3d4984b746e`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a6f2dd1d597249ee9e821ff329437a94cd5fdf27f241db76281d489d0ff46c`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
