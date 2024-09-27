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
-	[`nats:2.10.21`](#nats21021)
-	[`nats:2.10.21-alpine`](#nats21021-alpine)
-	[`nats:2.10.21-alpine3.20`](#nats21021-alpine320)
-	[`nats:2.10.21-linux`](#nats21021-linux)
-	[`nats:2.10.21-nanoserver`](#nats21021-nanoserver)
-	[`nats:2.10.21-nanoserver-1809`](#nats21021-nanoserver-1809)
-	[`nats:2.10.21-scratch`](#nats21021-scratch)
-	[`nats:2.10.21-windowsservercore`](#nats21021-windowsservercore)
-	[`nats:2.10.21-windowsservercore-1809`](#nats21021-windowsservercore-1809)
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
$ docker pull nats@sha256:483da837e851f02d9aad064d13993ba0b48c24226a5c7eaea46cb76f39aadc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6293; amd64

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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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

### `nats:2` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:483da837e851f02d9aad064d13993ba0b48c24226a5c7eaea46cb76f39aadc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6293; amd64

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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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

### `nats:2.10` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21`

```console
$ docker pull nats@sha256:26097bc27dca6ab9ea68ed1fc081fe22e35514231ea549238239b8fe59495f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.21` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-alpine`

```console
$ docker pull nats@sha256:4ceb5dc7518cb4ddd8b44b0245b6912826d9bcabc5e44e5ebe195ea755e9d7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.10.21-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-alpine3.20`

```console
$ docker pull nats@sha256:4ceb5dc7518cb4ddd8b44b0245b6912826d9bcabc5e44e5ebe195ea755e9d7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.10.21-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-linux`

```console
$ docker pull nats@sha256:ba85d5e71ab14ab66f40fa7c7c7361f9d624f0321110ee8af8fcea68ceee13e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.10.21-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-nanoserver`

```console
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10.21-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-nanoserver-1809`

```console
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10.21-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-scratch`

```console
$ docker pull nats@sha256:ba85d5e71ab14ab66f40fa7c7c7361f9d624f0321110ee8af8fcea68ceee13e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `nats:2.10.21-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-windowsservercore`

```console
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10.21-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.21-windowsservercore-1809`

```console
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:2.10.21-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:33777315578510f72f38b41dbc161aac0cc97bf2fc0aa1cf32d82c8e3d478339
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
$ docker pull nats@sha256:9ae2285ba8718dd7a23b515251e257af3bb5890fd1e54949cc7595c5ccf8aad8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9818901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64317dc1b9a7fc32bc1dca050e6c4274c3a356b45f1755250cc6a788a28f78e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:22:50 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:22:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:22:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:22:52 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:22:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4774d0b8cb6dbff819af188d430877382e759fa3005dbff2f55dfaea6c34059`  
		Last Modified: Sat, 07 Sep 2024 02:23:31 GMT  
		Size: 6.2 MB (6194121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bed436f780c43e6a8f2c266b232dd6a612ec147a4655ee5d7f91c4e0cf9ac`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ced4730132d0cbfaf5d958bd86cffc5d588e3da8d9f0e6ef20ce49da0e390`  
		Last Modified: Sat, 07 Sep 2024 02:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:6197ceddf55573aac85eae50db38b41af6ade12d77c408fde9cbe0d2f7017d14
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b93809924197a7d0e2586978c3906facb84b7ac8ac828f648b78ee8adbcb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:27:41 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:27:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:27:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:27:44 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:27:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa58d86bf37d4adebd0a0101d006a50158f88e1707a0573d6507d5428b75695`  
		Last Modified: Fri, 06 Sep 2024 22:28:12 GMT  
		Size: 5.9 MB (5853786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfc06514b18547411ab07edb4487a4c9a6dc8951b298c89279d56dd56187482`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4515eb8c3a866a98296306a598a2da1b45568189df32f88ce20e0b41f5741b6`  
		Last Modified: Fri, 06 Sep 2024 22:28:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dfe93338b4f0a8113d2c92a1ea23b9680b732602f91b4a65479ff18cd5999d24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc6bd663b386af506158b3b69a2b44ea1b5e22ad11f930ebdc47c0cf5002ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:31:15 GMT
ENV NATS_SERVER=2.10.20
# Sat, 07 Sep 2024 02:31:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 07 Sep 2024 02:31:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 07 Sep 2024 02:31:17 GMT
EXPOSE 4222 6222 8222
# Sat, 07 Sep 2024 02:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 02:31:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bfa0ea6db79e386c9fe992d6c0268fba34251403c4c2aaa25f95de64ef4ea`  
		Last Modified: Sat, 07 Sep 2024 02:32:02 GMT  
		Size: 5.8 MB (5760414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0aff301e7942c7b0f7119f7bad2c51849f6d9d22e2579095546c47f2711cf1`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887850b6c6a304825f96afe62bfc9a9542c04359a360c780afa5e70ec0210686`  
		Last Modified: Sat, 07 Sep 2024 02:32:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:0adcaaa768701ae5554c053761c1d3311e22b8eecfed011e6a402e34fe8d63c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9306984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294837df3517a3f9d9152b9e323f1111830c70906404e2b6564315b906895c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:46:06 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 22:46:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 22:46:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 22:46:11 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 22:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:46:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b584078f27737442d852e251bf2db69454e62bba2cf769dfa46dc726a79dab`  
		Last Modified: Fri, 06 Sep 2024 22:46:33 GMT  
		Size: 5.7 MB (5733593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa162233a15f6f7e0a180a35a5195a94b0064d3abdd9eb42cff4d9cc40f9ebd9`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54703c1f124c0b3869da1f3b76cb7bd318dfc65acc1ecdffaa6b52b8b6694078`  
		Last Modified: Fri, 06 Sep 2024 22:46:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:b6e20e5f247fcb723038100e5fa64783a6a823eb3187b9db233855406fba0973
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9518072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd0e47bb5362627fea639b334359df52b621846a5d8e62ec7fc395d48955aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:19:02 GMT
ENV NATS_SERVER=2.10.20
# Fri, 06 Sep 2024 23:19:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Sep 2024 23:19:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Sep 2024 23:19:05 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Sep 2024 23:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:19:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47132673d9c4d1164f7b86e227c339dd0fe753cc990125ec3dac5e25a698c38d`  
		Last Modified: Fri, 06 Sep 2024 23:19:31 GMT  
		Size: 6.1 MB (6055501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ae02de914e590a8410183459a8e579b1974afefbfde069eef6236fdda9d89`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f364d7707ccf1fc2c7918cfbca95d336b0b78c442c04013917a5e26ef23cb`  
		Last Modified: Fri, 06 Sep 2024 23:19:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:483da837e851f02d9aad064d13993ba0b48c24226a5c7eaea46cb76f39aadc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6293; amd64

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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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

### `nats:latest` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:fd287f355c34fc9abc487bd27661791dfa2891ad370e5708f46119a775dde47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:87ace5d069e852125da917dda949d4aa6acdab5374627a66fe10f8cc87ba93c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0915461f35eea5cbf474b3a83589bf2681fb0525a911e616d482316ee455380`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:41:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:17:05 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 26 Sep 2024 23:17:06 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:17:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:17:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:17:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56238ef630ea819f3bf5690628ac46f909bf2db26027a52788070368a5bc5c9e`  
		Last Modified: Wed, 11 Sep 2024 01:43:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7c507ab6397aa528317b55856888f9d7d70a82ff1751dc5c8472bd5c0f1184`  
		Last Modified: Thu, 26 Sep 2024 23:17:52 GMT  
		Size: 5.9 MB (5866529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e365b7e8ebc77a322a4102db0ffa4c3f82d08794cfaf31551bfc2017b1497b5`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199d33a4267046e29838cc1d5f637ae3ce97a563861fcb00210554cb5d6d1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1bd8f223b33ccf82d3e5662dd544e9371c2c47da7193dc9f47f4b176822995`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce76cb6a73a5951419a038193e69b5ab95258ccd192b1c43db76ee4b92a854`  
		Last Modified: Thu, 26 Sep 2024 23:17:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:e74a85bba7f5b971c2c83200de86d292c531c36b8c38c2a1c558cefd97170cff
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
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
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
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:1dab5da7bd4e26f933d8a2fc039bd8f16a5c261cfecc264f68443efc186b796c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull nats@sha256:7a5e5c4d9bdb73d40c15d581e919c9358e8da9fde946d0b3c67ec2971669334b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1726734115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2e45b2d353fde11877ee6b101237c34867b496599da7ec4f3fc81f4ea8c68a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 01:39:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 01:39:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Sep 2024 23:15:21 GMT
ENV NATS_SERVER=2.10.21
# Thu, 26 Sep 2024 23:15:22 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.21/nats-server-v2.10.21-windows-amd64.zip
# Thu, 26 Sep 2024 23:15:23 GMT
ENV NATS_SERVER_SHASUM=2cbb325b34df6c98895d5ef4f2511df8ed0b3f7d2c6b267f9fe7e06938952699
# Thu, 26 Sep 2024 23:15:43 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Sep 2024 23:16:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Sep 2024 23:16:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 26 Sep 2024 23:16:41 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Sep 2024 23:16:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Sep 2024 23:16:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5162739754b5642e9d9ce80db93d3e8a06d96d4b7af006e2af2edfd913d17`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4c2846a970a55183799315672cef44169207a712160d08dfb8942b0f04cd0`  
		Last Modified: Wed, 11 Sep 2024 01:43:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba93cb9edf50e74b831bfbb464cb960e8d681bcf99954b6f04272dd3b7b88`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21dcb761b05182aeee5f3d97e80cd4e1df1335aaebfa1d302f036c36174c115`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918bd7c9b1620555d59d646534feb225f00dbd34d03996c8df95975f9b144a`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f59220850aaa47ba5f338563c40053905a42fcdac08ebe9af16e9b092107468`  
		Last Modified: Thu, 26 Sep 2024 23:17:38 GMT  
		Size: 302.3 KB (302303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43908768cca6035f3d35579b6dc523f5604f272880afd69d39118e22f9e32038`  
		Last Modified: Thu, 26 Sep 2024 23:17:37 GMT  
		Size: 6.2 MB (6150246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1c68a04c4043b5aa35f3371961797f22a154044350fe922fc428b89b2bb13`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1f5a7f20bc5aaeb3e95501f8c7d131a2d5c21336e669ad1bfd107060acb8f8`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc06f9420ab82b34701799b6a01180b09ed158a8d92575b397c4c7150737e1d`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfedc83b0b2cfa47f3b39ff26d3e02742d5057374ac5499ff398776da7e5da`  
		Last Modified: Thu, 26 Sep 2024 23:17:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
