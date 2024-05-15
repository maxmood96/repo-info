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
-	[`nats:2.10.14`](#nats21014)
-	[`nats:2.10.14-alpine`](#nats21014-alpine)
-	[`nats:2.10.14-alpine3.19`](#nats21014-alpine319)
-	[`nats:2.10.14-linux`](#nats21014-linux)
-	[`nats:2.10.14-nanoserver`](#nats21014-nanoserver)
-	[`nats:2.10.14-nanoserver-1809`](#nats21014-nanoserver-1809)
-	[`nats:2.10.14-scratch`](#nats21014-scratch)
-	[`nats:2.10.14-windowsservercore`](#nats21014-windowsservercore)
-	[`nats:2.10.14-windowsservercore-1809`](#nats21014-windowsservercore-1809)
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
$ docker pull nats@sha256:1f3fcccbc2116701ae0d648bfbb3a0dc285edd4bac2ba8c99fff819588ffc204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:1f3fcccbc2116701ae0d648bfbb3a0dc285edd4bac2ba8c99fff819588ffc204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14`

```console
$ docker pull nats@sha256:1f3fcccbc2116701ae0d648bfbb3a0dc285edd4bac2ba8c99fff819588ffc204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.14` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-alpine`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.14-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-alpine3.19`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.14-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-linux`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.14-linux` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-nanoserver`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.14-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-nanoserver-1809`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.14-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-scratch`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.14-scratch` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-windowsservercore`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.14-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14-windowsservercore-1809`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.10.14-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
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
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
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
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
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
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
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
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
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
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
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
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
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
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
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
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
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
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
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
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
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
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
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
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
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
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
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
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
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
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
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
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:8b8699adecfb4e2088dc8cc3dbd27fbdeb02a6d9a8cfc3f94eb134a5cfb27085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:5caa448ed8d0d2681eccfda619261ba7fed209e3192080f5c22afdf65c5a7985
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476e3e4260dc494484d8f4202d52f0ae5ff49dbea1c915fcbf7056ac4917158`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:12:43 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6907cb5ae64d5580cc2ed0c53877b5a15073904eb506586822016671ca762`  
		Last Modified: Wed, 15 May 2024 21:13:59 GMT  
		Size: 5.3 MB (5330226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cec024febaaea2c85546b54fb6fd50962237c51b4e58a0b02a2256064133da`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5015bfc52f47ca9a764991cd8418e81e26d703a8f2236ec898e3c6cb198577`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2480d004d8c19f4e5ee9979ad207627882d4aa001160082a0242da6ce84dc5`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69389d566bdac0778f7de71a98be01137b5e20527e8561831e8345143bc73d`  
		Last Modified: Wed, 15 May 2024 21:13:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:d105a2aec5d7607b2d64b7e727bb299d6639906b90f65c62aec1c023646fb629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:d6c8ef52baefbd23d260c0968de8a3a9e623c5a1e6c1c084fc4cc9c4bd083955
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc18a9a5bd3a99e5270cd5ccbb602d851b0d82af6fc71a20f0f9e988882048`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:09:07 GMT
ENV NATS_SERVER=2.9.25
# Wed, 15 May 2024 21:09:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 15 May 2024 21:09:09 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 15 May 2024 21:10:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:12:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:12:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:12:20 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:12:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:12:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ee38c395afa6a56d89d2fb6a4e4416a29532867ac749ed891d8afbcda1135`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849d3d89dda77cca52a136f7b2efd5d49db6a15023779c247271b88e617af134`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bf4363371aaf97d2f904389bb10eaa3084ae31144835f977ff70ff65cbfa8`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29960b46711d8942c7067c001f2cf2da2e307d07df0496e770982e7a94dd1885`  
		Last Modified: Wed, 15 May 2024 21:13:48 GMT  
		Size: 432.5 KB (432533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b49209267b4fe2543a0f5fa467f5ca0fa4d48b310dd00a04976d3ca886bc8f`  
		Last Modified: Wed, 15 May 2024 21:13:47 GMT  
		Size: 5.6 MB (5602269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67580450fcb49521ca804f4b54bd2bd07ebc4f3263724a69998c832ae9983d9e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c707e65fefffaaeb1d096da9ef99da0eb845614c50f044b8352cd2ae8534b39e`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97529e380ed09b82c2db2acc2e2135a082f3dfc94d51d32058a554fa0fe35067`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a52fda9fb0314e5eb96e601bc6d393b2e5d480a135c2ffb1de54122fb9e5fee`  
		Last Modified: Wed, 15 May 2024 21:13:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:1f3fcccbc2116701ae0d648bfbb3a0dc285edd4bac2ba8c99fff819588ffc204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5820; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:80753d55dfa855a50efaca931a797c9104bce528493456979a4c47dc80a7eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:75d9103cf358e2209f4fbf0be12e236175c87b567abda5fde828b839d5e84d10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160618176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92ec12d81150804963da23a12ad0595fa592a6904c8e3ca9b60804c59a1121b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:08:57 GMT
RUN cmd /S /C #(nop) COPY file:d87795d159e46999757150e2d8f7e66e8f209e1e618883dfa828c7749f3fafe0 in C:\nats-server.exe 
# Wed, 15 May 2024 21:08:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:09:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1637dcb2470f1d54b881a40c8993f897be944817c37077b317224d435d67057`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 5.7 MB (5670375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970d7c03c956fb3c5333444f7cca193b02782f2238411ffe9faf753b04dcd200`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab41423dfe7eb3bf2521227ef1a256cc4aed1597bb62d8345f7352dce3d89f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ae35e0e5e0e212be27ef601786fb362bc363cdec4316af477fa8fd1fcec6f`  
		Last Modified: Wed, 15 May 2024 21:13:32 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03a058f91787d77a6df75cc4176699cf0adb6a0ccb55a6e55c8b190d213f66`  
		Last Modified: Wed, 15 May 2024 21:13:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0f83e2cbdbe9ab6b8dd442a8fbf8eacb86e41e388dd72370392b564797662cd4
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
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:00c6ae4bb08c7b1f04960139200f18c89faee4e44642b161fbfc44bc8f68623f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf707781cab6de8d588aac657d8decf86888d7df77b2cb2ce8b15325e40729`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2a3877105d78e512cee0e7298a413f32e6ca9a7194c6f5c16a23b9fe252554f9 in /nats-server 
# Fri, 12 Apr 2024 06:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 06:31:44 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:31:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 06:31:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a3b6b94ef6bf5a1dd267f013016e0e1a9888da747b9031ecd579f5a63e4cfff`  
		Last Modified: Fri, 12 Apr 2024 06:33:18 GMT  
		Size: 5.4 MB (5439305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c0ca3c9bb78529c620f6d5ee7aa1741824e2ed5f5cb071933896ad3c71f7a`  
		Last Modified: Fri, 12 Apr 2024 06:33:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:80500d52ffd163342d22c5a24c293cd43b391e0c6b6667b09625f7f603ad61f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats@sha256:1ecff4e21ba566067ad0892bc98601a0431fb9dc5c48edf3e803dc5ef635c10b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186101125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a24b988095ed919accd0ccfa77a8824a1a9ea51ebc50a266330be0bda4892b6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:05:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:05:13 GMT
ENV NATS_SERVER=2.10.14
# Wed, 15 May 2024 21:05:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.14/nats-server-v2.10.14-windows-amd64.zip
# Wed, 15 May 2024 21:05:15 GMT
ENV NATS_SERVER_SHASUM=ee799a0cdf79a631749dd8603186c09e2502e5cfde984552e461b89a23fb6551
# Wed, 15 May 2024 21:06:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 May 2024 21:08:32 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 15 May 2024 21:08:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 15 May 2024 21:08:34 GMT
EXPOSE 4222 6222 8222
# Wed, 15 May 2024 21:08:34 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 May 2024 21:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7274f776737e98439583e21fd0c4ff8dedfa0009226d44af30e91a144f1d44b`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc0e64d2024463ed60d3672fe6067839e3b23d912046685d28053bccb8997`  
		Last Modified: Wed, 15 May 2024 21:13:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38941cbdefb23bbe27e9f2ccdf4b05e302deb1a09558ea9e622760957de74d6c`  
		Last Modified: Wed, 15 May 2024 21:13:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe78d56e0475c5cef611b8ce783fb0bc3ba51c1a345ba9730f9102a144678e`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c982c6716f24f161b637f15214df04980e724081b46594f692a60d9c480ef0`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b54a7e6380caed810d2f298b3171402f4f5d4f49875aa38971155e95b0b524`  
		Last Modified: Wed, 15 May 2024 21:13:17 GMT  
		Size: 432.1 KB (432119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0ef9975d8140e1bad2c0e7300f1aa4a40647eba3a815b369d70ca9e38e36b`  
		Last Modified: Wed, 15 May 2024 21:13:16 GMT  
		Size: 5.9 MB (5944370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ebdf4fdf87965526e431a7257e01e41530320b995cf899e036d91e35bed8ec`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 2.0 KB (1959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd05d69338cd6e6a02ad6e45879fcb3c1385190c6f4ce310a183b3bd4e6f2a1`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929f087e9d7ae087b9134d7cf6cf68dfa5fe0d520757400d420c4baaaf4366f`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba0b330e4d8d3d8c56c3da010cfed1faf161ae032bf6efdaa1e4db590c841a`  
		Last Modified: Wed, 15 May 2024 21:13:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
