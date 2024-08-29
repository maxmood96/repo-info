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
-	[`nats:2.10.20`](#nats21020)
-	[`nats:2.10.20-alpine`](#nats21020-alpine)
-	[`nats:2.10.20-alpine3.20`](#nats21020-alpine320)
-	[`nats:2.10.20-linux`](#nats21020-linux)
-	[`nats:2.10.20-nanoserver`](#nats21020-nanoserver)
-	[`nats:2.10.20-nanoserver-1809`](#nats21020-nanoserver-1809)
-	[`nats:2.10.20-scratch`](#nats21020-scratch)
-	[`nats:2.10.20-windowsservercore`](#nats21020-windowsservercore)
-	[`nats:2.10.20-windowsservercore-1809`](#nats21020-windowsservercore-1809)
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
$ docker pull nats@sha256:579b54f01eeb7bfe01d866649c7339cd6ab8f368cd9bf349dfca817f9af5921d
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:579b54f01eeb7bfe01d866649c7339cd6ab8f368cd9bf349dfca817f9af5921d
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20`

```console
$ docker pull nats@sha256:ac6d6cf0a860e9031ac096bb7c6604576cb2090e5a41e2b411619ae4f7fc943a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10.20` - linux; amd64

```console
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-alpine`

```console
$ docker pull nats@sha256:edc7f533ad45d961ff68a03a403ea6b6311bb73f2b2fe24ef440fb47eb5def69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `nats:2.10.20-alpine` - linux; amd64

```console
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-alpine3.20`

```console
$ docker pull nats@sha256:edc7f533ad45d961ff68a03a403ea6b6311bb73f2b2fe24ef440fb47eb5def69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `nats:2.10.20-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-linux`

```console
$ docker pull nats@sha256:2b45381b32e3d628749da64af8d1fdd6b73cb7cd54be29fabac457d7efd77f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `nats:2.10.20-linux` - linux; amd64

```console
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-nanoserver`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10.20-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-nanoserver-1809`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10.20-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-scratch`

```console
$ docker pull nats@sha256:2b45381b32e3d628749da64af8d1fdd6b73cb7cd54be29fabac457d7efd77f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `nats:2.10.20-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-windowsservercore`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10.20-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-windowsservercore-1809`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:2.10.20-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:14ee7d63234c0f4556e5c96e5992c2cb439dd2398369df096f791e8ddc6627b0
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
$ docker pull nats@sha256:c5be4a27b87aae01a6d0153ab4436604ae3362b4ff8040f2ef236d7a46470384
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82722cb9e66783f9656aacac235a74da901230f438392a6cb5659331af575a6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Tue, 27 Aug 2024 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:35 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f280fcc4645c52999454803efe2e23f7aa2c94ef1c79240cc8cd5aba7245110`  
		Last Modified: Tue, 27 Aug 2024 23:50:30 GMT  
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
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:db8fb5cd2dae3a949549ebcdbadc71bbf18e87b02e1d8640491fe8799c2e993c
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
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:b387e47e02265dffb0c609eb3ab1a3055ec59ff20e6c6c596e711d252ce9e57c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefc873213ad32b63e8b49677fa48fc4e166acbdabcf341ce1406f204f4a096`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:49:24 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:49:27 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47500846360fe03ad88bcc976feb1e1fd0d1215c020b336774c38e457c5b713`  
		Last Modified: Tue, 27 Aug 2024 23:49:54 GMT  
		Size: 5.9 MB (5870228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88b83c9262b0a638afb560f61fddf659a2c7d2570379b9d30be976318e5d183`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34604c36acf7691b566e01431f32fec53aff846cf5253efa96560ebfd9c32c9f`  
		Last Modified: Tue, 27 Aug 2024 23:49:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:51229051c2c5a033aca3e881286e4897fbcc985ee19925d0da07903e5cd8a4f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb81cc02113f4a78d874705b74c0074fe1382b7ccad4cfeb68e291c6622fb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Wed, 28 Aug 2024 00:04:41 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:04:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 28 Aug 2024 00:04:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 28 Aug 2024 00:04:44 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 00:04:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a221e57745a16b17d3976d6826606c4cd2f7361322552bd9c6665d380d4f6`  
		Last Modified: Wed, 28 Aug 2024 00:05:21 GMT  
		Size: 5.9 MB (5860288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c1be5707558523cc500077061664b6c1c74eedee8ee39ab00b0b8ae8ea9d9`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64b977849fe196194f9a3d86c8b3c4718ba97158b24f9adf2caef6ab2f2067`  
		Last Modified: Wed, 28 Aug 2024 00:05:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09a5427970ec97e02f4428bae14a7ee36b255e0fddfc4bb76695978c6206eb36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed2259969df730c4eb7710cf4ebd750bb0b282850ecfdbd48397ccf0153615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:39:45 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:39:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:39:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4317496a97c839fb8a8704304b30ebe4d7a5430748de2e911059f4e8b697d4`  
		Last Modified: Tue, 27 Aug 2024 23:40:19 GMT  
		Size: 5.8 MB (5767048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f360094e98d86ada402acd306bc760eae539480602a0a6c0881e1f8f3c9938`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144041ca200fd85f03e234c7e0613430b32ccbc442f30c8efe04bdc0ead46f05`  
		Last Modified: Tue, 27 Aug 2024 23:40:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:6abcbeb8e11bbcfcb14d866dcf3cbc2b73ab6e9deba999d63143c2e5abc45a54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45535fd3c03ae3fdfb6d37b1db4553b4fcd2e6f280c9d7d9b4d1b7310a423d84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:42:59 GMT
ENV NATS_SERVER=2.10.19
# Tue, 27 Aug 2024 23:43:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='41e8d3fb78e255f1303d856e590a96a174edee02277edc72d58f882958f6449f' ;; 		armhf) natsArch='arm6'; sha256='3c2fbdda83c9ff25e90abcca5b8c156b2c29fc9a8cab198626a80e9843ea5bdd' ;; 		armv7) natsArch='arm7'; sha256='271b055c2bdb86dcc0de49001dce320f1fbf76949b5f3a8d730985d864144f88' ;; 		x86_64) natsArch='amd64'; sha256='e64e6628795d26fc9c9b15b3894757cde3cefb85cb4a12c23001c997abd276dc' ;; 		x86) natsArch='386'; sha256='bcf3d343e8877139c8af0713c380d073f6c0a773def1db75c81a8fdbe96a4e92' ;; 		s390x) natsArch='s390x'; sha256='e7317aa5ea10047f6eb20e2dd6b5a305156b42928663a865be5f6f35bac56880' ;; 		ppc64le) natsArch='ppc64le'; sha256='effd70f1322344c6a5261c5ccf6ccc6b67b77a6da23133d498628ed530ee8a62' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 27 Aug 2024 23:43:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 27 Aug 2024 23:43:02 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:43:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12363dad404a4f097f349227dd46692d255912bc587a67a043eb5d7106be638b`  
		Last Modified: Tue, 27 Aug 2024 23:43:38 GMT  
		Size: 6.1 MB (6061862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba5e955b1253a7283501078d8a87edd80c706317952a13b6490165e1757acf`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82524550ffe9d6d9e83e43cc9d7fd761cf157e48a76d2ba68a53b6e498f954b2`  
		Last Modified: Tue, 27 Aug 2024 23:43:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:579b54f01eeb7bfe01d866649c7339cd6ab8f368cd9bf349dfca817f9af5921d
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:717994507e7a8e1e9f7f2c34764d94a7f1d58edf2c7e5ad835f6b4e6805e1f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f586322fc563105a2955fc67db5ec12ff9a2a58e0ab7427511f8dbe5826265a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160945826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a984f12908ca9c332bb69c54425f4396c23e40808ef03e63436711d13da7b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:48:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 29 Aug 2024 22:18:27 GMT
RUN cmd /S /C #(nop) COPY file:c54cab0bcb90d215c31a13829d36e0dab6494e8460be22ca70c4e415081fe7b0 in C:\nats-server.exe 
# Thu, 29 Aug 2024 22:18:28 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:31 GMT
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
	-	`sha256:0606cf6d38af9f3a7180900cfa685bd7c903a41b3dc21086986a1b4b04df4c50`  
		Last Modified: Thu, 29 Aug 2024 22:19:33 GMT  
		Size: 5.9 MB (5856226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c3ff1b612015afeb0c93544b3a92ca6c2c762b6fa6ffa956fd914c69eda429`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e5875c9eed7e1830bc242a622d077f9d7b2bfa4b520904fcdb4f9555edec8`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e73b970ff491155beccf798936be0ac69210fb493680ee924f24412ea16d838`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e738aab06f4c4db9578827ae0e003211d49453372282da16ca9e4a88c1838b`  
		Last Modified: Thu, 29 Aug 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:94e1eaf45c054dbc930035e76b89e85eab6c266c17534b0d063ed8e3c032bc60
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
$ docker pull nats@sha256:26f9940ea550f1d389e8d5260fe185353829e6814d8805ee2541fb2b53d634e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22356c9f54ceb0ddd41c5cfea9fb5c89b48993e9accd9781985a9a4418fb50f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:20:17 GMT
COPY file:4d4c6bbcd202b388b8eff8cce9964b31d0997fc62cdae2adadfaa86026571621 in /nats-server 
# Thu, 29 Aug 2024 22:20:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:20:18 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:20:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:083c87973157a09ec07f0dd6dd5110ba9e1a57c6d647dc61514fb59cbb42da4a`  
		Last Modified: Thu, 29 Aug 2024 22:21:04 GMT  
		Size: 5.7 MB (5739284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f59b5522908b0b9758561c85eefef18f863ae2dd35ca41414aca4f16707c3b`  
		Last Modified: Thu, 29 Aug 2024 22:21:03 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:176b95c4062fd85702f49bbc78dff4b57edd5790245aa0e1c699cbbc49a35aa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b022c686673449d9d2205da1b289ea73535dd7a7b89f741d7c074d73c5dee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Aug 2024 23:49:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:0f3043e78404aeee0c1926e22dfa81bcfe207f7abb098a6fdd2d33dcc6b4a1d9 in /nats-server 
# Tue, 27 Aug 2024 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:49:31 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:49:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:686fb205a38e15909f87592b273ac6008601d1223818c700942acbc8e4f54529`  
		Last Modified: Tue, 27 Aug 2024 23:50:13 GMT  
		Size: 5.4 MB (5404058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e337c2b8e2c2d07a6e385a3e6583a3cc101056c653fb45ba772eb41e7c9b8`  
		Last Modified: Tue, 27 Aug 2024 23:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61ba665ac13ca66df96588019703687bffc077d701860712a3aa0a93f9f4facd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7956b2f0b8e4fb51c8ee977b7ce4873427d0c5b884e9ebe8bbd50b43c9c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:c8ee0b15c325c5088e57b5e5492ee2c01695495a2b757a951121446d1ffd90b7 in /nats-server 
# Wed, 28 Aug 2024 00:04:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 28 Aug 2024 00:04:53 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:04:53 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Aug 2024 00:04:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d6b0c5ddf29ba3a84a0793d5bfaeb7f563047168e1c12443dcdd930e32bd872`  
		Last Modified: Wed, 28 Aug 2024 00:05:39 GMT  
		Size: 5.4 MB (5397911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5683077b4071b5151ded7b9fcd9d271a5fc856551c6b94cc46b82d947dbb63fb`  
		Last Modified: Wed, 28 Aug 2024 00:05:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:61322136f4d8a9232e2cdb8ae5b736415bc201b07500855ee8aa49afeaaf326d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0dff002fd8334800d3cfbe204ba000d8b699d15c4c0989c77789199386b67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:39:53 GMT
COPY file:277590be7861f3cf15baf11372aae16f964b193d0d3a607e7ecc03b1cca74b9a in /nats-server 
# Tue, 27 Aug 2024 23:39:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:39:54 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1536caa8c610091658759b64913e3c0effbcb91887a17183434a4d54e3b5d937`  
		Last Modified: Tue, 27 Aug 2024 23:40:37 GMT  
		Size: 5.3 MB (5303255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a6360be093c9b01286accbc4d319e4251d1b7d9c88aae3733850c2b87219e`  
		Last Modified: Tue, 27 Aug 2024 23:40:36 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ea88a24f5ac53d55afe5c5c38d743675b1d3fa668aa486c7e84697d66f759bc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e301c2dbf05db489d319a3743b1dc16d5d29a4b24c2b2bd5aff4a371d084304`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:718222216801d1c2996467e7100b9f56c3c29518d4a649f841aec107d9d59201 in /nats-server 
# Thu, 29 Aug 2024 22:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:18:10 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:18:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1d29609fe0a3017982bc88b4bba8c874dd1ed1dfd9129ad75b7379f1deb7a9b`  
		Last Modified: Thu, 29 Aug 2024 22:18:50 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c04e39e857f0741e987fd5be70bc340f797420da1de1fb5495945dd3ca174a`  
		Last Modified: Thu, 29 Aug 2024 22:18:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:c87088ebf4e79060a373a6c1f1fc60e7fecb9a41eb49637589e8e5a5c266b5f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661336d758f38c24ccb698eeade837b3d86090ebf7a7b1e1ad8c73ab4f52ffc2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:52551ec29ba6335f03c9bd2a9a5d4864865380a166065e08075334bcdfee5e35 in /nats-server 
# Tue, 27 Aug 2024 23:43:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 27 Aug 2024 23:43:11 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Aug 2024 23:43:11 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Aug 2024 23:43:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ddb84faf584ab5adad5c027a3864bb7818cff4333a74f7aa7192b3338f0cf6c`  
		Last Modified: Tue, 27 Aug 2024 23:43:49 GMT  
		Size: 5.6 MB (5598854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4bd06b12ff8a1a8df4ed6516a6a634fc3428de1ca1bd509a23e845b3b67004`  
		Last Modified: Tue, 27 Aug 2024 23:43:48 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:cb6328be8b110a77e133cf6563ecf60a3fb05f2935bc0e96f8a5dd2f7e8b48e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:9fad6c4863943446d592590e79cb11ff553e6fc191778720110f756df33657e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251857590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be6364da5c3d0e9e048ada69b72a0838e7b1008175e1ca31fda37c7638df8aa`
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
# Thu, 29 Aug 2024 22:14:58 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.20/nats-server-v2.10.20-windows-amd64.zip
# Thu, 29 Aug 2024 22:15:00 GMT
ENV NATS_SERVER_SHASUM=8c95a904e0c2c7413d3671fca3d41cbce6d71af797362c394a24bbb15f95dc7f
# Thu, 29 Aug 2024 22:16:15 GMT
RUN Set-PSDebug -Trace 2
# Thu, 29 Aug 2024 22:18:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 29 Aug 2024 22:18:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 29 Aug 2024 22:18:14 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 29 Aug 2024 22:18:16 GMT
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
	-	`sha256:941f3a5cc11d8a7fbfbd4e829b3c7a9ae76dee2abaae9d6e868e1748486f3368`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca51263da3a2de900934ec683721597afdd2d2425a83a5c9ab3d3c92718c7c`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011007d5fc07497ebd202455eda52967d15dc7cd82ddaaaea4a3e065ac0dc87`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073b2d25f44c8c42efcd2187bd5b55ab5b79fa77d5fafddb85410f2814fd691`  
		Last Modified: Thu, 29 Aug 2024 22:19:19 GMT  
		Size: 471.9 KB (471885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0492ad69b1e8bdd0d23994a4a3a34c734c05dee99e4b5ceee2c7469095dc2`  
		Last Modified: Thu, 29 Aug 2024 22:19:18 GMT  
		Size: 6.2 MB (6169168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970f9ed7f958aecdcd2ceefe686404de25c77f9c9ac0e2bf106b9e5e45ec23b3`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10dad646d9e6377922ecc8e09974aa0a75d43fe346d96b58b8fa8e743c2513`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14dda7874c31357043651dbb5a77d45efef0ad13d61954d861527697a56367`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b340e1c0e1043e7c180bbea7fb252f25d08b982896a61938d5484aeba71de9`  
		Last Modified: Thu, 29 Aug 2024 22:19:17 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
