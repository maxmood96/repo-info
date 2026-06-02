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
