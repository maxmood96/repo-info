## `nats:alpine3.22`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
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

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
