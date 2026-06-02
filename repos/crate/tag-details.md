<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.8`](#crate628)
-	[`crate:6.3`](#crate63)
-	[`crate:6.3.2`](#crate632)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:22f086da0117038524b8d40269e5da91c8eeb1a36c0d9a130415420eb8a8ab39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:28ca9d93f64f21453d58b15352c437b9e894d3a1f17d8973e5bdb7676e907b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243550867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dbf9370e2f704d440a51d058831f7b5e34a173fcdcf1f1d642a2ed69fcac3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:05 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:21 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 02 Jun 2026 19:07:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff57f6352d1d1855272fb9b26dfaa2dd1df31958024ccb5c8bbe398ab967bb99`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 18.2 MB (18205825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1686197d6f0bf825d2a13aa26478926f309ab6768602f97a78a7c5a34d74ff`  
		Last Modified: Tue, 02 Jun 2026 19:07:46 GMT  
		Size: 149.0 MB (149020542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c76bf7e2b990f44a8d7754d135a1d0748958a656766d17345d64b074f86fb5`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 7.8 MB (7769618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304bf95de83cc3082f9bd5f90ddc1ad0d2e610a7acd96e8288270775416021c`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08b686dcca473c74b8c38bdfaa578dfc92d4306b64b3d715bb172788ff8a5d`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7788a5b8238a668e832ca0b157481a0f3f0d5ebb672a66953054c249fe3b4b`  
		Last Modified: Tue, 02 Jun 2026 19:07:42 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc147040328bc96fee913d05d2a51763ef7094d82aa3938a83418a241a1a81a8`  
		Last Modified: Tue, 02 Jun 2026 19:07:42 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:c39ba7cd14bd614b54c74d9531a873d50146ab327f5482b6d17d7d67864edcbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8c51ce9cfdd79113c5014bdab414e1e41b2f4512861daaef30b184bff04ebd`

```dockerfile
```

-	Layers:
	-	`sha256:4f3c3d371a9e15b46f83c81e3f3d29e60d424de1b9b4586fdb6cd7d6f05cc57c`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 6.7 MB (6652299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352f3dca70d8f57da32c6eab6127b45562bc1b341db4012e53a4596560d45b0d`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5ce19e6baa033a4d5f4282f9a6f7befb295c8d96c8e13108fcd2c52714323567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242869565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb2a7123aa453f514a6e0e48b0952238c5a44f2357a2b3e5f90028c9f9b451d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:42 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 02 Jun 2026 19:07:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2063dde8a88609c56821efdc1d6c3c44258f072b8d8f84eeb26fad7f5a9eee67`  
		Last Modified: Tue, 02 Jun 2026 19:08:02 GMT  
		Size: 18.3 MB (18256401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbb329a6d2b75b3f6b235a4a46330a226f97bf26218dc144f417bc6999f19a`  
		Last Modified: Tue, 02 Jun 2026 19:08:05 GMT  
		Size: 149.7 MB (149712743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d71c6bbe730bc3c48d03a0e4441c9cb37e79ac8284afc9773998ee7229e98`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 7.8 MB (7765364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c16db1a9a3e2eb2feda0109917623e5d52fd76166d01df04e365d9904eb8`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab61f3c17d3ec5538fbd624ecac7783a747b1e703715a12edaa342a2e18eb3c`  
		Last Modified: Tue, 02 Jun 2026 19:08:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74319ac213ad64de08099227dffd0e7a40ff9618a5c3803530b56108a7d9a30`  
		Last Modified: Tue, 02 Jun 2026 19:08:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b39d5d09d6b4e36f2951b3f9153eab9e97487ba7fb1af320a20274751def83`  
		Last Modified: Tue, 02 Jun 2026 19:08:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:b17b8605c746033b0812f80fb6590df36cc6304d4d45b3cfbed41aa5d6bd043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a79fe3fce38729c1da41a88bf27a5f9d631e231c910b814b98976e84380b53`

```dockerfile
```

-	Layers:
	-	`sha256:17d75b8d15b0eeed046801730e62f4a0fe7defb8ec8a639a05907edb68266ebc`  
		Last Modified: Tue, 02 Jun 2026 19:08:02 GMT  
		Size: 6.7 MB (6650211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac411906fa45c8ce4a19530b1f5b4ba958280399ea825b4ae84510b633397e58`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:22f086da0117038524b8d40269e5da91c8eeb1a36c0d9a130415420eb8a8ab39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:28ca9d93f64f21453d58b15352c437b9e894d3a1f17d8973e5bdb7676e907b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243550867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dbf9370e2f704d440a51d058831f7b5e34a173fcdcf1f1d642a2ed69fcac3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:05 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:21 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 02 Jun 2026 19:07:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff57f6352d1d1855272fb9b26dfaa2dd1df31958024ccb5c8bbe398ab967bb99`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 18.2 MB (18205825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1686197d6f0bf825d2a13aa26478926f309ab6768602f97a78a7c5a34d74ff`  
		Last Modified: Tue, 02 Jun 2026 19:07:46 GMT  
		Size: 149.0 MB (149020542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c76bf7e2b990f44a8d7754d135a1d0748958a656766d17345d64b074f86fb5`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 7.8 MB (7769618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304bf95de83cc3082f9bd5f90ddc1ad0d2e610a7acd96e8288270775416021c`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08b686dcca473c74b8c38bdfaa578dfc92d4306b64b3d715bb172788ff8a5d`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7788a5b8238a668e832ca0b157481a0f3f0d5ebb672a66953054c249fe3b4b`  
		Last Modified: Tue, 02 Jun 2026 19:07:42 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc147040328bc96fee913d05d2a51763ef7094d82aa3938a83418a241a1a81a8`  
		Last Modified: Tue, 02 Jun 2026 19:07:42 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:c39ba7cd14bd614b54c74d9531a873d50146ab327f5482b6d17d7d67864edcbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8c51ce9cfdd79113c5014bdab414e1e41b2f4512861daaef30b184bff04ebd`

```dockerfile
```

-	Layers:
	-	`sha256:4f3c3d371a9e15b46f83c81e3f3d29e60d424de1b9b4586fdb6cd7d6f05cc57c`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 6.7 MB (6652299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352f3dca70d8f57da32c6eab6127b45562bc1b341db4012e53a4596560d45b0d`  
		Last Modified: Tue, 02 Jun 2026 19:07:40 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5ce19e6baa033a4d5f4282f9a6f7befb295c8d96c8e13108fcd2c52714323567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242869565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb2a7123aa453f514a6e0e48b0952238c5a44f2357a2b3e5f90028c9f9b451d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:42 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 02 Jun 2026 19:07:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2063dde8a88609c56821efdc1d6c3c44258f072b8d8f84eeb26fad7f5a9eee67`  
		Last Modified: Tue, 02 Jun 2026 19:08:02 GMT  
		Size: 18.3 MB (18256401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbb329a6d2b75b3f6b235a4a46330a226f97bf26218dc144f417bc6999f19a`  
		Last Modified: Tue, 02 Jun 2026 19:08:05 GMT  
		Size: 149.7 MB (149712743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d71c6bbe730bc3c48d03a0e4441c9cb37e79ac8284afc9773998ee7229e98`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 7.8 MB (7765364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c16db1a9a3e2eb2feda0109917623e5d52fd76166d01df04e365d9904eb8`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab61f3c17d3ec5538fbd624ecac7783a747b1e703715a12edaa342a2e18eb3c`  
		Last Modified: Tue, 02 Jun 2026 19:08:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74319ac213ad64de08099227dffd0e7a40ff9618a5c3803530b56108a7d9a30`  
		Last Modified: Tue, 02 Jun 2026 19:08:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b39d5d09d6b4e36f2951b3f9153eab9e97487ba7fb1af320a20274751def83`  
		Last Modified: Tue, 02 Jun 2026 19:08:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:b17b8605c746033b0812f80fb6590df36cc6304d4d45b3cfbed41aa5d6bd043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a79fe3fce38729c1da41a88bf27a5f9d631e231c910b814b98976e84380b53`

```dockerfile
```

-	Layers:
	-	`sha256:17d75b8d15b0eeed046801730e62f4a0fe7defb8ec8a639a05907edb68266ebc`  
		Last Modified: Tue, 02 Jun 2026 19:08:02 GMT  
		Size: 6.7 MB (6650211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac411906fa45c8ce4a19530b1f5b4ba958280399ea825b4ae84510b633397e58`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:753365db9731e36a877cfe96ea6fbb0d3ee1b40313d8da3535c221a79f139e82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:2e3b4a7a39737a7cc2f921b44395a658323cbc70a54693108341e7dde443d6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243678500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666dafbab0339a15e8ef0d0c31f52f0eaf487114093d542020b6da8918ac97d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:19 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e052d92adf7148aa9b835ffddf93fd54630929c5fefd071bad70925a3547f50`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 18.2 MB (18205737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f83a0481b4e877a894f65fc03ad961007450d38e01235244e33426bc4cc48a`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 149.1 MB (149148315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1132439d4a63d1deb1b2a925b2500914d1e8d5727d35c71e033838b724279831`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 7.8 MB (7769569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d717ddb753565ae6d8b2918b13ac52f0d3903351c218e46bb0446828ddef01`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2afb107c94b753ea1c981b2a7cbaf9310a489f1ddcf71d46e2febf804ae9a`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a753e2c8492466ff3aa70d0b771c786a8d730afa752dbfb7917f7b64a58fc5`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147fb3832c464a244e72eb85da6e203a94e91b2726459b815c7dc046fcee364`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:c336c6de0c164564a37a441b2031b02330af91669a966c2e33708820506f5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6574bc5a7a5acfe60c8ed9a4cf97f72574400c0fe825bc669958ab8f05529fc8`

```dockerfile
```

-	Layers:
	-	`sha256:d304293455deedbad9d30318e5cdf785eaa0d2ae9385cf969a1f8294c44bb63d`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 6.7 MB (6651083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dcd647a21a4ab9197c17637c6b1cb3fad73fff3a4eb13b82b09385a1618424`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:eef0870a7d8fa8aaf2bf2c62c1671848f0117740852678ead325e0d9582c0948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242995244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e538fc1619dd443946fc09df4612b3a6a30f34aa0b22a0060995cbfd8c7aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:39 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88506b1de13c16a213e6a3b4f0711aa96d74476f569e561548a2f9989d4ea48b`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 18.3 MB (18256355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4c930f405362f947670cdf0f3bafda81e3fe3d3d89b375150cece8aa54a55b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.8 MB (149838687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ac36343d380d856b7e9a0930da0b1c6cec4dd888c9fae02e1d1a21ea13d15`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 7.8 MB (7765143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5219489f75d85cfc703ef97fe3d55281174720c7f6999ca5231c4226704f0f`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2676ec0bb7378a497c644e2191271e47101600767d83327d3edb559c6a9cc7`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5dec100a8744c89c3d7864a55c571c949dfbd1094ba32fd6e3d6e07867ac54`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66510f3c681343e67232ceb7f1213b24c9e4c486dd798ef6c2fa046ad28658c1`  
		Last Modified: Tue, 02 Jun 2026 19:08:00 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:13b95e1897aed537996abca63c4f5e326f89616ea4fdaef06ae3586dbc3c6233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf792062332f44bb4c8d5fd4378ecc8a3f424c653314ba217d9a8a5691b6236`

```dockerfile
```

-	Layers:
	-	`sha256:cec2eaf56c130c25a32d8d95aa74a4039c8e97503b04a5e6182db6b390179440`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 6.6 MB (6648995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c24d9590dee1bacb7cd5f5c9a99dc979d002b0f6a60efb8aa3c8f8958d4bd3`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:753365db9731e36a877cfe96ea6fbb0d3ee1b40313d8da3535c221a79f139e82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:2e3b4a7a39737a7cc2f921b44395a658323cbc70a54693108341e7dde443d6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243678500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666dafbab0339a15e8ef0d0c31f52f0eaf487114093d542020b6da8918ac97d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:19 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e052d92adf7148aa9b835ffddf93fd54630929c5fefd071bad70925a3547f50`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 18.2 MB (18205737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f83a0481b4e877a894f65fc03ad961007450d38e01235244e33426bc4cc48a`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 149.1 MB (149148315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1132439d4a63d1deb1b2a925b2500914d1e8d5727d35c71e033838b724279831`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 7.8 MB (7769569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d717ddb753565ae6d8b2918b13ac52f0d3903351c218e46bb0446828ddef01`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2afb107c94b753ea1c981b2a7cbaf9310a489f1ddcf71d46e2febf804ae9a`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a753e2c8492466ff3aa70d0b771c786a8d730afa752dbfb7917f7b64a58fc5`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147fb3832c464a244e72eb85da6e203a94e91b2726459b815c7dc046fcee364`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:c336c6de0c164564a37a441b2031b02330af91669a966c2e33708820506f5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6574bc5a7a5acfe60c8ed9a4cf97f72574400c0fe825bc669958ab8f05529fc8`

```dockerfile
```

-	Layers:
	-	`sha256:d304293455deedbad9d30318e5cdf785eaa0d2ae9385cf969a1f8294c44bb63d`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 6.7 MB (6651083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dcd647a21a4ab9197c17637c6b1cb3fad73fff3a4eb13b82b09385a1618424`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:eef0870a7d8fa8aaf2bf2c62c1671848f0117740852678ead325e0d9582c0948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242995244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e538fc1619dd443946fc09df4612b3a6a30f34aa0b22a0060995cbfd8c7aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:39 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88506b1de13c16a213e6a3b4f0711aa96d74476f569e561548a2f9989d4ea48b`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 18.3 MB (18256355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4c930f405362f947670cdf0f3bafda81e3fe3d3d89b375150cece8aa54a55b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.8 MB (149838687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ac36343d380d856b7e9a0930da0b1c6cec4dd888c9fae02e1d1a21ea13d15`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 7.8 MB (7765143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5219489f75d85cfc703ef97fe3d55281174720c7f6999ca5231c4226704f0f`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2676ec0bb7378a497c644e2191271e47101600767d83327d3edb559c6a9cc7`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5dec100a8744c89c3d7864a55c571c949dfbd1094ba32fd6e3d6e07867ac54`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66510f3c681343e67232ceb7f1213b24c9e4c486dd798ef6c2fa046ad28658c1`  
		Last Modified: Tue, 02 Jun 2026 19:08:00 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:13b95e1897aed537996abca63c4f5e326f89616ea4fdaef06ae3586dbc3c6233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf792062332f44bb4c8d5fd4378ecc8a3f424c653314ba217d9a8a5691b6236`

```dockerfile
```

-	Layers:
	-	`sha256:cec2eaf56c130c25a32d8d95aa74a4039c8e97503b04a5e6182db6b390179440`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 6.6 MB (6648995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c24d9590dee1bacb7cd5f5c9a99dc979d002b0f6a60efb8aa3c8f8958d4bd3`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:fb7da5dce6474050ba9af1de47792b4e010a472af164169b3ff316b0acea21a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:ca6abd99a1a723ae63cb13444d3bf32af23fbfea52ec43a90b71f0ef573d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245862201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71309bec52c84b6b26fa385ec904f1158bc8ed6d81a2dac26bb2b8900707e095`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:06:59 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:16 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 02 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d57bf6d0e094b4b1b9cbf5737863b556758ff32e3719c2c3555a02758a28f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 18.2 MB (18205778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96466fce04bae4a327b3c235447cd266b724d526466f011fa67572a67901eec5`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 151.3 MB (151332059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e52a1ded66c6da4b3d265808487c8724a4c3df076a64ff4e5d7ce3fc6052f2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 7.8 MB (7769483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994310f6de7258a9bffa98438ab782dd6d58c2627842ca23c0df6b1fc70de99`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707402e4edbdaf6b276c36ee8bd695963a2e210ccf6e8a8db583f0674c6f4b6`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba803b145604c9dd1c325300a63cb450168f8e94f7dd59235448ea09b71a37`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bac732d7ce8167b2784dc12fe73cacddf7d57722ce5bb0db4f7b9da08bc8e51`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:f1f74fa8e04eef95edc55a302f0fdf0a9983b2599653e235e1b2a4e25fd0eddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c016819c6cb88a798eea733dd2a8470496e60ad6561b070ba8c9d0761269bb9`

```dockerfile
```

-	Layers:
	-	`sha256:9e2cfdf7c19a8561bde184ccc011926f643cf193520738c35b734782f15c42c6`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 6.7 MB (6656611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86133f7c624ea931662257365ecd20f00a5da73776fee2585337a3d9f9f51cb`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0eedbfb1bcd28b80d54cbffe67878eca7683aeb1e7d932bdd4e7121e773f38e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242456664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772eedbe300965154e7f7eecd3a457465513cb7d396025bef3c27a82d92dfcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:38 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 02 Jun 2026 19:07:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f50013860399037ec23244da6e267bffc985d3a46a384516cde44cca3abeab4`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 18.3 MB (18256413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699c24824116ac464b67899bbc6e95df0dd9e31f554971789728dbc101dbb80b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.3 MB (149300218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094af6e609fda62dc58a3dff0ada2f5b99d9ebaed23e14123fd3eeb0b059c47e`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 7.8 MB (7764973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f798caa62ee725cf008611d03c7d483e5858bbe525fe0c1fabafd6e1478837`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce34758a181dc9ba4bc87ffe8ed735e9bd172c29dbbc03227f716a33c89d4b`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efa61520e6e6da222d600e9092cad169273881a106daa1e153425b84f132181`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e413e4489bd598377f91ff33302f034e9b0e98f3f100f80ec75d95d196835cf`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:610d93676f7d912ec0200f8152f365e2d425f93e24d6527b39069f24426dee59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e1d0897d63684f331b269f88afcbdc0aaeb550844b2e253813d17dcf4725c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed4e67f63edbfaa09205a5d77a841c8365d53fcca3014349e63ce029cff1d7e2`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 6.7 MB (6654523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd86a99f9f139d19bcb0cfd7dba093a05bdfb5a1653f5fe44c06164bc0aef73`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.8`

```console
$ docker pull crate@sha256:fb7da5dce6474050ba9af1de47792b4e010a472af164169b3ff316b0acea21a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.8` - linux; amd64

```console
$ docker pull crate@sha256:ca6abd99a1a723ae63cb13444d3bf32af23fbfea52ec43a90b71f0ef573d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245862201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71309bec52c84b6b26fa385ec904f1158bc8ed6d81a2dac26bb2b8900707e095`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:06:59 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:16 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 02 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d57bf6d0e094b4b1b9cbf5737863b556758ff32e3719c2c3555a02758a28f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 18.2 MB (18205778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96466fce04bae4a327b3c235447cd266b724d526466f011fa67572a67901eec5`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 151.3 MB (151332059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e52a1ded66c6da4b3d265808487c8724a4c3df076a64ff4e5d7ce3fc6052f2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 7.8 MB (7769483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994310f6de7258a9bffa98438ab782dd6d58c2627842ca23c0df6b1fc70de99`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707402e4edbdaf6b276c36ee8bd695963a2e210ccf6e8a8db583f0674c6f4b6`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba803b145604c9dd1c325300a63cb450168f8e94f7dd59235448ea09b71a37`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bac732d7ce8167b2784dc12fe73cacddf7d57722ce5bb0db4f7b9da08bc8e51`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:f1f74fa8e04eef95edc55a302f0fdf0a9983b2599653e235e1b2a4e25fd0eddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c016819c6cb88a798eea733dd2a8470496e60ad6561b070ba8c9d0761269bb9`

```dockerfile
```

-	Layers:
	-	`sha256:9e2cfdf7c19a8561bde184ccc011926f643cf193520738c35b734782f15c42c6`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 6.7 MB (6656611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86133f7c624ea931662257365ecd20f00a5da73776fee2585337a3d9f9f51cb`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0eedbfb1bcd28b80d54cbffe67878eca7683aeb1e7d932bdd4e7121e773f38e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242456664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772eedbe300965154e7f7eecd3a457465513cb7d396025bef3c27a82d92dfcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:38 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:38 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:38 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:38 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:38 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 02 Jun 2026 19:07:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f50013860399037ec23244da6e267bffc985d3a46a384516cde44cca3abeab4`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 18.3 MB (18256413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699c24824116ac464b67899bbc6e95df0dd9e31f554971789728dbc101dbb80b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.3 MB (149300218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094af6e609fda62dc58a3dff0ada2f5b99d9ebaed23e14123fd3eeb0b059c47e`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 7.8 MB (7764973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f798caa62ee725cf008611d03c7d483e5858bbe525fe0c1fabafd6e1478837`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce34758a181dc9ba4bc87ffe8ed735e9bd172c29dbbc03227f716a33c89d4b`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efa61520e6e6da222d600e9092cad169273881a106daa1e153425b84f132181`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e413e4489bd598377f91ff33302f034e9b0e98f3f100f80ec75d95d196835cf`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:610d93676f7d912ec0200f8152f365e2d425f93e24d6527b39069f24426dee59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e1d0897d63684f331b269f88afcbdc0aaeb550844b2e253813d17dcf4725c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed4e67f63edbfaa09205a5d77a841c8365d53fcca3014349e63ce029cff1d7e2`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 6.7 MB (6654523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd86a99f9f139d19bcb0cfd7dba093a05bdfb5a1653f5fe44c06164bc0aef73`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3`

```console
$ docker pull crate@sha256:b46cd1348de7da728ed256c35e703749a11bb10ea2a5f10a3beaa36de0413b2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3` - linux; amd64

```console
$ docker pull crate@sha256:b183cb958db92d2882a97efb0ecb15a2af444e9c18c5bf66156a799f1a5dcc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233599162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee5fbf38f7d4a7f89fbaf8e250faf84e0a175aba6694581f14045811b43d6aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:16 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b15f9711887f0aaa4d6ef0e1a5dee3f6202cc1f263947d92ceeefb36c36d323`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 18.2 MB (18205751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2961cfbc87ac033094ed17de9d1bc4900b29850734f849e5a3a2c88ab1a75d`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 139.1 MB (139069118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6523b3b2035695bc5c0bb1c0dc7835c386d191429b4cafb15e5848797eddb20e`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 7.8 MB (7769412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994310f6de7258a9bffa98438ab782dd6d58c2627842ca23c0df6b1fc70de99`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8329fd9de7c236405545eda2c7b50c3a34721504ed6ffc27e0616745f427eeb`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abeaa1759ca70336ff3861d393b525b3b4ee895f90fc8568d23e1d4f3b9c848`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39a4b073eddcc972b0244a31d432f63475e1457be0da966d4c9b652051f4037`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:0af7c2fc3fcd50e9623d89ae0dd9344410ffc94e3385118bd77d16440ce1575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b18c31e3c1e29c2059f01fad5df046a98ce463ed31b174e6fe06a8957df7c`

```dockerfile
```

-	Layers:
	-	`sha256:a39ff9c5019f9005b08aa4984667ee78e0fd18d724cb662999920a305b519fbc`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 6.6 MB (6606392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1103a757755c0ceacd9b326063fecb92b51449bf12c16ae3fb1f90f674307c4`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:274c340a020b55dacd885ca20fc2196fee557110565a01d26df0be11ae230f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06ef21d811898b937a604cc917a2a6dc327884dd4541a368d37f86181644518`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:37 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94230a5495bc9c3f20522a31004e26dedd1e286eefdee345a89d4edbd38361c`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 18.3 MB (18256623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c130b5e058e122de413b8c1a52cbd4a3d30491b4dc84bc2309e7b9c886170`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 137.0 MB (137026815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162525c659744579ed162cbc5372de59cefb203a22239e3bea9113bf0c8b6e0`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 7.8 MB (7765052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a75d0391312119d1a1ee616f56db6c3adb1d7433ef565f64e705e2d72b5d987`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f962b6d3677fc17ccb935f566d260fb940d0f75517405cef8131d725409fc6`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63edb2cc81539606989eb83fd4689296b9afa98ffe8eaa385cf8d64ef549aa`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abd267a83ebedd2151e0e8f13072c0fdb4e6d6cec40205430aac104cc2713`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:c86ecec5ca8ffe27c330abb835d791ff384ef5e0ee9a42aa1a22b1f8cb827585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da5fe9e55dffba7a1739ffc6916a68c384e74418bf42836a529cd97e57999a5`

```dockerfile
```

-	Layers:
	-	`sha256:2190e76179adb58b55d0a4901a0c7afcf74d79d7e6ba47304d92031497db3fa6`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 6.6 MB (6604316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76811daff921564f4caa055b3b86298a0ccaf627fff8b652695f044a7bb62b3`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3.2`

```console
$ docker pull crate@sha256:b46cd1348de7da728ed256c35e703749a11bb10ea2a5f10a3beaa36de0413b2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3.2` - linux; amd64

```console
$ docker pull crate@sha256:b183cb958db92d2882a97efb0ecb15a2af444e9c18c5bf66156a799f1a5dcc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233599162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee5fbf38f7d4a7f89fbaf8e250faf84e0a175aba6694581f14045811b43d6aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:16 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b15f9711887f0aaa4d6ef0e1a5dee3f6202cc1f263947d92ceeefb36c36d323`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 18.2 MB (18205751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2961cfbc87ac033094ed17de9d1bc4900b29850734f849e5a3a2c88ab1a75d`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 139.1 MB (139069118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6523b3b2035695bc5c0bb1c0dc7835c386d191429b4cafb15e5848797eddb20e`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 7.8 MB (7769412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994310f6de7258a9bffa98438ab782dd6d58c2627842ca23c0df6b1fc70de99`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8329fd9de7c236405545eda2c7b50c3a34721504ed6ffc27e0616745f427eeb`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abeaa1759ca70336ff3861d393b525b3b4ee895f90fc8568d23e1d4f3b9c848`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39a4b073eddcc972b0244a31d432f63475e1457be0da966d4c9b652051f4037`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:0af7c2fc3fcd50e9623d89ae0dd9344410ffc94e3385118bd77d16440ce1575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b18c31e3c1e29c2059f01fad5df046a98ce463ed31b174e6fe06a8957df7c`

```dockerfile
```

-	Layers:
	-	`sha256:a39ff9c5019f9005b08aa4984667ee78e0fd18d724cb662999920a305b519fbc`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 6.6 MB (6606392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1103a757755c0ceacd9b326063fecb92b51449bf12c16ae3fb1f90f674307c4`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:274c340a020b55dacd885ca20fc2196fee557110565a01d26df0be11ae230f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06ef21d811898b937a604cc917a2a6dc327884dd4541a368d37f86181644518`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:37 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94230a5495bc9c3f20522a31004e26dedd1e286eefdee345a89d4edbd38361c`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 18.3 MB (18256623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c130b5e058e122de413b8c1a52cbd4a3d30491b4dc84bc2309e7b9c886170`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 137.0 MB (137026815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162525c659744579ed162cbc5372de59cefb203a22239e3bea9113bf0c8b6e0`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 7.8 MB (7765052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a75d0391312119d1a1ee616f56db6c3adb1d7433ef565f64e705e2d72b5d987`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f962b6d3677fc17ccb935f566d260fb940d0f75517405cef8131d725409fc6`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63edb2cc81539606989eb83fd4689296b9afa98ffe8eaa385cf8d64ef549aa`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abd267a83ebedd2151e0e8f13072c0fdb4e6d6cec40205430aac104cc2713`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:c86ecec5ca8ffe27c330abb835d791ff384ef5e0ee9a42aa1a22b1f8cb827585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da5fe9e55dffba7a1739ffc6916a68c384e74418bf42836a529cd97e57999a5`

```dockerfile
```

-	Layers:
	-	`sha256:2190e76179adb58b55d0a4901a0c7afcf74d79d7e6ba47304d92031497db3fa6`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 6.6 MB (6604316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76811daff921564f4caa055b3b86298a0ccaf627fff8b652695f044a7bb62b3`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:b46cd1348de7da728ed256c35e703749a11bb10ea2a5f10a3beaa36de0413b2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:b183cb958db92d2882a97efb0ecb15a2af444e9c18c5bf66156a799f1a5dcc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233599162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee5fbf38f7d4a7f89fbaf8e250faf84e0a175aba6694581f14045811b43d6aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:16 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b15f9711887f0aaa4d6ef0e1a5dee3f6202cc1f263947d92ceeefb36c36d323`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 18.2 MB (18205751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2961cfbc87ac033094ed17de9d1bc4900b29850734f849e5a3a2c88ab1a75d`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 139.1 MB (139069118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6523b3b2035695bc5c0bb1c0dc7835c386d191429b4cafb15e5848797eddb20e`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 7.8 MB (7769412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1994310f6de7258a9bffa98438ab782dd6d58c2627842ca23c0df6b1fc70de99`  
		Last Modified: Tue, 02 Jun 2026 19:07:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8329fd9de7c236405545eda2c7b50c3a34721504ed6ffc27e0616745f427eeb`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abeaa1759ca70336ff3861d393b525b3b4ee895f90fc8568d23e1d4f3b9c848`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39a4b073eddcc972b0244a31d432f63475e1457be0da966d4c9b652051f4037`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:0af7c2fc3fcd50e9623d89ae0dd9344410ffc94e3385118bd77d16440ce1575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b18c31e3c1e29c2059f01fad5df046a98ce463ed31b174e6fe06a8957df7c`

```dockerfile
```

-	Layers:
	-	`sha256:a39ff9c5019f9005b08aa4984667ee78e0fd18d724cb662999920a305b519fbc`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 6.6 MB (6606392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1103a757755c0ceacd9b326063fecb92b51449bf12c16ae3fb1f90f674307c4`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:274c340a020b55dacd885ca20fc2196fee557110565a01d26df0be11ae230f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06ef21d811898b937a604cc917a2a6dc327884dd4541a368d37f86181644518`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:37 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 02 Jun 2026 19:07:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94230a5495bc9c3f20522a31004e26dedd1e286eefdee345a89d4edbd38361c`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 18.3 MB (18256623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c130b5e058e122de413b8c1a52cbd4a3d30491b4dc84bc2309e7b9c886170`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 137.0 MB (137026815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162525c659744579ed162cbc5372de59cefb203a22239e3bea9113bf0c8b6e0`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 7.8 MB (7765052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a75d0391312119d1a1ee616f56db6c3adb1d7433ef565f64e705e2d72b5d987`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f962b6d3677fc17ccb935f566d260fb940d0f75517405cef8131d725409fc6`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63edb2cc81539606989eb83fd4689296b9afa98ffe8eaa385cf8d64ef549aa`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abd267a83ebedd2151e0e8f13072c0fdb4e6d6cec40205430aac104cc2713`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c86ecec5ca8ffe27c330abb835d791ff384ef5e0ee9a42aa1a22b1f8cb827585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da5fe9e55dffba7a1739ffc6916a68c384e74418bf42836a529cd97e57999a5`

```dockerfile
```

-	Layers:
	-	`sha256:2190e76179adb58b55d0a4901a0c7afcf74d79d7e6ba47304d92031497db3fa6`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 6.6 MB (6604316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76811daff921564f4caa055b3b86298a0ccaf627fff8b652695f044a7bb62b3`  
		Last Modified: Tue, 02 Jun 2026 19:07:56 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
