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
$ docker pull nats@sha256:a1105b489f2a690feb0d294bfa67aaebed02cd9af841a80f474808576353c8ff
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:a1105b489f2a690feb0d294bfa67aaebed02cd9af841a80f474808576353c8ff
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:a1105b489f2a690feb0d294bfa67aaebed02cd9af841a80f474808576353c8ff
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-alpine3.21`

```console
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-linux`

```console
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-linux` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-scratch` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:05c73c15c6f4aab8681718fe8f0df25fe00b74a87a4454a4dfa6e3dc90d5865a
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
$ docker pull nats@sha256:ef817b50edbd406aa51ac0beca95db0fd67ba652b6e2776a5fd2ca9889382395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10014320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247867c39cf14d077df2de9e57377b735ffd2f6d95d04d01744e9852e1e22608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dbc6e510af38547e91ea1c2c762a067d97b0b1aba2af1df5f8de3a9f39011`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.4 MB (6371631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fb37a3623725ee46ed461083a875a98716dbdb318b405784a99804b67bbfc3`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b3de2a352044c02839307cd0f02992ebecd88f4be570c77dc79a24b7a6292`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4880c7aee8bba2d66bd3cd1ea3af69870013d5580c720ca9e9a687abe00e21e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83aa0a1a2697d095ce2f502aa02838753149c2579ff98f59a283abdc50a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bdcaf755448d27490e2d8c2711918063648097d5ab2c6bca1f46a47d5a53d91`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Fri, 24 Jan 2025 07:57:45 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:9885bb99da1d2bb8a40bf954ced7d56298d82d9f3c4916d9360a63d12d37ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd192d718f75171ab197d259f2c17363d3a6ba4f46ed11382a70ef7426d06bf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcd578e6676cb22c80beadb90bc8a97d628da38aa5bc54c6f8f93ca26b7617`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 6.0 MB (6006282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b579ee6d7ed4a4602e26cb577c7a02f771e5733301a4a85cc9f073a4c3a03`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a37700fe50339e10cfb9f1bae1593d95cde6b8cf9c9a311907338bc4c829e`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6c0efd5d9d8b7bf501fd7a51659bc7636f66f16d656f8d486867c30a80c93562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d218772a1b11c8004b1e6ed3f84e5d2b7b2c0478fad69f039b58ca6584f0bb38`

```dockerfile
```

-	Layers:
	-	`sha256:f29e5d05ad2517ccff0b59b4bb385c9963f6fbfb045ab99e87d9437f8a794bda`  
		Last Modified: Fri, 24 Jan 2025 07:57:46 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Fri, 24 Jan 2025 07:57:48 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Fri, 24 Jan 2025 07:57:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Fri, 24 Jan 2025 07:57:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:ab2f63de17f9963942bb14b0cd80f430b6b330fa4e892640baf429c618d4cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9683479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c45d9c1c62d1424327d4ea8d813726cadc6ed787e21aba538b78842710b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3955bf84c648916e8cf5ffdf43a0c0bc1fb6e94a41b8fd9f4cc6b8f6949d6f`  
		Last Modified: Fri, 24 Jan 2025 07:57:51 GMT  
		Size: 6.2 MB (6215645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03050424f606d788d51ad17e145c0191a9f2407d0188566b6e10cdaafcd1aa41`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920fd412ae27c5d584537d532f92369fa42edf461c11d8975a387925f225b06`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ee282fda68491fbec776c5e47dd29e9e3a490974a7c63322bae0d1d995ee9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b795cf804e6753b3cbbf4fbc72a7c610de978ea4a8083ba336be120ec3b29`

```dockerfile
```

