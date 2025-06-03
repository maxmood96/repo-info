<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.7`](#crate5107)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:c5caade92e46ecea1c3314bcb655657f6a9410bb02f4619b44f71d4665cd3313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:edfba2a524615e9f1b638fdffdaa9ab153f33e023c4e95fd9a7918c7e4d28c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247095743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd49976110aec71763897aa8ff78d32d17d09e47e20ec278ba13a30cccbdd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835ce96e6b1f27bdd0c0224485a36f9c6085f68fd66481fd5a934561d71364b`  
		Last Modified: Tue, 03 Jun 2025 13:36:12 GMT  
		Size: 28.3 MB (28266988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd78e0a9d38b7423dd2c928378e0375e88d7b00f93b1c984b5a10f420dbd8c`  
		Last Modified: Tue, 03 Jun 2025 13:36:26 GMT  
		Size: 149.7 MB (149661519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f5e50714391c01347a5e87166042cddce0697062e5004d7d6adf1e4c816761`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0537a3ac1d941f6ff797f52a2e097e34d32a8cbf658139e30906dd60abfb41d`  
		Last Modified: Tue, 03 Jun 2025 13:36:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238c067bbdde41138d1a979a174eefae1e7ff27a798d30d2be08c2f274b5f507`  
		Last Modified: Tue, 03 Jun 2025 13:36:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa72989d662935776dd298812cecb8a7ff22540404f7ca06b42fcf6bed0c3c`  
		Last Modified: Tue, 03 Jun 2025 13:36:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79d0aaf656d50df0d2f3ad836623caa999672bb5d42505cac64b0780aa418cf`  
		Last Modified: Tue, 03 Jun 2025 13:36:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:f53473c2ddc77ba6ffc56168ae5339143108727169189274b7050672dc65e708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acebf4d2ca0eef89d9d45e182c57c09e1646424b340ade018e9ba85d4c549995`

```dockerfile
```

-	Layers:
	-	`sha256:4e66c4629743f056f8ef8b051000f228f0af37fa6c973d22fdf952782b7fa810`  
		Last Modified: Tue, 03 Jun 2025 14:16:16 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5f9c124183771f88e669251a51b30a5bc390a790692966075d0e442945233`  
		Last Modified: Tue, 03 Jun 2025 14:16:17 GMT  
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
		Last Modified: Thu, 29 May 2025 18:12:16 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Thu, 29 May 2025 18:12:15 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.7`

```console
$ docker pull crate@sha256:c5caade92e46ecea1c3314bcb655657f6a9410bb02f4619b44f71d4665cd3313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.7` - linux; amd64

```console
$ docker pull crate@sha256:edfba2a524615e9f1b638fdffdaa9ab153f33e023c4e95fd9a7918c7e4d28c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247095743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd49976110aec71763897aa8ff78d32d17d09e47e20ec278ba13a30cccbdd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835ce96e6b1f27bdd0c0224485a36f9c6085f68fd66481fd5a934561d71364b`  
		Last Modified: Tue, 03 Jun 2025 13:36:12 GMT  
		Size: 28.3 MB (28266988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd78e0a9d38b7423dd2c928378e0375e88d7b00f93b1c984b5a10f420dbd8c`  
		Last Modified: Tue, 03 Jun 2025 13:36:26 GMT  
		Size: 149.7 MB (149661519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f5e50714391c01347a5e87166042cddce0697062e5004d7d6adf1e4c816761`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0537a3ac1d941f6ff797f52a2e097e34d32a8cbf658139e30906dd60abfb41d`  
		Last Modified: Tue, 03 Jun 2025 13:36:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238c067bbdde41138d1a979a174eefae1e7ff27a798d30d2be08c2f274b5f507`  
		Last Modified: Tue, 03 Jun 2025 13:36:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa72989d662935776dd298812cecb8a7ff22540404f7ca06b42fcf6bed0c3c`  
		Last Modified: Tue, 03 Jun 2025 13:36:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79d0aaf656d50df0d2f3ad836623caa999672bb5d42505cac64b0780aa418cf`  
		Last Modified: Tue, 03 Jun 2025 13:36:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.7` - unknown; unknown

```console
$ docker pull crate@sha256:f53473c2ddc77ba6ffc56168ae5339143108727169189274b7050672dc65e708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acebf4d2ca0eef89d9d45e182c57c09e1646424b340ade018e9ba85d4c549995`

```dockerfile
```

-	Layers:
	-	`sha256:4e66c4629743f056f8ef8b051000f228f0af37fa6c973d22fdf952782b7fa810`  
		Last Modified: Tue, 03 Jun 2025 14:16:16 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5f9c124183771f88e669251a51b30a5bc390a790692966075d0e442945233`  
		Last Modified: Tue, 03 Jun 2025 14:16:17 GMT  
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
		Last Modified: Thu, 29 May 2025 18:12:16 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Thu, 29 May 2025 18:12:15 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:ae26ed73e2c4936fae3796160dbef7d09a66c3ca8cee148235d95a0121631e61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:084a04c51e5d125a3e12143854575e5e9ed6096436fc76489f37a3d8f75c840f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233598122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c116f493891f09c1e6ed04348a35b6f1de4330ca3a9f2a82a26b4deacc29c2f`
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0bf3fca5b5cc6ca367287374cec091954893be167b0e058b557fb9c8cada0`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 15.4 MB (15421182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ebde60ec227c951cb7f500c7b33114a77c068572ed97259beb4ba68e7a0690`  
		Last Modified: Tue, 20 May 2025 21:36:20 GMT  
		Size: 149.0 MB (149009708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e7dfb2c65caf1a63cfbfff27c15147d5d77fce970166d44c325b3437c91d8`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2486ae9b744af5cbd0a2548d1e975f6c9236999a1f499c1a5fb31f5d9ddc2b`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488da3fd806f4aeb510977b15cf933f8cafe576457eceb262671b7346a2b74a`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a4ca7bc0363fde84883ac9c06f69a0f20789af443af9a66ae87ae2d0c89a3`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b5f2398c0016e43b99037d2131ead2af52542cc6cb5ecfa023386fede11973`  
		Last Modified: Tue, 20 May 2025 21:36:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:cf1aaeb402a4ba66648bbf9760f1e02a53a9db39735db472619270246f053a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97595934d167d66b46d961c6dc4f10468872c8c19d94ad22a11591edc3902bcd`

```dockerfile
```

-	Layers:
	-	`sha256:d12a80722e38c1e7de23a581902bd56f41e8ba2cc4fe1c8200c168d61b7fc312`  
		Last Modified: Tue, 03 Jun 2025 14:16:30 GMT  
		Size: 5.2 MB (5178426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25169c71ab59d7452bafca4aca1d8272877f72a138a29a30d272c8074c5dc36b`  
		Last Modified: Tue, 03 Jun 2025 14:16:32 GMT  
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
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:ae26ed73e2c4936fae3796160dbef7d09a66c3ca8cee148235d95a0121631e61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:084a04c51e5d125a3e12143854575e5e9ed6096436fc76489f37a3d8f75c840f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233598122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c116f493891f09c1e6ed04348a35b6f1de4330ca3a9f2a82a26b4deacc29c2f`
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0bf3fca5b5cc6ca367287374cec091954893be167b0e058b557fb9c8cada0`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 15.4 MB (15421182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ebde60ec227c951cb7f500c7b33114a77c068572ed97259beb4ba68e7a0690`  
		Last Modified: Tue, 20 May 2025 21:36:20 GMT  
		Size: 149.0 MB (149009708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e7dfb2c65caf1a63cfbfff27c15147d5d77fce970166d44c325b3437c91d8`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2486ae9b744af5cbd0a2548d1e975f6c9236999a1f499c1a5fb31f5d9ddc2b`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488da3fd806f4aeb510977b15cf933f8cafe576457eceb262671b7346a2b74a`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a4ca7bc0363fde84883ac9c06f69a0f20789af443af9a66ae87ae2d0c89a3`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b5f2398c0016e43b99037d2131ead2af52542cc6cb5ecfa023386fede11973`  
		Last Modified: Tue, 20 May 2025 21:36:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:cf1aaeb402a4ba66648bbf9760f1e02a53a9db39735db472619270246f053a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97595934d167d66b46d961c6dc4f10468872c8c19d94ad22a11591edc3902bcd`

```dockerfile
```

-	Layers:
	-	`sha256:d12a80722e38c1e7de23a581902bd56f41e8ba2cc4fe1c8200c168d61b7fc312`  
		Last Modified: Tue, 03 Jun 2025 14:16:30 GMT  
		Size: 5.2 MB (5178426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25169c71ab59d7452bafca4aca1d8272877f72a138a29a30d272c8074c5dc36b`  
		Last Modified: Tue, 03 Jun 2025 14:16:32 GMT  
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
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:c5caade92e46ecea1c3314bcb655657f6a9410bb02f4619b44f71d4665cd3313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:edfba2a524615e9f1b638fdffdaa9ab153f33e023c4e95fd9a7918c7e4d28c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247095743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd49976110aec71763897aa8ff78d32d17d09e47e20ec278ba13a30cccbdd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 20 May 2025 20:59:41 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835ce96e6b1f27bdd0c0224485a36f9c6085f68fd66481fd5a934561d71364b`  
		Last Modified: Tue, 03 Jun 2025 13:36:12 GMT  
		Size: 28.3 MB (28266988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd78e0a9d38b7423dd2c928378e0375e88d7b00f93b1c984b5a10f420dbd8c`  
		Last Modified: Tue, 03 Jun 2025 13:36:26 GMT  
		Size: 149.7 MB (149661519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f5e50714391c01347a5e87166042cddce0697062e5004d7d6adf1e4c816761`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0537a3ac1d941f6ff797f52a2e097e34d32a8cbf658139e30906dd60abfb41d`  
		Last Modified: Tue, 03 Jun 2025 13:36:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238c067bbdde41138d1a979a174eefae1e7ff27a798d30d2be08c2f274b5f507`  
		Last Modified: Tue, 03 Jun 2025 13:36:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa72989d662935776dd298812cecb8a7ff22540404f7ca06b42fcf6bed0c3c`  
		Last Modified: Tue, 03 Jun 2025 13:36:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79d0aaf656d50df0d2f3ad836623caa999672bb5d42505cac64b0780aa418cf`  
		Last Modified: Tue, 03 Jun 2025 13:36:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f53473c2ddc77ba6ffc56168ae5339143108727169189274b7050672dc65e708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acebf4d2ca0eef89d9d45e182c57c09e1646424b340ade018e9ba85d4c549995`

```dockerfile
```

-	Layers:
	-	`sha256:4e66c4629743f056f8ef8b051000f228f0af37fa6c973d22fdf952782b7fa810`  
		Last Modified: Tue, 03 Jun 2025 14:16:16 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5f9c124183771f88e669251a51b30a5bc390a790692966075d0e442945233`  
		Last Modified: Tue, 03 Jun 2025 14:16:17 GMT  
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
		Last Modified: Thu, 29 May 2025 18:12:16 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f33706d1babf997ab64410760aa60f0ac6823ac3413aa0c48d35af2b39aa293`  
		Last Modified: Thu, 29 May 2025 18:12:15 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
