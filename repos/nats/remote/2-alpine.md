## `nats:2-alpine`

```console
$ docker pull nats@sha256:d26b2c764e207148f0f5d297bc003e5db69e59c0de197adb0a0254c3d84872e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b8c33c1775880f98b37ec8555ccbb7ab2db2e89d807864dbce3abf18e0ee6a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8635882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2be1dee271f717feb961aefbc00fbc062498bcfe2bfc68ef28f4993f4a0353c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:17:40 GMT
ENV NATS_SERVER=2.9.15
# Wed, 29 Mar 2023 22:17:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 29 Mar 2023 22:17:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 29 Mar 2023 22:17:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Mar 2023 22:17:43 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Mar 2023 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:17:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b555478c97d500423b4ec4b759dea8d7222f5483c0d05faf690bcf65cca6b8b5`  
		Last Modified: Wed, 29 Mar 2023 22:18:00 GMT  
		Size: 5.3 MB (5260322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d097206350ad8a3fa170f350eaa1983c4aa285235aba3735eb54293cf68b1b5`  
		Last Modified: Wed, 29 Mar 2023 22:17:59 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9acb3e08b26b83e42880e24fda19c80b1dc76010886c3e58a940e56d1a803fe`  
		Last Modified: Wed, 29 Mar 2023 22:17:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34069e01b53202550c58fb5ad62314ba3bd47bff825de7f9bf815e33db2e1d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8135652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187ff1764fbf00849fa72dd74711b2fc4604771b0810ec9d0f74b51dfa6e6a02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:56 GMT
ENV NATS_SERVER=2.9.15
# Wed, 29 Mar 2023 19:25:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 29 Mar 2023 19:25:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 29 Mar 2023 19:25:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:59 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Mar 2023 19:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6e895df39b31ddef480bd558704def131db5e52235a0f7f6d6a0e549ef48`  
		Last Modified: Wed, 29 Mar 2023 19:26:46 GMT  
		Size: 5.0 MB (5023853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185e76d48b40900624d64d497f45053dc1c8f1669fd5929d59fff490f1acd946`  
		Last Modified: Wed, 29 Mar 2023 19:26:45 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907019fd32e315a992bdf93b69c2881d8583660aa015cd6f371aca1446ac7baa`  
		Last Modified: Wed, 29 Mar 2023 19:26:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a07b10b9d4b0270547b1829ec2654e86f79abc88aacc6205185377e670505542
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7887583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bb41326e49a9a4a84cd8fa0e6251ec300d8e66861fc5dedc6445c11b8d8bab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:24:01 GMT
ENV NATS_SERVER=2.9.15
# Wed, 29 Mar 2023 19:24:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 29 Mar 2023 19:24:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 29 Mar 2023 19:24:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Mar 2023 19:24:04 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Mar 2023 19:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:24:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c782d9234ff70b39bfff1c9fae811b6502cb9f751cc42adb8fea7a1cae072b`  
		Last Modified: Wed, 29 Mar 2023 19:24:46 GMT  
		Size: 5.0 MB (5018067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6550b200cd2b3bc8c94ad0423e19eb7bb2111322df8eed66c3312d2d62b36ec3`  
		Last Modified: Wed, 29 Mar 2023 19:24:45 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac38931f834e11c161f4de58f07336f18185b088a6306d3f9d3938945e360df`  
		Last Modified: Wed, 29 Mar 2023 19:24:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:26c93c2e512a5be5cf69f6a77981f65bd2a34aa0a267808a78044900523a2273
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8103920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6594aa95a6a12292c371fbbdb19b57c50f425b9f714408537241356a8489758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:28:21 GMT
ENV NATS_SERVER=2.9.15
# Wed, 29 Mar 2023 18:28:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f4f86a5c10914bc6fb40effd2fdaa3d4f69bbbd14ca68571c4afe49c7cd1356d' ;; 		armhf) natsArch='arm6'; sha256='29c8e26624011d05a2befcb3a25d00eaae098baba34f02e93cc3e336b6aa61ec' ;; 		armv7) natsArch='arm7'; sha256='83b6c1cb1b9d7d15b6fa042b63bd4af1cd66884d1b46849ba362b171611c19ad' ;; 		x86_64) natsArch='amd64'; sha256='32ba26c522b3c245f2105e9642256b0bd8f993f3f9a034b701a327721576d761' ;; 		x86) natsArch='386'; sha256='b32b54780fdc7527e0414a852effbbfab8e2c3f3482935b9459f586095e39945' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 29 Mar 2023 18:28:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 29 Mar 2023 18:28:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Mar 2023 18:28:23 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Mar 2023 18:28:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 18:28:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a70aa6cf97869cec2d16b8b65f99275cce8c3cf655624bfc181c7276d19641`  
		Last Modified: Wed, 29 Mar 2023 18:28:38 GMT  
		Size: 4.8 MB (4841068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a9ab842bf93fd56404bc8c33ba71ee9e747c755a2dc2c1720aa82c6b178aae`  
		Last Modified: Wed, 29 Mar 2023 18:28:37 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52624160d291d3643a842fdeb0ad2337c0dded7d37ad0a250d2ec6ae7615b66`  
		Last Modified: Wed, 29 Mar 2023 18:28:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
