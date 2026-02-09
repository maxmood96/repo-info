## `crate:latest`

```console
$ docker pull crate@sha256:8a376b20b70675825402315fd436402b6b67353c0a1763c2583fddfe863d4e16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:03f3d51f8726d08b3ff9ed7318d5f6f364df68c132055eb59dfecc4e511bbe1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247588307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9705bff711b60cb4e88ecf0a1391b457ea081bce06d10c9ba3e69c959321b90c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:50:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Feb 2026 19:50:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:50:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Feb 2026 19:50:49 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
VOLUME [/data]
# Mon, 09 Feb 2026 19:50:49 GMT
WORKDIR /data
# Mon, 09 Feb 2026 19:50:49 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Feb 2026 19:50:49 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Mon, 09 Feb 2026 19:50:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:50:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:50:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587925aa4022fe76691fabcff65ca7f74478decbc6c21aabe9b5ec5100ce5749`  
		Last Modified: Mon, 09 Feb 2026 19:51:06 GMT  
		Size: 26.8 MB (26817687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cfd321c6147dd35c2d1203bee823f67b059a85154240e7c0e3845baaa0dc4`  
		Last Modified: Mon, 09 Feb 2026 19:51:09 GMT  
		Size: 151.3 MB (151327540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c440832afa389870f5d86c01e307230c2a1c9ed94b9b94274e46a772144dbf1b`  
		Last Modified: Mon, 09 Feb 2026 19:51:05 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389371ce375cbed42cf842e217ca921a0306f4961c59c6f69461173f256f9a3`  
		Last Modified: Mon, 09 Feb 2026 19:51:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621f73eb8a0d92cb37efc374f4c4abc44b169a97fa330eea4a9286256b10f3b2`  
		Last Modified: Mon, 09 Feb 2026 19:51:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dc9ac200fcdc77849027c3eb6253998e48916c0e7dcaffec0f30b0cebc3131`  
		Last Modified: Mon, 09 Feb 2026 19:51:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab054d00df6945082440a940dc8f11d37cfaa70ae1cb578a7a7f496dbf45f4`  
		Last Modified: Mon, 09 Feb 2026 19:51:08 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:0472771220581aeb511e1d3fa29d695e0e3300d78cea514b5051cbba3b6c1f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4df075ed9575c09bf76429d035a77c84a1d7cddd65cbcc8b21fa14d0f57409`

```dockerfile
```

-	Layers:
	-	`sha256:abdf4c4dd3257fcf72f71f0ece8c42c5af42b3700cdc41e19b8869aba00a464e`  
		Last Modified: Mon, 09 Feb 2026 19:51:05 GMT  
		Size: 5.2 MB (5154796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee09cd55a1893e341b9d861a2ab1cfad53aaee7d7e84996deb965d7124a90da`  
		Last Modified: Mon, 09 Feb 2026 19:51:05 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:06489771e3259546351d3499945953f98d1f5b28c2432cc06f0ace845e0372df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243963592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5631e423d700b7a6f9dcafcab114ed5f45d6c4b3f274adb2db4fc9d90911c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:51:50 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Feb 2026 19:52:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:52:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Feb 2026 19:52:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
VOLUME [/data]
# Mon, 09 Feb 2026 19:52:04 GMT
WORKDIR /data
# Mon, 09 Feb 2026 19:52:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Feb 2026 19:52:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Mon, 09 Feb 2026 19:52:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:52:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca219f362a8f6ca53bfbb26defeb91342608550469117b0bf74810c2f8276b6`  
		Last Modified: Mon, 09 Feb 2026 19:52:23 GMT  
		Size: 26.7 MB (26739934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7893f6157fc9acf8fb2c54ffb3513b12bb966699add1ce56defacbb6e594194`  
		Last Modified: Mon, 09 Feb 2026 19:52:26 GMT  
		Size: 149.3 MB (149299629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c0200de10107e5307b57a815c85143f1cc746a88ba615653f461c6823072`  
		Last Modified: Mon, 09 Feb 2026 19:52:22 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f1f4066c55fd711b1ce58b6ccdfc2c9275c36cda61072b90630ed4d058447f`  
		Last Modified: Mon, 09 Feb 2026 19:52:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de30cfe1b039316047895467bc7bbadf08139a843749a654e98719c37c1919b6`  
		Last Modified: Mon, 09 Feb 2026 19:52:23 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aae73825704262a18034f369e7ee7d6a6c359ec6680258d1440df36a4fbe2c`  
		Last Modified: Mon, 09 Feb 2026 19:52:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e937f979d0f7a91d28b1319fc46184df6fc76f126c9797034e7da9e43e572`  
		Last Modified: Mon, 09 Feb 2026 19:52:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:e5af0df6f8a270a8844d91252bcd169429ba03cf1bb88fcb6f45d25bd7221e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff6240fb66cf80fa72c41e12ad2c70a9874335e99d0ffc334a56e6e64a629ee`

```dockerfile
```

-	Layers:
	-	`sha256:d106834d8387b7ca42a2c5f29c7147311c4e617edb2ca1425def73f2eccc5d1f`  
		Last Modified: Mon, 09 Feb 2026 19:52:22 GMT  
		Size: 5.2 MB (5152715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517e3ac5067fb4a9b0fa752800bec54689205c3d8ff5de131cb51d293dfd9be1`  
		Last Modified: Mon, 09 Feb 2026 19:52:22 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
