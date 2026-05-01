<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.7`](#crate627)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:4b6ab7c094aea706e3761e8ee0817ce3a5ac605f256263cada93294bf52dd228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:d7cd2897ee79d6a90744cc83a6318d1bb1f1ce0646cd9c0315938866d7c9c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243640750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a1c799dfa0834c5b71f727b8184df84ba338dee4d85dc09c10335efadb0452`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:35 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 28 Apr 2026 00:05:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92a95f7a1e7a7f35d079beb695ed32dd7e7a5db3a077024c5c0cb729d805b9b`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 18.4 MB (18366560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be86a6bee0b487862befe1f8c10a8a41f7accbee5b2169dca999e6623bf824c7`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 149.0 MB (149020498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedaec8fabe1e76ec5bcc5d31b48dd6711e75bde62a3bfba70afec5b63191692`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 7.7 MB (7699374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89b061f0fb95224dbfc91b8c396fba6554c48f0bed0411c49716836915d492b`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941862d64ea33bd67b6cf6ae97c1e8b32ed1770515d0fc78ffef104546bce8b7`  
		Last Modified: Tue, 28 Apr 2026 00:05:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b3dda2c3480fb15faeae5f614394fc5ff6680a53e04d0b1d299101af4061e`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6efb28e520c9b6fb1268e3e0fc44bc053b48cb1cf83111b427d278be34fed4`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:90a4f6a15c239edaf68e870734bc5c383c8c92551a9f00a21e26c9319615af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bad82995ce30a3a85a8002671955fd2a25b8662bb3c9c56cf52279c00dcd231`

```dockerfile
```

-	Layers:
	-	`sha256:e1bfe80d9895bf9b21ed9330a7e103a7c18d0b4ee4a827d8628aec21aa6123c3`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 6.7 MB (6652275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5416d77c3bd5bad60b43d50228aee2489e165861e356eb3696fcfad24d6c11ad`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bbcb7351d0bf1bb630e489bcac01b532d6f4ac461f5cd6cc400504cb50a55b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242965815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7978fabc03bd613e7dac04b066cc4af51b3c4cd01ba52312c3e093d22763f527`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:30 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 28 Apr 2026 00:05:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3c48aea421b5286b02f709b6f70fce900bcaad327ed34e0ae9bd0fbb91487`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 18.4 MB (18416217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118ab4af716273200c4b1eb8746edd1c88dbc448720fc1141dc838def54b476`  
		Last Modified: Tue, 28 Apr 2026 00:05:54 GMT  
		Size: 149.7 MB (149712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f61835965961fcc80146154207971bdab843fd1ba4d8a9772a146469ea154a`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 7.7 MB (7696828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8763df240918324d37d97e2bdeb82e9f0fd82fc7f63b99a67d5eb2b9712bad9`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e720ba3256b3c3b80350e27b3a452a6a541fc91afcd3c4983bcf60ad6a3313b3`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a787adb903ff1bc75e878a0abfbef04fcc62a2c062804dd9fa046d02f207998d`  
		Last Modified: Tue, 28 Apr 2026 00:05:51 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b72eb9866e2d83522494aba11fddf1132259c73d9437b815a91982c9c527d`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:e3c5d0549cd91c05c34f0a24b0169681761469091a81ae56e91b87df55e29745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881802cf25f43893a06891682305d7ed6b61273b138dfa352093b44e2c5a8b12`

```dockerfile
```

-	Layers:
	-	`sha256:fe32bd6070bdc5de1a4b78f5a57ce864e50a2c94dd1188205cdb32630b258189`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 6.7 MB (6650187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e47e4649e848619fb0da96ef9333b0a18fade953f37303333804f5a3f1e740`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:4b6ab7c094aea706e3761e8ee0817ce3a5ac605f256263cada93294bf52dd228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:d7cd2897ee79d6a90744cc83a6318d1bb1f1ce0646cd9c0315938866d7c9c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243640750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a1c799dfa0834c5b71f727b8184df84ba338dee4d85dc09c10335efadb0452`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:35 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 28 Apr 2026 00:05:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92a95f7a1e7a7f35d079beb695ed32dd7e7a5db3a077024c5c0cb729d805b9b`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 18.4 MB (18366560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be86a6bee0b487862befe1f8c10a8a41f7accbee5b2169dca999e6623bf824c7`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 149.0 MB (149020498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedaec8fabe1e76ec5bcc5d31b48dd6711e75bde62a3bfba70afec5b63191692`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 7.7 MB (7699374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89b061f0fb95224dbfc91b8c396fba6554c48f0bed0411c49716836915d492b`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941862d64ea33bd67b6cf6ae97c1e8b32ed1770515d0fc78ffef104546bce8b7`  
		Last Modified: Tue, 28 Apr 2026 00:05:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b3dda2c3480fb15faeae5f614394fc5ff6680a53e04d0b1d299101af4061e`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6efb28e520c9b6fb1268e3e0fc44bc053b48cb1cf83111b427d278be34fed4`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:90a4f6a15c239edaf68e870734bc5c383c8c92551a9f00a21e26c9319615af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bad82995ce30a3a85a8002671955fd2a25b8662bb3c9c56cf52279c00dcd231`

```dockerfile
```

-	Layers:
	-	`sha256:e1bfe80d9895bf9b21ed9330a7e103a7c18d0b4ee4a827d8628aec21aa6123c3`  
		Last Modified: Tue, 28 Apr 2026 00:05:53 GMT  
		Size: 6.7 MB (6652275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5416d77c3bd5bad60b43d50228aee2489e165861e356eb3696fcfad24d6c11ad`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bbcb7351d0bf1bb630e489bcac01b532d6f4ac461f5cd6cc400504cb50a55b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242965815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7978fabc03bd613e7dac04b066cc4af51b3c4cd01ba52312c3e093d22763f527`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:30 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 28 Apr 2026 00:05:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3c48aea421b5286b02f709b6f70fce900bcaad327ed34e0ae9bd0fbb91487`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 18.4 MB (18416217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118ab4af716273200c4b1eb8746edd1c88dbc448720fc1141dc838def54b476`  
		Last Modified: Tue, 28 Apr 2026 00:05:54 GMT  
		Size: 149.7 MB (149712802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f61835965961fcc80146154207971bdab843fd1ba4d8a9772a146469ea154a`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 7.7 MB (7696828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8763df240918324d37d97e2bdeb82e9f0fd82fc7f63b99a67d5eb2b9712bad9`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e720ba3256b3c3b80350e27b3a452a6a541fc91afcd3c4983bcf60ad6a3313b3`  
		Last Modified: Tue, 28 Apr 2026 00:05:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a787adb903ff1bc75e878a0abfbef04fcc62a2c062804dd9fa046d02f207998d`  
		Last Modified: Tue, 28 Apr 2026 00:05:51 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b72eb9866e2d83522494aba11fddf1132259c73d9437b815a91982c9c527d`  
		Last Modified: Tue, 28 Apr 2026 00:05:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:e3c5d0549cd91c05c34f0a24b0169681761469091a81ae56e91b87df55e29745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881802cf25f43893a06891682305d7ed6b61273b138dfa352093b44e2c5a8b12`

```dockerfile
```

-	Layers:
	-	`sha256:fe32bd6070bdc5de1a4b78f5a57ce864e50a2c94dd1188205cdb32630b258189`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 6.7 MB (6650187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e47e4649e848619fb0da96ef9333b0a18fade953f37303333804f5a3f1e740`  
		Last Modified: Tue, 28 Apr 2026 00:05:49 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:e63ad3494ff056dce2488247034a04d3f4fdfca0c804f1a58e795bed08d2734e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:610238755a68c483ba683b8add557f6f42d01b00cd1c9856430539f3f6cc3300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243769095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a536e392292fd77711408205526158d24de4bd88a23ed14b1359faa84be00a97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:37 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 28 Apr 2026 00:05:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3d7901ca345d362637ba4f1048b7a80b9a026912c574adf0dcd23e121eafa`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 18.4 MB (18366605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a78dbd830c25df3a75fcb6d93cf63444880b3b4731f2d6ee0abfe5d53bda6c7`  
		Last Modified: Tue, 28 Apr 2026 00:05:59 GMT  
		Size: 149.1 MB (149148283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a6bd362343736a5d68a5d7797489c5f8c6a6dad03861f949be506a46ec7d2`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 7.7 MB (7699889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d277bbba7ee32b2ea30e26ad4e39dcac14b13f251ddd8b9677b85663adf8dba5`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf7053dabb4da5d1f5a285ed69990e567f6bbf79447610d302124e08b14d40e`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7d7665be7146d280fedbfd9ad26faa3efbc337f2433552539272488716ca1`  
		Last Modified: Tue, 28 Apr 2026 00:05:57 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91330661f83b50b695c198ad3f606eb1d76aa910ab4cdfbac107df73d75b6e0e`  
		Last Modified: Tue, 28 Apr 2026 00:05:58 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:c694476a0f609aa27c2657ee9d8a957eb0d9a1ec918e1e08e8a94098cf78a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae61161ccb30791312f75d73c8a0e61749529f95c1380af9e31a24c7e33401`

```dockerfile
```

-	Layers:
	-	`sha256:e83a26eebbd63684ee418b809050e695532013c6d27cd42cb7db6efa07ea6ace`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 6.7 MB (6651059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20544d5495b040e14641fff615557e1b009fe3f82a9aeb3aa70239225ee23998`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aac43916c3ce6ebe7be181ffb323e8d3494fb8b93d356867fc94dd3d3c1ad7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243091848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c775b39477824c999c3db928bc29bd22d04672a45a5350d7c082c738bea7f0da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:39 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:57 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:58 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:58 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:58 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:58 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:58 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 28 Apr 2026 00:05:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:58 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368cf568adb277f4282bcc67d6f7b1d868f2bd5163e2c197ba8eb0fbae5a4f53`  
		Last Modified: Tue, 28 Apr 2026 00:06:22 GMT  
		Size: 18.4 MB (18416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56feca059c2eeaa34f83ed4a8501bdefcbf9fb1da7bbdb5a916f85fb1170612`  
		Last Modified: Tue, 28 Apr 2026 00:06:28 GMT  
		Size: 149.8 MB (149838523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe0b3061370507167525a6344b9fff101d856b0d2bf75a32b5ebc08d1af127f`  
		Last Modified: Tue, 28 Apr 2026 00:06:21 GMT  
		Size: 7.7 MB (7697046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa85bfe9f78bbed5bf5429bcfad4e85a033540d6828edfbb6454b85f5ebf13d`  
		Last Modified: Tue, 28 Apr 2026 00:06:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cba28ff07f9bab6435d035e70ba4e373c1e2edc2a4ac6f0ead575e6f5cdc5a`  
		Last Modified: Tue, 28 Apr 2026 00:06:21 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4737434aaa6648dc301af449d8cdc7ddc32d594cdd262d3349beed3f4efaf41`  
		Last Modified: Tue, 28 Apr 2026 00:06:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91330661f83b50b695c198ad3f606eb1d76aa910ab4cdfbac107df73d75b6e0e`  
		Last Modified: Tue, 28 Apr 2026 00:05:58 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:899eee0ee59fabd5110241c8172c6f600d8833948dc6ae8de006c07d1a1ee404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07d1da5147a06fab4c8b22a2444affbcf818a6e31eb95b998ea27faf3f4b3cd`

```dockerfile
```

-	Layers:
	-	`sha256:724c15f0f4f717db23684e0f526b85b9d8cd8ebd7781e16ae0ceb17fa8461726`  
		Last Modified: Tue, 28 Apr 2026 00:06:20 GMT  
		Size: 6.6 MB (6648971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69b37408cb0a61e41c154ed861c2600d488b701ade4da2d4ff02e2b0eef1057`  
		Last Modified: Tue, 28 Apr 2026 00:06:19 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:e63ad3494ff056dce2488247034a04d3f4fdfca0c804f1a58e795bed08d2734e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:610238755a68c483ba683b8add557f6f42d01b00cd1c9856430539f3f6cc3300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243769095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a536e392292fd77711408205526158d24de4bd88a23ed14b1359faa84be00a97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:37 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 28 Apr 2026 00:05:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3d7901ca345d362637ba4f1048b7a80b9a026912c574adf0dcd23e121eafa`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 18.4 MB (18366605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a78dbd830c25df3a75fcb6d93cf63444880b3b4731f2d6ee0abfe5d53bda6c7`  
		Last Modified: Tue, 28 Apr 2026 00:05:59 GMT  
		Size: 149.1 MB (149148283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a6bd362343736a5d68a5d7797489c5f8c6a6dad03861f949be506a46ec7d2`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 7.7 MB (7699889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d277bbba7ee32b2ea30e26ad4e39dcac14b13f251ddd8b9677b85663adf8dba5`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf7053dabb4da5d1f5a285ed69990e567f6bbf79447610d302124e08b14d40e`  
		Last Modified: Tue, 28 Apr 2026 00:05:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7d7665be7146d280fedbfd9ad26faa3efbc337f2433552539272488716ca1`  
		Last Modified: Tue, 28 Apr 2026 00:05:57 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91330661f83b50b695c198ad3f606eb1d76aa910ab4cdfbac107df73d75b6e0e`  
		Last Modified: Tue, 28 Apr 2026 00:05:58 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:c694476a0f609aa27c2657ee9d8a957eb0d9a1ec918e1e08e8a94098cf78a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae61161ccb30791312f75d73c8a0e61749529f95c1380af9e31a24c7e33401`

```dockerfile
```

-	Layers:
	-	`sha256:e83a26eebbd63684ee418b809050e695532013c6d27cd42cb7db6efa07ea6ace`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 6.7 MB (6651059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20544d5495b040e14641fff615557e1b009fe3f82a9aeb3aa70239225ee23998`  
		Last Modified: Tue, 28 Apr 2026 00:05:55 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aac43916c3ce6ebe7be181ffb323e8d3494fb8b93d356867fc94dd3d3c1ad7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243091848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c775b39477824c999c3db928bc29bd22d04672a45a5350d7c082c738bea7f0da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 00:05:39 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 28 Apr 2026 00:05:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 28 Apr 2026 00:05:57 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:05:58 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Apr 2026 00:05:58 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
VOLUME [/data]
# Tue, 28 Apr 2026 00:05:58 GMT
WORKDIR /data
# Tue, 28 Apr 2026 00:05:58 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 28 Apr 2026 00:05:58 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 28 Apr 2026 00:05:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Apr 2026 00:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:05:58 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368cf568adb277f4282bcc67d6f7b1d868f2bd5163e2c197ba8eb0fbae5a4f53`  
		Last Modified: Tue, 28 Apr 2026 00:06:22 GMT  
		Size: 18.4 MB (18416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56feca059c2eeaa34f83ed4a8501bdefcbf9fb1da7bbdb5a916f85fb1170612`  
		Last Modified: Tue, 28 Apr 2026 00:06:28 GMT  
		Size: 149.8 MB (149838523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe0b3061370507167525a6344b9fff101d856b0d2bf75a32b5ebc08d1af127f`  
		Last Modified: Tue, 28 Apr 2026 00:06:21 GMT  
		Size: 7.7 MB (7697046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa85bfe9f78bbed5bf5429bcfad4e85a033540d6828edfbb6454b85f5ebf13d`  
		Last Modified: Tue, 28 Apr 2026 00:06:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cba28ff07f9bab6435d035e70ba4e373c1e2edc2a4ac6f0ead575e6f5cdc5a`  
		Last Modified: Tue, 28 Apr 2026 00:06:21 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4737434aaa6648dc301af449d8cdc7ddc32d594cdd262d3349beed3f4efaf41`  
		Last Modified: Tue, 28 Apr 2026 00:06:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91330661f83b50b695c198ad3f606eb1d76aa910ab4cdfbac107df73d75b6e0e`  
		Last Modified: Tue, 28 Apr 2026 00:05:58 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:899eee0ee59fabd5110241c8172c6f600d8833948dc6ae8de006c07d1a1ee404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07d1da5147a06fab4c8b22a2444affbcf818a6e31eb95b998ea27faf3f4b3cd`

```dockerfile
```

-	Layers:
	-	`sha256:724c15f0f4f717db23684e0f526b85b9d8cd8ebd7781e16ae0ceb17fa8461726`  
		Last Modified: Tue, 28 Apr 2026 00:06:20 GMT  
		Size: 6.6 MB (6648971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69b37408cb0a61e41c154ed861c2600d488b701ade4da2d4ff02e2b0eef1057`  
		Last Modified: Tue, 28 Apr 2026 00:06:19 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:f9d72d76c78836f3bb9c9ad423f065bb4df683b6bb6eed9a160beea4e6ac3255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:df824933c4be1d912229786ab34c92719d4b924abf4e1c0e9144e0e2f7544dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245938958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eea202967fd6810dd8966c97b3c1f91c81f270330f0fc8ba471ebab2a2d5af5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:25:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:25:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:25:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:25:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:25:40 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:25:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:25:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:25:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50537d3e35d5db283eea8a2e0650d49f4045de9041e7fb9574e8e7d749c0a5`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 18.4 MB (18367506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119834775cb5dab48b3e2c3ac7ca2a1df3b548546b30b7654c6e1b5d7439a18`  
		Last Modified: Thu, 30 Apr 2026 23:26:03 GMT  
		Size: 151.3 MB (151317597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f521aac87aa3fb6f908eb00e514c4d15c451ea21ed7fa6b53796123fcbecf1d`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 7.7 MB (7699535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6f793a004d96b30d2309cebabd4d689355975301f9d3c795ef5d5a24d25eb`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e449a28970ee3ec5483dce75c08f8e24ed220c62dad40d2fecef58bad31da5`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310ea6165f6bf994ef651fa9d8baf5b61de593e8507b20c92efbf1309c5e7ff`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cb11a9d82750eb52f895edb7281c15be9782c1c3f9f1d9380423ad8d2706d`  
		Last Modified: Thu, 30 Apr 2026 23:26:02 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:03ea6a7f6f388bde09db4802b45dd6633acfb61f47cd80ddaf868b2deebd9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4c48fd29935747a8e0739d37fdc5f01e3b5e0981132b6b0a3ec1db7353d13c`

```dockerfile
```

-	Layers:
	-	`sha256:5bf06b0c62586a51ed4f06cd6c52775b0cb19310a80d5c98716e04a41a14efb4`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 6.7 MB (6656883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7457cfe3bbdf651b75584d9f44a905a19e5311cbe24d74bc068d1071d1e5ad3`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1e42ebb83d303420863d862142cb0c7692b2cac278aa434d7e8daa1f7ad91c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242536163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde23c10d541527a8290cb623fadbdeb597ca144bbdec9a73539fe19455d8b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:26:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:26:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:26:22 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:26:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:26:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e79055875104e491b1adaa789299c82fcc794fd3b0495f5b51ca807812d2d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 18.4 MB (18416446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e091587ec4dc15bdd40ff5c61a1060f08f8a3f72575ddd13becf423a86ec3648`  
		Last Modified: Thu, 30 Apr 2026 23:26:48 GMT  
		Size: 149.3 MB (149282817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea96a8025503f892c67b0a96e651ac3c26be6236f7b25b171da0cdba59db30`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 7.7 MB (7696932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e57c29095ed18fe8a10de33548b6f3e2673f80954a32bd4a58ac1e9a7fce1`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a0bd00aab25109bfb071eb55234565307272e71f45338ed1aa1535154dc4e`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce01436e258c79187258e4970fec0062061030e17305af6f604b81d4696d36`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42064fcf1b7c6a2ea1a881d5782b11c87ad1655601236bcb7522de8a3b77e06`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:486f0d0b1d300757b2d88cec3f6330325a1c9b44d8e64d12da3639e70ba15b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a428e8d8b417170fb8c135d9f4524a5db5fd71818ef330049d2011da61afac`

```dockerfile
```

-	Layers:
	-	`sha256:2d6e9995c4dd26d0a352584ff180fa467bc70e05b1a147cc8df6642f82020e76`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 6.7 MB (6654807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce6f847c0415d626da65c7195c89c4471634b94720d3426c883089188821587`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 21.8 KB (21776 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.7`

```console
$ docker pull crate@sha256:f9d72d76c78836f3bb9c9ad423f065bb4df683b6bb6eed9a160beea4e6ac3255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.7` - linux; amd64

```console
$ docker pull crate@sha256:df824933c4be1d912229786ab34c92719d4b924abf4e1c0e9144e0e2f7544dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245938958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eea202967fd6810dd8966c97b3c1f91c81f270330f0fc8ba471ebab2a2d5af5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:25:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:25:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:25:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:25:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:25:40 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:25:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:25:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:25:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50537d3e35d5db283eea8a2e0650d49f4045de9041e7fb9574e8e7d749c0a5`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 18.4 MB (18367506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119834775cb5dab48b3e2c3ac7ca2a1df3b548546b30b7654c6e1b5d7439a18`  
		Last Modified: Thu, 30 Apr 2026 23:26:03 GMT  
		Size: 151.3 MB (151317597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f521aac87aa3fb6f908eb00e514c4d15c451ea21ed7fa6b53796123fcbecf1d`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 7.7 MB (7699535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6f793a004d96b30d2309cebabd4d689355975301f9d3c795ef5d5a24d25eb`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e449a28970ee3ec5483dce75c08f8e24ed220c62dad40d2fecef58bad31da5`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310ea6165f6bf994ef651fa9d8baf5b61de593e8507b20c92efbf1309c5e7ff`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cb11a9d82750eb52f895edb7281c15be9782c1c3f9f1d9380423ad8d2706d`  
		Last Modified: Thu, 30 Apr 2026 23:26:02 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:03ea6a7f6f388bde09db4802b45dd6633acfb61f47cd80ddaf868b2deebd9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4c48fd29935747a8e0739d37fdc5f01e3b5e0981132b6b0a3ec1db7353d13c`

```dockerfile
```

-	Layers:
	-	`sha256:5bf06b0c62586a51ed4f06cd6c52775b0cb19310a80d5c98716e04a41a14efb4`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 6.7 MB (6656883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7457cfe3bbdf651b75584d9f44a905a19e5311cbe24d74bc068d1071d1e5ad3`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1e42ebb83d303420863d862142cb0c7692b2cac278aa434d7e8daa1f7ad91c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242536163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde23c10d541527a8290cb623fadbdeb597ca144bbdec9a73539fe19455d8b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:26:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:26:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:26:22 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:26:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:26:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e79055875104e491b1adaa789299c82fcc794fd3b0495f5b51ca807812d2d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 18.4 MB (18416446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e091587ec4dc15bdd40ff5c61a1060f08f8a3f72575ddd13becf423a86ec3648`  
		Last Modified: Thu, 30 Apr 2026 23:26:48 GMT  
		Size: 149.3 MB (149282817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea96a8025503f892c67b0a96e651ac3c26be6236f7b25b171da0cdba59db30`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 7.7 MB (7696932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e57c29095ed18fe8a10de33548b6f3e2673f80954a32bd4a58ac1e9a7fce1`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a0bd00aab25109bfb071eb55234565307272e71f45338ed1aa1535154dc4e`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce01436e258c79187258e4970fec0062061030e17305af6f604b81d4696d36`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42064fcf1b7c6a2ea1a881d5782b11c87ad1655601236bcb7522de8a3b77e06`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:486f0d0b1d300757b2d88cec3f6330325a1c9b44d8e64d12da3639e70ba15b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a428e8d8b417170fb8c135d9f4524a5db5fd71818ef330049d2011da61afac`

```dockerfile
```

-	Layers:
	-	`sha256:2d6e9995c4dd26d0a352584ff180fa467bc70e05b1a147cc8df6642f82020e76`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 6.7 MB (6654807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce6f847c0415d626da65c7195c89c4471634b94720d3426c883089188821587`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 21.8 KB (21776 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:f9d72d76c78836f3bb9c9ad423f065bb4df683b6bb6eed9a160beea4e6ac3255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:df824933c4be1d912229786ab34c92719d4b924abf4e1c0e9144e0e2f7544dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245938958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eea202967fd6810dd8966c97b3c1f91c81f270330f0fc8ba471ebab2a2d5af5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:25:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:25:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:25:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:25:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:25:40 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:25:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:25:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:25:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50537d3e35d5db283eea8a2e0650d49f4045de9041e7fb9574e8e7d749c0a5`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 18.4 MB (18367506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119834775cb5dab48b3e2c3ac7ca2a1df3b548546b30b7654c6e1b5d7439a18`  
		Last Modified: Thu, 30 Apr 2026 23:26:03 GMT  
		Size: 151.3 MB (151317597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f521aac87aa3fb6f908eb00e514c4d15c451ea21ed7fa6b53796123fcbecf1d`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 7.7 MB (7699535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6f793a004d96b30d2309cebabd4d689355975301f9d3c795ef5d5a24d25eb`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e449a28970ee3ec5483dce75c08f8e24ed220c62dad40d2fecef58bad31da5`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310ea6165f6bf994ef651fa9d8baf5b61de593e8507b20c92efbf1309c5e7ff`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cb11a9d82750eb52f895edb7281c15be9782c1c3f9f1d9380423ad8d2706d`  
		Last Modified: Thu, 30 Apr 2026 23:26:02 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:03ea6a7f6f388bde09db4802b45dd6633acfb61f47cd80ddaf868b2deebd9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4c48fd29935747a8e0739d37fdc5f01e3b5e0981132b6b0a3ec1db7353d13c`

```dockerfile
```

-	Layers:
	-	`sha256:5bf06b0c62586a51ed4f06cd6c52775b0cb19310a80d5c98716e04a41a14efb4`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 6.7 MB (6656883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7457cfe3bbdf651b75584d9f44a905a19e5311cbe24d74bc068d1071d1e5ad3`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1e42ebb83d303420863d862142cb0c7692b2cac278aa434d7e8daa1f7ad91c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242536163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde23c10d541527a8290cb623fadbdeb597ca144bbdec9a73539fe19455d8b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:26:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:26:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:26:22 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:26:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:26:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e79055875104e491b1adaa789299c82fcc794fd3b0495f5b51ca807812d2d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 18.4 MB (18416446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e091587ec4dc15bdd40ff5c61a1060f08f8a3f72575ddd13becf423a86ec3648`  
		Last Modified: Thu, 30 Apr 2026 23:26:48 GMT  
		Size: 149.3 MB (149282817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea96a8025503f892c67b0a96e651ac3c26be6236f7b25b171da0cdba59db30`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 7.7 MB (7696932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e57c29095ed18fe8a10de33548b6f3e2673f80954a32bd4a58ac1e9a7fce1`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a0bd00aab25109bfb071eb55234565307272e71f45338ed1aa1535154dc4e`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce01436e258c79187258e4970fec0062061030e17305af6f604b81d4696d36`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42064fcf1b7c6a2ea1a881d5782b11c87ad1655601236bcb7522de8a3b77e06`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:486f0d0b1d300757b2d88cec3f6330325a1c9b44d8e64d12da3639e70ba15b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a428e8d8b417170fb8c135d9f4524a5db5fd71818ef330049d2011da61afac`

```dockerfile
```

-	Layers:
	-	`sha256:2d6e9995c4dd26d0a352584ff180fa467bc70e05b1a147cc8df6642f82020e76`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 6.7 MB (6654807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce6f847c0415d626da65c7195c89c4471634b94720d3426c883089188821587`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 21.8 KB (21776 bytes)  
		MIME: application/vnd.in-toto+json
