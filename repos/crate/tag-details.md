<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.7`](#crate5107)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:f9b2a2039ad1a793e7f64267b44b8d5d9442314235e6cb45b219b33a010c4634
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:f8b75c5398dcfd7d93f4287ead916a7b91eb36449a749a1b17313e7a21d5a1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234152850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213309da335c806853039944dc33bd7815399715666c95cbf47a57652f05ceeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e721abbbcb58c29477a55c8d3d3b30cab0e2e8924454729683616bd8488c936c`  
		Last Modified: Wed, 11 Jun 2025 20:38:45 GMT  
		Size: 15.4 MB (15357879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d817f2dcf68a444aff0445c5c0c81db7f01842004d965b6cebfb02dd7ceac0f`  
		Last Modified: Wed, 11 Jun 2025 20:38:58 GMT  
		Size: 149.7 MB (149661544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf15ba17ff1596ed61a733be27c3d2e1a42cd923d39a35324d88b899aef1d486`  
		Last Modified: Wed, 11 Jun 2025 18:11:43 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0df149301b226294672f6c3e285b35eca59c12d0f52efc097dc62d81b489d`  
		Last Modified: Wed, 11 Jun 2025 18:11:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b69c8ca518ff60df6ae5fade6713749e82608085596af9c285ae42404905c8`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a857f25fa4a78fcdf41c80a30476a16e5459e088c8982cb593a19391fa0dcf`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:7b4611be72809687b46ea670d83b9cebe0ca3ce6119595db2d853accc4758ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9323e1812dce74fbcbfbab6957f12e55612ccdbb4af4a7fdabf572cda9b515`

```dockerfile
```

-	Layers:
	-	`sha256:28c69fb962f91294a732a6b4944fec9b147bd621e88b986f3d41be2920db4875`  
		Last Modified: Wed, 11 Jun 2025 20:38:20 GMT  
		Size: 5.2 MB (5183295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc37bdcff6b6b8324392b45419020766a490e4fc0a53650b5f4f6b8f4ab727`  
		Last Modified: Wed, 11 Jun 2025 20:38:21 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:256d0d0465f518a80107e6fc04e78d8072ee63cf8244616b4416487f7f607b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246202890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e415bbb65420a0a0d97b99cc2c5ae8ffea2c6b3e161a4ce2b392b5af2d5fc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 20 May 2025 20:59:41 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 03 Jun 2025 14:13:30 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8421c9df578ba6bad1db1ec176a188676bf7966c176f2e1a492a0a3d2943f7`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 28.2 MB (28178764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e1fcb47651128bd05a221ad5ae6b98863916548a3715729e496c6b03a0d0f`  
		Last Modified: Tue, 03 Jun 2025 17:06:54 GMT  
		Size: 150.3 MB (150336847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3cfcf2a6461665f8a5953767115ca0199df577e04094be4d624ef7999439c`  
		Last Modified: Tue, 03 Jun 2025 17:06:57 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e92e67b5c49e73c87d608cba2ff0d6d63fc31984e412ee1fdfc346c528c10`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d011e3bee0571a4b3f3441e3bde84430481a5d3ec85e31ff5fff80af33ed80f5`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8962b95e995bcc27270db0e7bde19b0ffb81ee4cdb52871a0c00f4d565f5f00`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce68581250d5947f6d48b788d933540d0f606f9526fc05711574d4147b4a75`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:d6e409c20c21347eff83fb9dd78b4529b4cd8e86ac4f5efd78f8d35e59659064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe3d6ce1801985edf2b81f54c1e029d8890ea69637e71e60fed0c83ec08b497`

```dockerfile
```

-	Layers:
	-	`sha256:f6710111fb7b4e0ff8f9ec8b35d0dff0d5f38ab6b75fb0c4256e43772c1af0be`  
		Last Modified: Wed, 11 Jun 2025 02:57:03 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Wed, 11 Jun 2025 02:57:00 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.7`

```console
$ docker pull crate@sha256:f9b2a2039ad1a793e7f64267b44b8d5d9442314235e6cb45b219b33a010c4634
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.7` - linux; amd64

```console
$ docker pull crate@sha256:f8b75c5398dcfd7d93f4287ead916a7b91eb36449a749a1b17313e7a21d5a1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234152850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213309da335c806853039944dc33bd7815399715666c95cbf47a57652f05ceeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e721abbbcb58c29477a55c8d3d3b30cab0e2e8924454729683616bd8488c936c`  
		Last Modified: Wed, 11 Jun 2025 20:38:45 GMT  
		Size: 15.4 MB (15357879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d817f2dcf68a444aff0445c5c0c81db7f01842004d965b6cebfb02dd7ceac0f`  
		Last Modified: Wed, 11 Jun 2025 20:38:58 GMT  
		Size: 149.7 MB (149661544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf15ba17ff1596ed61a733be27c3d2e1a42cd923d39a35324d88b899aef1d486`  
		Last Modified: Wed, 11 Jun 2025 18:11:43 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0df149301b226294672f6c3e285b35eca59c12d0f52efc097dc62d81b489d`  
		Last Modified: Wed, 11 Jun 2025 18:11:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b69c8ca518ff60df6ae5fade6713749e82608085596af9c285ae42404905c8`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a857f25fa4a78fcdf41c80a30476a16e5459e088c8982cb593a19391fa0dcf`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.7` - unknown; unknown

```console
$ docker pull crate@sha256:7b4611be72809687b46ea670d83b9cebe0ca3ce6119595db2d853accc4758ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9323e1812dce74fbcbfbab6957f12e55612ccdbb4af4a7fdabf572cda9b515`

```dockerfile
```

-	Layers:
	-	`sha256:28c69fb962f91294a732a6b4944fec9b147bd621e88b986f3d41be2920db4875`  
		Last Modified: Wed, 11 Jun 2025 20:38:20 GMT  
		Size: 5.2 MB (5183295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc37bdcff6b6b8324392b45419020766a490e4fc0a53650b5f4f6b8f4ab727`  
		Last Modified: Wed, 11 Jun 2025 20:38:21 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:256d0d0465f518a80107e6fc04e78d8072ee63cf8244616b4416487f7f607b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246202890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e415bbb65420a0a0d97b99cc2c5ae8ffea2c6b3e161a4ce2b392b5af2d5fc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 20 May 2025 20:59:41 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 03 Jun 2025 14:13:30 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8421c9df578ba6bad1db1ec176a188676bf7966c176f2e1a492a0a3d2943f7`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 28.2 MB (28178764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e1fcb47651128bd05a221ad5ae6b98863916548a3715729e496c6b03a0d0f`  
		Last Modified: Tue, 03 Jun 2025 17:06:54 GMT  
		Size: 150.3 MB (150336847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3cfcf2a6461665f8a5953767115ca0199df577e04094be4d624ef7999439c`  
		Last Modified: Tue, 03 Jun 2025 17:06:57 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e92e67b5c49e73c87d608cba2ff0d6d63fc31984e412ee1fdfc346c528c10`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d011e3bee0571a4b3f3441e3bde84430481a5d3ec85e31ff5fff80af33ed80f5`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8962b95e995bcc27270db0e7bde19b0ffb81ee4cdb52871a0c00f4d565f5f00`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce68581250d5947f6d48b788d933540d0f606f9526fc05711574d4147b4a75`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.7` - unknown; unknown

```console
$ docker pull crate@sha256:d6e409c20c21347eff83fb9dd78b4529b4cd8e86ac4f5efd78f8d35e59659064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe3d6ce1801985edf2b81f54c1e029d8890ea69637e71e60fed0c83ec08b497`

```dockerfile
```

-	Layers:
	-	`sha256:f6710111fb7b4e0ff8f9ec8b35d0dff0d5f38ab6b75fb0c4256e43772c1af0be`  
		Last Modified: Wed, 11 Jun 2025 02:57:03 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Wed, 11 Jun 2025 02:57:00 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:f8eaa17a9743f27704e44e1c35e5a7536896acb4c8dd7f4e31046d3825842457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:5b4446f6465c45ec8b1d490dd978596ec48a0593aaea164500ebaa6e6433ac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233500953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db96544d983dee5a0e34312c086a49add28a1de1dce76aa2764faa13e4d4fa14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b65326593f93bdd91d295d7e557450e325451b3b3b1b93f6a40fb1963a36f`  
		Last Modified: Wed, 11 Jun 2025 18:05:11 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 18:05:13 GMT  
		Size: 149.0 MB (149009698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a10eb670d32e35520cbddc7a9350633f3b91ce0c44f08a6c11ce115b500fca`  
		Last Modified: Wed, 11 Jun 2025 18:10:05 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d190e0a48abb2f0c93b39f6f891ebc627e5aba0f3bf302a4b7b5963d797fa14`  
		Last Modified: Wed, 11 Jun 2025 18:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10e918c1f6fd6245d53606186c00c196e41b38468b78d23d62b6108373707d7`  
		Last Modified: Wed, 11 Jun 2025 18:10:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94e6e4cfc75c14691e52244fb83defb2b7552e499311ef8d82634218375f5f`  
		Last Modified: Wed, 11 Jun 2025 18:10:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:4c4160f567b7e8d331e2a5736cb5f096bb9efba1091dd12c66aa7046314888c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5901757c1bcfb4fcb9f4c942783703a5a0f7feb7a18c1e9cfcb0a037e1244ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5c9a4f0c90b41fd3ed3fabb7aa63dc9a6b160cfe85452c13ad2157706652b030`  
		Last Modified: Wed, 11 Jun 2025 20:38:26 GMT  
		Size: 5.2 MB (5181428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aa68934dd28bbf5541eab122c195a8c33f9f8cd6b7aee38286d65c938cf924`  
		Last Modified: Wed, 11 Jun 2025 20:38:27 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:240133e4dfb02cd9ac38033f4bf455f8e4c7335974bd90a2c6b0c54607667768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232870865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea976b5623f273f89347063c796b298e0c72e9ddf3287fb1d8c6055d9d21c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 03 Jun 2025 14:13:30 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e25f1665ae5c3fce08cbaa86a27dbd468087c2e48e4b1d3f50316265d8aa6`  
		Last Modified: Tue, 20 May 2025 21:36:02 GMT  
		Size: 149.7 MB (149708577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d5e2d0f8f9da3244218732c75a2dca1be6cbdb9d7ad9166540bcac87373454`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9071465ca3719ad9937260bc70fde031fd45ad5b2f4f3f8fe6b87bf5474760b`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88279d887e62c03cbe416998e82c03f3416dbb14edec74a732a633120df730`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe376dd8d1ceaddea988006e242601369ff886914d3da06fbf41517d44b544b2`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea881fae8579feb45d6ac18970f3e5002ab453b5f8359d5f000ea39062dfa7`  
		Last Modified: Tue, 20 May 2025 21:36:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:38f3064444f672e50bc8730f55369de836e25d9b737843d01f7d7315f899b82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5fcd8719594ca1341547510a352936435bc34ebb6266aecd017eccf9917813`

```dockerfile
```

-	Layers:
	-	`sha256:123d34466579c123f0a9d090ce68afd61e19d2d28e550c72dc8ad8d675941e0c`  
		Last Modified: Wed, 11 Jun 2025 20:38:33 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Wed, 11 Jun 2025 20:38:33 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:f8eaa17a9743f27704e44e1c35e5a7536896acb4c8dd7f4e31046d3825842457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:5b4446f6465c45ec8b1d490dd978596ec48a0593aaea164500ebaa6e6433ac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233500953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db96544d983dee5a0e34312c086a49add28a1de1dce76aa2764faa13e4d4fa14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b65326593f93bdd91d295d7e557450e325451b3b3b1b93f6a40fb1963a36f`  
		Last Modified: Wed, 11 Jun 2025 18:05:11 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 18:05:13 GMT  
		Size: 149.0 MB (149009698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a10eb670d32e35520cbddc7a9350633f3b91ce0c44f08a6c11ce115b500fca`  
		Last Modified: Wed, 11 Jun 2025 18:10:05 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d190e0a48abb2f0c93b39f6f891ebc627e5aba0f3bf302a4b7b5963d797fa14`  
		Last Modified: Wed, 11 Jun 2025 18:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10e918c1f6fd6245d53606186c00c196e41b38468b78d23d62b6108373707d7`  
		Last Modified: Wed, 11 Jun 2025 18:10:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94e6e4cfc75c14691e52244fb83defb2b7552e499311ef8d82634218375f5f`  
		Last Modified: Wed, 11 Jun 2025 18:10:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:4c4160f567b7e8d331e2a5736cb5f096bb9efba1091dd12c66aa7046314888c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5901757c1bcfb4fcb9f4c942783703a5a0f7feb7a18c1e9cfcb0a037e1244ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5c9a4f0c90b41fd3ed3fabb7aa63dc9a6b160cfe85452c13ad2157706652b030`  
		Last Modified: Wed, 11 Jun 2025 20:38:26 GMT  
		Size: 5.2 MB (5181428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aa68934dd28bbf5541eab122c195a8c33f9f8cd6b7aee38286d65c938cf924`  
		Last Modified: Wed, 11 Jun 2025 20:38:27 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:240133e4dfb02cd9ac38033f4bf455f8e4c7335974bd90a2c6b0c54607667768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232870865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea976b5623f273f89347063c796b298e0c72e9ddf3287fb1d8c6055d9d21c73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 03 Jun 2025 14:13:30 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e25f1665ae5c3fce08cbaa86a27dbd468087c2e48e4b1d3f50316265d8aa6`  
		Last Modified: Tue, 20 May 2025 21:36:02 GMT  
		Size: 149.7 MB (149708577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d5e2d0f8f9da3244218732c75a2dca1be6cbdb9d7ad9166540bcac87373454`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9071465ca3719ad9937260bc70fde031fd45ad5b2f4f3f8fe6b87bf5474760b`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88279d887e62c03cbe416998e82c03f3416dbb14edec74a732a633120df730`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe376dd8d1ceaddea988006e242601369ff886914d3da06fbf41517d44b544b2`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea881fae8579feb45d6ac18970f3e5002ab453b5f8359d5f000ea39062dfa7`  
		Last Modified: Tue, 20 May 2025 21:36:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:38f3064444f672e50bc8730f55369de836e25d9b737843d01f7d7315f899b82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5fcd8719594ca1341547510a352936435bc34ebb6266aecd017eccf9917813`

```dockerfile
```

-	Layers:
	-	`sha256:123d34466579c123f0a9d090ce68afd61e19d2d28e550c72dc8ad8d675941e0c`  
		Last Modified: Wed, 11 Jun 2025 20:38:33 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Wed, 11 Jun 2025 20:38:33 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:f9b2a2039ad1a793e7f64267b44b8d5d9442314235e6cb45b219b33a010c4634
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f8b75c5398dcfd7d93f4287ead916a7b91eb36449a749a1b17313e7a21d5a1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234152850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213309da335c806853039944dc33bd7815399715666c95cbf47a57652f05ceeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e721abbbcb58c29477a55c8d3d3b30cab0e2e8924454729683616bd8488c936c`  
		Last Modified: Wed, 11 Jun 2025 20:38:45 GMT  
		Size: 15.4 MB (15357879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d817f2dcf68a444aff0445c5c0c81db7f01842004d965b6cebfb02dd7ceac0f`  
		Last Modified: Wed, 11 Jun 2025 20:38:58 GMT  
		Size: 149.7 MB (149661544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf15ba17ff1596ed61a733be27c3d2e1a42cd923d39a35324d88b899aef1d486`  
		Last Modified: Wed, 11 Jun 2025 18:11:43 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0df149301b226294672f6c3e285b35eca59c12d0f52efc097dc62d81b489d`  
		Last Modified: Wed, 11 Jun 2025 18:11:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b69c8ca518ff60df6ae5fade6713749e82608085596af9c285ae42404905c8`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a857f25fa4a78fcdf41c80a30476a16e5459e088c8982cb593a19391fa0dcf`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7b4611be72809687b46ea670d83b9cebe0ca3ce6119595db2d853accc4758ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9323e1812dce74fbcbfbab6957f12e55612ccdbb4af4a7fdabf572cda9b515`

```dockerfile
```

-	Layers:
	-	`sha256:28c69fb962f91294a732a6b4944fec9b147bd621e88b986f3d41be2920db4875`  
		Last Modified: Wed, 11 Jun 2025 20:38:20 GMT  
		Size: 5.2 MB (5183295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc37bdcff6b6b8324392b45419020766a490e4fc0a53650b5f4f6b8f4ab727`  
		Last Modified: Wed, 11 Jun 2025 20:38:21 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:256d0d0465f518a80107e6fc04e78d8072ee63cf8244616b4416487f7f607b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246202890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e415bbb65420a0a0d97b99cc2c5ae8ffea2c6b3e161a4ce2b392b5af2d5fc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 20 May 2025 20:59:41 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 03 Jun 2025 14:13:30 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8421c9df578ba6bad1db1ec176a188676bf7966c176f2e1a492a0a3d2943f7`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 28.2 MB (28178764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e1fcb47651128bd05a221ad5ae6b98863916548a3715729e496c6b03a0d0f`  
		Last Modified: Tue, 03 Jun 2025 17:06:54 GMT  
		Size: 150.3 MB (150336847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3cfcf2a6461665f8a5953767115ca0199df577e04094be4d624ef7999439c`  
		Last Modified: Tue, 03 Jun 2025 17:06:57 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e92e67b5c49e73c87d608cba2ff0d6d63fc31984e412ee1fdfc346c528c10`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d011e3bee0571a4b3f3441e3bde84430481a5d3ec85e31ff5fff80af33ed80f5`  
		Last Modified: Tue, 03 Jun 2025 17:06:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8962b95e995bcc27270db0e7bde19b0ffb81ee4cdb52871a0c00f4d565f5f00`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce68581250d5947f6d48b788d933540d0f606f9526fc05711574d4147b4a75`  
		Last Modified: Tue, 03 Jun 2025 17:06:49 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d6e409c20c21347eff83fb9dd78b4529b4cd8e86ac4f5efd78f8d35e59659064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe3d6ce1801985edf2b81f54c1e029d8890ea69637e71e60fed0c83ec08b497`

```dockerfile
```

-	Layers:
	-	`sha256:f6710111fb7b4e0ff8f9ec8b35d0dff0d5f38ab6b75fb0c4256e43772c1af0be`  
		Last Modified: Wed, 11 Jun 2025 02:57:03 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Wed, 11 Jun 2025 02:57:00 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
