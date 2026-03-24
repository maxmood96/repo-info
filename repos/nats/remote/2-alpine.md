## `nats:2-alpine`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
