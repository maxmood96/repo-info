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
-	[`nats:2.10.17`](#nats21017)
-	[`nats:2.10.17-alpine`](#nats21017-alpine)
-	[`nats:2.10.17-alpine3.20`](#nats21017-alpine320)
-	[`nats:2.10.17-linux`](#nats21017-linux)
-	[`nats:2.10.17-nanoserver`](#nats21017-nanoserver)
-	[`nats:2.10.17-nanoserver-1809`](#nats21017-nanoserver-1809)
-	[`nats:2.10.17-scratch`](#nats21017-scratch)
-	[`nats:2.10.17-windowsservercore`](#nats21017-windowsservercore)
-	[`nats:2.10.17-windowsservercore-1809`](#nats21017-windowsservercore-1809)
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
$ docker pull nats@sha256:cd49507948f7a11535ba72b3bd6c0847909bede2385b6c2e638f96a943c2e746
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:8f5c163cf6a1547423e75f78b98ed556cb7b712c96818f8d9b2b9be44aa23496
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
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
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
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
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

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:8121751d080c8576d985395388b306ce5e0672f628ab216f4ff3d612fee9c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:cd49507948f7a11535ba72b3bd6c0847909bede2385b6c2e638f96a943c2e746
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:8f5c163cf6a1547423e75f78b98ed556cb7b712c96818f8d9b2b9be44aa23496
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
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
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
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
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

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:8121751d080c8576d985395388b306ce5e0672f628ab216f4ff3d612fee9c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2.10-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17`

```console
$ docker pull nats@sha256:6841cde247f9d06696056558ec7fe130316229ca62856e663fed60fb6976c303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.17` - linux; amd64

```console
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17` - linux; ppc64le

```console
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-alpine`

```console
$ docker pull nats@sha256:8121751d080c8576d985395388b306ce5e0672f628ab216f4ff3d612fee9c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2.10.17-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-alpine3.20`

```console
$ docker pull nats@sha256:8121751d080c8576d985395388b306ce5e0672f628ab216f4ff3d612fee9c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2.10.17-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-linux`

```console
$ docker pull nats@sha256:4ae6a6877e6d0d0ff317a8525a7019848a36bf7d2d25dbc9db5fb790e4d45799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2.10.17-linux` - linux; amd64

```console
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-nanoserver`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.17-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-nanoserver-1809`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.17-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-scratch`

```console
$ docker pull nats@sha256:4ae6a6877e6d0d0ff317a8525a7019848a36bf7d2d25dbc9db5fb790e4d45799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:2.10.17-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.17-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-windowsservercore`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.17-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.17-windowsservercore-1809`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2.10.17-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:617210c5ac29e7d1705bb8a5366f5746165e45b3fcb7d73eb0a0b89b402696c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e64de38e8ecf735c324c3ed8de9a751faf2344f506716eb05f512dc1a13bb9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9295886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed031e31403872b30f30eaefb41f8627f7113cd87959dd1965b99fb36cb1d4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:17:09 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 22:17:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 22:17:12 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 22:17:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25faef01a7d46c1afc1198db301ca08dd50e0550297004b21fac0a6be8ead8fb`  
		Last Modified: Wed, 26 Jun 2024 17:03:44 GMT  
		Size: 5.9 MB (5881019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e7c0bc47510c424337da100ad9209dbfc3e960fa6417c35853bce3ec0cf8b`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591270b119c9a12362c820cfaf6ad8b7b9a24606a5c1f2bf7fb16016e6f9ef87`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
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
$ docker pull nats@sha256:4048ada4e5f796b3d2a5770088ad3e36826bd1c0f88a79393cda1f6b63248f9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba5b0d6ec29205983bbc4da22a0788ac7b1f73475a518668008fc0d85c3512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:36 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Thu, 20 Jun 2024 18:00:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:30:11 GMT
ENV NATS_SERVER=2.9.25
# Fri, 21 Jun 2024 00:30:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 21 Jun 2024 00:30:16 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:30:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7daed24513b21bbce9d45ac2d152db6635ba4c9f814809bd3711ed73b277cf8`  
		Last Modified: Fri, 21 Jun 2024 00:39:39 GMT  
		Size: 5.6 MB (5607450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00941480d8cff64500d8820b584e11a7b73937b77331e0e89030e9943cc5394`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0c8ce45101ab3338ce9b67b97a6dcfd01cb98f00bb2a6db2508ce7bff6443f`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:617210c5ac29e7d1705bb8a5366f5746165e45b3fcb7d73eb0a0b89b402696c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e64de38e8ecf735c324c3ed8de9a751faf2344f506716eb05f512dc1a13bb9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9295886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed031e31403872b30f30eaefb41f8627f7113cd87959dd1965b99fb36cb1d4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:17:09 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 22:17:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 22:17:12 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 22:17:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25faef01a7d46c1afc1198db301ca08dd50e0550297004b21fac0a6be8ead8fb`  
		Last Modified: Wed, 26 Jun 2024 17:03:44 GMT  
		Size: 5.9 MB (5881019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e7c0bc47510c424337da100ad9209dbfc3e960fa6417c35853bce3ec0cf8b`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591270b119c9a12362c820cfaf6ad8b7b9a24606a5c1f2bf7fb16016e6f9ef87`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
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
$ docker pull nats@sha256:4048ada4e5f796b3d2a5770088ad3e36826bd1c0f88a79393cda1f6b63248f9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba5b0d6ec29205983bbc4da22a0788ac7b1f73475a518668008fc0d85c3512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:36 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Thu, 20 Jun 2024 18:00:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:30:11 GMT
ENV NATS_SERVER=2.9.25
# Fri, 21 Jun 2024 00:30:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 21 Jun 2024 00:30:16 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:30:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7daed24513b21bbce9d45ac2d152db6635ba4c9f814809bd3711ed73b277cf8`  
		Last Modified: Fri, 21 Jun 2024 00:39:39 GMT  
		Size: 5.6 MB (5607450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00941480d8cff64500d8820b584e11a7b73937b77331e0e89030e9943cc5394`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0c8ce45101ab3338ce9b67b97a6dcfd01cb98f00bb2a6db2508ce7bff6443f`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:617210c5ac29e7d1705bb8a5366f5746165e45b3fcb7d73eb0a0b89b402696c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e64de38e8ecf735c324c3ed8de9a751faf2344f506716eb05f512dc1a13bb9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9295886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed031e31403872b30f30eaefb41f8627f7113cd87959dd1965b99fb36cb1d4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:17:09 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 22:17:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 22:17:12 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 22:17:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25faef01a7d46c1afc1198db301ca08dd50e0550297004b21fac0a6be8ead8fb`  
		Last Modified: Wed, 26 Jun 2024 17:03:44 GMT  
		Size: 5.9 MB (5881019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e7c0bc47510c424337da100ad9209dbfc3e960fa6417c35853bce3ec0cf8b`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591270b119c9a12362c820cfaf6ad8b7b9a24606a5c1f2bf7fb16016e6f9ef87`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
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
$ docker pull nats@sha256:4048ada4e5f796b3d2a5770088ad3e36826bd1c0f88a79393cda1f6b63248f9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba5b0d6ec29205983bbc4da22a0788ac7b1f73475a518668008fc0d85c3512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:36 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Thu, 20 Jun 2024 18:00:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:30:11 GMT
ENV NATS_SERVER=2.9.25
# Fri, 21 Jun 2024 00:30:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 21 Jun 2024 00:30:16 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:30:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7daed24513b21bbce9d45ac2d152db6635ba4c9f814809bd3711ed73b277cf8`  
		Last Modified: Fri, 21 Jun 2024 00:39:39 GMT  
		Size: 5.6 MB (5607450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00941480d8cff64500d8820b584e11a7b73937b77331e0e89030e9943cc5394`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0c8ce45101ab3338ce9b67b97a6dcfd01cb98f00bb2a6db2508ce7bff6443f`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:617210c5ac29e7d1705bb8a5366f5746165e45b3fcb7d73eb0a0b89b402696c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e64de38e8ecf735c324c3ed8de9a751faf2344f506716eb05f512dc1a13bb9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9295886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed031e31403872b30f30eaefb41f8627f7113cd87959dd1965b99fb36cb1d4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:17:09 GMT
ENV NATS_SERVER=2.9.25
# Thu, 20 Jun 2024 22:17:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 22:17:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 22:17:12 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 22:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 22:17:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25faef01a7d46c1afc1198db301ca08dd50e0550297004b21fac0a6be8ead8fb`  
		Last Modified: Wed, 26 Jun 2024 17:03:44 GMT  
		Size: 5.9 MB (5881019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e7c0bc47510c424337da100ad9209dbfc3e960fa6417c35853bce3ec0cf8b`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591270b119c9a12362c820cfaf6ad8b7b9a24606a5c1f2bf7fb16016e6f9ef87`  
		Last Modified: Wed, 26 Jun 2024 17:03:43 GMT  
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
$ docker pull nats@sha256:4048ada4e5f796b3d2a5770088ad3e36826bd1c0f88a79393cda1f6b63248f9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba5b0d6ec29205983bbc4da22a0788ac7b1f73475a518668008fc0d85c3512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:36 GMT
ADD file:660e92101a2e85e85255c5cb167543738aac99ac498b869c973195a800ff39db in / 
# Thu, 20 Jun 2024 18:00:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:30:11 GMT
ENV NATS_SERVER=2.9.25
# Fri, 21 Jun 2024 00:30:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 21 Jun 2024 00:30:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 21 Jun 2024 00:30:16 GMT
EXPOSE 4222 6222 8222
# Fri, 21 Jun 2024 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:30:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e128aeb9f03d63e0dfe7f909e6d964354408536719a932f0a457c7290129694a`  
		Last Modified: Thu, 20 Jun 2024 18:01:15 GMT  
		Size: 2.9 MB (2908678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7daed24513b21bbce9d45ac2d152db6635ba4c9f814809bd3711ed73b277cf8`  
		Last Modified: Fri, 21 Jun 2024 00:39:39 GMT  
		Size: 5.6 MB (5607450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00941480d8cff64500d8820b584e11a7b73937b77331e0e89030e9943cc5394`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0c8ce45101ab3338ce9b67b97a6dcfd01cb98f00bb2a6db2508ce7bff6443f`  
		Last Modified: Fri, 21 Jun 2024 00:39:37 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:7aaa76066889ab067e01625077ab2475f39d7464a882a1a8b597953939ecf7f1
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
$ docker pull nats@sha256:8f5c163cf6a1547423e75f78b98ed556cb7b712c96818f8d9b2b9be44aa23496
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
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
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
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
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

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:8121751d080c8576d985395388b306ce5e0672f628ab216f4ff3d612fee9c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:cd49507948f7a11535ba72b3bd6c0847909bede2385b6c2e638f96a943c2e746
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
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
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
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
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
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
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:5195ecf10c2b516fec5bfb6ae487b75b5ec433338cc704c9a6971ec907e617f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:b246a667c2242326002d7d1ed0294cb23f4abac2d32d409e67e4ef4affb0b148
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6e57f49ed021a3dc329373285295a6d9d6f9166ef80f220dc96f820433a67a`
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
# Fri, 28 Jun 2024 00:15:18 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:15:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.17/nats-server-v2.10.17-windows-amd64.zip
# Fri, 28 Jun 2024 00:15:20 GMT
ENV NATS_SERVER_SHASUM=05590ce7be8802cbd8a75ce84fd74bd4f6ffd65f141277363936143f264d2f47
# Fri, 28 Jun 2024 00:16:47 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Jun 2024 00:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Jun 2024 00:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:18:45 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:18:46 GMT
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
	-	`sha256:2e5ee191911514cca388e8d1ebf484f9f3944a19fb91eaf9ed76f653bca33a89`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdab00343c3faca0fb40fd3134a76287e1b4beeb1f7ea80d08a563cf7cc81c6`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5e764e166ec7aa93a112437a4b66b16d215188f86c8419d7e62381d1e9028`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ddb79019e553acb5349dd73d085d500a4ee9420cc7b93cf89b7938b6dc36`  
		Last Modified: Fri, 28 Jun 2024 00:19:56 GMT  
		Size: 469.0 KB (468968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc23581425fe55182e7fc54a0004f41d7f58797172de12751103aadf12e9011`  
		Last Modified: Fri, 28 Jun 2024 00:19:55 GMT  
		Size: 6.1 MB (6116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19fb7e5ee2395b6497f5c95cf0864cd65dee59545d651c82b053c9d7de2323`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdce20e5095d9ab2ceb3523be142be0b3050f0e233346a0cccc9b689970ffe5`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3dcaf7d2d9287f586f2b3984ccbeb8361b9b6983c7c26e6401cf7e8bfb0d9`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f6f0d9b837ab19a8a1e340aa6154847732e81f5f99140cc06a3cfb0e55f49`  
		Last Modified: Fri, 28 Jun 2024 00:19:54 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
