<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.16`](#nats21016)
-	[`nats:2.10.16-alpine`](#nats21016-alpine)
-	[`nats:2.10.16-alpine3.19`](#nats21016-alpine319)
-	[`nats:2.10.16-linux`](#nats21016-linux)
-	[`nats:2.10.16-nanoserver`](#nats21016-nanoserver)
-	[`nats:2.10.16-nanoserver-1809`](#nats21016-nanoserver-1809)
-	[`nats:2.10.16-scratch`](#nats21016-scratch)
-	[`nats:2.10.16-windowsservercore`](#nats21016-windowsservercore)
-	[`nats:2.10.16-windowsservercore-1809`](#nats21016-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.25`](#nats2925)
-	[`nats:2.9.25-alpine`](#nats2925-alpine)
-	[`nats:2.9.25-alpine3.18`](#nats2925-alpine318)
-	[`nats:2.9.25-linux`](#nats2925-linux)
-	[`nats:2.9.25-nanoserver`](#nats2925-nanoserver)
-	[`nats:2.9.25-nanoserver-1809`](#nats2925-nanoserver-1809)
-	[`nats:2.9.25-scratch`](#nats2925-scratch)
-	[`nats:2.9.25-windowsservercore`](#nats2925-windowsservercore)
-	[`nats:2.9.25-windowsservercore-1809`](#nats2925-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:939e07b8bf71e6211face0fb08a878b59fb7c0ea4ce1abc6202091d8d394e41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5936; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:939e07b8bf71e6211face0fb08a878b59fb7c0ea4ce1abc6202091d8d394e41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16`

```console
$ docker pull nats@sha256:939e07b8bf71e6211face0fb08a878b59fb7c0ea4ce1abc6202091d8d394e41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.16` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-alpine`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-alpine3.19`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-linux`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-linux` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-nanoserver`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.16-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-nanoserver-1809`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.16-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-scratch`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.16-scratch` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.16-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-windowsservercore`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.16-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.16-windowsservercore-1809`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.16-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:50dab7ea6a1972081bc6303419091079d948d3d71fef1a06ead698cf029e64ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:22248f2a7b6f0a69a609f4b26e7c137dc9fa5c6a1e585c77aeed40559b68e1d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38025782bff8c5072f17a59413b470916a3205a55edceed569a2f093994ad5af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:47:01 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:47:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ae3bd251b62ead6333304a3c5de147759d4803a1a23e2f0129e69c5c2ae4e0c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8770348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc9368b0b299caa07ca5bd89d1f995ae2f9e51c840d4a6c15120ee081c7e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:21 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Thu, 20 Jun 2024 17:49:21 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:30 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 18:05:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:34 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b649d5487f1d50264f744e544431b5cc518c83512126c36fa7fe4fb153c13d`  
		Last Modified: Thu, 20 Jun 2024 18:06:35 GMT  
		Size: 5.6 MB (5612666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14662edc5cbeabee0f6ce3d82340269e8ee6fb752bbd50e0e1a31292bdb99291`  
		Last Modified: Thu, 20 Jun 2024 18:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12ee8853d1c7c970aa7d2eb1264f4dec598cedb418315a1e2081bb2ddeee5d7`  
		Last Modified: Thu, 20 Jun 2024 18:06:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3f5b15256a65d97915e270e2542546e1443360defbcd1515e233a21104b1d9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d71b7d539a6c13234b2b44a7542e00b48beff1b0dfb1607cb62b09b19f5d1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:31 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b57d564aa71648a88228012c647a8ec00bff06dc28d6cc300a249dff3d4b8311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94615f552762b021e6bdc145ab89d8fc30bacd74e67264d7a280f84d8d8f5234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:43 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 19:07:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:46 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d66846d3901141636e86948a493158d780a2a9d4f3954035da6ac8b260b246`  
		Last Modified: Thu, 20 Jun 2024 19:08:50 GMT  
		Size: 5.4 MB (5415899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1fe6b898e972cc655e990a98b73f623c2579f4865d27b4f5618081c496a84`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e6fe609f5e3bb41d71772d93c3f4df446b1af6a519e670368218e499e9bc9`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:50dab7ea6a1972081bc6303419091079d948d3d71fef1a06ead698cf029e64ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:22248f2a7b6f0a69a609f4b26e7c137dc9fa5c6a1e585c77aeed40559b68e1d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38025782bff8c5072f17a59413b470916a3205a55edceed569a2f093994ad5af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:47:01 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:47:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ae3bd251b62ead6333304a3c5de147759d4803a1a23e2f0129e69c5c2ae4e0c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8770348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc9368b0b299caa07ca5bd89d1f995ae2f9e51c840d4a6c15120ee081c7e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:21 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Thu, 20 Jun 2024 17:49:21 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:30 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 18:05:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:34 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b649d5487f1d50264f744e544431b5cc518c83512126c36fa7fe4fb153c13d`  
		Last Modified: Thu, 20 Jun 2024 18:06:35 GMT  
		Size: 5.6 MB (5612666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14662edc5cbeabee0f6ce3d82340269e8ee6fb752bbd50e0e1a31292bdb99291`  
		Last Modified: Thu, 20 Jun 2024 18:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12ee8853d1c7c970aa7d2eb1264f4dec598cedb418315a1e2081bb2ddeee5d7`  
		Last Modified: Thu, 20 Jun 2024 18:06:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3f5b15256a65d97915e270e2542546e1443360defbcd1515e233a21104b1d9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d71b7d539a6c13234b2b44a7542e00b48beff1b0dfb1607cb62b09b19f5d1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:31 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b57d564aa71648a88228012c647a8ec00bff06dc28d6cc300a249dff3d4b8311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94615f552762b021e6bdc145ab89d8fc30bacd74e67264d7a280f84d8d8f5234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:43 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 19:07:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:46 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d66846d3901141636e86948a493158d780a2a9d4f3954035da6ac8b260b246`  
		Last Modified: Thu, 20 Jun 2024 19:08:50 GMT  
		Size: 5.4 MB (5415899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1fe6b898e972cc655e990a98b73f623c2579f4865d27b4f5618081c496a84`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e6fe609f5e3bb41d71772d93c3f4df446b1af6a519e670368218e499e9bc9`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:ed040c97c7ddf6403d2550b785c9a3729e7dd3ec414255ee5caa91668757814b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b5a15cb5b1dc462542c26aa3a107da528370149f0cca869ab23f798f7ad2c09d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160369859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19446900df5bbf6df0055a4bcf6b88e8ff66f64f82e09f9ce66e49d47f34c2e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:06:23 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca5fcb20ed78736516eb29867b1d97e9b6d6ebacaf2dbf41f660899b8bfc47`  
		Last Modified: Wed, 12 Jun 2024 19:07:37 GMT  
		Size: 5.3 MB (5330227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48944798979d5e6d6ddb990fedcfe7a15d94368c72252bbb217a01c46df76b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4bd7e1db06934d53245f35f20ef1cd18a5a7c0c5e76cb6bf09cf5a58b3dec`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cf33d818951d2fc02f1bd8ecb0dca713173aa23947c477f0be2559b9b15d6`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66303cb4fd8bd51e568323f3b2a1093c9bf83b795dfcdc4e49284b9b2e0d6b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:ed040c97c7ddf6403d2550b785c9a3729e7dd3ec414255ee5caa91668757814b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b5a15cb5b1dc462542c26aa3a107da528370149f0cca869ab23f798f7ad2c09d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160369859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19446900df5bbf6df0055a4bcf6b88e8ff66f64f82e09f9ce66e49d47f34c2e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:06:23 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca5fcb20ed78736516eb29867b1d97e9b6d6ebacaf2dbf41f660899b8bfc47`  
		Last Modified: Wed, 12 Jun 2024 19:07:37 GMT  
		Size: 5.3 MB (5330227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48944798979d5e6d6ddb990fedcfe7a15d94368c72252bbb217a01c46df76b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4bd7e1db06934d53245f35f20ef1cd18a5a7c0c5e76cb6bf09cf5a58b3dec`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cf33d818951d2fc02f1bd8ecb0dca713173aa23947c477f0be2559b9b15d6`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66303cb4fd8bd51e568323f3b2a1093c9bf83b795dfcdc4e49284b9b2e0d6b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:0d3895b0fb598f82088398c245280d88f0e754bbf4797d626be9fd8ae7155e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:26a220234b48db76408335fdfe6c351c5dc79682e4d0c8bb666feb08af89cbc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2226728413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783fe5afbcc233218a40f0074f37858bd09243881b042df31c6f44b445ec45c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER=2.9.25
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 12 Jun 2024 19:03:10 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 12 Jun 2024 19:04:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:06:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:06:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:12 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf240d70beaf947df7f559375f6ebd0632daf3ee263272f2288b1d5b71fca74`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36040bac48949f9a3d11725f4e342f152aa28cf1dd6df420b24dae867765c185`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c30cb99b4b57715ca4f3dd80a49b7e375a569f6184f09a9d7a9891a43cb41e6`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8d1ba53845fb79f8eb733143f5241ba351d723497dbda0b48f25f41a78061`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 432.1 KB (432062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3804090125cd0295b547c6629456c4e285374c22c9a71347c2365db5ad636`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 5.6 MB (5601815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d835d1ee00d826482c929ea4813f6dfb267475919f5a362daa8051338e4aca`  
		Last Modified: Wed, 12 Jun 2024 19:07:26 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96f44f663c915bfc2b0a3d3e45ec60b06330a4ca2206c4a1b6efd949bb887c`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1c9a4a33ec9899a742751ab843215ddb11a7edb8faf013848ea03478bb4ff5`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eded9a6927218f087ad55744f5d895c5db539c5e5d5017c5dc8c0f9c7a17fb`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:0d3895b0fb598f82088398c245280d88f0e754bbf4797d626be9fd8ae7155e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:26a220234b48db76408335fdfe6c351c5dc79682e4d0c8bb666feb08af89cbc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2226728413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783fe5afbcc233218a40f0074f37858bd09243881b042df31c6f44b445ec45c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER=2.9.25
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 12 Jun 2024 19:03:10 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 12 Jun 2024 19:04:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:06:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:06:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:12 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf240d70beaf947df7f559375f6ebd0632daf3ee263272f2288b1d5b71fca74`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36040bac48949f9a3d11725f4e342f152aa28cf1dd6df420b24dae867765c185`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c30cb99b4b57715ca4f3dd80a49b7e375a569f6184f09a9d7a9891a43cb41e6`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8d1ba53845fb79f8eb733143f5241ba351d723497dbda0b48f25f41a78061`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 432.1 KB (432062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3804090125cd0295b547c6629456c4e285374c22c9a71347c2365db5ad636`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 5.6 MB (5601815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d835d1ee00d826482c929ea4813f6dfb267475919f5a362daa8051338e4aca`  
		Last Modified: Wed, 12 Jun 2024 19:07:26 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96f44f663c915bfc2b0a3d3e45ec60b06330a4ca2206c4a1b6efd949bb887c`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1c9a4a33ec9899a742751ab843215ddb11a7edb8faf013848ea03478bb4ff5`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eded9a6927218f087ad55744f5d895c5db539c5e5d5017c5dc8c0f9c7a17fb`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine`

```console
$ docker pull nats@sha256:50dab7ea6a1972081bc6303419091079d948d3d71fef1a06ead698cf029e64ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:22248f2a7b6f0a69a609f4b26e7c137dc9fa5c6a1e585c77aeed40559b68e1d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38025782bff8c5072f17a59413b470916a3205a55edceed569a2f093994ad5af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:47:01 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:47:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ae3bd251b62ead6333304a3c5de147759d4803a1a23e2f0129e69c5c2ae4e0c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8770348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc9368b0b299caa07ca5bd89d1f995ae2f9e51c840d4a6c15120ee081c7e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:21 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Thu, 20 Jun 2024 17:49:21 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:30 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 18:05:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:34 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b649d5487f1d50264f744e544431b5cc518c83512126c36fa7fe4fb153c13d`  
		Last Modified: Thu, 20 Jun 2024 18:06:35 GMT  
		Size: 5.6 MB (5612666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14662edc5cbeabee0f6ce3d82340269e8ee6fb752bbd50e0e1a31292bdb99291`  
		Last Modified: Thu, 20 Jun 2024 18:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12ee8853d1c7c970aa7d2eb1264f4dec598cedb418315a1e2081bb2ddeee5d7`  
		Last Modified: Thu, 20 Jun 2024 18:06:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3f5b15256a65d97915e270e2542546e1443360defbcd1515e233a21104b1d9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d71b7d539a6c13234b2b44a7542e00b48beff1b0dfb1607cb62b09b19f5d1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:31 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b57d564aa71648a88228012c647a8ec00bff06dc28d6cc300a249dff3d4b8311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94615f552762b021e6bdc145ab89d8fc30bacd74e67264d7a280f84d8d8f5234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:43 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 19:07:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:46 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d66846d3901141636e86948a493158d780a2a9d4f3954035da6ac8b260b246`  
		Last Modified: Thu, 20 Jun 2024 19:08:50 GMT  
		Size: 5.4 MB (5415899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1fe6b898e972cc655e990a98b73f623c2579f4865d27b4f5618081c496a84`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e6fe609f5e3bb41d71772d93c3f4df446b1af6a519e670368218e499e9bc9`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:50dab7ea6a1972081bc6303419091079d948d3d71fef1a06ead698cf029e64ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:22248f2a7b6f0a69a609f4b26e7c137dc9fa5c6a1e585c77aeed40559b68e1d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38025782bff8c5072f17a59413b470916a3205a55edceed569a2f093994ad5af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:47:01 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:47:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ae3bd251b62ead6333304a3c5de147759d4803a1a23e2f0129e69c5c2ae4e0c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8770348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc9368b0b299caa07ca5bd89d1f995ae2f9e51c840d4a6c15120ee081c7e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:21 GMT
ADD file:230fce01d9c96cbd9cd838a9f35e92d82c331d7d5e07f0b901757344140c780d in / 
# Thu, 20 Jun 2024 17:49:21 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:30 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 18:05:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:34 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff6dd47581ed08c02ef24f2a6fa0daba6ec413e52f7a5bd7b9b6e4eae9a43b6c`  
		Last Modified: Thu, 20 Jun 2024 17:49:56 GMT  
		Size: 3.2 MB (3156709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b649d5487f1d50264f744e544431b5cc518c83512126c36fa7fe4fb153c13d`  
		Last Modified: Thu, 20 Jun 2024 18:06:35 GMT  
		Size: 5.6 MB (5612666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14662edc5cbeabee0f6ce3d82340269e8ee6fb752bbd50e0e1a31292bdb99291`  
		Last Modified: Thu, 20 Jun 2024 18:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12ee8853d1c7c970aa7d2eb1264f4dec598cedb418315a1e2081bb2ddeee5d7`  
		Last Modified: Thu, 20 Jun 2024 18:06:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3f5b15256a65d97915e270e2542546e1443360defbcd1515e233a21104b1d9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d71b7d539a6c13234b2b44a7542e00b48beff1b0dfb1607cb62b09b19f5d1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:31 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b57d564aa71648a88228012c647a8ec00bff06dc28d6cc300a249dff3d4b8311
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94615f552762b021e6bdc145ab89d8fc30bacd74e67264d7a280f84d8d8f5234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:43 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 19:07:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:46 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d66846d3901141636e86948a493158d780a2a9d4f3954035da6ac8b260b246`  
		Last Modified: Thu, 20 Jun 2024 19:08:50 GMT  
		Size: 5.4 MB (5415899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1fe6b898e972cc655e990a98b73f623c2579f4865d27b4f5618081c496a84`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e6fe609f5e3bb41d71772d93c3f4df446b1af6a519e670368218e499e9bc9`  
		Last Modified: Thu, 20 Jun 2024 19:08:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver`

```console
$ docker pull nats@sha256:ed040c97c7ddf6403d2550b785c9a3729e7dd3ec414255ee5caa91668757814b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b5a15cb5b1dc462542c26aa3a107da528370149f0cca869ab23f798f7ad2c09d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160369859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19446900df5bbf6df0055a4bcf6b88e8ff66f64f82e09f9ce66e49d47f34c2e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:06:23 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca5fcb20ed78736516eb29867b1d97e9b6d6ebacaf2dbf41f660899b8bfc47`  
		Last Modified: Wed, 12 Jun 2024 19:07:37 GMT  
		Size: 5.3 MB (5330227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48944798979d5e6d6ddb990fedcfe7a15d94368c72252bbb217a01c46df76b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4bd7e1db06934d53245f35f20ef1cd18a5a7c0c5e76cb6bf09cf5a58b3dec`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cf33d818951d2fc02f1bd8ecb0dca713173aa23947c477f0be2559b9b15d6`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66303cb4fd8bd51e568323f3b2a1093c9bf83b795dfcdc4e49284b9b2e0d6b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:ed040c97c7ddf6403d2550b785c9a3729e7dd3ec414255ee5caa91668757814b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b5a15cb5b1dc462542c26aa3a107da528370149f0cca869ab23f798f7ad2c09d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160369859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19446900df5bbf6df0055a4bcf6b88e8ff66f64f82e09f9ce66e49d47f34c2e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:06:23 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:25 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca5fcb20ed78736516eb29867b1d97e9b6d6ebacaf2dbf41f660899b8bfc47`  
		Last Modified: Wed, 12 Jun 2024 19:07:37 GMT  
		Size: 5.3 MB (5330227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48944798979d5e6d6ddb990fedcfe7a15d94368c72252bbb217a01c46df76b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4bd7e1db06934d53245f35f20ef1cd18a5a7c0c5e76cb6bf09cf5a58b3dec`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cf33d818951d2fc02f1bd8ecb0dca713173aa23947c477f0be2559b9b15d6`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66303cb4fd8bd51e568323f3b2a1093c9bf83b795dfcdc4e49284b9b2e0d6b`  
		Last Modified: Wed, 12 Jun 2024 19:07:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:cd595db54564a02307fb059a29c80e1cbe5327c5a3f2846d0c1bebbf258fdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:41ac26a55be045d16dd4acc5b9e06585a7e0882f4b3912dfd520da5aeb4a2220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571b121eb3fe79a8407d38fd3a53a018ce3c894cccdab404c50108be8891a10`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:47:06 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Wed, 22 May 2024 19:47:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:47:06 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:47:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:47:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba4a72f8f34d641590fdf6c560adaea8fd07958917710c1ced52726cdc07188`  
		Last Modified: Wed, 22 May 2024 19:48:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4a625c0bca7e415028b5589830e8490d52593176e99e5c1af9452f7f35cdd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901238a6956a12edd5494c1337015e1f4d87d4af3a790aa31f1a7d9fb93011b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 20 Jun 2024 18:05:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:37 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:37 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384c041e2a9fb82af309274b43bf36c71db3780575595218860fadcf500593c`  
		Last Modified: Thu, 20 Jun 2024 18:06:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0830c8b9db5b3083d145eebbc6f46360a26fc237d0a596e7b62cbef8de152e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2435d1eacf092add957bbfb04a54de998ec352abf44ca86cf1b7bab21a6b50d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Wed, 22 May 2024 18:33:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ec9ded1ef48f0772f1c10b009fd6894074aa02f8222bbc7b833668f4fb109`  
		Last Modified: Wed, 22 May 2024 18:34:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a381b5d7172d72f1e324e0e2c45db11a4bb239aaa9a3adab61b4b5cd8e1369e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943c4e146a60ec9bf33613622b0f1390b439e1d6135ecf869ee55a91b10a620`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Thu, 20 Jun 2024 19:07:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:50 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a552624bb90ffce91239a942779ec32d98777dfb2a530bb8f4ccf739a4bf09`  
		Last Modified: Thu, 20 Jun 2024 19:09:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore`

```console
$ docker pull nats@sha256:0d3895b0fb598f82088398c245280d88f0e754bbf4797d626be9fd8ae7155e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:26a220234b48db76408335fdfe6c351c5dc79682e4d0c8bb666feb08af89cbc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2226728413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783fe5afbcc233218a40f0074f37858bd09243881b042df31c6f44b445ec45c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER=2.9.25
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 12 Jun 2024 19:03:10 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 12 Jun 2024 19:04:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:06:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:06:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:12 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf240d70beaf947df7f559375f6ebd0632daf3ee263272f2288b1d5b71fca74`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36040bac48949f9a3d11725f4e342f152aa28cf1dd6df420b24dae867765c185`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c30cb99b4b57715ca4f3dd80a49b7e375a569f6184f09a9d7a9891a43cb41e6`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8d1ba53845fb79f8eb733143f5241ba351d723497dbda0b48f25f41a78061`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 432.1 KB (432062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3804090125cd0295b547c6629456c4e285374c22c9a71347c2365db5ad636`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 5.6 MB (5601815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d835d1ee00d826482c929ea4813f6dfb267475919f5a362daa8051338e4aca`  
		Last Modified: Wed, 12 Jun 2024 19:07:26 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96f44f663c915bfc2b0a3d3e45ec60b06330a4ca2206c4a1b6efd949bb887c`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1c9a4a33ec9899a742751ab843215ddb11a7edb8faf013848ea03478bb4ff5`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eded9a6927218f087ad55744f5d895c5db539c5e5d5017c5dc8c0f9c7a17fb`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:0d3895b0fb598f82088398c245280d88f0e754bbf4797d626be9fd8ae7155e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:26a220234b48db76408335fdfe6c351c5dc79682e4d0c8bb666feb08af89cbc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2226728413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783fe5afbcc233218a40f0074f37858bd09243881b042df31c6f44b445ec45c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER=2.9.25
# Wed, 12 Jun 2024 19:03:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 12 Jun 2024 19:03:10 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 12 Jun 2024 19:04:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:06:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:06:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:06:12 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:06:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:06:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf240d70beaf947df7f559375f6ebd0632daf3ee263272f2288b1d5b71fca74`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36040bac48949f9a3d11725f4e342f152aa28cf1dd6df420b24dae867765c185`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c30cb99b4b57715ca4f3dd80a49b7e375a569f6184f09a9d7a9891a43cb41e6`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8d1ba53845fb79f8eb733143f5241ba351d723497dbda0b48f25f41a78061`  
		Last Modified: Wed, 12 Jun 2024 19:07:28 GMT  
		Size: 432.1 KB (432062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3804090125cd0295b547c6629456c4e285374c22c9a71347c2365db5ad636`  
		Last Modified: Wed, 12 Jun 2024 19:07:27 GMT  
		Size: 5.6 MB (5601815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d835d1ee00d826482c929ea4813f6dfb267475919f5a362daa8051338e4aca`  
		Last Modified: Wed, 12 Jun 2024 19:07:26 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96f44f663c915bfc2b0a3d3e45ec60b06330a4ca2206c4a1b6efd949bb887c`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1c9a4a33ec9899a742751ab843215ddb11a7edb8faf013848ea03478bb4ff5`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eded9a6927218f087ad55744f5d895c5db539c5e5d5017c5dc8c0f9c7a17fb`  
		Last Modified: Wed, 12 Jun 2024 19:07:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:b6e8745cc2728999532d53dfdaa281d741546713df73e87551c91b4289276de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:4cc3e9271504c3be9c2bd5af4f6929265d7db626e986b4a7abc66f4fc4004a92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae314433bdd4af30a81e32caea9c43056f75b53586b1cc45349605ea77a0dd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 19:46:51 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:46:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:c1c3f0bceb82215bc89c429d235dfd564a0154336df7611788915005d5d22bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a23fad47456e330d6140ec4dbe02add093ab97c9485ee26efd5c5e61894ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 May 2024 18:33:16 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:33:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0e63d4320bcaa44889213777f61e65e2a901756d401261f33855c43477513cb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9205558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03460eb31ac504df5dc558624b0c5ebfee69ba1899e3c94d737fdcacbbfdf91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:52:51 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:52:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:52:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:52:55 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:52:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:52:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8820d85da5e75c931f8257d0d65d232efe6a1e4dec7dc0d8a5ac07ff4d564d59`  
		Last Modified: Thu, 20 Jun 2024 19:53:20 GMT  
		Size: 5.8 MB (5843953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7aa3204ca60b59abd2cf6485e479d54ef0b530211983e9e5bdec651774527`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f501600b1dcc188e17f1d168a356d059246d2fde18aa29939e237e00c931883`  
		Last Modified: Thu, 20 Jun 2024 19:53:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:939e07b8bf71e6211face0fb08a878b59fb7c0ea4ce1abc6202091d8d394e41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5936; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:b279b57be0c67002a3b1dc109db09717b74732bd476cbcb2ab79378c0b9b2ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:6d843fc5789b6322365e46e36203cd2ab90afddde5b235ff62e878c1899c841a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8498fd2c3fa67ee8d453ae1bfc2a569863a5597730adf8345dd41db71d19e9c7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:02:59 GMT
RUN cmd /S /C #(nop) COPY file:e634b8d8431824b53f95f04a1a787a66fac400f6b27037e57e00122926afdb6c in C:\nats-server.exe 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:03:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:03:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:03:02 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18c55d79b89f124847b02586c11e32ee91b5d72dd79f1b9d4ab95fd7657f4f8`  
		Last Modified: Wed, 12 Jun 2024 19:07:13 GMT  
		Size: 5.8 MB (5786620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f9e0ab7a827e96dc53db05bc3f4b82305ed3a417d0c7a2452df23221ea06d`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8017b28b1604e787037c50a439a87ff39501d1341c05834685c96ad690dd69`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e944fc3a6c6e2f7e9146b945257c914a7d31711f4643a9680cb5770ad9a7185`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325201c2db5caba2f48577f16d44be6376161386d43397e092a59dc0ff3ef41`  
		Last Modified: Wed, 12 Jun 2024 19:07:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0c16d0ae4810124d679d4d5b90428c647a9271aea6c2cca7e41875a2b27ad70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:32e1e8abb5a8cfdf609faa5a42f8ac7a7c197bb505481a0f2ca8dec96c92fcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5672973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed1eae653c9e468d6aab8948dfeed03248e5f67d2f2da27c630d7a1bd668e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 19:46:57 GMT
COPY file:bde3b96323851506bdb8dee1a5c849f57fed0675a388571c8ae8bdb78fbb308f in /nats-server 
# Wed, 22 May 2024 19:46:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 19:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 19:46:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 19:46:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d79939f5589ddcdfe25deacd46470779a671bda9460d28dcc354413093601b95`  
		Last Modified: Tue, 21 May 2024 23:35:47 GMT  
		Size: 5.7 MB (5672465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc84a4e89ca7d5be0bf5171bf5436fd0b90af5d9e581180824a8e11137f006`  
		Last Modified: Wed, 22 May 2024 19:47:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e3aa3be2c67194016b3f11276b1ba5d7099d61e00cd83b8cf6a2447367de0704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee458741b6b2f61474f34a27770215e71e07d677698d2df0e74f83b168a9f61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 22 May 2024 18:33:26 GMT
COPY file:9bd22b280d9474da700b413662ba97d86693461a656554c7d65e50aa664d72d2 in /nats-server 
# Wed, 22 May 2024 18:33:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 22 May 2024 18:33:26 GMT
EXPOSE 4222 6222 8222
# Wed, 22 May 2024 18:33:27 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 May 2024 18:33:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b7c9f79cc0b5fadd268a6afc358930f56c66b60358751ef77ef18f5e0e13a75`  
		Last Modified: Tue, 21 May 2024 23:04:53 GMT  
		Size: 5.3 MB (5337507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36381f89dbcb69410eaee4d31b42055ec46d797db481affddcb39bc62a9534d`  
		Last Modified: Wed, 22 May 2024 18:34:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a651b2d76541fa428ed0ca09c3bdd8c959684fa1f0e62a6c8c8771e963476c57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcdece433818613588c4b3b9dfb3c7a80da774a7e13ff9071787a657805b3c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:aeec7db8c859fc6772a1e71152ae0edf2fbb33888beee45ff6f537021682c368 in /nats-server 
# Thu, 20 Jun 2024 19:53:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:53:02 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:53:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:53:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3554a35f86605472601753e787e946b0399c33611a4892aeed776bd0c951d04b`  
		Last Modified: Tue, 21 May 2024 23:22:15 GMT  
		Size: 5.2 MB (5214803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e6c0a75b1efcc5091e3d2e007c13249f5f153818300c138840287e6a6d29f`  
		Last Modified: Thu, 20 Jun 2024 19:53:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:63188017df97d6f235939f4faae26048d022f162366d0b5c1df6c593540f06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:387623c8ab7708f67935a1cecb8d885a9ced4532b2771a32206e3d22cce0e02f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227190599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d86ff192fe23a6f5fd72e06a6fcc71a671f355ffd3b6100f52217a6dbc278`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER=2.10.16
# Wed, 12 Jun 2024 18:59:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.16/nats-server-v2.10.16-windows-amd64.zip
# Wed, 12 Jun 2024 18:59:32 GMT
ENV NATS_SERVER_SHASUM=22a5ef3a54200ebdebaa325822f477c89dc6533ec6fc1f531d897aa876517ccf
# Wed, 12 Jun 2024 19:00:41 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:02:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:02:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 12 Jun 2024 19:02:37 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Jun 2024 19:02:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Jun 2024 19:02:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf10af5700dee66f0176705f7ad9ee491e7e7670bac854f191f3f6f9c483cca`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189dfff9be015aae3a758d1bd613cf72bfaec12c212c78f46cadcb651c36954`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc43101c103447137c69c9b5e660147c54ba5909a615b3f63844e67e6e23436`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cbb9b9673f98caac01392c7ffd9923e7debe72009cbcb79978a625c99f6c`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 432.6 KB (432625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e4e2e867a45ffa7ed08b57d13050279965f0bfa7fdfa01746a009d9bbc63c6`  
		Last Modified: Wed, 12 Jun 2024 19:06:57 GMT  
		Size: 6.1 MB (6063772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c584dd6ceb7812ff65923ce0d2cf1d2bd0afeaeebd43d25b8bfa8dc9706004`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231229c6db78e3a3ca716520f0346d4fb1c9d1f593027ff7e4b338c13e20ec84`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eddf6a5b53d31abc46120c896c736d97efb8fb4affdd07046bf6630c64683e`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccfcbcfa66c59eb4b91e89264119b1f986c718a176cbaad49eff3b8fb864fa4`  
		Last Modified: Wed, 12 Jun 2024 19:06:55 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
