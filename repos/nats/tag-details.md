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
-	[`nats:2.10.18`](#nats21018)
-	[`nats:2.10.18-alpine`](#nats21018-alpine)
-	[`nats:2.10.18-alpine3.20`](#nats21018-alpine320)
-	[`nats:2.10.18-linux`](#nats21018-linux)
-	[`nats:2.10.18-nanoserver`](#nats21018-nanoserver)
-	[`nats:2.10.18-nanoserver-1809`](#nats21018-nanoserver-1809)
-	[`nats:2.10.18-scratch`](#nats21018-scratch)
-	[`nats:2.10.18-windowsservercore`](#nats21018-windowsservercore)
-	[`nats:2.10.18-windowsservercore-1809`](#nats21018-windowsservercore-1809)
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
$ docker pull nats@sha256:05bf691418146d1c7b171cd06b62eae32f1a5e05c3f80e4842c365849596b248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6054; amd64

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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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

### `nats:2` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:05bf691418146d1c7b171cd06b62eae32f1a5e05c3f80e4842c365849596b248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6054; amd64

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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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

### `nats:2.10` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18`

```console
$ docker pull nats@sha256:05bf691418146d1c7b171cd06b62eae32f1a5e05c3f80e4842c365849596b248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10.18` - linux; amd64

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

### `nats:2.10.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18` - linux; arm variant v7

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

### `nats:2.10.18` - linux; arm64 variant v8

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

### `nats:2.10.18` - linux; ppc64le

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

### `nats:2.10.18` - linux; s390x

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

### `nats:2.10.18` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-alpine`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.18-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-alpine3.20`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.18-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-linux`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.18-linux` - linux; amd64

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

### `nats:2.10.18-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-linux` - linux; arm variant v7

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

### `nats:2.10.18-linux` - linux; arm64 variant v8

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

### `nats:2.10.18-linux` - linux; ppc64le

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

### `nats:2.10.18-linux` - linux; s390x

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

## `nats:2.10.18-nanoserver`

```console
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10.18-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-nanoserver-1809`

```console
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10.18-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-scratch`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.18-scratch` - linux; amd64

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

### `nats:2.10.18-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.18-scratch` - linux; arm variant v7

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

### `nats:2.10.18-scratch` - linux; arm64 variant v8

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

### `nats:2.10.18-scratch` - linux; ppc64le

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

### `nats:2.10.18-scratch` - linux; s390x

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

## `nats:2.10.18-windowsservercore`

```console
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10.18-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.18-windowsservercore-1809`

```console
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.10.18-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:8869876f9796173fa30882b1776a971932cbfa343197af9cc17e554711c9fc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:24087a3a56f3542aa76594bdbf60ec2d5cdc5c3a37b147929e036033c5960b34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160417834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009ec0ef5fa05d65e637632d81fc83f95a782f954b38372d3cebde0145807a23`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:50:07 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7842936c7a3b549ce1d7723e685a0b7155324b9d1bd8a48d119d49598e36b827`  
		Last Modified: Wed, 10 Jul 2024 17:51:17 GMT  
		Size: 5.3 MB (5330185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecebd27e858b9c2f81159753b9ca9c3dc356c8a0f424de6b2dc1e4dca4849f1`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af439e567ac5a6e8ac01ebc3821440fa51e60a2e642d7bd711b17d00ccd317bf`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755e229eef1121ec2128f0138ae3b09172f52015cdc841fd00988939387e5334`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7aceea265cfb43d525c62226aed26269770664c45a89a94e9d4873272ae97`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:8869876f9796173fa30882b1776a971932cbfa343197af9cc17e554711c9fc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:24087a3a56f3542aa76594bdbf60ec2d5cdc5c3a37b147929e036033c5960b34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160417834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009ec0ef5fa05d65e637632d81fc83f95a782f954b38372d3cebde0145807a23`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:50:07 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7842936c7a3b549ce1d7723e685a0b7155324b9d1bd8a48d119d49598e36b827`  
		Last Modified: Wed, 10 Jul 2024 17:51:17 GMT  
		Size: 5.3 MB (5330185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecebd27e858b9c2f81159753b9ca9c3dc356c8a0f424de6b2dc1e4dca4849f1`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af439e567ac5a6e8ac01ebc3821440fa51e60a2e642d7bd711b17d00ccd317bf`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755e229eef1121ec2128f0138ae3b09172f52015cdc841fd00988939387e5334`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7aceea265cfb43d525c62226aed26269770664c45a89a94e9d4873272ae97`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:5e4cb5bd0125ad60e1ac0a8f7d47512f8d66ca09207481226d24c4f00b637790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:6f15766bd375c2a4e083ea3da0dc17ab9421e9d6ba7670f8e63530b32026e7a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244522827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5f47c24199973add8fb939a5d0a35950e4419f93230949a270c36e56a926e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:39 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Jul 2024 17:48:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Jul 2024 17:49:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Jul 2024 17:49:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:49:57 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:49:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:49:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d3c2b5f2b5ccf41453354651ad302348b4bb8f11b3847f2e01b953fb91723`  
		Last Modified: Wed, 10 Jul 2024 17:51:08 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312388bc1ac3f43c23f278f59000070f2259532bc686a75d8e29e08e05757d8`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af6f92a72eee24d1fa8472fa142a66123b75939684be086fa34c4e58babb99`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e3e604bb86f204c06909e636643b9dd2b2eda44208a213f08f480e59aa08a6`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f86bb855d1fb3fdb2d9955fcc2cb55fe3fca979ff33fcd849c421c72858ddc3`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 5.6 MB (5623046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca339e549500cf7175cdc5923d75c9acdefdc9f96837bb72b64cc30c7b1f667f`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210819114fa8486b611008257be45ee7a832a9544606fff077ee7264c45a0ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5bd0330550a5e01b31cc20769d720c38e130b28cfd2983253995e4851792ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f6c991626fdba5301b56de0d17255f0d5990e44de35dc033d4245630d6f8c`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:5e4cb5bd0125ad60e1ac0a8f7d47512f8d66ca09207481226d24c4f00b637790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:6f15766bd375c2a4e083ea3da0dc17ab9421e9d6ba7670f8e63530b32026e7a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244522827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5f47c24199973add8fb939a5d0a35950e4419f93230949a270c36e56a926e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:39 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Jul 2024 17:48:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Jul 2024 17:49:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Jul 2024 17:49:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:49:57 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:49:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:49:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d3c2b5f2b5ccf41453354651ad302348b4bb8f11b3847f2e01b953fb91723`  
		Last Modified: Wed, 10 Jul 2024 17:51:08 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312388bc1ac3f43c23f278f59000070f2259532bc686a75d8e29e08e05757d8`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af6f92a72eee24d1fa8472fa142a66123b75939684be086fa34c4e58babb99`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e3e604bb86f204c06909e636643b9dd2b2eda44208a213f08f480e59aa08a6`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f86bb855d1fb3fdb2d9955fcc2cb55fe3fca979ff33fcd849c421c72858ddc3`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 5.6 MB (5623046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca339e549500cf7175cdc5923d75c9acdefdc9f96837bb72b64cc30c7b1f667f`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210819114fa8486b611008257be45ee7a832a9544606fff077ee7264c45a0ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5bd0330550a5e01b31cc20769d720c38e130b28cfd2983253995e4851792ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f6c991626fdba5301b56de0d17255f0d5990e44de35dc033d4245630d6f8c`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:8869876f9796173fa30882b1776a971932cbfa343197af9cc17e554711c9fc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:24087a3a56f3542aa76594bdbf60ec2d5cdc5c3a37b147929e036033c5960b34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160417834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009ec0ef5fa05d65e637632d81fc83f95a782f954b38372d3cebde0145807a23`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:50:07 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7842936c7a3b549ce1d7723e685a0b7155324b9d1bd8a48d119d49598e36b827`  
		Last Modified: Wed, 10 Jul 2024 17:51:17 GMT  
		Size: 5.3 MB (5330185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecebd27e858b9c2f81159753b9ca9c3dc356c8a0f424de6b2dc1e4dca4849f1`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af439e567ac5a6e8ac01ebc3821440fa51e60a2e642d7bd711b17d00ccd317bf`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755e229eef1121ec2128f0138ae3b09172f52015cdc841fd00988939387e5334`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7aceea265cfb43d525c62226aed26269770664c45a89a94e9d4873272ae97`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:8869876f9796173fa30882b1776a971932cbfa343197af9cc17e554711c9fc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:24087a3a56f3542aa76594bdbf60ec2d5cdc5c3a37b147929e036033c5960b34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160417834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009ec0ef5fa05d65e637632d81fc83f95a782f954b38372d3cebde0145807a23`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:50:07 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:50:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:50:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7842936c7a3b549ce1d7723e685a0b7155324b9d1bd8a48d119d49598e36b827`  
		Last Modified: Wed, 10 Jul 2024 17:51:17 GMT  
		Size: 5.3 MB (5330185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecebd27e858b9c2f81159753b9ca9c3dc356c8a0f424de6b2dc1e4dca4849f1`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af439e567ac5a6e8ac01ebc3821440fa51e60a2e642d7bd711b17d00ccd317bf`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755e229eef1121ec2128f0138ae3b09172f52015cdc841fd00988939387e5334`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d7aceea265cfb43d525c62226aed26269770664c45a89a94e9d4873272ae97`  
		Last Modified: Wed, 10 Jul 2024 17:51:16 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:5f6579e5c5ce5581238c5c355f11fd26a08704afc59f9b0c675580f908151c66
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
$ docker pull nats@sha256:269f9e82be9fd22403cb06059d4a99c5c02bc34a02de7bff8426a15bbcefc0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcc04348ce21068b1074d07c2797fd62aaa0d7228c3e6573625ac6222c3c369`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Wed, 17 Jul 2024 17:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:33 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d5554985edfae1a5c24b5a220ceb3b81c2512bff0f259d6b858170d6ab093`  
		Last Modified: Wed, 17 Jul 2024 17:50:29 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:5e4cb5bd0125ad60e1ac0a8f7d47512f8d66ca09207481226d24c4f00b637790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:6f15766bd375c2a4e083ea3da0dc17ab9421e9d6ba7670f8e63530b32026e7a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244522827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5f47c24199973add8fb939a5d0a35950e4419f93230949a270c36e56a926e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:39 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Jul 2024 17:48:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Jul 2024 17:49:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Jul 2024 17:49:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:49:57 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:49:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:49:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d3c2b5f2b5ccf41453354651ad302348b4bb8f11b3847f2e01b953fb91723`  
		Last Modified: Wed, 10 Jul 2024 17:51:08 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312388bc1ac3f43c23f278f59000070f2259532bc686a75d8e29e08e05757d8`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af6f92a72eee24d1fa8472fa142a66123b75939684be086fa34c4e58babb99`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e3e604bb86f204c06909e636643b9dd2b2eda44208a213f08f480e59aa08a6`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f86bb855d1fb3fdb2d9955fcc2cb55fe3fca979ff33fcd849c421c72858ddc3`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 5.6 MB (5623046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca339e549500cf7175cdc5923d75c9acdefdc9f96837bb72b64cc30c7b1f667f`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210819114fa8486b611008257be45ee7a832a9544606fff077ee7264c45a0ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5bd0330550a5e01b31cc20769d720c38e130b28cfd2983253995e4851792ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f6c991626fdba5301b56de0d17255f0d5990e44de35dc033d4245630d6f8c`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:5e4cb5bd0125ad60e1ac0a8f7d47512f8d66ca09207481226d24c4f00b637790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:6f15766bd375c2a4e083ea3da0dc17ab9421e9d6ba7670f8e63530b32026e7a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244522827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5f47c24199973add8fb939a5d0a35950e4419f93230949a270c36e56a926e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:39 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Jul 2024 17:47:40 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Jul 2024 17:48:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Jul 2024 17:49:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Jul 2024 17:49:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:49:57 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:49:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:49:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d3c2b5f2b5ccf41453354651ad302348b4bb8f11b3847f2e01b953fb91723`  
		Last Modified: Wed, 10 Jul 2024 17:51:08 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312388bc1ac3f43c23f278f59000070f2259532bc686a75d8e29e08e05757d8`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af6f92a72eee24d1fa8472fa142a66123b75939684be086fa34c4e58babb99`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e3e604bb86f204c06909e636643b9dd2b2eda44208a213f08f480e59aa08a6`  
		Last Modified: Wed, 10 Jul 2024 17:51:07 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f86bb855d1fb3fdb2d9955fcc2cb55fe3fca979ff33fcd849c421c72858ddc3`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 5.6 MB (5623046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca339e549500cf7175cdc5923d75c9acdefdc9f96837bb72b64cc30c7b1f667f`  
		Last Modified: Wed, 10 Jul 2024 17:51:06 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210819114fa8486b611008257be45ee7a832a9544606fff077ee7264c45a0ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5bd0330550a5e01b31cc20769d720c38e130b28cfd2983253995e4851792ce`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f6c991626fdba5301b56de0d17255f0d5990e44de35dc033d4245630d6f8c`  
		Last Modified: Wed, 10 Jul 2024 17:51:05 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:a6b42d3ee450da9f632fcd293a04fb7e57549d9a9fbb6f8ce724b6e7e34c5a27
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
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:ccec9581f7ed13909bde90fc06e201fd3d6b0c6fc9698368f37099ece21e53a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a88ffebe3513b18db6f563ded9d1901b10e5236decf334f81fb65e54aef56f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:49:21 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:49:24 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09cf7cc1e8b2b2c70dbeb895ecdf30b1ed61013e638ce8f6700bf060c78222`  
		Last Modified: Wed, 17 Jul 2024 17:49:51 GMT  
		Size: 5.8 MB (5834889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d52a03044b49dfb62139308d8eba060922fedca8d3025845ab7f17ba6394a4a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be5eb6efff9d6fbaf593f8856ccb80a01fdf5a8871f6dd0d4cdd0c4217403a`  
		Last Modified: Wed, 17 Jul 2024 17:49:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:00d1c17393b176370b64a8be371d51264256e1ecc7bc3ad86b62720170766686
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b199588b907124b95fd7ace8ccdee1be9a5c0c2442167f4f4c4b71472b908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:57:31 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:57:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:57:34 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:57:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec33482ef3aba8e1d1c369a3b4582c37be2ff9da7e7e6bd2fcfea6d70978ca`  
		Last Modified: Wed, 17 Jul 2024 17:58:04 GMT  
		Size: 5.8 MB (5826248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912024ec2c9a01ca04d82db1013c818479a583674f651dbf27671cd5687a1d`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03f0e7b05b2063df230ea2a2b1bcec5258220c05134a1071e59421340645a4`  
		Last Modified: Wed, 17 Jul 2024 17:58:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1de67b0cc8a78750906ab771fe9cbe72d79db0b5c5d2062152c0bc618456b158
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9821715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78496f7d575177ea3f04b2bf88dc72b7d8d8db0cff45fb9083f68b43c47b6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:39:47 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:39:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee585f0df40135708fe4b09e6d54f4cad57ee3f5b3238beb1e33303ba94a5d`  
		Last Modified: Wed, 17 Jul 2024 17:40:20 GMT  
		Size: 5.7 MB (5731941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc35e0bcedd70d820b08e4dcf2d4a346147c090bd1bd524a23719b42d5094a7`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffff6eb58c31d1da15b8cf28829887e13b35e10d98e8582bea0dd50e58d265ed`  
		Last Modified: Wed, 17 Jul 2024 17:40:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:6905eacdd1cd9ef9f2303351270ae379db03b58f375f48b1e7d47d7c3792d4e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8f01b1dedc513af164b1fc1f4a4a3d50039fe3ff5e60b130bbfcd2773cecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:16:44 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:16:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:16:49 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:16:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fbea26874c16662f9f936107a0bf71ac276bd7d66992fcbe22cfb7f3b6a0eb`  
		Last Modified: Wed, 17 Jul 2024 17:17:12 GMT  
		Size: 5.7 MB (5702187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727edb145a1987401ac40f931c96ec53807591a19c6eadf2c912ea30e77c1a6b`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc107e80c46b9a3320bc50acfac3531c241096c43a3fe3cd8d452258f1c339`  
		Last Modified: Wed, 17 Jul 2024 17:17:11 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:61f7086935bb4991b1fe3fbe857fdcbb8e6f70dd4a99c2ec0e5e3a4d275b12c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9488374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c33fb15f0c37a7c00c9fd93b3c84b3d9209bb7ef02f5be08805eb88779c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:42:56 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:42:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:42:59 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861276ee3ad214cdaec615fff5a427569a31121636acd7d19f6818f526c6c9ba`  
		Last Modified: Wed, 17 Jul 2024 17:43:33 GMT  
		Size: 6.0 MB (6025545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166d2cc7c318d2ebe7692f993d3d82770d227cf09019d36106b91b1e803d2a0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6e57e3bd5fb7ff7b9ac1c436af85ba7916eb33ba32c8358846920df851ff0`  
		Last Modified: Wed, 17 Jul 2024 17:43:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:05bf691418146d1c7b171cd06b62eae32f1a5e05c3f80e4842c365849596b248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6054; amd64

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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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

### `nats:latest` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:a32650771db8fc87c317df90aa864710222e28cbe07e095c5bac2f2fd61f1193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:aa07163813de1969072b3da5e8865541fb60b06444321b06714118f14f2e9b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160900542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9605f54704c7f759942dc0fb21aac6ebf83e79ab250b4cec8e0dee246e604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:bdee19eefa3452dc8e8329305c884b0dc5a6096b0944d839de28eb3f7c4aee25 in C:\nats-server.exe 
# Wed, 17 Jul 2024 17:19:02 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:19:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:19:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eceff99048356ba96a76a432e4e9fabf0d519ebdd5df53c9f8cd3ebb1ea42`  
		Last Modified: Wed, 17 Jul 2024 17:20:07 GMT  
		Size: 5.8 MB (5812770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a61bf40f8c243f2efe398cee3f3c66e828af1f64b881414912864af43dc63e`  
		Last Modified: Wed, 17 Jul 2024 17:20:05 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae7f817b7bcfdc4865db4092f748c64d3973e45ed430dc3d60b18ea4714a82`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c126ad89072ec4c17aba7a89bc269be10dc5bfd7872b2d65c3935bae05e54916`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6771a10f9ed6f60a186bfb04e725c63dc40587b724f6933a10d99fbc31906`  
		Last Modified: Wed, 17 Jul 2024 17:20:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:ccb5be55cd6cc353b034a9048ceb3f302ac53afbffa4339377eb82dcfa5023fa
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
$ docker pull nats@sha256:c5e665dcc3dde36f6b7570096532764d0f0a28439acd95fe29580e5531c429bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ce6ec10382a3e98124a45cfa7e77026da925328b919eb9bfb06f97b74883`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Jul 2024 17:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:54f31e2f71860b4d2dd32487d6cb87ca7f2314b08e1965804d728ee8a6cd49af in /nats-server 
# Wed, 17 Jul 2024 17:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 17 Jul 2024 17:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:49:28 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Jul 2024 17:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62a0e6b486eaef085945611ff5808baa9b4e38aaca560d9cd6cb72e04df1ea6a`  
		Last Modified: Wed, 17 Jul 2024 17:50:10 GMT  
		Size: 5.4 MB (5370819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df837d6a50c92d812718022a33b55e92450552f197f8196f69b20a9d08444c`  
		Last Modified: Wed, 17 Jul 2024 17:50:09 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f061588ebb5de876b48871e1f966ba8b4bef2cf0db8b75f25574089b0a998094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:7eda922bb1ae209bc4660056b0ff7b49495b0605ff73eb4c2262ab7a8b0eeb91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245004654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738912394cade4565891e02520fc2f774b86ccd5a71253c34eb54910f4132db5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:44:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:44:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 17 Jul 2024 17:15:49 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:15:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.18/nats-server-v2.10.18-windows-amd64.zip
# Wed, 17 Jul 2024 17:15:51 GMT
ENV NATS_SERVER_SHASUM=191a6cb6f7391005b5f886ae4fb700907dd977149f650febda9ae433701bf547
# Wed, 17 Jul 2024 17:17:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 17 Jul 2024 17:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 17 Jul 2024 17:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 17 Jul 2024 17:18:44 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:18:45 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Jul 2024 17:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a98dcd9daf159f1236926d9dc167c3eae47ced648677935430f397dcc14fd`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e678489989cf390ead87514d51d181acca475028131556cce860fd55db781c`  
		Last Modified: Wed, 10 Jul 2024 17:50:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520d598111d2a7a7cb7ad213059b5ccddddb181966dedddce69d350603102006`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cd6c898bb55a233a05d7609525662606f5fbb9f7112a0ddabed1099995b5`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b039424e43c6748bc489fbcfd548d0e6e7f0c607108900d6d76651a52bbbe4`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e81cadf9e5412a7a4161ce0cb84afece08caf8b5bd018423f6371117ef7320`  
		Last Modified: Wed, 17 Jul 2024 17:19:52 GMT  
		Size: 455.8 KB (455782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273eb88a675bef59c2e38ce9465a2951f87c71136189d92a228c3acc42f2fe9`  
		Last Modified: Wed, 17 Jul 2024 17:19:51 GMT  
		Size: 6.1 MB (6106156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc97e0d2a7f0f3c3e7566b25bd6897c090e995c2a94ee750829a2bad448a57e`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67b511a8e58c7aef493a941a57e25e16b67a25a8e9122abd11deefedaf8019`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca037178e75590812f7a9dc35a15c94fa43a26086932482b8c33a75e43ec2a`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47433c5a608e3bcaf6011381a20d9b74c62d644a6dab5d652dd1e2dadfb75e31`  
		Last Modified: Wed, 17 Jul 2024 17:19:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
