## `nats:alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
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
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