-	Layers:
	-	`sha256:7c4c5cfc79cdd77f59ca916c8e22d4ab38c53345255cd46581e17009971da518`  
		Last Modified: Fri, 24 Jan 2025 07:57:50 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:a1105b489f2a690feb0d294bfa67aaebed02cd9af841a80f474808576353c8ff
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
$ docker pull nats@sha256:f27a0d9b38f09cb238a86208f3198792e5d9be652f03a5627749356ec0540a7d
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
$ docker pull nats@sha256:058993cd566f797471b784ff9d99edb6ca80266cddc0793a4c038b5ba8253bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33d245f03832da2e962897c2672923fa7e30e6b67732edc9425679c26c8668`
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
	-	`sha256:c4517354fa95edb858e5bfcbbdd9ca7bd2b67347236a01e12f3636bfa40f92e2`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c120f77fbe5ae80e5924880d91c1f03bb9949e80583670ff845c07b747936be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544a9a50d0e74ea1de30eb4869abd06d44e01d4782cd9ef09550c8382743eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ce6ae35819d0fc195e86fde939966eb5e6a81e8aa5725563b65ca9390ee16207`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:907407420d3e9ba94671a7c000937b1a0dcdf18331a8b99a7d7e19e88895b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab1619fc65e8146b5b114ff9d595ae238d0721250f1f51ddc72f514786a5bff`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0bb608d112d13f92d2126b84d0251ea63930d03a10fb27c45d05d31c57f780c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89066d5d3d9e338d818e7c2aa03b09333e6e431746e67d73ef1b2c746b6ae358`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb13e94c06463c9a1e7db8944b4ef2f51270e9a9f9ef3aa05684d9445c562a`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488b90f04339fca9728f4951e9ad8ba55f8f900cb8c4751756637e7d8bd2d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0b2fa9c3ab6ac63944db04254bd5e5d17ad1ebe0638fc63fad21e9865853fa`
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
	-	`sha256:481dcd244ab71a71ee9b9fe26c2964654abe92238c9f0d884ee0c699ccf59640`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7c9614a8f08c2147e7188ea2ff5b0c52f28ffd502158643855b52f42223a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce5f946a7951df51bf1a314c263faf9026b15a2082e73c4def270135f6bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:07711e5ebb4f91ff8c9c5ed71d8487590a3c5789740123f154f8cb6617e4df17`  
		Last Modified: Fri, 24 Jan 2025 01:11:45 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:63bdc87cb63f584a3a60786100ae1195bcd67c9c6e8c9a8aa10de82ae5ab7e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e445c826e9720a9666773ed4e3ac2406f8b4d0eeaa0af2d7059b8e37597ee1`
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
	-	`sha256:d97295afa42b2558422039cb042bc418cfdc6df8afc9b6e8e7a9d9cc0f96169b`  
		Last Modified: Fri, 24 Jan 2025 01:11:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a98ab643def392a3228cb986f42774fd3fd387751bfd7ebda9bcae8ea5a2112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185708e96c1654a4c771e548cc6b45da84ddbb18969a03f169da285cbffeafb8`

```dockerfile
```

-	Layers:
	-	`sha256:812b02d5eb49e9f6787679987eda5039cc446dec7b062f61ab99b11cef1b70d9`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d41958b27e4d81982a4e4b6ccdec359577a9c8d4b43b0d210434a153dba0de5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5255252e8f6543baa18ca99abbad1f30d05d255e7152dbe257a16161d6cdc3b`
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
	-	`sha256:d717c84ab12b4a51093484769eaf3bc6701832fba7e85cc2e9dbf3196f88c72c`  
		Last Modified: Fri, 24 Jan 2025 01:11:47 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf0653b936aa2ba75e95ce02bd2c15f6f941164d374c5bc783c3bde80d90275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ac0c76457bb639e17973ff76b132b586e18679fe5156294e2dd95297f0749`

```dockerfile
```

-	Layers:
	-	`sha256:2e7f242acf8cb665c590ba14eeeef0d1fba2d6dc23d5b1a891afec3324f18435`  
		Last Modified: Fri, 24 Jan 2025 01:11:48 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:120f05f21700741861065232b957d34875b121529dcfebd4e4e2ed1b65243aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9a6d423e17760a1c0596eab9d1b2d58f619748bd5738cb3643ab9d565d4a7`
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
	-	`sha256:78bb58bc5c01f048f85b7106af4b332f3b0b3ebdb2c8686f83ea2a3cb5085fec`  
		Last Modified: Fri, 24 Jan 2025 01:11:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2680e2ebdb2231cf9f2c1a7caed0ead5654c7067080669530accc8dbc402fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f808ecf65a3b9a11f96880bd8e99059848afcd1c374040a6bb9349203aff4162`

```dockerfile
```

-	Layers:
	-	`sha256:4b106a1a302d1726161028aba125a47ba72b3899e91ce153422cdb67b669748d`  
		Last Modified: Fri, 24 Jan 2025 01:11:50 GMT  
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
