<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.20`](#nats2-alpine320)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.20`](#nats210-alpine320)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.19`](#nats21019)
-	[`nats:2.10.19-alpine`](#nats21019-alpine)
-	[`nats:2.10.19-alpine3.20`](#nats21019-alpine320)
-	[`nats:2.10.19-linux`](#nats21019-linux)
-	[`nats:2.10.19-nanoserver`](#nats21019-nanoserver)
-	[`nats:2.10.19-nanoserver-1809`](#nats21019-nanoserver-1809)
-	[`nats:2.10.19-scratch`](#nats21019-scratch)
-	[`nats:2.10.19-windowsservercore`](#nats21019-windowsservercore)
-	[`nats:2.10.19-windowsservercore-1809`](#nats21019-windowsservercore-1809)
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
-	[`nats:alpine3.20`](#natsalpine320)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:52ee3d9be4b1f146f36b21a32a8dedbf5c99786dc0cdd8f7f93542b8f3c70203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6189; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
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
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:52ee3d9be4b1f146f36b21a32a8dedbf5c99786dc0cdd8f7f93542b8f3c70203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
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
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.19`

**does not exist** (yet?)

## `nats:2.10.19-alpine`

**does not exist** (yet?)

## `nats:2.10.19-alpine3.20`

**does not exist** (yet?)

## `nats:2.10.19-linux`

**does not exist** (yet?)

## `nats:2.10.19-nanoserver`

**does not exist** (yet?)

## `nats:2.10.19-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.10.19-scratch`

**does not exist** (yet?)

## `nats:2.10.19-windowsservercore`

**does not exist** (yet?)

## `nats:2.10.19-windowsservercore-1809`

**does not exist** (yet?)

## `nats:2.9`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:6bdf324d678ccc2959c5338f4350fa651cd19c82fda8f450e354137dcef29655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:97d8d1816c67fc2a75c1e82f8e1530a1e4a460568ffe4b712e9f3a4197597598
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9297616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb78ff6f71553abe5a2f44fa9cf2c8c5695fd96cc5105afbc0aa0066272b81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:55 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Mon, 22 Jul 2024 22:26:55 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:38 GMT
ENV NATS_SERVER=2.9.25
# Tue, 23 Jul 2024 00:33:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:41 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c5eff9b0bd7324c1c54a16ca40021b55440355ffd2c0a0feca6c49d9ab5946`  
		Last Modified: Tue, 23 Jul 2024 00:34:23 GMT  
		Size: 5.9 MB (5881002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0981bfff83e1601d6b76cad61dc5e29844755723f51e2b614e2ebeaa8cc0b5d2`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b2952ce224f4dc4b28f9847d426b3ec8834091a4e9589836d5426d5f85bd3`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d3124db7d71eb3f93ff6b73acc2eea53c6f2e048b1001db03e6ae95492f5a87e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8771740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad9bd1a94fe7f8f7a2a952b6e5e9ef826e2a6bc27239ddbf198f23fb15c113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:25 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 22 Jul 2024 21:49:25 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:34 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:11:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:38 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445dac1070d4ead63942bf836e58146930bf8192e99f077a9dbca31546191373`  
		Last Modified: Mon, 22 Jul 2024 22:12:34 GMT  
		Size: 5.6 MB (5612681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3829eb6d43490c868994eb19cf4c81f7a3c9be398a15c943936902364e7a0107`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63540a6d65449525b71f59e8fce823e5b45886a50d21668a938be75225e7c47d`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5d5372308de400d9fc058a62c23dc6525793545538b7c7d6c82d39e8d9c3691
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8519014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f0c7d1db0990f6b6cd52bc54431a5378447e892be9ccafd7cecfd883f36c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:57 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Mon, 22 Jul 2024 21:59:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:49 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:21:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:54 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad5d06bb97b9444680ea8aa8ec64a885935af6872de584d0bcd2d43413e010`  
		Last Modified: Mon, 22 Jul 2024 22:22:52 GMT  
		Size: 5.6 MB (5607479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bfac5cb032004e30d0b64a67aca8daa81c391130086cf1099331be30b83794`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d4188b79ceac8a631666958404586090462f9f6c258c651d07eb2af892a52`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f43cd15398204a72b748f715f85c7d4a70ccdbd334305eed0f47cd43dd667d76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2a1d2c0ac78b4c972b77bb9bac9ec1d8ea215a7c2202716ef85946ef1938a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:21 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 22 Jul 2024 21:44:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:46 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 23:25:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:49 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef07d8370103e642268c1366cc004fcd327445498acabf57caba63fec8148ad`  
		Last Modified: Mon, 22 Jul 2024 23:26:28 GMT  
		Size: 5.4 MB (5415909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de877fb114538261fb7ce703696900aaea49173ccb5ee155a39fd87f033daee`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238aaf2b6b91420648abe1b3e24571975d9248bbd8dfabce2496ccd9a53ce7b`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:6bdf324d678ccc2959c5338f4350fa651cd19c82fda8f450e354137dcef29655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:97d8d1816c67fc2a75c1e82f8e1530a1e4a460568ffe4b712e9f3a4197597598
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9297616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb78ff6f71553abe5a2f44fa9cf2c8c5695fd96cc5105afbc0aa0066272b81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:55 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Mon, 22 Jul 2024 22:26:55 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:38 GMT
ENV NATS_SERVER=2.9.25
# Tue, 23 Jul 2024 00:33:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:41 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c5eff9b0bd7324c1c54a16ca40021b55440355ffd2c0a0feca6c49d9ab5946`  
		Last Modified: Tue, 23 Jul 2024 00:34:23 GMT  
		Size: 5.9 MB (5881002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0981bfff83e1601d6b76cad61dc5e29844755723f51e2b614e2ebeaa8cc0b5d2`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b2952ce224f4dc4b28f9847d426b3ec8834091a4e9589836d5426d5f85bd3`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:d3124db7d71eb3f93ff6b73acc2eea53c6f2e048b1001db03e6ae95492f5a87e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8771740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad9bd1a94fe7f8f7a2a952b6e5e9ef826e2a6bc27239ddbf198f23fb15c113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:25 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 22 Jul 2024 21:49:25 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:34 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:11:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:38 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445dac1070d4ead63942bf836e58146930bf8192e99f077a9dbca31546191373`  
		Last Modified: Mon, 22 Jul 2024 22:12:34 GMT  
		Size: 5.6 MB (5612681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3829eb6d43490c868994eb19cf4c81f7a3c9be398a15c943936902364e7a0107`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63540a6d65449525b71f59e8fce823e5b45886a50d21668a938be75225e7c47d`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5d5372308de400d9fc058a62c23dc6525793545538b7c7d6c82d39e8d9c3691
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8519014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f0c7d1db0990f6b6cd52bc54431a5378447e892be9ccafd7cecfd883f36c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:57 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Mon, 22 Jul 2024 21:59:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:49 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:21:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:54 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad5d06bb97b9444680ea8aa8ec64a885935af6872de584d0bcd2d43413e010`  
		Last Modified: Mon, 22 Jul 2024 22:22:52 GMT  
		Size: 5.6 MB (5607479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bfac5cb032004e30d0b64a67aca8daa81c391130086cf1099331be30b83794`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d4188b79ceac8a631666958404586090462f9f6c258c651d07eb2af892a52`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f43cd15398204a72b748f715f85c7d4a70ccdbd334305eed0f47cd43dd667d76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2a1d2c0ac78b4c972b77bb9bac9ec1d8ea215a7c2202716ef85946ef1938a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:21 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 22 Jul 2024 21:44:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:46 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 23:25:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:49 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef07d8370103e642268c1366cc004fcd327445498acabf57caba63fec8148ad`  
		Last Modified: Mon, 22 Jul 2024 23:26:28 GMT  
		Size: 5.4 MB (5415909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de877fb114538261fb7ce703696900aaea49173ccb5ee155a39fd87f033daee`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238aaf2b6b91420648abe1b3e24571975d9248bbd8dfabce2496ccd9a53ce7b`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:e38fb48401a324d510d80bbb43eba7ad9ece8d05eea7da998dcefbcca33d8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:95db46ac13e416bfa83d4fc41a239694f3d5b1732a355e99486bcf71a0e02f17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160419358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250992696a93294dbddf891a71134d15cc44f478676e1331712e909ae139f3e4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:50:44 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:50:45 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:47 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37edcce3cfb1512d774c1f24c7b9adc01a1594da7415d27573e0c4b3ef5a037`  
		Last Modified: Tue, 13 Aug 2024 20:51:47 GMT  
		Size: 5.3 MB (5330058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8e5b75b44c30b610c34abfb5d0269f2e442c953a50104c32d45ae280f5223`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eba2c70ccd6b582dcd630231b70234db0ae64b41164865dadc539c0a58ba21`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a159d4a9a5b2acd9b6bb507f99fd052c61c24f68648bae779bc3b245be8fa4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deaea889248ab399da0efd2dac81b31439f51a6713eb780eb3e6f07f7e2713b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:e38fb48401a324d510d80bbb43eba7ad9ece8d05eea7da998dcefbcca33d8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:95db46ac13e416bfa83d4fc41a239694f3d5b1732a355e99486bcf71a0e02f17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160419358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250992696a93294dbddf891a71134d15cc44f478676e1331712e909ae139f3e4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:50:44 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:50:45 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:47 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37edcce3cfb1512d774c1f24c7b9adc01a1594da7415d27573e0c4b3ef5a037`  
		Last Modified: Tue, 13 Aug 2024 20:51:47 GMT  
		Size: 5.3 MB (5330058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8e5b75b44c30b610c34abfb5d0269f2e442c953a50104c32d45ae280f5223`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eba2c70ccd6b582dcd630231b70234db0ae64b41164865dadc539c0a58ba21`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a159d4a9a5b2acd9b6bb507f99fd052c61c24f68648bae779bc3b245be8fa4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deaea889248ab399da0efd2dac81b31439f51a6713eb780eb3e6f07f7e2713b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:8db29d0fa613c52a250397f402579d4716f8bec378ec4d2c4ebd87eb11a733d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:dc5625077b3a00e6057f6fe8602cc9bf82fc9aeaffc42dfe8ed7c7ee1d2ae687
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251282095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87cd897289649471fb5f88156ce8c6f8fe05c83f0dae0118f3186a69ed401f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER=2.9.25
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Tue, 13 Aug 2024 20:48:17 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Tue, 13 Aug 2024 20:49:10 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:50:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:50:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:27 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c60c222b69c30eccd6340196bcf76d048d54bf78d4c397112fc895cc6ca26`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c2be44e67cb500b840ed3772b0bf6d1c842700856e111666de0e72c219d78`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17a5d514072810513652219871a6767fd60865068bb9154f9eb68713d29933`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6660d2c3f7e1bc36c9ab0e37d9a3ae2790388c749b2c5eb2fe419367849133a8`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 447.8 KB (447832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3b897c9eeeb6955d3aff1d6887f408a2bf708a32b70f7474970733cae240cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:38 GMT  
		Size: 5.6 MB (5618185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e7a506dfeae7ce9769000faa9b359b52c724cea5090fc946bce8fb164d244`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821f1c1bcbcb062eca5aa69356d4c93a152ef97fba574567f4457ffe3cd2568b`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d0d30e0791107b5a2803a3d00da9d15a9fe37e81c63e649b299932a68549cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a6cd6672d51b35ebfb9d230fe2edaef4d13e5d57ef9409a33175b3a483eae`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:8db29d0fa613c52a250397f402579d4716f8bec378ec4d2c4ebd87eb11a733d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:dc5625077b3a00e6057f6fe8602cc9bf82fc9aeaffc42dfe8ed7c7ee1d2ae687
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251282095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87cd897289649471fb5f88156ce8c6f8fe05c83f0dae0118f3186a69ed401f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER=2.9.25
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Tue, 13 Aug 2024 20:48:17 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Tue, 13 Aug 2024 20:49:10 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:50:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:50:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:27 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c60c222b69c30eccd6340196bcf76d048d54bf78d4c397112fc895cc6ca26`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c2be44e67cb500b840ed3772b0bf6d1c842700856e111666de0e72c219d78`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17a5d514072810513652219871a6767fd60865068bb9154f9eb68713d29933`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6660d2c3f7e1bc36c9ab0e37d9a3ae2790388c749b2c5eb2fe419367849133a8`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 447.8 KB (447832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3b897c9eeeb6955d3aff1d6887f408a2bf708a32b70f7474970733cae240cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:38 GMT  
		Size: 5.6 MB (5618185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e7a506dfeae7ce9769000faa9b359b52c724cea5090fc946bce8fb164d244`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821f1c1bcbcb062eca5aa69356d4c93a152ef97fba574567f4457ffe3cd2568b`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d0d30e0791107b5a2803a3d00da9d15a9fe37e81c63e649b299932a68549cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a6cd6672d51b35ebfb9d230fe2edaef4d13e5d57ef9409a33175b3a483eae`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:6bdf324d678ccc2959c5338f4350fa651cd19c82fda8f450e354137dcef29655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:97d8d1816c67fc2a75c1e82f8e1530a1e4a460568ffe4b712e9f3a4197597598
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9297616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb78ff6f71553abe5a2f44fa9cf2c8c5695fd96cc5105afbc0aa0066272b81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:55 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Mon, 22 Jul 2024 22:26:55 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:38 GMT
ENV NATS_SERVER=2.9.25
# Tue, 23 Jul 2024 00:33:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:41 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c5eff9b0bd7324c1c54a16ca40021b55440355ffd2c0a0feca6c49d9ab5946`  
		Last Modified: Tue, 23 Jul 2024 00:34:23 GMT  
		Size: 5.9 MB (5881002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0981bfff83e1601d6b76cad61dc5e29844755723f51e2b614e2ebeaa8cc0b5d2`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b2952ce224f4dc4b28f9847d426b3ec8834091a4e9589836d5426d5f85bd3`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d3124db7d71eb3f93ff6b73acc2eea53c6f2e048b1001db03e6ae95492f5a87e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8771740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad9bd1a94fe7f8f7a2a952b6e5e9ef826e2a6bc27239ddbf198f23fb15c113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:25 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 22 Jul 2024 21:49:25 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:34 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:11:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:38 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445dac1070d4ead63942bf836e58146930bf8192e99f077a9dbca31546191373`  
		Last Modified: Mon, 22 Jul 2024 22:12:34 GMT  
		Size: 5.6 MB (5612681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3829eb6d43490c868994eb19cf4c81f7a3c9be398a15c943936902364e7a0107`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63540a6d65449525b71f59e8fce823e5b45886a50d21668a938be75225e7c47d`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5d5372308de400d9fc058a62c23dc6525793545538b7c7d6c82d39e8d9c3691
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8519014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f0c7d1db0990f6b6cd52bc54431a5378447e892be9ccafd7cecfd883f36c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:57 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Mon, 22 Jul 2024 21:59:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:49 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:21:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:54 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad5d06bb97b9444680ea8aa8ec64a885935af6872de584d0bcd2d43413e010`  
		Last Modified: Mon, 22 Jul 2024 22:22:52 GMT  
		Size: 5.6 MB (5607479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bfac5cb032004e30d0b64a67aca8daa81c391130086cf1099331be30b83794`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d4188b79ceac8a631666958404586090462f9f6c258c651d07eb2af892a52`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f43cd15398204a72b748f715f85c7d4a70ccdbd334305eed0f47cd43dd667d76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2a1d2c0ac78b4c972b77bb9bac9ec1d8ea215a7c2202716ef85946ef1938a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:21 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 22 Jul 2024 21:44:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:46 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 23:25:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:49 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef07d8370103e642268c1366cc004fcd327445498acabf57caba63fec8148ad`  
		Last Modified: Mon, 22 Jul 2024 23:26:28 GMT  
		Size: 5.4 MB (5415909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de877fb114538261fb7ce703696900aaea49173ccb5ee155a39fd87f033daee`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238aaf2b6b91420648abe1b3e24571975d9248bbd8dfabce2496ccd9a53ce7b`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:6bdf324d678ccc2959c5338f4350fa651cd19c82fda8f450e354137dcef29655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:97d8d1816c67fc2a75c1e82f8e1530a1e4a460568ffe4b712e9f3a4197597598
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9297616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb78ff6f71553abe5a2f44fa9cf2c8c5695fd96cc5105afbc0aa0066272b81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:55 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Mon, 22 Jul 2024 22:26:55 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:38 GMT
ENV NATS_SERVER=2.9.25
# Tue, 23 Jul 2024 00:33:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:41 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c5eff9b0bd7324c1c54a16ca40021b55440355ffd2c0a0feca6c49d9ab5946`  
		Last Modified: Tue, 23 Jul 2024 00:34:23 GMT  
		Size: 5.9 MB (5881002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0981bfff83e1601d6b76cad61dc5e29844755723f51e2b614e2ebeaa8cc0b5d2`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b2952ce224f4dc4b28f9847d426b3ec8834091a4e9589836d5426d5f85bd3`  
		Last Modified: Tue, 23 Jul 2024 00:34:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:d3124db7d71eb3f93ff6b73acc2eea53c6f2e048b1001db03e6ae95492f5a87e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8771740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad9bd1a94fe7f8f7a2a952b6e5e9ef826e2a6bc27239ddbf198f23fb15c113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:25 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 22 Jul 2024 21:49:25 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:34 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:11:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:38 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445dac1070d4ead63942bf836e58146930bf8192e99f077a9dbca31546191373`  
		Last Modified: Mon, 22 Jul 2024 22:12:34 GMT  
		Size: 5.6 MB (5612681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3829eb6d43490c868994eb19cf4c81f7a3c9be398a15c943936902364e7a0107`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63540a6d65449525b71f59e8fce823e5b45886a50d21668a938be75225e7c47d`  
		Last Modified: Mon, 22 Jul 2024 22:12:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5d5372308de400d9fc058a62c23dc6525793545538b7c7d6c82d39e8d9c3691
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8519014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f0c7d1db0990f6b6cd52bc54431a5378447e892be9ccafd7cecfd883f36c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:57 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
# Mon, 22 Jul 2024 21:59:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:49 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 22:21:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:54 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad5d06bb97b9444680ea8aa8ec64a885935af6872de584d0bcd2d43413e010`  
		Last Modified: Mon, 22 Jul 2024 22:22:52 GMT  
		Size: 5.6 MB (5607479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bfac5cb032004e30d0b64a67aca8daa81c391130086cf1099331be30b83794`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d4188b79ceac8a631666958404586090462f9f6c258c651d07eb2af892a52`  
		Last Modified: Mon, 22 Jul 2024 22:22:50 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f43cd15398204a72b748f715f85c7d4a70ccdbd334305eed0f47cd43dd667d76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2a1d2c0ac78b4c972b77bb9bac9ec1d8ea215a7c2202716ef85946ef1938a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:21 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 22 Jul 2024 21:44:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:46 GMT
ENV NATS_SERVER=2.9.25
# Mon, 22 Jul 2024 23:25:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:49 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef07d8370103e642268c1366cc004fcd327445498acabf57caba63fec8148ad`  
		Last Modified: Mon, 22 Jul 2024 23:26:28 GMT  
		Size: 5.4 MB (5415909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de877fb114538261fb7ce703696900aaea49173ccb5ee155a39fd87f033daee`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238aaf2b6b91420648abe1b3e24571975d9248bbd8dfabce2496ccd9a53ce7b`  
		Last Modified: Mon, 22 Jul 2024 23:26:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:e38fb48401a324d510d80bbb43eba7ad9ece8d05eea7da998dcefbcca33d8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:95db46ac13e416bfa83d4fc41a239694f3d5b1732a355e99486bcf71a0e02f17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160419358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250992696a93294dbddf891a71134d15cc44f478676e1331712e909ae139f3e4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:50:44 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:50:45 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:47 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37edcce3cfb1512d774c1f24c7b9adc01a1594da7415d27573e0c4b3ef5a037`  
		Last Modified: Tue, 13 Aug 2024 20:51:47 GMT  
		Size: 5.3 MB (5330058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8e5b75b44c30b610c34abfb5d0269f2e442c953a50104c32d45ae280f5223`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eba2c70ccd6b582dcd630231b70234db0ae64b41164865dadc539c0a58ba21`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a159d4a9a5b2acd9b6bb507f99fd052c61c24f68648bae779bc3b245be8fa4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deaea889248ab399da0efd2dac81b31439f51a6713eb780eb3e6f07f7e2713b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:e38fb48401a324d510d80bbb43eba7ad9ece8d05eea7da998dcefbcca33d8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:95db46ac13e416bfa83d4fc41a239694f3d5b1732a355e99486bcf71a0e02f17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160419358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250992696a93294dbddf891a71134d15cc44f478676e1331712e909ae139f3e4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:50:44 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:50:45 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:47 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37edcce3cfb1512d774c1f24c7b9adc01a1594da7415d27573e0c4b3ef5a037`  
		Last Modified: Tue, 13 Aug 2024 20:51:47 GMT  
		Size: 5.3 MB (5330058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8e5b75b44c30b610c34abfb5d0269f2e442c953a50104c32d45ae280f5223`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eba2c70ccd6b582dcd630231b70234db0ae64b41164865dadc539c0a58ba21`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a159d4a9a5b2acd9b6bb507f99fd052c61c24f68648bae779bc3b245be8fa4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deaea889248ab399da0efd2dac81b31439f51a6713eb780eb3e6f07f7e2713b`  
		Last Modified: Tue, 13 Aug 2024 20:51:46 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:337eb17c97bad24772f68d48b385f61ca472a2cace17f07a9067f3e54febeb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f712a8a2c0ecd3563f19d79f4f085f5e27db2cfb04f50baf5ff820b887fea52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61792c56a1f5dd463525e41bc82c894d6270886e2a8a36c454b42c2c6f8d1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Thu, 20 Jun 2024 22:17:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 22:17:18 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 22:17:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09942ef7141412b41665a9873c419060ae4febb7c2b60464739dc5a0b4a9c341`  
		Last Modified: Wed, 26 Jun 2024 17:03:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f6ed317f022b7c27ae4c87d6103a0d99758ca3be7e5ed9a98b53eaa14068390
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f04b84d11e264daa97d4348eaa1a864e08df6e9b28aebc64e7f955c7cb29b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Mon, 22 Jul 2024 22:11:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:42 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2cbdfe114a825a970e3c3e1638614933afbe1208ddd7c90ff9b0a087355e0f`  
		Last Modified: Mon, 22 Jul 2024 22:12:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8532fa28aef1bb565fa00aac89b5301dde23d40c8e473052369cd80baeb54340
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c858d9a64413990afe3d599907c8a9b29e26b598c5b732147a751c22f1ddd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 21 Jun 2024 00:31:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 21 Jun 2024 00:31:24 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:31:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 21 Jun 2024 00:31:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4264be9b98297815b8b5ed0df0434a5b35351b48c34a571b60edc336f27884b`  
		Last Modified: Fri, 21 Jun 2024 00:40:50 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:8db29d0fa613c52a250397f402579d4716f8bec378ec4d2c4ebd87eb11a733d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:dc5625077b3a00e6057f6fe8602cc9bf82fc9aeaffc42dfe8ed7c7ee1d2ae687
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251282095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87cd897289649471fb5f88156ce8c6f8fe05c83f0dae0118f3186a69ed401f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER=2.9.25
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Tue, 13 Aug 2024 20:48:17 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Tue, 13 Aug 2024 20:49:10 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:50:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:50:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:27 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c60c222b69c30eccd6340196bcf76d048d54bf78d4c397112fc895cc6ca26`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c2be44e67cb500b840ed3772b0bf6d1c842700856e111666de0e72c219d78`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17a5d514072810513652219871a6767fd60865068bb9154f9eb68713d29933`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6660d2c3f7e1bc36c9ab0e37d9a3ae2790388c749b2c5eb2fe419367849133a8`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 447.8 KB (447832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3b897c9eeeb6955d3aff1d6887f408a2bf708a32b70f7474970733cae240cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:38 GMT  
		Size: 5.6 MB (5618185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e7a506dfeae7ce9769000faa9b359b52c724cea5090fc946bce8fb164d244`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821f1c1bcbcb062eca5aa69356d4c93a152ef97fba574567f4457ffe3cd2568b`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d0d30e0791107b5a2803a3d00da9d15a9fe37e81c63e649b299932a68549cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a6cd6672d51b35ebfb9d230fe2edaef4d13e5d57ef9409a33175b3a483eae`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:8db29d0fa613c52a250397f402579d4716f8bec378ec4d2c4ebd87eb11a733d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:dc5625077b3a00e6057f6fe8602cc9bf82fc9aeaffc42dfe8ed7c7ee1d2ae687
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251282095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87cd897289649471fb5f88156ce8c6f8fe05c83f0dae0118f3186a69ed401f6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER=2.9.25
# Tue, 13 Aug 2024 20:48:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Tue, 13 Aug 2024 20:48:17 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Tue, 13 Aug 2024 20:49:10 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:50:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:50:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:50:27 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:50:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:50:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c60c222b69c30eccd6340196bcf76d048d54bf78d4c397112fc895cc6ca26`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c2be44e67cb500b840ed3772b0bf6d1c842700856e111666de0e72c219d78`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17a5d514072810513652219871a6767fd60865068bb9154f9eb68713d29933`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6660d2c3f7e1bc36c9ab0e37d9a3ae2790388c749b2c5eb2fe419367849133a8`  
		Last Modified: Tue, 13 Aug 2024 20:51:39 GMT  
		Size: 447.8 KB (447832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3b897c9eeeb6955d3aff1d6887f408a2bf708a32b70f7474970733cae240cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:38 GMT  
		Size: 5.6 MB (5618185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e7a506dfeae7ce9769000faa9b359b52c724cea5090fc946bce8fb164d244`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821f1c1bcbcb062eca5aa69356d4c93a152ef97fba574567f4457ffe3cd2568b`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d0d30e0791107b5a2803a3d00da9d15a9fe37e81c63e649b299932a68549cb`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a6cd6672d51b35ebfb9d230fe2edaef4d13e5d57ef9409a33175b3a483eae`  
		Last Modified: Tue, 13 Aug 2024 20:51:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
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
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:2b0c80d75966dde3077e59483a95b14a2803bbb550cd0f9f30fa3712490e2cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:dc7816805cdf645ce301357229c1659c9f64a2734c13e2e78c47246187011374
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9784636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e58c1966c013e7096115e437fef9fa1be2a5c42dd2ebf03b41236a4c4eee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:33:28 GMT
ENV NATS_SERVER=2.10.18
# Tue, 23 Jul 2024 00:33:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 23 Jul 2024 00:33:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 23 Jul 2024 00:33:30 GMT
EXPOSE 4222 6222 8222
# Tue, 23 Jul 2024 00:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf45a8197940112572ad1508b8e3facb3ba4f77145c385d21d4286fdac7fe1`  
		Last Modified: Tue, 23 Jul 2024 00:34:03 GMT  
		Size: 6.2 MB (6160769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7378735454ecb46ae3e29bfc3a1b44492f6878c4337e86f7b5c16be1bb3a90`  
		Last Modified: Tue, 23 Jul 2024 00:34:01 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768c385bfe4c523cea5de59362ffb91977378c126afd52ba43de4840ae62732f`  
		Last Modified: Tue, 23 Jul 2024 00:34:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:52ee3d9be4b1f146f36b21a32a8dedbf5c99786dc0cdd8f7f93542b8f3c70203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6189; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:26738056a26bb551d144142d299c11f8f5db1c87c267e5867ccee6d6bc603620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:0f65593a0e842a436514c83002371de287a47fa5cd53837a9014aeb33e2041f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160902188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03671d0f82d8f023561796144fb423f0d95a87f4cfaf8c3522fc7a1edcd7b34d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:48:07 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:48:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:48:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:48:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59504fe84b783a646f611f6703f9231ff69ce3e2fcb61f1252efaf05982665f9`  
		Last Modified: Tue, 13 Aug 2024 20:51:26 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ce5bfbc1cf807b5cb52c09dfca5abc9283b0b4359a4a99cf5adf7b28a1643a`  
		Last Modified: Tue, 13 Aug 2024 20:51:25 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d3eeddb5b235c670c8de3d2371381c5972af9f7bc0c98af98853db28b0a1b8`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b2344f322d64c0a57c3652c28b3e203353a4401259920d3e1d3bd72a7e857`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec260706b5cf529f8e9239a10aface161d9f2a276e295b9ba063f4474a907bb2`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e5f39e2eacdeae83fcd84755594130d5fccd32fe889c59c82f3c347678ccd`  
		Last Modified: Tue, 13 Aug 2024 20:51:24 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:5941297ee98027de144ea20d3ee38bbace69b1480d1e707ff477b3b52ab8d26c
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
$ docker pull nats@sha256:8621aeb0589934f67f1ae8d04de8cd0807a6815aff004b7a2cbe4e86142cfa70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8df11043e0dd108dedc7741b1df4ae6e0a133a442b4f3f136b2d9acc73357`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:d928c2735fb6afb32248a29c78fab7eb3ddad9f5655cdeb410bd86b34431af55 in /nats-server 
# Wed, 17 Jul 2024 17:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:20:16 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:20:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6440db5cdc8d807108e27afd301553133c478ba6cb2df1b09f5d410b462429df`  
		Last Modified: Wed, 17 Jul 2024 17:21:02 GMT  
		Size: 5.7 MB (5696324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1946ef8ef2bcc47afa5f15377b74da708c39b1738c1371541c9c466de0fc9`  
		Last Modified: Wed, 17 Jul 2024 17:21:01 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:092436208a27c545ae0b2b2859f612afbc7890e9b89ccbbde3c0866da30b53aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e592af5917afd2910020fad9ff393c98518ad7f84064cb1e1ec2426351a95`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Mon, 22 Jul 2024 22:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 22 Jul 2024 22:11:32 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jul 2024 22:11:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b707802c49348b96615d9b883be3f8f4791712a0513eb2d1487fd973057b46`  
		Last Modified: Mon, 22 Jul 2024 22:12:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7238539e08ba9761eb5d745f7d17a761dc487ee5da711c09d918250ce0f59f1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d147798d5ef33e407b6540e4d66eb9301fc49be135b5ee8b9cc5d8e9bf3aa6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:0ea44b1e765e5ee5dd3441daf4ca2f9a579e418e57d36a5dbe701c082fc97f74 in /nats-server 
# Wed, 17 Jul 2024 17:57:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:57:39 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:57:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706018663addcf2ca6b4dda371e0be8192f47363fbed68d82063f432c7a49696`  
		Last Modified: Wed, 17 Jul 2024 17:58:23 GMT  
		Size: 5.4 MB (5360045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6c730aaf3a900688a13a5919fddee2e8d70002d44a16f56c7230ad7d1d168e`  
		Last Modified: Wed, 17 Jul 2024 17:58:22 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:113f5fd076fc57d888e8c50e1ec8571bf44fcae344ac82eacfa5fa3c464a285f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790799900863f48944fc5f55f286cf208bc34f66752d18ddc443861d40ecfc39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:39:53 GMT
COPY file:99de7375d60117160cf05282142acc75d18208b5572af3984f5de80bb27823f2 in /nats-server 
# Wed, 17 Jul 2024 17:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:39:54 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b5b15b906c6e4276c4cb98c30d4655b011a9eab0ae948f7bcd13c161b98da96`  
		Last Modified: Wed, 17 Jul 2024 17:40:38 GMT  
		Size: 5.3 MB (5264459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748e0030645504f6205f5c03c84bf48870a4c3b5ac75d8985ac022676bf600`  
		Last Modified: Wed, 17 Jul 2024 17:40:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:cdd19a8dc00bdf7522703ba47873120ff590497757bc3807663ac7e6ba51979e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d627f7f7555587610c0cc206a23afe43ef8efd0eeda47ca06639d858c5d411`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:16:54 GMT
COPY file:7936f1d8e19f42f3586b79d5da4dfba80b24eb878a9cff0595f27b6c0f5efa83 in /nats-server 
# Wed, 17 Jul 2024 17:16:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:16:55 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:56 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a155d3618f73d3bfbc1246c725d34aae7711f189035ce958b80ae16755d414fb`  
		Last Modified: Wed, 17 Jul 2024 17:17:31 GMT  
		Size: 5.2 MB (5238344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40e991476a0bd465d9c5aabb3ccebd02bfc9f95dd1e36cec072cc0deafb45d`  
		Last Modified: Wed, 17 Jul 2024 17:17:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:285741b93a53360a3715c93288de7eeb2ecd76afecd06399715d79be4bd36e75
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592840651ff5d38b925f9405209d7f3f06f696582827f3d7a6a8492eb7d3d9a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:d3aaa1bc2d3834d84437c32d5955c0c64d3389e0565e1a8dd37f3696c9e2f9b0 in /nats-server 
# Wed, 17 Jul 2024 17:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:43:06 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:43:06 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7967b31194ba754d4405e3d8d526f23abcd888a52b746b03810db215abd014a8`  
		Last Modified: Wed, 17 Jul 2024 17:43:41 GMT  
		Size: 5.6 MB (5561376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11953a6ece35958fce68846b7bf32f3055e1ce5ee282b41079e3fc58aa5a13`  
		Last Modified: Wed, 17 Jul 2024 17:43:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:15d9704c30682833528a5815c262cf95f046b7da412183425e7a87517cf40595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9deb3d85ee4a7313a1a7defc1dde3752112125c3f462c9960c7a5d9607648ba8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251766997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce49344ab08729315489c1817eadb7bbdbc60535969f780fa3846c8544657a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER=2.10.18
# Tue, 13 Aug 2024 20:45:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Tue, 13 Aug 2024 20:45:41 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Tue, 13 Aug 2024 20:46:34 GMT
RUN Set-PSDebug -Trace 2
# Tue, 13 Aug 2024 20:47:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 13 Aug 2024 20:47:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Aug 2024 20:47:56 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Aug 2024 20:47:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Aug 2024 20:47:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c910c8d678572d8e48160d9face57f1ce0b7adf4cde7d11f5f7741af8feed8a`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eabbb4d0b71be6e451b4985f34eb1822d7caf828feb1de07dcf4ca27a2ccfce`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04856d100d25b0685b009b6c272646f0ceb1f8af538124e0797af7e763295e`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699203a8af558d97aab77c2e798b5b822b003cbe17c3b5a8a981cc5d2c5ccec`  
		Last Modified: Tue, 13 Aug 2024 20:51:11 GMT  
		Size: 448.3 KB (448326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd0c2303d56a322f8734315be86ce538db6358d06084a0935622915c75c748`  
		Last Modified: Tue, 13 Aug 2024 20:51:10 GMT  
		Size: 6.1 MB (6102263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed1f2d2efd078f52ce4ba389e8e512e2d7326377ec1ccdb677258db0ccc6135`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993179548ba778ab1bd08307bba50a05d8fdfa0f7134a2cf90f58bf22793b0c7`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b663cad9877357139f8c191c15e724f9c4a52ef7ec2674e0e658531671d78b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4de46aaa98aea62afe476e42c0d9eb20f074df65dab03b022a73090d5be37b`  
		Last Modified: Tue, 13 Aug 2024 20:51:09 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
