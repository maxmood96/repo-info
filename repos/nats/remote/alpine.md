## `nats:alpine`

```console
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
