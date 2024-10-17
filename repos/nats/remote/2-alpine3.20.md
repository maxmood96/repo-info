## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
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
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
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
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
