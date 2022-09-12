<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.16`](#nats2-alpine316)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.16`](#nats29-alpine316)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.0`](#nats290)
-	[`nats:2.9.0-alpine`](#nats290-alpine)
-	[`nats:2.9.0-alpine3.16`](#nats290-alpine316)
-	[`nats:2.9.0-linux`](#nats290-linux)
-	[`nats:2.9.0-nanoserver`](#nats290-nanoserver)
-	[`nats:2.9.0-nanoserver-1809`](#nats290-nanoserver-1809)
-	[`nats:2.9.0-scratch`](#nats290-scratch)
-	[`nats:2.9.0-windowsservercore`](#nats290-windowsservercore)
-	[`nats:2.9.0-windowsservercore-1809`](#nats290-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.16`](#natsalpine316)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:236498b19ca0ef368dae3931043e7ff3e16b27facae33f3723aca5b7d8c6f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3287; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.16`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:236498b19ca0ef368dae3931043e7ff3e16b27facae33f3723aca5b7d8c6f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.16`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0`

```console
$ docker pull nats@sha256:236498b19ca0ef368dae3931043e7ff3e16b27facae33f3723aca5b7d8c6f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9.0` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-alpine`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.0-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-alpine3.16`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.0-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-linux`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.0-linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-nanoserver`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9.0-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-nanoserver-1809`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9.0-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-scratch`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.0-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-windowsservercore`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9.0-windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.0-windowsservercore-1809`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:2.9.0-windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.16`

```console
$ docker pull nats@sha256:369d96bfb77439b67c975045e9d15ba37999e691094361ff6c447a9e78b7b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:085e2d3603a5ffeb96a5e784f11532c03a4f0840b6d68974c49981ff00ae2403
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82d17b5c2168901fc2938dbcf28eb4107996ab8bc9eb7f577b8561f959058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:49:32 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:49:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:49:35 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:49:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddff5163e8c58a7497154f421e89aff54a43caec19e95069cc494375041aa`  
		Last Modified: Mon, 12 Sep 2022 18:50:45 GMT  
		Size: 5.0 MB (4952345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8019ab673b790b4ed63a97187571f3d0e5f4eb16dfa17399f6a243d11ff5722b`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceaa398303883b9d5e592ce9aeaccbcf4b34b99a27a67d1578a0d6de4e69d3`  
		Last Modified: Mon, 12 Sep 2022 18:50:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:b95fa7ad87668f84962e4ef5abed9890fb57640ad479112b7f8c119bfa45dfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06933b06c17a95c6cd21d33dc823a06314c6b8517ebbfaf5b76c3b3cf11b155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:03:51 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:03:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:03:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:03:54 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:03:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3571a588810a8fe42813cdd7bcdc3e7b0be7bfc9084e38508f050f9826bba19`  
		Last Modified: Mon, 12 Sep 2022 19:05:22 GMT  
		Size: 4.9 MB (4945636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1bcd898e16c2896f273f1b98e85da9bae6f599fb25e92fcdb2cab7ba63d64d`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdba5340addabedb9b0801b2c8d51c4b04c684965b7e4f9b25e8b44573fb78`  
		Last Modified: Mon, 12 Sep 2022 19:05:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7869a7f7498ee46895e9948a102087841874c9ee049696fe96edc9c4c5f7b17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cded970df3ac075d6833bcc805ee1cd39b6de8728ce00785f95016a231117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 18:50:02 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 18:50:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 18:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 18:50:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 18:50:07 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 18:50:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13b8dbdcf7252f528110cd3097a32511e40b830a0e7690d5d3c7c544cbbace`  
		Last Modified: Mon, 12 Sep 2022 18:51:12 GMT  
		Size: 4.8 MB (4773665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8435ac86def6a8973b25db155dbd8c3f0c407542046937eb1ab78b99276e`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47359896823731079e2553b7cf975eba66a0095c51b1ccffbe582b732a6d41b`  
		Last Modified: Mon, 12 Sep 2022 18:51:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:236498b19ca0ef368dae3931043e7ff3e16b27facae33f3723aca5b7d8c6f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3287; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:595b9a185f5baf1025a20a990f181319ac3b1f94b0214b7e01f4dbf624dfb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:9f9679f278fbf584992e8d8fabe26ce93bc8d3c91d389ecf5de5b1bd619886dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108165102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cb4438a6fb065a40e7dba2da39341d32b88fa5218b2eb38f0c7ade22c2c78`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:30:21 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:19:12 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Mon, 12 Sep 2022 19:19:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a5df16ce106b092b5399678da04735c18584e4f99ea301691eb433072953e9a`  
		Last Modified: Wed, 10 Aug 2022 15:31:14 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661370d9d27020e3da7fd87855fd46c4b84dcad2a7734c033fd5d58f7cc10d99`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 5.0 MB (4954584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebeb8f020417c79d7f9a4b96a5b4d8461fb8005ccf0f9d2a2ab15d23270852b`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319410bd22fd8059a26939aab07894fa611ce65503ce2b50d40ac33ec1fe3591`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e2f36b209328be490059b4a70b5f7451c842a2354410f2644a49676f4995`  
		Last Modified: Mon, 12 Sep 2022 19:20:03 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b020f5e205db60854c94a796e92914eb10c1fba1edea565697247d23c21321`  
		Last Modified: Mon, 12 Sep 2022 19:20:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:42ea68a87c9a0b0e3c60b3ccb49f24264af98dd85602a6450e03ab726015d7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:118585c5efc972b7af723b603811e3146ee914a26b54bcb892c506e8080d2fac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd239e963a20ee15d599802357bd7485cbf652b2c7a5d9c77d6485c07168bce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:37e0cdc4ef3cae050b7a622e477f07fea2b89f2849c5c229803b12157182aa73 in /nats-server 
# Mon, 12 Sep 2022 18:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:49:48 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:49:49 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:49:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5a54d3866fde0d65a287b5e00b2251f84936c27eed638ecef0fa1e8f95134bd6`  
		Last Modified: Mon, 12 Sep 2022 18:51:17 GMT  
		Size: 4.7 MB (4664750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2846c8f5d71bd80327105a167594ce9f72272f7c6a141cf378e206141a075ab`  
		Last Modified: Mon, 12 Sep 2022 18:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a48ca64c022b50e4612f11b7b0bdf380e886ad449c8eb5a48624b2df386ceab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4658073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43328d44a144020547148c52c8b0e257f2553339a66f15912b23f9b377d646d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:88b07716d72d7b053cbf196c5562712b60f9d8875ee610f10839774e5aa8fd5e in /nats-server 
# Mon, 12 Sep 2022 19:04:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:04:24 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:04:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:04:24 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:04:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fdc81c83bc1df58c4e224556b8224d1e7425add4047736a641d435c2097b7c10`  
		Last Modified: Mon, 12 Sep 2022 19:05:53 GMT  
		Size: 4.7 MB (4657565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012d019d0dd61d6f41306e0a2009771e9b75625f46458973bd5db00d964d0d28`  
		Last Modified: Mon, 12 Sep 2022 19:05:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:09ddfc36cc0a08d6c04828f085c33c72e9641c712d6a0f1a78126e3267a10699
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28d3ca7b6670d9a7ef545dae9da4b8dfb8cb06b7f35b0a1fb9db72eb9327038`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 18:50:22 GMT
COPY file:2793f903eadf963d049d95e6645a7fc0e41632a84eff5d1055bd4de285218751 in /nats-server 
# Mon, 12 Sep 2022 18:50:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 18:50:23 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 18:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 18:50:25 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 18:50:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29ad82f04593c429e1ee6bf6c0c2687549bee49e553052bf5b67eec17de00f9b`  
		Last Modified: Mon, 12 Sep 2022 18:51:40 GMT  
		Size: 4.5 MB (4492060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138da13517dd9cec8dbf0a87e0ce1dc5c15dbde69247362fc9895c07830e7f72`  
		Last Modified: Mon, 12 Sep 2022 18:51:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b37318e22e6c2bca5e2d092fbab4905b4dd53290044c8dbd8cbd677261d3a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull nats@sha256:4a559a5453abebb4d56e482d381590b2b1d61191be333c254172c1d27773a84b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683377209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f6380d1357690f0092632218fce699a83134468e03023479e9e67e7317588`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 15:27:50 GMT
ENV NATS_DOCKERIZED=1
# Mon, 12 Sep 2022 19:16:00 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:16:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Mon, 12 Sep 2022 19:16:02 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Mon, 12 Sep 2022 19:17:19 GMT
RUN Set-PSDebug -Trace 2
# Mon, 12 Sep 2022 19:18:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 12 Sep 2022 19:18:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 12 Sep 2022 19:18:51 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:18:52 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 12 Sep 2022 19:18:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc1c1069568772f0068cef343e37284e5f5e488dbfc15e037d95bce032d917`  
		Last Modified: Wed, 10 Aug 2022 15:30:56 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dc5196335dbb75c5b511c3b7f88d1ea863a5fd9c948ed2284c61bce8d05f7`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cab5aeb6f1c72acf727c92921b388759093ed4f8109a731f08a93ccce6df92`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a14b7e5d70af9acd178b843943bf573128c25c44b9085c9afb843132d103f`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945be30f32456b0704b1bf873985926e899f43099f0473ac39a6b1bc59dce55`  
		Last Modified: Mon, 12 Sep 2022 19:19:48 GMT  
		Size: 355.5 KB (355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9c99958ecc108eb4d345fcce1858463fbca041d04da8f36ffb117bf0b34b1`  
		Last Modified: Mon, 12 Sep 2022 19:19:47 GMT  
		Size: 5.3 MB (5295678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddb96d7096a0d1a680c5ff1fe7b31e8135bef30b4f0fe5b9290ec90520213e`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f15e23683198de7411b9a1a6508b91b3e7a2335b39bc952824eaa754d27d3`  
		Last Modified: Mon, 12 Sep 2022 19:19:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56027e9880bd41ea09c2f65aa361a6f3a8d18b43c467f3aa55d8eb0497778`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1693476cfeceab25d4ab31b997456d983001a60e1d7f0e9256423648e0acc357`  
		Last Modified: Mon, 12 Sep 2022 19:19:45 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
