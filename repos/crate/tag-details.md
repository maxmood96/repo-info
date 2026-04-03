<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.1`](#crate61)
-	[`crate:6.1.3`](#crate613)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.4`](#crate624)
-	[`crate:latest`](#cratelatest)

## `crate:6.1`

```console
$ docker pull crate@sha256:9174c9012a15486603ad9758d4bb223386f934c6ee9f2632fc751a06d465e1a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:0db9b678f96e5e7eac5a0caa5e82e3f94ab27bf48c7ed793b0ab69a6e82f7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231648104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee74b63bdca4906627386f585f5636facce36fa6ebe339806815ec284fdf71`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:31:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:31:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:31:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:31:28 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:31:28 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:31:28 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:31:28 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Mon, 30 Mar 2026 18:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:31:28 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb613ccae2ab7ce64493d4d5944a6e51679d436d50a41420e4b6552d2e1cfe6`  
		Last Modified: Mon, 30 Mar 2026 18:31:47 GMT  
		Size: 13.0 MB (13034409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c77289c35bef17cd75d05cba0bb1bac3028f4b8aceaec336c610df7adcfe9a`  
		Last Modified: Mon, 30 Mar 2026 18:31:50 GMT  
		Size: 149.2 MB (149152325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f875e3b9e9ed81d5e02af53575e1b8cb9e202fd7686f573b0c8a4a50f1b177`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a7e65cc5a847c8d2983451adde1bcfc5739dfa220d7c9b5cf9298dfa818d6`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a529af5f6635307c676aa67c7901d0533266d172a59d7786e955ea8b7b5140f0`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f395def1fa332ff2b96b79a363582fbe0311a72c4d943f97b8358f3f26c67e9e`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ed4c1ae20edfc80ba409ec4bbb5f5c014c6f7f30f04a74db1b39afb1c964c6`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:f9831d8a23f884747ecc74b21b3148ca84e0a6b59804df2ae0168787b11b81cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085da0aefacce284950946499db1fe3ad0f4f1b216a8b35b9d24a263a7d65678`

```dockerfile
```

-	Layers:
	-	`sha256:be567aaeb133d9415ac65b454847fb7b852e34ac0468f8b692f6bf6e0cdfcc28`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 5.2 MB (5150710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7929bca27d9bb461caabde46a15ca3ac20ea2b2215a80a68093816bedbf0bfc4`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4399d49508675390b56339e016fa6f034b8be6a8191dc5d657f7ab6a3ed40081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230974055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41abe2f7ed24efb3246a45b736de7f23ace5543aef1d2b9ed03324b0a318608f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:31:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:31:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:31:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:31:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:31:22 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:31:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:31:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Mon, 30 Mar 2026 18:31:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:31:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde5a537ee1900f216f341a70b3a9160e8befce83876e00814c4f681bdc9090f`  
		Last Modified: Mon, 30 Mar 2026 18:31:41 GMT  
		Size: 13.1 MB (13091434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e704e546bc96ea18e7e798a1f0fcaf256f097f16623ecc38c0e33dd284db9b2`  
		Last Modified: Mon, 30 Mar 2026 18:31:45 GMT  
		Size: 149.8 MB (149841137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ece94fa83db2a61a529630380e988c4b6d007cdaa4bafca18a442cfad9df128`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a969214710690f9fc8d9a80af8ec98605d78925bf48a173600793c265405cdc`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61144f091727adf224a3ebf14f6732d0420d4fce6538e5cdb18fdf7569543e54`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db58513f08d3d31e6303b35bdd59f24dcc2efcf09152155f779c4c35fdc34e81`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a184b0125ed63b2aa64f1d82dca02d51711cbe972b2e355017c5ff2cfd43af0`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:03e9fb1d63cbad6916c74df4f442c0a35571b29d2fc7d2b6dec3a95503fa4b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8e71bd0dc2d7450afd1b1cfe58a5db4fd87f97661c1d95ffdaf160371ceede`

```dockerfile
```

-	Layers:
	-	`sha256:1d870328faa86462e97598965f942ba9b30437d35393e0ec66a4a7724a0c54ee`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 5.1 MB (5148617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e6f75123e19ca46023216b9bd93265a56b94764ede3a26b61a10d5d00ced25`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.3`

```console
$ docker pull crate@sha256:9174c9012a15486603ad9758d4bb223386f934c6ee9f2632fc751a06d465e1a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.3` - linux; amd64

```console
$ docker pull crate@sha256:0db9b678f96e5e7eac5a0caa5e82e3f94ab27bf48c7ed793b0ab69a6e82f7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231648104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee74b63bdca4906627386f585f5636facce36fa6ebe339806815ec284fdf71`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:31:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:31:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:31:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:31:28 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:31:28 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:31:28 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:31:28 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Mon, 30 Mar 2026 18:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:31:28 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb613ccae2ab7ce64493d4d5944a6e51679d436d50a41420e4b6552d2e1cfe6`  
		Last Modified: Mon, 30 Mar 2026 18:31:47 GMT  
		Size: 13.0 MB (13034409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c77289c35bef17cd75d05cba0bb1bac3028f4b8aceaec336c610df7adcfe9a`  
		Last Modified: Mon, 30 Mar 2026 18:31:50 GMT  
		Size: 149.2 MB (149152325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f875e3b9e9ed81d5e02af53575e1b8cb9e202fd7686f573b0c8a4a50f1b177`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a7e65cc5a847c8d2983451adde1bcfc5739dfa220d7c9b5cf9298dfa818d6`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a529af5f6635307c676aa67c7901d0533266d172a59d7786e955ea8b7b5140f0`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f395def1fa332ff2b96b79a363582fbe0311a72c4d943f97b8358f3f26c67e9e`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ed4c1ae20edfc80ba409ec4bbb5f5c014c6f7f30f04a74db1b39afb1c964c6`  
		Last Modified: Mon, 30 Mar 2026 18:31:48 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.3` - unknown; unknown

```console
$ docker pull crate@sha256:f9831d8a23f884747ecc74b21b3148ca84e0a6b59804df2ae0168787b11b81cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085da0aefacce284950946499db1fe3ad0f4f1b216a8b35b9d24a263a7d65678`

```dockerfile
```

-	Layers:
	-	`sha256:be567aaeb133d9415ac65b454847fb7b852e34ac0468f8b692f6bf6e0cdfcc28`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 5.2 MB (5150710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7929bca27d9bb461caabde46a15ca3ac20ea2b2215a80a68093816bedbf0bfc4`  
		Last Modified: Mon, 30 Mar 2026 18:31:46 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4399d49508675390b56339e016fa6f034b8be6a8191dc5d657f7ab6a3ed40081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230974055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41abe2f7ed24efb3246a45b736de7f23ace5543aef1d2b9ed03324b0a318608f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 18:31:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Mar 2026 18:31:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:31:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Mar 2026 18:31:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
VOLUME [/data]
# Mon, 30 Mar 2026 18:31:22 GMT
WORKDIR /data
# Mon, 30 Mar 2026 18:31:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Mar 2026 18:31:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Mon, 30 Mar 2026 18:31:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 18:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Mar 2026 18:31:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde5a537ee1900f216f341a70b3a9160e8befce83876e00814c4f681bdc9090f`  
		Last Modified: Mon, 30 Mar 2026 18:31:41 GMT  
		Size: 13.1 MB (13091434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e704e546bc96ea18e7e798a1f0fcaf256f097f16623ecc38c0e33dd284db9b2`  
		Last Modified: Mon, 30 Mar 2026 18:31:45 GMT  
		Size: 149.8 MB (149841137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ece94fa83db2a61a529630380e988c4b6d007cdaa4bafca18a442cfad9df128`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a969214710690f9fc8d9a80af8ec98605d78925bf48a173600793c265405cdc`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61144f091727adf224a3ebf14f6732d0420d4fce6538e5cdb18fdf7569543e54`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db58513f08d3d31e6303b35bdd59f24dcc2efcf09152155f779c4c35fdc34e81`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a184b0125ed63b2aa64f1d82dca02d51711cbe972b2e355017c5ff2cfd43af0`  
		Last Modified: Mon, 30 Mar 2026 18:31:42 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.3` - unknown; unknown

```console
$ docker pull crate@sha256:03e9fb1d63cbad6916c74df4f442c0a35571b29d2fc7d2b6dec3a95503fa4b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8e71bd0dc2d7450afd1b1cfe58a5db4fd87f97661c1d95ffdaf160371ceede`

```dockerfile
```

-	Layers:
	-	`sha256:1d870328faa86462e97598965f942ba9b30437d35393e0ec66a4a7724a0c54ee`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 5.1 MB (5148617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e6f75123e19ca46023216b9bd93265a56b94764ede3a26b61a10d5d00ced25`  
		Last Modified: Mon, 30 Mar 2026 18:31:40 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:d12a9a205b96ff931a7bcaa6d42e604e78b9d987ae0b76b91cc144e1912456f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:38d87b960752f31036c000b24fa4c112afac0ead3e7678012093e1e1568af593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257062852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9f2b5aa259b3a3edc63f520453fb68502ea6b6f497261b4b0fef25c3b0d3a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:43:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:09 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e762efc9e8e4772a4f3f7cf6918e5000b3ca967ee0da427e12dc1f67241862`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 30.5 MB (30527460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be53f16372611090879590675bacd4b589f0be08ea7416fb1442ea2cd66bb71`  
		Last Modified: Thu, 02 Apr 2026 18:44:32 GMT  
		Size: 151.3 MB (151318718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24111ce89181d209d6c387b30c0fef7fc8421b80eea3df607789b712d661527`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 7.7 MB (7698935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40408dce7530e7edab8b5e524da7db2cd4414654d930b4d41dbccd3e4e2550a0`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeec46a028b956d77e1cb454ee0242a7cdb7f1c8f930aa2ced1b95f21396fc5`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d015d0f4b57ca1ebe2a416144bdec7d90a8ac2b675aa20866812aeeb72309`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2e05bd1da726c014e4591b52c54f72595e4a96026366c2598b90e25bb5143`  
		Last Modified: Thu, 02 Apr 2026 18:44:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:e6488f8c6541d975e7e3fd4f689e0319341bf06f5775ca923eaf6fcf490f8d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e02e1d6af32c28dd76bef48e95d8f64f1dfca5d665b882db8994505fcada8`

```dockerfile
```

-	Layers:
	-	`sha256:dbe3d2ccd47be976c126795767dd1568de7e1d5a91da449afe948968f8d34db9`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 6.5 MB (6462633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a511acf7b5519ca664d65d929bfa09948dbe6be90dc7c6c8cbd4733f997736cf`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:395a0fd7155e8a68ba712a2ae35f22f10af71ff8fbbe1938fa2b6a91fa6b7df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253523932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9abd79fc2f92206a117dbc93aa26dc2d87f8f00c3081cd6aad7779df37a3a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:44:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:25 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:28 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:29 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:29 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:29 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:29 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920e3d4f0a54eb443dfff1ff527305aefbd0d64a71cba2cf3fbc8d6554ad687`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 30.4 MB (30439525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d9148cc0f776c091a9a507dec052ccdca79072eb962a1b3ebd7833d1d3aa3`  
		Last Modified: Thu, 02 Apr 2026 18:44:51 GMT  
		Size: 149.3 MB (149289160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fee6945842b533c4ccba842d963e73293e2b59ca98a7bcc7497fab852bd66a`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 7.7 MB (7697393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf40f52c20d5aecf2d848176c146c7bce50154aad8ce0e909d3dc6e0a6ec90e`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59d22957f148ce0c36116149212ebebb27d69c4d5272d855e6de79f59b8f5`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dd14fc9fe37de10895beab54ca694fa27d08f0689eacc32e4aaef73b5d312d`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eae20ec88cee3844e342651770821d536c7cf1744e37e35478a12df2516c6a`  
		Last Modified: Thu, 02 Apr 2026 18:44:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:c86583d6d7d279ff9d1665918cf26dcb2959c8f4b304dec44a6eadeff8c253ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70afa005db939913c600d362a67652c4f4900a40e548ad64746631f56d565b1e`

```dockerfile
```

-	Layers:
	-	`sha256:c6be00219b3a6cd93a85bf7078b6a39f34e57418cae4d3220ef70fbaba9c3600`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 6.5 MB (6460552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4df36f5e74eb137c6416523ffaae11205c80dc2aa58b4ab3a8d515720b2e914`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.4`

```console
$ docker pull crate@sha256:d12a9a205b96ff931a7bcaa6d42e604e78b9d987ae0b76b91cc144e1912456f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.4` - linux; amd64

```console
$ docker pull crate@sha256:38d87b960752f31036c000b24fa4c112afac0ead3e7678012093e1e1568af593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257062852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9f2b5aa259b3a3edc63f520453fb68502ea6b6f497261b4b0fef25c3b0d3a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:43:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:09 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e762efc9e8e4772a4f3f7cf6918e5000b3ca967ee0da427e12dc1f67241862`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 30.5 MB (30527460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be53f16372611090879590675bacd4b589f0be08ea7416fb1442ea2cd66bb71`  
		Last Modified: Thu, 02 Apr 2026 18:44:32 GMT  
		Size: 151.3 MB (151318718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24111ce89181d209d6c387b30c0fef7fc8421b80eea3df607789b712d661527`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 7.7 MB (7698935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40408dce7530e7edab8b5e524da7db2cd4414654d930b4d41dbccd3e4e2550a0`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeec46a028b956d77e1cb454ee0242a7cdb7f1c8f930aa2ced1b95f21396fc5`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d015d0f4b57ca1ebe2a416144bdec7d90a8ac2b675aa20866812aeeb72309`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2e05bd1da726c014e4591b52c54f72595e4a96026366c2598b90e25bb5143`  
		Last Modified: Thu, 02 Apr 2026 18:44:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.4` - unknown; unknown

```console
$ docker pull crate@sha256:e6488f8c6541d975e7e3fd4f689e0319341bf06f5775ca923eaf6fcf490f8d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e02e1d6af32c28dd76bef48e95d8f64f1dfca5d665b882db8994505fcada8`

```dockerfile
```

-	Layers:
	-	`sha256:dbe3d2ccd47be976c126795767dd1568de7e1d5a91da449afe948968f8d34db9`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 6.5 MB (6462633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a511acf7b5519ca664d65d929bfa09948dbe6be90dc7c6c8cbd4733f997736cf`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:395a0fd7155e8a68ba712a2ae35f22f10af71ff8fbbe1938fa2b6a91fa6b7df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253523932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9abd79fc2f92206a117dbc93aa26dc2d87f8f00c3081cd6aad7779df37a3a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:44:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:25 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:28 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:29 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:29 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:29 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:29 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920e3d4f0a54eb443dfff1ff527305aefbd0d64a71cba2cf3fbc8d6554ad687`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 30.4 MB (30439525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d9148cc0f776c091a9a507dec052ccdca79072eb962a1b3ebd7833d1d3aa3`  
		Last Modified: Thu, 02 Apr 2026 18:44:51 GMT  
		Size: 149.3 MB (149289160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fee6945842b533c4ccba842d963e73293e2b59ca98a7bcc7497fab852bd66a`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 7.7 MB (7697393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf40f52c20d5aecf2d848176c146c7bce50154aad8ce0e909d3dc6e0a6ec90e`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59d22957f148ce0c36116149212ebebb27d69c4d5272d855e6de79f59b8f5`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dd14fc9fe37de10895beab54ca694fa27d08f0689eacc32e4aaef73b5d312d`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eae20ec88cee3844e342651770821d536c7cf1744e37e35478a12df2516c6a`  
		Last Modified: Thu, 02 Apr 2026 18:44:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.4` - unknown; unknown

```console
$ docker pull crate@sha256:c86583d6d7d279ff9d1665918cf26dcb2959c8f4b304dec44a6eadeff8c253ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70afa005db939913c600d362a67652c4f4900a40e548ad64746631f56d565b1e`

```dockerfile
```

-	Layers:
	-	`sha256:c6be00219b3a6cd93a85bf7078b6a39f34e57418cae4d3220ef70fbaba9c3600`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 6.5 MB (6460552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4df36f5e74eb137c6416523ffaae11205c80dc2aa58b4ab3a8d515720b2e914`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:d12a9a205b96ff931a7bcaa6d42e604e78b9d987ae0b76b91cc144e1912456f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:38d87b960752f31036c000b24fa4c112afac0ead3e7678012093e1e1568af593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257062852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9f2b5aa259b3a3edc63f520453fb68502ea6b6f497261b4b0fef25c3b0d3a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:09:00 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:09:00 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:43:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:09 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:cabb5edb8ed650ef967fbc90afe8d726b34a50a1e65faaeb9925d97c0baa7db2`  
		Last Modified: Mon, 30 Mar 2026 18:09:17 GMT  
		Size: 67.5 MB (67515860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e762efc9e8e4772a4f3f7cf6918e5000b3ca967ee0da427e12dc1f67241862`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 30.5 MB (30527460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be53f16372611090879590675bacd4b589f0be08ea7416fb1442ea2cd66bb71`  
		Last Modified: Thu, 02 Apr 2026 18:44:32 GMT  
		Size: 151.3 MB (151318718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24111ce89181d209d6c387b30c0fef7fc8421b80eea3df607789b712d661527`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 7.7 MB (7698935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40408dce7530e7edab8b5e524da7db2cd4414654d930b4d41dbccd3e4e2550a0`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeec46a028b956d77e1cb454ee0242a7cdb7f1c8f930aa2ced1b95f21396fc5`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d015d0f4b57ca1ebe2a416144bdec7d90a8ac2b675aa20866812aeeb72309`  
		Last Modified: Thu, 02 Apr 2026 18:44:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2e05bd1da726c014e4591b52c54f72595e4a96026366c2598b90e25bb5143`  
		Last Modified: Thu, 02 Apr 2026 18:44:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:e6488f8c6541d975e7e3fd4f689e0319341bf06f5775ca923eaf6fcf490f8d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e02e1d6af32c28dd76bef48e95d8f64f1dfca5d665b882db8994505fcada8`

```dockerfile
```

-	Layers:
	-	`sha256:dbe3d2ccd47be976c126795767dd1568de7e1d5a91da449afe948968f8d34db9`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 6.5 MB (6462633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a511acf7b5519ca664d65d929bfa09948dbe6be90dc7c6c8cbd4733f997736cf`  
		Last Modified: Thu, 02 Apr 2026 18:44:28 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:395a0fd7155e8a68ba712a2ae35f22f10af71ff8fbbe1938fa2b6a91fa6b7df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253523932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9abd79fc2f92206a117dbc93aa26dc2d87f8f00c3081cd6aad7779df37a3a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Mar 2026 18:08:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Mar 2026 18:08:41 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 18:44:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 Apr 2026 18:44:25 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.4.tar.gz.asc crate-6.2.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.4.tar.gz.asc     && tar -xf crate-6.2.4.tar.gz -C /crate --strip-components=1     && rm crate-6.2.4.tar.gz # buildkit
# Thu, 02 Apr 2026 18:44:28 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Apr 2026 18:44:29 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 Apr 2026 18:44:29 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
VOLUME [/data]
# Thu, 02 Apr 2026 18:44:29 GMT
WORKDIR /data
# Thu, 02 Apr 2026 18:44:29 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-30T10:53:02.365389+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.4
# Thu, 02 Apr 2026 18:44:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 Apr 2026 18:44:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Apr 2026 18:44:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:aff9c4a67c7feab8186c047ca5e56df79a2206806fa85a5bce2fe732724828ed`  
		Last Modified: Mon, 30 Mar 2026 18:08:58 GMT  
		Size: 66.1 MB (66095973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920e3d4f0a54eb443dfff1ff527305aefbd0d64a71cba2cf3fbc8d6554ad687`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 30.4 MB (30439525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d9148cc0f776c091a9a507dec052ccdca79072eb962a1b3ebd7833d1d3aa3`  
		Last Modified: Thu, 02 Apr 2026 18:44:51 GMT  
		Size: 149.3 MB (149289160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fee6945842b533c4ccba842d963e73293e2b59ca98a7bcc7497fab852bd66a`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 7.7 MB (7697393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf40f52c20d5aecf2d848176c146c7bce50154aad8ce0e909d3dc6e0a6ec90e`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59d22957f148ce0c36116149212ebebb27d69c4d5272d855e6de79f59b8f5`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dd14fc9fe37de10895beab54ca694fa27d08f0689eacc32e4aaef73b5d312d`  
		Last Modified: Thu, 02 Apr 2026 18:44:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eae20ec88cee3844e342651770821d536c7cf1744e37e35478a12df2516c6a`  
		Last Modified: Thu, 02 Apr 2026 18:44:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c86583d6d7d279ff9d1665918cf26dcb2959c8f4b304dec44a6eadeff8c253ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70afa005db939913c600d362a67652c4f4900a40e548ad64746631f56d565b1e`

```dockerfile
```

-	Layers:
	-	`sha256:c6be00219b3a6cd93a85bf7078b6a39f34e57418cae4d3220ef70fbaba9c3600`  
		Last Modified: Thu, 02 Apr 2026 18:44:48 GMT  
		Size: 6.5 MB (6460552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4df36f5e74eb137c6416523ffaae11205c80dc2aa58b4ab3a8d515720b2e914`  
		Last Modified: Thu, 02 Apr 2026 18:44:47 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
