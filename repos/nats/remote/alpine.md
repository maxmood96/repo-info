## `nats:alpine`

```console
$ docker pull nats@sha256:2d5fce3229ae5741f4ef9225aff95dc4dc036455931eaf77a3eec33fddaa192d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:fc1c8bdbdc6022061eb5af5e4b3b6432e5f3a365accbc9a722d749c7683a7fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10841695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df746b7bcf365200aafff27fbd0014c006f448df201306c518b498bd6a464f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 18:59:37 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 18:59:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 18:59:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 18:59:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e8850fb39d1cdfe9d9764d876a1c2af2e1b031b9ffc5d54461415ed4878081`  
		Last Modified: Thu, 13 Nov 2025 19:00:36 GMT  
		Size: 7.0 MB (7038273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0788cce1180337daa09a47ecbebe082c49316b1f5eb8da349db52191e09677`  
		Last Modified: Thu, 13 Nov 2025 19:00:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc300e0e9c1ce50be0a0e9b87e0063df1822a62e6b40f2f308f7e65a89aa3494`  
		Last Modified: Thu, 13 Nov 2025 19:00:35 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:398f929d5fd60eff04baa094cbceece9bb080ed57c9812d739414cdd79fd2136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c2b129d6e62126e7f56ae8d09adaa17bb8aaef360f504e7d4835a9d8f1fb39`

```dockerfile
```

-	Layers:
	-	`sha256:b01ba45757ea5d1929b2606b243d2729c998334250c0d3d9379ac61f9016b3e4`  
		Last Modified: Thu, 13 Nov 2025 21:57:07 GMT  
		Size: 14.7 KB (14670 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9656a128cf9b7e1dd5622ba4b45a1debb1be713930fb1df31fa17d8c78d1fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28182853e68b8f26040ac1115afac23312f5c425a2584d7e048b6a39a150b553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:00:03 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 19:00:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 19:00:03 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 19:00:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 19:00:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 19:00:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:00:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5975dcf8e3a76fc9d6758ed7ad12d870cd08968264f6803e7e37d46e2270d2c`  
		Last Modified: Thu, 13 Nov 2025 19:00:35 GMT  
		Size: 6.8 MB (6761361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eaa94ddceff0a37d5a53f0ae5686c9b3bb3a500f9b91802b0cd43bc5a1ca6b`  
		Last Modified: Thu, 13 Nov 2025 19:00:34 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bded36ad582361662190f1ddda1479553d16963e321e6aa1e4bec0d1f91720`  
		Last Modified: Thu, 13 Nov 2025 19:00:34 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:64f467c91fb8a80e165006a997b88ae1872766bce08cb1d3a6ad0fa4967e09c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2050cd59432a987d7c3224e16dcb6d8df44d2a81325571434c253a1d5dc2791b`

```dockerfile
```

-	Layers:
	-	`sha256:1fbb5d13617537458a949a21f09277742f91dbe5a0217670f3d9890a4fff2f4a`  
		Last Modified: Thu, 13 Nov 2025 21:57:10 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e63a19f42aa80785a99a63e0f8f40902976d9f56c152610367c2a4501d4df7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9975024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc750cde24ab543f38d1cc28d28a2ce2b7b4b40dfd074a390e0c7cc13c99860a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 18:59:32 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 18:59:32 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 18:59:32 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 18:59:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 18:59:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 18:59:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 18:59:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17b5396fcdd93a811d7313a2cf3ef7970a2ca74d54612d7f807bcc8f57c566e`  
		Last Modified: Thu, 13 Nov 2025 19:00:20 GMT  
		Size: 6.8 MB (6752498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c579088783b5a7d71b610fce3f02391792ee811f3149c98100eb9ab2e005cc54`  
		Last Modified: Thu, 13 Nov 2025 19:00:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b389299c2084c79352ecc02535b21db334ae4b3e62208a467da008769f397`  
		Last Modified: Thu, 13 Nov 2025 19:00:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f5e13e393759646b0b6c242afb2a9667c25737a61db5464e136bf557a3b56cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc933add868863a1a589084206384295c4b3f52da2dd6ee1a7862ce32f064255`

```dockerfile
```

-	Layers:
	-	`sha256:9bb5ba2f0f9bf56be87aafea4c2f9afe14a57449e39a532bd76d9cab533f0036`  
		Last Modified: Thu, 13 Nov 2025 21:57:13 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3fcd03a0d23896278a1df2b0b6b39c5bfbfb92cbf6e191d33648a171c2003842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10592264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8b8bb06ac768c4a3ecc3d0fd894d42c7a1de49dfc3f92920f7e537c1887917`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 18:59:55 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 18:59:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 18:59:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 18:59:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 18:59:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 18:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 18:59:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc493ba16f9df029334abef5bbb55b6f7de167f9c46f71e9068d7a57a522913c`  
		Last Modified: Thu, 13 Nov 2025 19:00:51 GMT  
		Size: 6.5 MB (6453225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca1b5435ce4ba9fefb5ea9a0f14f3e4a5b94ab2faf7c9728e21f80bf6cd0ad3`  
		Last Modified: Thu, 13 Nov 2025 19:00:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3bfd46b64df7cd9171cfe9ad1145af420654e6ad3586296658dca7524febf9`  
		Last Modified: Thu, 13 Nov 2025 19:00:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:68510e980244c9db2c124cf28765bd62c81d153049b8b288956fecd792b57800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f56274e7dc30e3e533aa6fef464516b5796858eab2e524c5665e13a388f21f0`

```dockerfile
```

-	Layers:
	-	`sha256:c0c55d79a624f3872c4be9e7d7a7c041f651426cbb575d1f2acc458f0bac1eb8`  
		Last Modified: Thu, 13 Nov 2025 21:57:16 GMT  
		Size: 14.8 KB (14822 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:93f9d087d660dec36296f5c082aa0cc98c6b9e82a4b02c1a22dbbba3f03db64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e690954a93a53f565626fcc95b8dfec72725a80bf655d79a3db36c96a41bae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 18:58:39 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 18:58:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 18:58:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 18:58:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 18:58:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 18:58:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0070ccdf9092fa18bec2fd25eacbd7d206f9f689d80d4a9d0aff60f684f6bef7`  
		Last Modified: Thu, 13 Nov 2025 18:59:26 GMT  
		Size: 6.5 MB (6501730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c08914101ea6a0aa81a0b6238878090e02f6dc811f1b5382f5c2d5282e26cfa`  
		Last Modified: Thu, 13 Nov 2025 18:59:25 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a1a99bdd9747aca25d3c55e02563f2a8d2e78450344fc8f223b14eeeffde7`  
		Last Modified: Thu, 13 Nov 2025 18:59:25 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4eb0ac7ba6e7a2552af1fba748e80fe2401cdb5a39b5e9334e93f87d55279e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432cdec9f58896588b3569b4a895edb22bab8985f1486d33fdf22beb26d4006b`

```dockerfile
```

-	Layers:
	-	`sha256:8a73f132a48e4990de333b00a335c8171f2a783e7bd3f201dc077359fcd8e51e`  
		Last Modified: Thu, 13 Nov 2025 21:57:20 GMT  
		Size: 14.7 KB (14737 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:8465df20a91b5cd9cf3b7266f68e4b070c95f76cc8f856ca284aed965b3252b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10529378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebad6d7a8a97f7e9e73b46a045cc113e577d6a919557d8655ea9b96d8528a033`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 18:59:37 GMT
ENV NATS_SERVER=2.12.2
# Thu, 13 Nov 2025 18:59:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='84d33b50a39bab605b0d5e0223fc15979ef97419b2184a5a5b7eb6a6d7561fc6' ;;     armhf) natsArch='arm6'; sha256='1098aeba5873d91a485dcb60ef483e1ebcc337fbfb1eeec2ffbf3ba9d4c10242' ;;     armv7) natsArch='arm7'; sha256='6f16c8718957c646bb7ea5a6d762492bf78be94018a7057ce36ab9ad550ad32d' ;;     x86_64) natsArch='amd64'; sha256='db587fd8b36ac732a8434e748b026ef77ed9cb714a4e57bd010b1de93c2f3801' ;;     x86) natsArch='386'; sha256='a117846d4495e809a5e42655488f44d0d4044b5a076f7753df759e7e6099f60f' ;;     s390x) natsArch='s390x'; sha256='c3812ec35c52c4b9d0b19e848d82586236bd913c056f8c3673f2990b9de8feaa' ;;     ppc64le) natsArch='ppc64le'; sha256='2d2f028c8747c606abfd7d653f492d43deb79a387b9643962b09dfb628c57e17' ;;     loong64) natsArch='loong64'; sha256='9b66d798d12afbe643bdee07fb1fbc9f0f7ebfc347cb40a2274a7b4445f914b6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 13 Nov 2025 18:59:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 13 Nov 2025 18:59:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 18:59:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6719e160e21d9b2cfe8d6f33db06333f0f1af61125a2163571aee1b8cce5e01a`  
		Last Modified: Thu, 13 Nov 2025 19:00:39 GMT  
		Size: 6.9 MB (6879165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893f428f3830db424a0a434422c82629f5fc491ffeb11908efe4c7a9b589dd1f`  
		Last Modified: Thu, 13 Nov 2025 19:00:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1cbf754bb9b50e0989e752b9fec34854fbf783f0e2ac6a3896b0b8cf66f1d`  
		Last Modified: Thu, 13 Nov 2025 19:00:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9350d40a63d240e4189505d0c29bd93790011ec9ade31b1ad9bd05c44f849338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a28437c807f973ab145db8b9f4bd7343f7b71ba2662b4b95828c60fe21f8e5b`

```dockerfile
```

-	Layers:
	-	`sha256:37d2be97158bcafa4dd3a7f94a0344ea97207d2cd24c46080ca447bfec7aec36`  
		Last Modified: Thu, 13 Nov 2025 21:57:23 GMT  
		Size: 14.7 KB (14670 bytes)  
		MIME: application/vnd.in-toto+json
