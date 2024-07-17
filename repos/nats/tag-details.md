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
$ docker pull nats@sha256:a36cd84b52aca78d82909c43ca04331da74cfc0735359c7d74b9b67aa4349a33
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:a36cd84b52aca78d82909c43ca04331da74cfc0735359c7d74b9b67aa4349a33
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:722ca1a1d4466b5344918a44a4ad0d6ced6fdacf7f1f1dadea2a318745a7e6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
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
$ docker pull nats@sha256:0dc35a6261c4c8aa6153171daeadeffd0007ed4f036cba6221ec49bd356b8267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

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

## `nats:2.10.18-alpine3.20`

```console
$ docker pull nats@sha256:0dc35a6261c4c8aa6153171daeadeffd0007ed4f036cba6221ec49bd356b8267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

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

## `nats:2.10.18-linux`

```console
$ docker pull nats@sha256:79272d4ac8508f56c8643b2e08a44ba04197566de3e07179394b1996c74ee4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

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
$ docker pull nats@sha256:79272d4ac8508f56c8643b2e08a44ba04197566de3e07179394b1996c74ee4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:5cbb3b0484ce4af56fbea10165ad04acb8d41f537282510a938c1ee5adcb6f6f
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
$ docker pull nats@sha256:9befa2d1ef16ddc9bf5e455fd38d04ce347c691ed56aeca4b28731282c9a23d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f3630876f79747242ce81b2afabf049dea2462061be16e722763723389d59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 28 Jun 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c68a0dfeb5f0da031c1ce62973e6f5fafbed7d64584be76e31b33afadff46`  
		Last Modified: Fri, 28 Jun 2024 00:50:34 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:2c1c661ea4174758a9d9d141ee3a4650948cb0c1da04e151544f9cac1aeb67be
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
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
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

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:a36cd84b52aca78d82909c43ca04331da74cfc0735359c7d74b9b67aa4349a33
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3dbd810795c8c22870bd3a2c07d75c24525136c3e73b6aaeaf1cb31ac0d2170b
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
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
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
