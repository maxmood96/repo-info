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
$ docker pull nats@sha256:2a236a3a130c9ec11d16a735fdc464fa8088cb222ecc5ababb2a02c4bac83050
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:2a236a3a130c9ec11d16a735fdc464fa8088cb222ecc5ababb2a02c4bac83050
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:2a236a3a130c9ec11d16a735fdc464fa8088cb222ecc5ababb2a02c4bac83050
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

### `nats:2.10.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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

### `nats:2.10.20` - linux; s390x

```console
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
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
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

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

### `nats:2.10.20-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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

### `nats:2.10.20-alpine` - linux; s390x

```console
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-alpine3.20`

```console
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

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

### `nats:2.10.20-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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

### `nats:2.10.20-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.20-linux`

```console
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

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

### `nats:2.10.20-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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

### `nats:2.10.20-linux` - linux; s390x

```console
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
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
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

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

### `nats:2.10.20-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.20-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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

### `nats:2.10.20-scratch` - linux; s390x

```console
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:fb93a513dc7fcb74194f9f21de8b53feb4bff307318674c2a775aefc641e805a
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
$ docker pull nats@sha256:debabd4dcd8eda85e33c8a2fc830e4cc7a85108df77ef420d33da63dce69cbab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554aac3cbf80265488767a155fbdbbc7b999d47207bbfa7e7b553cb89423b88c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:33 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Thu, 29 Aug 2024 22:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09f29cd977f65dac6d44f61c6123f31fd5fd854abebd407b82263ea4dcbc13`  
		Last Modified: Thu, 29 Aug 2024 22:50:28 GMT  
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
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
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
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:2a236a3a130c9ec11d16a735fdc464fa8088cb222ecc5ababb2a02c4bac83050
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3308e837eead4b0aeac084332353153bbfd197a9db3ef966c6af71bf963ab8ce
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
$ docker pull nats@sha256:5265b7eb8e896b11f016120970ec153e54a50b53b8daaa104ad6e52fce6bf51e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a81364bb643c349002a48767b0500fe28dcf9c585541268f41db79f98fb2f3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 29 Aug 2024 22:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:ac658fb12bcdb7cd40b3d3097ffcfa78f50d46d96774dc02c9d195773d7e52ba in /nats-server 
# Thu, 29 Aug 2024 22:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:49:29 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c41b4b2468a159241e30133cd5adbf7c2191d7b5b854b67bfa47620944ceccd9`  
		Last Modified: Thu, 29 Aug 2024 22:50:10 GMT  
		Size: 5.4 MB (5404086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74ec7b59210fbd3d1a3a5b7650e4de27cbed56a45d741377042ffcd0b60bcb`  
		Last Modified: Thu, 29 Aug 2024 22:50:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:19c0572ce33bf9f915b08f320469e20af05afa2381ad84ed62fccce39e19a58f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70c53db195a414d8b4da69a9a9a79b66e2b22f6e1228978376218ce3853c088`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:74a10207a3902ee396bbb792050b9696deba77249109c95ab9371918b138a9ff in /nats-server 
# Thu, 29 Aug 2024 22:58:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:58:38 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:58:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6531d64beb656b90d0588ca1e9ee5baa9b31c60c43b92a162e8650afc24e7066`  
		Last Modified: Thu, 29 Aug 2024 22:59:21 GMT  
		Size: 5.4 MB (5397937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a539f2c989b9dd07de8fc0804fdc3e205851c58cca1876c944bb5ecd5e92b`  
		Last Modified: Thu, 29 Aug 2024 22:59:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ba7822e542a94faf6af1dcec9a916b16e1b1263a9a2ba6402c48501bd416e119
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5303788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4baeefffc6b16fee272be8679dcdb682415879b6e683a8bbf5a6f53d0ee676`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:c5d4b3d47c26488975afc541176b56cf7c6ccd7f3e5d0200f303d12268a852eb in /nats-server 
# Thu, 29 Aug 2024 22:40:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:40:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:40:03 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:40:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:09bddb13d9e64aaa6ab3394fe0d1b088ecfd0b7270b519276a9ecf02865cdadf`  
		Last Modified: Thu, 29 Aug 2024 22:40:43 GMT  
		Size: 5.3 MB (5303280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f745d4d198c9120853c8182bbccae4912dd657b26c7d5d1c25a1ae37ca143f6`  
		Last Modified: Thu, 29 Aug 2024 22:40:42 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:66094b9e4c2415278e45d8310a46d4173bc4e7464e57ed9b4e0e2c84032ca0d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb71815fbcdc0c9c8a6fa7b5a343c44b57ba690102e20f670496d00c280ba6d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:03c3fc08b74c712c3e71bd1c81d9242c4307ba294e3b35b6e2299d163dcbe7dc in /nats-server 
# Thu, 29 Aug 2024 22:43:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 29 Aug 2024 22:43:09 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:09 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 29 Aug 2024 22:43:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2e62649b495d16f1d94e1bf73a6fe201307f62a2f5a8d5d462108462cbe0ad05`  
		Last Modified: Thu, 29 Aug 2024 22:43:47 GMT  
		Size: 5.6 MB (5598951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdc7b959a53c76211ac1612f90cf81dd154ce2e9d544d0d214d5310e6da40a`  
		Last Modified: Thu, 29 Aug 2024 22:43:46 GMT  
		Size: 508.0 B  
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
