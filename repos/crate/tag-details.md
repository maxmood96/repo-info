<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.14`](#crate51014)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.3`](#crate603)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:6ad6d93dfcc65da1bab2a6617eb0c7c86a1868693a46864150c9496bbaef22d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:b051d622acb6be465625dd730c8313692733cb920092c31f30a87ac3ba09efb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233229637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d952b6ef7ac6c61e24572035af3c9ce6ef1b412b90d61df8b5daab563e2fb4af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 17:28:13 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 06 Nov 2025 17:28:25 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 17:28:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 06 Nov 2025 17:28:28 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
VOLUME [/data]
# Thu, 06 Nov 2025 17:28:28 GMT
WORKDIR /data
# Thu, 06 Nov 2025 17:28:28 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 06 Nov 2025 17:28:28 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Thu, 06 Nov 2025 17:28:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 17:28:28 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d276e68a6e211a38e7e159f09492adedddd7faeaba8e6af9c5e085eb644ac912`  
		Last Modified: Thu, 06 Nov 2025 17:28:57 GMT  
		Size: 14.5 MB (14534439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84784ce3728476385edba08b51bc5e8fcac5c4baf7a9b1fc1911328a9dccb9`  
		Last Modified: Thu, 06 Nov 2025 17:29:42 GMT  
		Size: 149.7 MB (149720636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857d0d1bc3193c137179665870e6226543770a079066f40644ec5ddf486116a`  
		Last Modified: Thu, 06 Nov 2025 17:28:57 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab29e0737f5fd58084f5eda9c178a758e0196b3e3691f007dc7061994a9b12dc`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26458b9f0613e98d9e8bca741b43498d4655e6172f67c458ed89f6ab95b7087d`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc4ce81cb8d30e2e6a654bf26cb45f141b4fb1e8ec4fd886c340a7f95682c0`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f013afee3e76323a78f28c520ed765b7a72f184bb7473cb45c7fc9b6747799`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:aef90fdf01321dfa6b35ab83d2ee0268a4b112a979df0aeb0ee4d23e8ba1004e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48013012c78bbeadfff02e6ea69ca3d79a6313280f809ec10e7d0d0439e5051`

```dockerfile
```

-	Layers:
	-	`sha256:c31acf4690bc5baf8401ecda23dadb0b8a814faaa4cdca208264c29114ac11cf`  
		Last Modified: Thu, 06 Nov 2025 18:38:34 GMT  
		Size: 5.2 MB (5188129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1fa5ec1eff278be86dca1068c06796b52efea260140534d47b91f2f86891fb5`  
		Last Modified: Thu, 06 Nov 2025 18:38:35 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:02bbea8a13eba5cddf635888d253711aee67d646f6356f671d0aaa50cac0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232447829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54e77382c9dda4124aa6381855e6a678cac2c86afb31cdd539dfe71da3c12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 17:28:23 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 06 Nov 2025 17:28:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 17:28:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 06 Nov 2025 17:28:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
VOLUME [/data]
# Thu, 06 Nov 2025 17:28:37 GMT
WORKDIR /data
# Thu, 06 Nov 2025 17:28:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 06 Nov 2025 17:28:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Thu, 06 Nov 2025 17:28:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 17:28:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0438e4150d5e9d47f93372e58b0d7acfac0da4885d67099bd5a56779c9a1b730`  
		Last Modified: Thu, 06 Nov 2025 17:29:08 GMT  
		Size: 14.6 MB (14585523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30752bef137ece15f31faf4c43e0f6f259ac1321ab9a2c9540036f4952dd4c5e`  
		Last Modified: Thu, 06 Nov 2025 22:58:52 GMT  
		Size: 150.4 MB (150398796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b1d73000d2868a147a21cd5a84951dfa62b58804454469cf4e83a76240e575`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a055aacbec6884812a510339e6db9e522678f5d77763e30f0406176c2205652`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f507c45bc6e356c7ed8a8d25fbe375394fd430f30a20a9fe5da6af05a213c9a`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec99532559dfd151ebeb3506b19f15b2b6428621d17a4706412c3c6aed0c2`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1f9d82aa3a525ecd30a6491bca7d67800eaba95e36c2a9abb8938e048dfec3`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:00c6b8d9df7bc682e6248986e01689dd8318d200e9ad05c5004bce790b8e53d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2eae9d30d1d30cb06d44bf0c2b132cccfed2c9b2b4e9226bc0b6b397a364d8`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a5bb04cce4d1e0cdb733b34b018a41a7d6e72d8c42782694f577e52b6400b`  
		Last Modified: Thu, 06 Nov 2025 18:38:40 GMT  
		Size: 5.2 MB (5185425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ed399f3c807064d53411c99c0ee508992af32c80d4cc51ff01c529d0f708f0`  
		Last Modified: Thu, 06 Nov 2025 18:38:41 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.14`

```console
$ docker pull crate@sha256:6ad6d93dfcc65da1bab2a6617eb0c7c86a1868693a46864150c9496bbaef22d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.14` - linux; amd64

```console
$ docker pull crate@sha256:b051d622acb6be465625dd730c8313692733cb920092c31f30a87ac3ba09efb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233229637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d952b6ef7ac6c61e24572035af3c9ce6ef1b412b90d61df8b5daab563e2fb4af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 17:28:13 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 06 Nov 2025 17:28:25 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 17:28:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 06 Nov 2025 17:28:28 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
VOLUME [/data]
# Thu, 06 Nov 2025 17:28:28 GMT
WORKDIR /data
# Thu, 06 Nov 2025 17:28:28 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 06 Nov 2025 17:28:28 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Thu, 06 Nov 2025 17:28:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 17:28:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 17:28:28 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d276e68a6e211a38e7e159f09492adedddd7faeaba8e6af9c5e085eb644ac912`  
		Last Modified: Thu, 06 Nov 2025 17:28:57 GMT  
		Size: 14.5 MB (14534439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84784ce3728476385edba08b51bc5e8fcac5c4baf7a9b1fc1911328a9dccb9`  
		Last Modified: Thu, 06 Nov 2025 17:29:42 GMT  
		Size: 149.7 MB (149720636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857d0d1bc3193c137179665870e6226543770a079066f40644ec5ddf486116a`  
		Last Modified: Thu, 06 Nov 2025 17:28:57 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab29e0737f5fd58084f5eda9c178a758e0196b3e3691f007dc7061994a9b12dc`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26458b9f0613e98d9e8bca741b43498d4655e6172f67c458ed89f6ab95b7087d`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc4ce81cb8d30e2e6a654bf26cb45f141b4fb1e8ec4fd886c340a7f95682c0`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f013afee3e76323a78f28c520ed765b7a72f184bb7473cb45c7fc9b6747799`  
		Last Modified: Thu, 06 Nov 2025 17:28:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.14` - unknown; unknown

```console
$ docker pull crate@sha256:aef90fdf01321dfa6b35ab83d2ee0268a4b112a979df0aeb0ee4d23e8ba1004e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48013012c78bbeadfff02e6ea69ca3d79a6313280f809ec10e7d0d0439e5051`

```dockerfile
```

-	Layers:
	-	`sha256:c31acf4690bc5baf8401ecda23dadb0b8a814faaa4cdca208264c29114ac11cf`  
		Last Modified: Thu, 06 Nov 2025 18:38:34 GMT  
		Size: 5.2 MB (5188129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1fa5ec1eff278be86dca1068c06796b52efea260140534d47b91f2f86891fb5`  
		Last Modified: Thu, 06 Nov 2025 18:38:35 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.14` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:02bbea8a13eba5cddf635888d253711aee67d646f6356f671d0aaa50cac0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232447829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54e77382c9dda4124aa6381855e6a678cac2c86afb31cdd539dfe71da3c12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 17:28:23 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 06 Nov 2025 17:28:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 17:28:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 06 Nov 2025 17:28:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
VOLUME [/data]
# Thu, 06 Nov 2025 17:28:37 GMT
WORKDIR /data
# Thu, 06 Nov 2025 17:28:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 06 Nov 2025 17:28:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Thu, 06 Nov 2025 17:28:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 17:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 17:28:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0438e4150d5e9d47f93372e58b0d7acfac0da4885d67099bd5a56779c9a1b730`  
		Last Modified: Thu, 06 Nov 2025 17:29:08 GMT  
		Size: 14.6 MB (14585523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30752bef137ece15f31faf4c43e0f6f259ac1321ab9a2c9540036f4952dd4c5e`  
		Last Modified: Thu, 06 Nov 2025 22:58:52 GMT  
		Size: 150.4 MB (150398796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b1d73000d2868a147a21cd5a84951dfa62b58804454469cf4e83a76240e575`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a055aacbec6884812a510339e6db9e522678f5d77763e30f0406176c2205652`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f507c45bc6e356c7ed8a8d25fbe375394fd430f30a20a9fe5da6af05a213c9a`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ec99532559dfd151ebeb3506b19f15b2b6428621d17a4706412c3c6aed0c2`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1f9d82aa3a525ecd30a6491bca7d67800eaba95e36c2a9abb8938e048dfec3`  
		Last Modified: Thu, 06 Nov 2025 17:29:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.14` - unknown; unknown

```console
$ docker pull crate@sha256:00c6b8d9df7bc682e6248986e01689dd8318d200e9ad05c5004bce790b8e53d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2eae9d30d1d30cb06d44bf0c2b132cccfed2c9b2b4e9226bc0b6b397a364d8`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a5bb04cce4d1e0cdb733b34b018a41a7d6e72d8c42782694f577e52b6400b`  
		Last Modified: Thu, 06 Nov 2025 18:38:40 GMT  
		Size: 5.2 MB (5185425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ed399f3c807064d53411c99c0ee508992af32c80d4cc51ff01c529d0f708f0`  
		Last Modified: Thu, 06 Nov 2025 18:38:41 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:a9948f3ed7b8984d2d3ab8019123852cee2b9d19333d12432c3b318167090710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:813ed0cdea3ec2c74b9a723decd92ba5447c1d1a86da5a45537d866de1da571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232534589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20580f8efcf6b5ed0fff03f528d235a3377335df72ea24342474fde8abf50c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa72b9a9687a3fdeab461aef880682ed5e111d019c6efcd7b5d66e4adcd32b`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 14.5 MB (14534324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1afe5cd5fff6ae2c8a4558e0be9d14199da25ceba36a96739ab01f11182460`  
		Last Modified: Thu, 16 Oct 2025 18:32:54 GMT  
		Size: 149.0 MB (149025700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865eeafcd1193101a872976bcd8de8c9091638e51f5a0504aacbfdaec5f63975`  
		Last Modified: Thu, 16 Oct 2025 18:32:38 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12875bb47a4594c7b83e1ceb84a23f2d047d194ee5cc01099d11b60732897efc`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720e2e1c54ae64d4941e7a5194cb4668c494eb59f57f65c2ef265680378056a2`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4611d4399efe580bfc490d9d209021f0688e3331598fbda12e2a24da61e7d1d`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e509bf4a30e6f0b3e017e5e3caa8a609c0aeb04ae454162c3e637b23b74e2b9`  
		Last Modified: Thu, 16 Oct 2025 18:32:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:792be79f6d84e535930ba8251750e70db9a303ad6e8cd8c2289a571dfb605feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00f67f7dde44d47dab6387dfea6cc9059472441ca4d12a6b8914d109ffa702`

```dockerfile
```

-	Layers:
	-	`sha256:115faf1ab6e66910438674be6db0b9dc5198d8168f7f1a4bae37d51bab3a6b10`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 5.2 MB (5191563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6796b4c1c7b40ab0124c1fb073c26e6fa1759c6ff0da6f72c415efe1606f21`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:446c34d96f894710257205f1bc01feb11b28a70356e496623f181904b3bdab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231763012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ef30ac82833939a440db22954c3ba4534e4bf4db76e99d0d99d8be426fc8e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee2c39130bfacf9515d5efc24ffb7082ef9cf1eb6582efaa417dc9ce65b9d7`  
		Last Modified: Thu, 16 Oct 2025 18:11:16 GMT  
		Size: 14.6 MB (14585576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b8821d5c5c11a572869e76b33d7b289886da091905ea7891989761602b28ac`  
		Last Modified: Thu, 16 Oct 2025 18:53:15 GMT  
		Size: 149.7 MB (149713921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a831a008cd327b103097dc472e34bd4555576e82684c2961ea3b8323a127e2`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e972aeccefde64f644ab5aec99738cce3b1db4927732885f7b2bab2d609042`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48c171ee965d9e3dedc0dfd62132da4c78be2e1b331c5dda234906960d036`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8957e4fea405a8c569e5a4e53c317ffd464cd35ab699910f4aa019246fd1004c`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e0d2187cb639e180b97f0ce2e9c24b02f95fb751dbde54e7e5507181226ada`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:d84e171a0c663626ed9db8490d05f5e5f4b99cb28689746bd4c565fc9fe02325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e168fde894b5948ac03ec7363d2cc4362e56d2409ddb5521a511869025e778`

```dockerfile
```

-	Layers:
	-	`sha256:e483f4f765e3180c51a0e44f11307861f56a8c5848af11b856e2a4a22c617bae`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 5.2 MB (5189482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f908ee93abf4c77ad4f51611c4b7ee1b389abfa692da82927fb216eb2bc7d813`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.3`

```console
$ docker pull crate@sha256:a9948f3ed7b8984d2d3ab8019123852cee2b9d19333d12432c3b318167090710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.3` - linux; amd64

```console
$ docker pull crate@sha256:813ed0cdea3ec2c74b9a723decd92ba5447c1d1a86da5a45537d866de1da571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232534589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20580f8efcf6b5ed0fff03f528d235a3377335df72ea24342474fde8abf50c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa72b9a9687a3fdeab461aef880682ed5e111d019c6efcd7b5d66e4adcd32b`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 14.5 MB (14534324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1afe5cd5fff6ae2c8a4558e0be9d14199da25ceba36a96739ab01f11182460`  
		Last Modified: Thu, 16 Oct 2025 18:32:54 GMT  
		Size: 149.0 MB (149025700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865eeafcd1193101a872976bcd8de8c9091638e51f5a0504aacbfdaec5f63975`  
		Last Modified: Thu, 16 Oct 2025 18:32:38 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12875bb47a4594c7b83e1ceb84a23f2d047d194ee5cc01099d11b60732897efc`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720e2e1c54ae64d4941e7a5194cb4668c494eb59f57f65c2ef265680378056a2`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4611d4399efe580bfc490d9d209021f0688e3331598fbda12e2a24da61e7d1d`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e509bf4a30e6f0b3e017e5e3caa8a609c0aeb04ae454162c3e637b23b74e2b9`  
		Last Modified: Thu, 16 Oct 2025 18:32:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.3` - unknown; unknown

```console
$ docker pull crate@sha256:792be79f6d84e535930ba8251750e70db9a303ad6e8cd8c2289a571dfb605feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00f67f7dde44d47dab6387dfea6cc9059472441ca4d12a6b8914d109ffa702`

```dockerfile
```

-	Layers:
	-	`sha256:115faf1ab6e66910438674be6db0b9dc5198d8168f7f1a4bae37d51bab3a6b10`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 5.2 MB (5191563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6796b4c1c7b40ab0124c1fb073c26e6fa1759c6ff0da6f72c415efe1606f21`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:446c34d96f894710257205f1bc01feb11b28a70356e496623f181904b3bdab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231763012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ef30ac82833939a440db22954c3ba4534e4bf4db76e99d0d99d8be426fc8e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee2c39130bfacf9515d5efc24ffb7082ef9cf1eb6582efaa417dc9ce65b9d7`  
		Last Modified: Thu, 16 Oct 2025 18:11:16 GMT  
		Size: 14.6 MB (14585576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b8821d5c5c11a572869e76b33d7b289886da091905ea7891989761602b28ac`  
		Last Modified: Thu, 16 Oct 2025 18:53:15 GMT  
		Size: 149.7 MB (149713921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a831a008cd327b103097dc472e34bd4555576e82684c2961ea3b8323a127e2`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e972aeccefde64f644ab5aec99738cce3b1db4927732885f7b2bab2d609042`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48c171ee965d9e3dedc0dfd62132da4c78be2e1b331c5dda234906960d036`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8957e4fea405a8c569e5a4e53c317ffd464cd35ab699910f4aa019246fd1004c`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e0d2187cb639e180b97f0ce2e9c24b02f95fb751dbde54e7e5507181226ada`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.3` - unknown; unknown

```console
$ docker pull crate@sha256:d84e171a0c663626ed9db8490d05f5e5f4b99cb28689746bd4c565fc9fe02325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e168fde894b5948ac03ec7363d2cc4362e56d2409ddb5521a511869025e778`

```dockerfile
```

-	Layers:
	-	`sha256:e483f4f765e3180c51a0e44f11307861f56a8c5848af11b856e2a4a22c617bae`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 5.2 MB (5189482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f908ee93abf4c77ad4f51611c4b7ee1b389abfa692da82927fb216eb2bc7d813`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:a9948f3ed7b8984d2d3ab8019123852cee2b9d19333d12432c3b318167090710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:813ed0cdea3ec2c74b9a723decd92ba5447c1d1a86da5a45537d866de1da571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232534589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce20580f8efcf6b5ed0fff03f528d235a3377335df72ea24342474fde8abf50c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa72b9a9687a3fdeab461aef880682ed5e111d019c6efcd7b5d66e4adcd32b`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 14.5 MB (14534324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1afe5cd5fff6ae2c8a4558e0be9d14199da25ceba36a96739ab01f11182460`  
		Last Modified: Thu, 16 Oct 2025 18:32:54 GMT  
		Size: 149.0 MB (149025700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865eeafcd1193101a872976bcd8de8c9091638e51f5a0504aacbfdaec5f63975`  
		Last Modified: Thu, 16 Oct 2025 18:32:38 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12875bb47a4594c7b83e1ceb84a23f2d047d194ee5cc01099d11b60732897efc`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720e2e1c54ae64d4941e7a5194cb4668c494eb59f57f65c2ef265680378056a2`  
		Last Modified: Thu, 16 Oct 2025 18:32:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4611d4399efe580bfc490d9d209021f0688e3331598fbda12e2a24da61e7d1d`  
		Last Modified: Thu, 16 Oct 2025 18:32:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e509bf4a30e6f0b3e017e5e3caa8a609c0aeb04ae454162c3e637b23b74e2b9`  
		Last Modified: Thu, 16 Oct 2025 18:32:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:792be79f6d84e535930ba8251750e70db9a303ad6e8cd8c2289a571dfb605feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00f67f7dde44d47dab6387dfea6cc9059472441ca4d12a6b8914d109ffa702`

```dockerfile
```

-	Layers:
	-	`sha256:115faf1ab6e66910438674be6db0b9dc5198d8168f7f1a4bae37d51bab3a6b10`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 5.2 MB (5191563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6796b4c1c7b40ab0124c1fb073c26e6fa1759c6ff0da6f72c415efe1606f21`  
		Last Modified: Thu, 16 Oct 2025 20:38:34 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:446c34d96f894710257205f1bc01feb11b28a70356e496623f181904b3bdab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231763012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ef30ac82833939a440db22954c3ba4534e4bf4db76e99d0d99d8be426fc8e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 15:42:38 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 15:42:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 13 Oct 2025 15:42:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
VOLUME [/data]
# Mon, 13 Oct 2025 15:42:38 GMT
WORKDIR /data
# Mon, 13 Oct 2025 15:42:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 13 Oct 2025 15:42:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 13 Oct 2025 15:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Oct 2025 15:42:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee2c39130bfacf9515d5efc24ffb7082ef9cf1eb6582efaa417dc9ce65b9d7`  
		Last Modified: Thu, 16 Oct 2025 18:11:16 GMT  
		Size: 14.6 MB (14585576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b8821d5c5c11a572869e76b33d7b289886da091905ea7891989761602b28ac`  
		Last Modified: Thu, 16 Oct 2025 18:53:15 GMT  
		Size: 149.7 MB (149713921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a831a008cd327b103097dc472e34bd4555576e82684c2961ea3b8323a127e2`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e972aeccefde64f644ab5aec99738cce3b1db4927732885f7b2bab2d609042`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48c171ee965d9e3dedc0dfd62132da4c78be2e1b331c5dda234906960d036`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8957e4fea405a8c569e5a4e53c317ffd464cd35ab699910f4aa019246fd1004c`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e0d2187cb639e180b97f0ce2e9c24b02f95fb751dbde54e7e5507181226ada`  
		Last Modified: Thu, 16 Oct 2025 18:11:14 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d84e171a0c663626ed9db8490d05f5e5f4b99cb28689746bd4c565fc9fe02325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e168fde894b5948ac03ec7363d2cc4362e56d2409ddb5521a511869025e778`

```dockerfile
```

-	Layers:
	-	`sha256:e483f4f765e3180c51a0e44f11307861f56a8c5848af11b856e2a4a22c617bae`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 5.2 MB (5189482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f908ee93abf4c77ad4f51611c4b7ee1b389abfa692da82927fb216eb2bc7d813`  
		Last Modified: Thu, 16 Oct 2025 20:38:40 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json
