<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.16`](#crate51016)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.5`](#crate605)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.2`](#crate612)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:1344993f7132e55fb8458c67de961a67572f04586517b4271c0dbc5c80dc2ea6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:515f68c29b190e7971ec8f6dfea8960106843182bbaea0623ec0bf78ee51658f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233677786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281eaa0d8e0064979a1f80ca32c8eb70b3f61437acd04191fb8e95359c96d99a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:47 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 05 Jan 2026 19:11:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a498bbb02e203cae94b907be14afa97f203f9119a85348b0abe04ea3087f2ab0`  
		Last Modified: Mon, 05 Jan 2026 19:12:36 GMT  
		Size: 149.7 MB (149721722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48d794852a972f6228e8851ce6b2ac05bbe2cd23f280b8153d54406bc87ccd`  
		Last Modified: Mon, 05 Jan 2026 19:12:03 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d98bb3bcbe21787115ff0d59af4ecc614765361d0eeb599382038d1455033e6`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a24df00647255cadb3527b304ac60e20ec1988e1ffa8d2ab9035cefadf358d`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e8b98bf189f29e4be2443cf7c046202859400a52c18a7e9acb2ea7a898979`  
		Last Modified: Mon, 05 Jan 2026 19:12:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925192894c67caf520c08bb1b027ff3f35ad2a14c80d4dc71a8f0a41ebd9c855`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:1d725900080d7be0b1714a4279fb62b7b1592b3a2e4a0dda3dae89a19b8b57a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07715e3f1d96a6845ac309aa6c162969a78f80d3f7538b82d774e98a03fe788`

```dockerfile
```

-	Layers:
	-	`sha256:52f671c1fc8e38aa7ec1e3b4f2a0053bb279aea51060cc38da3c37228a6c5fab`  
		Last Modified: Mon, 05 Jan 2026 21:38:23 GMT  
		Size: 5.2 MB (5188848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313de46715667f3057da9fe4cde8c7aea8204f30256b92a95122f1248132e932`  
		Last Modified: Mon, 05 Jan 2026 19:12:03 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0dc41b8c367296a05fb168103b3cf9f9334e06a5b3c1cb9f9a5867c0c190d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232880101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b17adbf129039f3af56ac3a8711a3f208f5ebd74eab16a0f243cb2e68988a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:37 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 05 Jan 2026 19:11:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:34 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb785ae2b92243abc933211db975d9c88add476d047fdad0e10321990aee9a3`  
		Last Modified: Mon, 05 Jan 2026 19:11:58 GMT  
		Size: 150.4 MB (150402351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd5941cbdbc2b6fd4f962b08ba2e3d5d726c06b8adef7e018ab0d4b113811b8`  
		Last Modified: Mon, 05 Jan 2026 19:11:55 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf8f3b21e50d04b70229a2644308b6132858ccb5e6a72e1dd99a4394c50431`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47685bdebea2c49b367a90b85f6f6dd3480010ad6ba7f227af11cfa2776e23`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa28b7fe9ef60cc91e4fa0ed31e4448a52d3845344a54a190340dec2abda43cc`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c9013efcbece50f2ab80c08dfb5340227b23988d99aaf53d2842cdc1f0a91`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:310de83881021fcd24f09e2e63f93c3c0c8dadb3aaedfeb52c7bd61c044cca79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4a4d8086b4213c42111656e2dab843d820d8c5d56bc9555f879ee76ee8990`

```dockerfile
```

-	Layers:
	-	`sha256:d274b0576e761e533858284ec5e5d2b19940d24c659c0e84c56a9e468bf8617a`  
		Last Modified: Mon, 05 Jan 2026 19:11:55 GMT  
		Size: 5.2 MB (5186144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab518bc9d0a154f1a4db54a294a4d19259925d4b98263ce5911544a9a29bc3d`  
		Last Modified: Mon, 05 Jan 2026 21:38:33 GMT  
		Size: 23.0 KB (23002 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.16`

```console
$ docker pull crate@sha256:1344993f7132e55fb8458c67de961a67572f04586517b4271c0dbc5c80dc2ea6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.16` - linux; amd64

```console
$ docker pull crate@sha256:515f68c29b190e7971ec8f6dfea8960106843182bbaea0623ec0bf78ee51658f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233677786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281eaa0d8e0064979a1f80ca32c8eb70b3f61437acd04191fb8e95359c96d99a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:47 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 05 Jan 2026 19:11:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a498bbb02e203cae94b907be14afa97f203f9119a85348b0abe04ea3087f2ab0`  
		Last Modified: Mon, 05 Jan 2026 19:12:36 GMT  
		Size: 149.7 MB (149721722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48d794852a972f6228e8851ce6b2ac05bbe2cd23f280b8153d54406bc87ccd`  
		Last Modified: Mon, 05 Jan 2026 19:12:03 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d98bb3bcbe21787115ff0d59af4ecc614765361d0eeb599382038d1455033e6`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a24df00647255cadb3527b304ac60e20ec1988e1ffa8d2ab9035cefadf358d`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e8b98bf189f29e4be2443cf7c046202859400a52c18a7e9acb2ea7a898979`  
		Last Modified: Mon, 05 Jan 2026 19:12:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925192894c67caf520c08bb1b027ff3f35ad2a14c80d4dc71a8f0a41ebd9c855`  
		Last Modified: Mon, 05 Jan 2026 19:12:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:1d725900080d7be0b1714a4279fb62b7b1592b3a2e4a0dda3dae89a19b8b57a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07715e3f1d96a6845ac309aa6c162969a78f80d3f7538b82d774e98a03fe788`

```dockerfile
```

-	Layers:
	-	`sha256:52f671c1fc8e38aa7ec1e3b4f2a0053bb279aea51060cc38da3c37228a6c5fab`  
		Last Modified: Mon, 05 Jan 2026 21:38:23 GMT  
		Size: 5.2 MB (5188848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313de46715667f3057da9fe4cde8c7aea8204f30256b92a95122f1248132e932`  
		Last Modified: Mon, 05 Jan 2026 19:12:03 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.16` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0dc41b8c367296a05fb168103b3cf9f9334e06a5b3c1cb9f9a5867c0c190d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232880101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b17adbf129039f3af56ac3a8711a3f208f5ebd74eab16a0f243cb2e68988a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:37 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 05 Jan 2026 19:11:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:34 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb785ae2b92243abc933211db975d9c88add476d047fdad0e10321990aee9a3`  
		Last Modified: Mon, 05 Jan 2026 19:11:58 GMT  
		Size: 150.4 MB (150402351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd5941cbdbc2b6fd4f962b08ba2e3d5d726c06b8adef7e018ab0d4b113811b8`  
		Last Modified: Mon, 05 Jan 2026 19:11:55 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf8f3b21e50d04b70229a2644308b6132858ccb5e6a72e1dd99a4394c50431`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47685bdebea2c49b367a90b85f6f6dd3480010ad6ba7f227af11cfa2776e23`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa28b7fe9ef60cc91e4fa0ed31e4448a52d3845344a54a190340dec2abda43cc`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c9013efcbece50f2ab80c08dfb5340227b23988d99aaf53d2842cdc1f0a91`  
		Last Modified: Mon, 05 Jan 2026 19:12:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:310de83881021fcd24f09e2e63f93c3c0c8dadb3aaedfeb52c7bd61c044cca79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4a4d8086b4213c42111656e2dab843d820d8c5d56bc9555f879ee76ee8990`

```dockerfile
```

-	Layers:
	-	`sha256:d274b0576e761e533858284ec5e5d2b19940d24c659c0e84c56a9e468bf8617a`  
		Last Modified: Mon, 05 Jan 2026 19:11:55 GMT  
		Size: 5.2 MB (5186144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab518bc9d0a154f1a4db54a294a4d19259925d4b98263ce5911544a9a29bc3d`  
		Last Modified: Mon, 05 Jan 2026 21:38:33 GMT  
		Size: 23.0 KB (23002 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:29b17aa5d82433f95689fe393fd23c4f7e3d4cf30b1da4adff15f381696c55a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:9fc9437b66f67253e903a437172673ee268e1c0ed29921aeaa7a90a32be4b634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd298964c5b56110a69c85ae02fc41d4ddf9f97a0773c589a53736b28f4d055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:11:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:26 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:27 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 05 Jan 2026 19:11:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9fe3de488955a4d68cded8ef4b2e9622415281035ea1def904eed380d5962`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 14.5 MB (14500480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea105951e5686176a7e32f8a6ffb6b9fd132c50fb4e73f135c157179bdaf1c93`  
		Last Modified: Mon, 05 Jan 2026 19:11:49 GMT  
		Size: 149.0 MB (149028832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597d0f9bebcf71ee9d77222e0005bb85ec639d22e769a0e8dff1acf170d9103`  
		Last Modified: Mon, 05 Jan 2026 19:11:45 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a899852777e9369503265d5e08063da2329b40f2837953f70c7e9c9a1c59b3cd`  
		Last Modified: Mon, 05 Jan 2026 19:11:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931dccbde6ea9464e4e74b57a3bc11f358c395cafd388d32bedc0c32767da5b2`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23d080bcbad94bf9cb72f7113b21a2f7bf43cbaffac892e88931f1f53866245`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a1e5632b1eafda400df70facd9996c5bf9f217e42ffb6ff19464bd2e1d377c`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:acceeb297eaf31f93e6906604775e5006e905357b66d2db715a823a8e7e908e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5adbd38d16b93c0d9c91bbf64647a4797cc943cb91ede15425ea9c98aadcc3`

```dockerfile
```

-	Layers:
	-	`sha256:673d49936eb71cf43f174498e46a01d50e0c2fa55569ddabaf6a89017282ac80`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 5.2 MB (5191986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a702c2f25535e61cd45014f764cb23c20e83bbd5f000e53e6e09d87081f52f92`  
		Last Modified: Mon, 05 Jan 2026 21:38:37 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3656743bda14dbf35e37a5d49ad8d7a0119e440175925a9e9290acf1e799ba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232194161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ee8bc4c9fdc6d75f2aa7d96655c9880cde7fb43ccb5e60d55e961bc54f3d5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:11:28 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:42 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 05 Jan 2026 19:11:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda0a0ee4ee06a63b34f79147295bcd10d0e4d7079300b1a798fbafbc02f42e`  
		Last Modified: Mon, 05 Jan 2026 19:12:01 GMT  
		Size: 14.6 MB (14557016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a752dcbcd035b2839f055dda6884357ea3322a984146224ce69190c2cdaeece2`  
		Last Modified: Mon, 05 Jan 2026 19:12:07 GMT  
		Size: 149.7 MB (149716184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e65bbf227894386072a79644aca8c3f73e31b8efe89e643daf869591897eaf`  
		Last Modified: Mon, 05 Jan 2026 19:12:00 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6de60d4014fe5f1a2a5542af9c8a92114921ad5ad028decfdec810ddd32bca`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484e309b1bc13680f84bdee3aaa8c7ebb40b95b68e6a62be719f3da29f7e556`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76716b5adcc69ce65a1e1e95f595c6a21314a0421b9cdd423b04f87ad2da402f`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f5d2c92ce82325a87aa6d386a9b9a1bc9af8519e5aa3fe9f6eee335eebe1ba`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:5081058455472da36401b710986859e0e8dbfd23ac739bb72b5a1a0ded60881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58df3329c0ea4a099cd346e1c433f6cd08f048d4b5d03b6adf7f353575ccb97d`

```dockerfile
```

-	Layers:
	-	`sha256:1737789686ae3f5ff8f15dd06f06214439e6a8ad3bc16062e032b57b5f3c3946`  
		Last Modified: Mon, 05 Jan 2026 19:12:01 GMT  
		Size: 5.2 MB (5189893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef7eeaed136a7dd9c3ae0b593eeaf61704bc32d9c0c3bf720e414db79abb23a`  
		Last Modified: Mon, 05 Jan 2026 21:38:43 GMT  
		Size: 23.0 KB (22968 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.5`

```console
$ docker pull crate@sha256:29b17aa5d82433f95689fe393fd23c4f7e3d4cf30b1da4adff15f381696c55a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.5` - linux; amd64

```console
$ docker pull crate@sha256:9fc9437b66f67253e903a437172673ee268e1c0ed29921aeaa7a90a32be4b634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd298964c5b56110a69c85ae02fc41d4ddf9f97a0773c589a53736b28f4d055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:11:12 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:26 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:27 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 05 Jan 2026 19:11:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9fe3de488955a4d68cded8ef4b2e9622415281035ea1def904eed380d5962`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 14.5 MB (14500480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea105951e5686176a7e32f8a6ffb6b9fd132c50fb4e73f135c157179bdaf1c93`  
		Last Modified: Mon, 05 Jan 2026 19:11:49 GMT  
		Size: 149.0 MB (149028832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597d0f9bebcf71ee9d77222e0005bb85ec639d22e769a0e8dff1acf170d9103`  
		Last Modified: Mon, 05 Jan 2026 19:11:45 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a899852777e9369503265d5e08063da2329b40f2837953f70c7e9c9a1c59b3cd`  
		Last Modified: Mon, 05 Jan 2026 19:11:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931dccbde6ea9464e4e74b57a3bc11f358c395cafd388d32bedc0c32767da5b2`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23d080bcbad94bf9cb72f7113b21a2f7bf43cbaffac892e88931f1f53866245`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a1e5632b1eafda400df70facd9996c5bf9f217e42ffb6ff19464bd2e1d377c`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:acceeb297eaf31f93e6906604775e5006e905357b66d2db715a823a8e7e908e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5adbd38d16b93c0d9c91bbf64647a4797cc943cb91ede15425ea9c98aadcc3`

```dockerfile
```

-	Layers:
	-	`sha256:673d49936eb71cf43f174498e46a01d50e0c2fa55569ddabaf6a89017282ac80`  
		Last Modified: Mon, 05 Jan 2026 19:11:46 GMT  
		Size: 5.2 MB (5191986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a702c2f25535e61cd45014f764cb23c20e83bbd5f000e53e6e09d87081f52f92`  
		Last Modified: Mon, 05 Jan 2026 21:38:37 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3656743bda14dbf35e37a5d49ad8d7a0119e440175925a9e9290acf1e799ba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232194161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ee8bc4c9fdc6d75f2aa7d96655c9880cde7fb43ccb5e60d55e961bc54f3d5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:11:28 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:42 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 05 Jan 2026 19:11:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda0a0ee4ee06a63b34f79147295bcd10d0e4d7079300b1a798fbafbc02f42e`  
		Last Modified: Mon, 05 Jan 2026 19:12:01 GMT  
		Size: 14.6 MB (14557016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a752dcbcd035b2839f055dda6884357ea3322a984146224ce69190c2cdaeece2`  
		Last Modified: Mon, 05 Jan 2026 19:12:07 GMT  
		Size: 149.7 MB (149716184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e65bbf227894386072a79644aca8c3f73e31b8efe89e643daf869591897eaf`  
		Last Modified: Mon, 05 Jan 2026 19:12:00 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6de60d4014fe5f1a2a5542af9c8a92114921ad5ad028decfdec810ddd32bca`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484e309b1bc13680f84bdee3aaa8c7ebb40b95b68e6a62be719f3da29f7e556`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76716b5adcc69ce65a1e1e95f595c6a21314a0421b9cdd423b04f87ad2da402f`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f5d2c92ce82325a87aa6d386a9b9a1bc9af8519e5aa3fe9f6eee335eebe1ba`  
		Last Modified: Mon, 05 Jan 2026 19:12:14 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:5081058455472da36401b710986859e0e8dbfd23ac739bb72b5a1a0ded60881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58df3329c0ea4a099cd346e1c433f6cd08f048d4b5d03b6adf7f353575ccb97d`

```dockerfile
```

-	Layers:
	-	`sha256:1737789686ae3f5ff8f15dd06f06214439e6a8ad3bc16062e032b57b5f3c3946`  
		Last Modified: Mon, 05 Jan 2026 19:12:01 GMT  
		Size: 5.2 MB (5189893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef7eeaed136a7dd9c3ae0b593eeaf61704bc32d9c0c3bf720e414db79abb23a`  
		Last Modified: Mon, 05 Jan 2026 21:38:43 GMT  
		Size: 23.0 KB (22968 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:1cae9c8cfe814bee7867cb643619f3e50a0349687a44aa9e4f3d3f58b03a2aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:fd76d1b9f6a59fef3579849dcf70896b9cacffe4056f23c508a4af41d850ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233089624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01549dc152fc90ce2d01053f4f78f294e915562e5286006c28aeb9146b5bbc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:04 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:11:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f3eb4f912636d874a99e50ca38b6138a1046a2845df02f42ba4788e6415820`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 149.1 MB (149133558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33126ec70617c2e99a89ab94195ba8e70459d09a3dc20f03300770642bb5dbc3`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5587d8039e028413927960e0af3ad8eea851b7e6707aebf5e8a78eac3d868`  
		Last Modified: Mon, 05 Jan 2026 19:11:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499414e23067d6c17cc7429e7992bc2a846203ce8eef5126556618b7c584733`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa3768dc6a70044c58e97e4734af0b94c2b392c939b06a0213c54d35830018`  
		Last Modified: Mon, 05 Jan 2026 19:11:23 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c72c75614345c96f74616aab3677a5588f4afbbcc4e1501f6778bcd10b0d458`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:c60023a6b2bc8cf1613c25aa37a539981c2f18036a46edc182e28691e2f61d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00916d57213e9c242ca3931911e35cad649f74e1b171df2f62a5647d0e7aa253`

```dockerfile
```

-	Layers:
	-	`sha256:01294e1f930349abb8b726ff630f768ad6578e2f3cb0214c23069ee1b6f246b0`  
		Last Modified: Mon, 05 Jan 2026 21:38:47 GMT  
		Size: 5.2 MB (5191066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb8c597756ff70313672c657eb61bbff6632864b3d9416d59f88d6083792720`  
		Last Modified: Mon, 05 Jan 2026 21:39:06 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6f0588dd705130e20776deb2ea508469841e8d6df273c3ec9c795a79bdf83ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232299708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bd7fcb863de98748fcfb05f98e9bf7e5156eff79f17202a3a6cc2112d8fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:10:54 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:34 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60c36734288713909bd1d362d192cdd2d9e035d0f1a328f1defd96f22fd0397`  
		Last Modified: Mon, 05 Jan 2026 19:11:16 GMT  
		Size: 149.8 MB (149821958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b61c8be80805bcd77a5783eb3c40f15fd1a6a2eec77539b46f86622c0af9b`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22400d915397da65fea77ef50d015c6688d4187c74dc972d918e00cb87b8ac94`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7929a8cb6b03858daed57ba39f3ecd54441ce49cbcd7de07869f493db5b42ba`  
		Last Modified: Mon, 05 Jan 2026 19:11:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3f6f90a2a7ad07dc212640ea3241bccc789273ae92bc38e7c298b7009cd57`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a03a7b43c271c70f02ec765acc240757df3f9fd90691ccad53fd2f0f0a3c2c`  
		Last Modified: Mon, 05 Jan 2026 19:11:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:20454104972590ecee7bfadc2e0a9c23a73bd45625e7942854a30bd94a80e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e7da3c7e3d2c6a0feba043903912e9082dbb80860a46cc01d638bd6e54496`

```dockerfile
```

-	Layers:
	-	`sha256:24ed7c16ea6bb876f70125e1e0f702e220361e1fed5ffff77fcf79abbaa04cd5`  
		Last Modified: Mon, 05 Jan 2026 19:11:12 GMT  
		Size: 5.2 MB (5188985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127491178df144883dfa88b10e4117be855880c9abbb59f622ef9eda55f6639e`  
		Last Modified: Mon, 05 Jan 2026 21:39:13 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.2`

```console
$ docker pull crate@sha256:1cae9c8cfe814bee7867cb643619f3e50a0349687a44aa9e4f3d3f58b03a2aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.2` - linux; amd64

```console
$ docker pull crate@sha256:fd76d1b9f6a59fef3579849dcf70896b9cacffe4056f23c508a4af41d850ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233089624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01549dc152fc90ce2d01053f4f78f294e915562e5286006c28aeb9146b5bbc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:04 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:11:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f3eb4f912636d874a99e50ca38b6138a1046a2845df02f42ba4788e6415820`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 149.1 MB (149133558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33126ec70617c2e99a89ab94195ba8e70459d09a3dc20f03300770642bb5dbc3`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5587d8039e028413927960e0af3ad8eea851b7e6707aebf5e8a78eac3d868`  
		Last Modified: Mon, 05 Jan 2026 19:11:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499414e23067d6c17cc7429e7992bc2a846203ce8eef5126556618b7c584733`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa3768dc6a70044c58e97e4734af0b94c2b392c939b06a0213c54d35830018`  
		Last Modified: Mon, 05 Jan 2026 19:11:23 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c72c75614345c96f74616aab3677a5588f4afbbcc4e1501f6778bcd10b0d458`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.2` - unknown; unknown

```console
$ docker pull crate@sha256:c60023a6b2bc8cf1613c25aa37a539981c2f18036a46edc182e28691e2f61d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00916d57213e9c242ca3931911e35cad649f74e1b171df2f62a5647d0e7aa253`

```dockerfile
```

-	Layers:
	-	`sha256:01294e1f930349abb8b726ff630f768ad6578e2f3cb0214c23069ee1b6f246b0`  
		Last Modified: Mon, 05 Jan 2026 21:38:47 GMT  
		Size: 5.2 MB (5191066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb8c597756ff70313672c657eb61bbff6632864b3d9416d59f88d6083792720`  
		Last Modified: Mon, 05 Jan 2026 21:39:06 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6f0588dd705130e20776deb2ea508469841e8d6df273c3ec9c795a79bdf83ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232299708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bd7fcb863de98748fcfb05f98e9bf7e5156eff79f17202a3a6cc2112d8fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:10:54 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:34 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60c36734288713909bd1d362d192cdd2d9e035d0f1a328f1defd96f22fd0397`  
		Last Modified: Mon, 05 Jan 2026 19:11:16 GMT  
		Size: 149.8 MB (149821958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b61c8be80805bcd77a5783eb3c40f15fd1a6a2eec77539b46f86622c0af9b`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22400d915397da65fea77ef50d015c6688d4187c74dc972d918e00cb87b8ac94`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7929a8cb6b03858daed57ba39f3ecd54441ce49cbcd7de07869f493db5b42ba`  
		Last Modified: Mon, 05 Jan 2026 19:11:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3f6f90a2a7ad07dc212640ea3241bccc789273ae92bc38e7c298b7009cd57`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a03a7b43c271c70f02ec765acc240757df3f9fd90691ccad53fd2f0f0a3c2c`  
		Last Modified: Mon, 05 Jan 2026 19:11:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.2` - unknown; unknown

```console
$ docker pull crate@sha256:20454104972590ecee7bfadc2e0a9c23a73bd45625e7942854a30bd94a80e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e7da3c7e3d2c6a0feba043903912e9082dbb80860a46cc01d638bd6e54496`

```dockerfile
```

-	Layers:
	-	`sha256:24ed7c16ea6bb876f70125e1e0f702e220361e1fed5ffff77fcf79abbaa04cd5`  
		Last Modified: Mon, 05 Jan 2026 19:11:12 GMT  
		Size: 5.2 MB (5188985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127491178df144883dfa88b10e4117be855880c9abbb59f622ef9eda55f6639e`  
		Last Modified: Mon, 05 Jan 2026 21:39:13 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:1cae9c8cfe814bee7867cb643619f3e50a0349687a44aa9e4f3d3f58b03a2aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:fd76d1b9f6a59fef3579849dcf70896b9cacffe4056f23c508a4af41d850ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233089624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01549dc152fc90ce2d01053f4f78f294e915562e5286006c28aeb9146b5bbc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:04 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:11:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f3eb4f912636d874a99e50ca38b6138a1046a2845df02f42ba4788e6415820`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 149.1 MB (149133558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33126ec70617c2e99a89ab94195ba8e70459d09a3dc20f03300770642bb5dbc3`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5587d8039e028413927960e0af3ad8eea851b7e6707aebf5e8a78eac3d868`  
		Last Modified: Mon, 05 Jan 2026 19:11:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499414e23067d6c17cc7429e7992bc2a846203ce8eef5126556618b7c584733`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa3768dc6a70044c58e97e4734af0b94c2b392c939b06a0213c54d35830018`  
		Last Modified: Mon, 05 Jan 2026 19:11:23 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c72c75614345c96f74616aab3677a5588f4afbbcc4e1501f6778bcd10b0d458`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c60023a6b2bc8cf1613c25aa37a539981c2f18036a46edc182e28691e2f61d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00916d57213e9c242ca3931911e35cad649f74e1b171df2f62a5647d0e7aa253`

```dockerfile
```

-	Layers:
	-	`sha256:01294e1f930349abb8b726ff630f768ad6578e2f3cb0214c23069ee1b6f246b0`  
		Last Modified: Mon, 05 Jan 2026 21:38:47 GMT  
		Size: 5.2 MB (5191066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb8c597756ff70313672c657eb61bbff6632864b3d9416d59f88d6083792720`  
		Last Modified: Mon, 05 Jan 2026 21:39:06 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6f0588dd705130e20776deb2ea508469841e8d6df273c3ec9c795a79bdf83ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232299708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bd7fcb863de98748fcfb05f98e9bf7e5156eff79f17202a3a6cc2112d8fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:10:54 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:34 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60c36734288713909bd1d362d192cdd2d9e035d0f1a328f1defd96f22fd0397`  
		Last Modified: Mon, 05 Jan 2026 19:11:16 GMT  
		Size: 149.8 MB (149821958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b61c8be80805bcd77a5783eb3c40f15fd1a6a2eec77539b46f86622c0af9b`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22400d915397da65fea77ef50d015c6688d4187c74dc972d918e00cb87b8ac94`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7929a8cb6b03858daed57ba39f3ecd54441ce49cbcd7de07869f493db5b42ba`  
		Last Modified: Mon, 05 Jan 2026 19:11:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3f6f90a2a7ad07dc212640ea3241bccc789273ae92bc38e7c298b7009cd57`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a03a7b43c271c70f02ec765acc240757df3f9fd90691ccad53fd2f0f0a3c2c`  
		Last Modified: Mon, 05 Jan 2026 19:11:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:20454104972590ecee7bfadc2e0a9c23a73bd45625e7942854a30bd94a80e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e7da3c7e3d2c6a0feba043903912e9082dbb80860a46cc01d638bd6e54496`

```dockerfile
```

-	Layers:
	-	`sha256:24ed7c16ea6bb876f70125e1e0f702e220361e1fed5ffff77fcf79abbaa04cd5`  
		Last Modified: Mon, 05 Jan 2026 19:11:12 GMT  
		Size: 5.2 MB (5188985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127491178df144883dfa88b10e4117be855880c9abbb59f622ef9eda55f6639e`  
		Last Modified: Mon, 05 Jan 2026 21:39:13 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
