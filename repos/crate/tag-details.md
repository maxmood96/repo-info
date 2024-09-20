<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.7`](#crate57)
-	[`crate:5.7.5`](#crate575)
-	[`crate:5.8`](#crate58)
-	[`crate:5.8.3`](#crate583)
-	[`crate:latest`](#cratelatest)

## `crate:5.7`

```console
$ docker pull crate@sha256:dff3840a7c94fae008348badcf889f8355c34ee5917c9fcd6a0af748a7aee01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:eeb5b14040dbd3627126d10016e6e1352e0d1f479e10e7c7cb6efe54df29126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209503759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f0d82d7d66455e22bc9f5553c1976949950da35a50a8fab47d8dc6f01a3836`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 10:03:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.5.tar.gz.asc crate-5.7.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.5.tar.gz.asc     && tar -xf crate-5.7.5.tar.gz -C /crate --strip-components=1     && rm crate-5.7.5.tar.gz # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 10:03:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Sep 2024 10:03:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
VOLUME [/data]
# Mon, 09 Sep 2024 10:03:56 GMT
WORKDIR /data
# Mon, 09 Sep 2024 10:03:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-09-09T10:03:56.480250 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.5
# Mon, 09 Sep 2024 10:03:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 10:03:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d6624d8356ca1d384c8b6c0b91780170e87ebf198581e4e62871db06d7784a`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 11.3 MB (11282433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f096389c623ab3aa5287eb8da0ff2f39e720d131bba4062a59831e31f31b6f`  
		Last Modified: Thu, 12 Sep 2024 18:56:21 GMT  
		Size: 127.7 MB (127686552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916bd1a09b9e7d5de60bc9a5eebed28d4c44e2562ea34459f4a9fe27b5ecd3cc`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0ff06c229f3705bc019df226ae12488e760694f6e82ab0ecaa46f9161fab7f`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2e999a536d17922edabea00ce6fef4ebb62aca0ef0105232b6686ced6d22d`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f0443ccd98f31db1225a48762f2a41bd821d086789058ee0c69f2c7c2bd93`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d554751b525d23a25e4c5dde6d3ba6ad23383f451a0b382eb478921226a9cd1a`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:577e4f9ade118b59c51caf3c1ec172e456580342c7b0484217a3abe1e0641ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5014728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6f8bf6418f33995348711c23d64bf86c35acf72b0932b2a7723712aa22dccc`

```dockerfile
```

-	Layers:
	-	`sha256:81f4d27443ebc90e4735008c1fa7094404b9efdb2d864d6aaca17023324e8c68`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 5.0 MB (4991936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f0cce8f237405422a4c9868b2dd2e717c1b30c70acac09094b714eb40ac49c`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:042a73b80b064c0e9ddb38874970ba7f9bc2db9fa380209a237bce1a9469dab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207915366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b512fb947ee206461b8dfbbe0c0267ecbc13f9364321db1dd10c32090f2700bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 10:03:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.5.tar.gz.asc crate-5.7.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.5.tar.gz.asc     && tar -xf crate-5.7.5.tar.gz -C /crate --strip-components=1     && rm crate-5.7.5.tar.gz # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 10:03:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Sep 2024 10:03:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
VOLUME [/data]
# Mon, 09 Sep 2024 10:03:56 GMT
WORKDIR /data
# Mon, 09 Sep 2024 10:03:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-09-09T10:03:56.480250 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.5
# Mon, 09 Sep 2024 10:03:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 10:03:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb8ec46862234bf18c1909229744924266f224e00e80497b05fb7d9d9611b4a`  
		Last Modified: Thu, 12 Sep 2024 18:56:15 GMT  
		Size: 11.3 MB (11262932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04155e3dd7db18aca33da9e00e6ee482e96f6fec35c64e1afed2cf507190fe35`  
		Last Modified: Thu, 12 Sep 2024 18:56:17 GMT  
		Size: 127.2 MB (127203453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c93b061cd7c361354fb513e12131349c3ca590989918a4218e9b5171e492bd1`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dfd4972679fe3aa3734c7fc62ddd9dc8716abe2fdd1f04bf8d93c8c55e614d`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed99fb4562c8cd879e8b461404f3b950f51bcd694adea4fc5894aa010a739e07`  
		Last Modified: Thu, 12 Sep 2024 18:56:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c785412a593368cbe1374f01839333829562cb96fc76f2693b6ca5183c8dfd2e`  
		Last Modified: Thu, 12 Sep 2024 18:56:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8401957bff9c906bc2da219195e6a5ccb32db0de6d75b51882579bec738ef89a`  
		Last Modified: Thu, 12 Sep 2024 18:56:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:bd5114cc43fbe730dc121855e42b0ef4ae5cb163e4666ffeb8f772f55dc13328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cb0476625735d9eb85b6298ee2125faea96f8a793b5c4338222a4d50d234f9`

```dockerfile
```

-	Layers:
	-	`sha256:82c579e8fd5ade5a6b41e525867505d1f15fdbb079b29a79f9fa7aba67cd3637`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 5.0 MB (4989853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bbf3552851589e530ac444134af37650a2514374f0b4ad6f94e9bb62f210a1`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 23.2 KB (23152 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.5`

```console
$ docker pull crate@sha256:dff3840a7c94fae008348badcf889f8355c34ee5917c9fcd6a0af748a7aee01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.5` - linux; amd64

```console
$ docker pull crate@sha256:eeb5b14040dbd3627126d10016e6e1352e0d1f479e10e7c7cb6efe54df29126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209503759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f0d82d7d66455e22bc9f5553c1976949950da35a50a8fab47d8dc6f01a3836`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 10:03:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.5.tar.gz.asc crate-5.7.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.5.tar.gz.asc     && tar -xf crate-5.7.5.tar.gz -C /crate --strip-components=1     && rm crate-5.7.5.tar.gz # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 10:03:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Sep 2024 10:03:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
VOLUME [/data]
# Mon, 09 Sep 2024 10:03:56 GMT
WORKDIR /data
# Mon, 09 Sep 2024 10:03:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-09-09T10:03:56.480250 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.5
# Mon, 09 Sep 2024 10:03:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 10:03:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d6624d8356ca1d384c8b6c0b91780170e87ebf198581e4e62871db06d7784a`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 11.3 MB (11282433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f096389c623ab3aa5287eb8da0ff2f39e720d131bba4062a59831e31f31b6f`  
		Last Modified: Thu, 12 Sep 2024 18:56:21 GMT  
		Size: 127.7 MB (127686552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916bd1a09b9e7d5de60bc9a5eebed28d4c44e2562ea34459f4a9fe27b5ecd3cc`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0ff06c229f3705bc019df226ae12488e760694f6e82ab0ecaa46f9161fab7f`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2e999a536d17922edabea00ce6fef4ebb62aca0ef0105232b6686ced6d22d`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f0443ccd98f31db1225a48762f2a41bd821d086789058ee0c69f2c7c2bd93`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d554751b525d23a25e4c5dde6d3ba6ad23383f451a0b382eb478921226a9cd1a`  
		Last Modified: Thu, 12 Sep 2024 18:56:20 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.5` - unknown; unknown

```console
$ docker pull crate@sha256:577e4f9ade118b59c51caf3c1ec172e456580342c7b0484217a3abe1e0641ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5014728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6f8bf6418f33995348711c23d64bf86c35acf72b0932b2a7723712aa22dccc`

```dockerfile
```

-	Layers:
	-	`sha256:81f4d27443ebc90e4735008c1fa7094404b9efdb2d864d6aaca17023324e8c68`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 5.0 MB (4991936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f0cce8f237405422a4c9868b2dd2e717c1b30c70acac09094b714eb40ac49c`  
		Last Modified: Thu, 12 Sep 2024 18:56:19 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:042a73b80b064c0e9ddb38874970ba7f9bc2db9fa380209a237bce1a9469dab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207915366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b512fb947ee206461b8dfbbe0c0267ecbc13f9364321db1dd10c32090f2700bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 10:03:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.5.tar.gz.asc crate-5.7.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.5.tar.gz.asc     && tar -xf crate-5.7.5.tar.gz -C /crate --strip-components=1     && rm crate-5.7.5.tar.gz # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 10:03:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 09 Sep 2024 10:03:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
VOLUME [/data]
# Mon, 09 Sep 2024 10:03:56 GMT
WORKDIR /data
# Mon, 09 Sep 2024 10:03:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-09-09T10:03:56.480250 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.5
# Mon, 09 Sep 2024 10:03:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 09 Sep 2024 10:03:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 10:03:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb8ec46862234bf18c1909229744924266f224e00e80497b05fb7d9d9611b4a`  
		Last Modified: Thu, 12 Sep 2024 18:56:15 GMT  
		Size: 11.3 MB (11262932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04155e3dd7db18aca33da9e00e6ee482e96f6fec35c64e1afed2cf507190fe35`  
		Last Modified: Thu, 12 Sep 2024 18:56:17 GMT  
		Size: 127.2 MB (127203453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c93b061cd7c361354fb513e12131349c3ca590989918a4218e9b5171e492bd1`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dfd4972679fe3aa3734c7fc62ddd9dc8716abe2fdd1f04bf8d93c8c55e614d`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed99fb4562c8cd879e8b461404f3b950f51bcd694adea4fc5894aa010a739e07`  
		Last Modified: Thu, 12 Sep 2024 18:56:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c785412a593368cbe1374f01839333829562cb96fc76f2693b6ca5183c8dfd2e`  
		Last Modified: Thu, 12 Sep 2024 18:56:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8401957bff9c906bc2da219195e6a5ccb32db0de6d75b51882579bec738ef89a`  
		Last Modified: Thu, 12 Sep 2024 18:56:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.5` - unknown; unknown

```console
$ docker pull crate@sha256:bd5114cc43fbe730dc121855e42b0ef4ae5cb163e4666ffeb8f772f55dc13328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cb0476625735d9eb85b6298ee2125faea96f8a793b5c4338222a4d50d234f9`

```dockerfile
```

-	Layers:
	-	`sha256:82c579e8fd5ade5a6b41e525867505d1f15fdbb079b29a79f9fa7aba67cd3637`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 5.0 MB (4989853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bbf3552851589e530ac444134af37650a2514374f0b4ad6f94e9bb62f210a1`  
		Last Modified: Thu, 12 Sep 2024 18:56:14 GMT  
		Size: 23.2 KB (23152 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8`

```console
$ docker pull crate@sha256:ab3c0f2aa656433ae354f6f0569a9597f0e6efea929091c023f6d49a21881c99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8` - linux; amd64

```console
$ docker pull crate@sha256:032cce85cecf20087a222fa3000c19a899915f5a5b7bea359646ef41c10f4bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211486955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c3af82ebb7bd2f54a2b481513e796755f21b3feb5cdd76687ea5cccba9c3fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Wed, 28 Aug 2024 08:18:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.2.tar.gz.asc crate-5.8.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.2.tar.gz.asc     && tar -xf crate-5.8.2.tar.gz -C /crate --strip-components=1     && rm crate-5.8.2.tar.gz # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 08:18:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 28 Aug 2024 08:18:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
VOLUME [/data]
# Wed, 28 Aug 2024 08:18:09 GMT
WORKDIR /data
# Wed, 28 Aug 2024 08:18:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-08-28T08:18:09.229386 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.2
# Wed, 28 Aug 2024 08:18:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Aug 2024 08:18:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1184b53e32c282ff6cdbaaeafdb12e2c86f00583ba657b4cc30cd2ed1844a376`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 11.0 MB (11004787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8c4d99d0b4ac79ec1c072a97573c8c136aec200774122b4079ff8324f4a20`  
		Last Modified: Tue, 03 Sep 2024 18:56:24 GMT  
		Size: 129.9 MB (129947407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f986638b11a6dad670940fea7ec0acaa931484a35e4db24346f8c3560e1d733`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604db00cf059cd7006c6a52a0104fa5aabb467a403a8d246efbd3ad3f1080a15`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf1474b54c3a3c1de8eeee623d4ec201febb0621ba123200759229335ecf4e`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7627560b067e8dd4cb7f7d33d3a225d1e740c7a9a990fcd33dda302b675bd0a`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a76eff9a04aa7356ff1d90699e3548bb3198edff2696a6bf451afb0f325983`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:2a04ba0226fbf57e52e302183aecc9c49ad8a80aaf9731a2e1557387ef9b7fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5008056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006c44c873be46223a9c2bf2153ffd1106c25a38db0739e7bb446863f6e475d`

```dockerfile
```

-	Layers:
	-	`sha256:20cf0deaef4e64a560f10a0b09a65104f859293a772dcc1a49ef352990170fc0`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 5.0 MB (4984968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e3e8a3b5e3cce26ff8be054e6106f2d385032eb94c897f308b66c682a5e1ab`  
		Last Modified: Tue, 03 Sep 2024 18:56:20 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ada3a785df3184535936f2d291760d7fe11adb7fe53c2ef24bc58a83b9b4b1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209826702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350fb2808b3f32adeb1686aa35c76526af9ccc352f0c16828250ca4e57da0b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Wed, 28 Aug 2024 08:18:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.2.tar.gz.asc crate-5.8.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.2.tar.gz.asc     && tar -xf crate-5.8.2.tar.gz -C /crate --strip-components=1     && rm crate-5.8.2.tar.gz # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 08:18:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 28 Aug 2024 08:18:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
VOLUME [/data]
# Wed, 28 Aug 2024 08:18:09 GMT
WORKDIR /data
# Wed, 28 Aug 2024 08:18:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-08-28T08:18:09.229386 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.2
# Wed, 28 Aug 2024 08:18:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Aug 2024 08:18:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa294afffab8bdcb14f5214fc333a4ae44343feec8f7f66bed9f59d023e43bc`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 11.0 MB (10983569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6bf9b04354dd7abc15df8def94e43ac7ed9823eca503002ca8c16be40113a3`  
		Last Modified: Tue, 03 Sep 2024 18:56:35 GMT  
		Size: 129.4 MB (129394149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eb27f1e4469b424e1e5d26aa2feebca3e2d317383ac88d845e836fe633c13e`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9d77f15601af40e8fec8cd77ec5b887a279bc6587fb011af5f500a92ee16f2`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974070880e7089ac652a55dc3040ff5d23fd76578c53f720ad035b2ec199118e`  
		Last Modified: Tue, 03 Sep 2024 18:56:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1df34388bed7df29f7d05d7cbc6727ce6f3c9f20cdb3601baf0e73bb615f26`  
		Last Modified: Tue, 03 Sep 2024 18:56:33 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e4756e5fe28339a30f37746322be25609b3e2e5848d28192a11d5388e34b6`  
		Last Modified: Tue, 03 Sep 2024 18:56:34 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:9293454546faf29ed12843f3c06c207f21881c721d57376104c9b0afff78331a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5006358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aa266183fd792e8c4d2e2ee60d86d07f3a5e87cabf7863ba05c2c17fce4e00`

```dockerfile
```

-	Layers:
	-	`sha256:99ffb3fc5fc191f16a431ebf7694ca86695a5fab46cbd9420b060992daa95bf1`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 5.0 MB (4982897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b47ae05cbc4ea797101d3d21325f3bd2f3440abdfdab63dc3ac156b57d97329`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 23.5 KB (23461 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8.3`

```console
$ docker pull crate@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `crate:latest`

```console
$ docker pull crate@sha256:ab3c0f2aa656433ae354f6f0569a9597f0e6efea929091c023f6d49a21881c99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:032cce85cecf20087a222fa3000c19a899915f5a5b7bea359646ef41c10f4bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211486955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c3af82ebb7bd2f54a2b481513e796755f21b3feb5cdd76687ea5cccba9c3fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Wed, 28 Aug 2024 08:18:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.2.tar.gz.asc crate-5.8.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.2.tar.gz.asc     && tar -xf crate-5.8.2.tar.gz -C /crate --strip-components=1     && rm crate-5.8.2.tar.gz # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 08:18:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 28 Aug 2024 08:18:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
VOLUME [/data]
# Wed, 28 Aug 2024 08:18:09 GMT
WORKDIR /data
# Wed, 28 Aug 2024 08:18:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-08-28T08:18:09.229386 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.2
# Wed, 28 Aug 2024 08:18:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Aug 2024 08:18:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1184b53e32c282ff6cdbaaeafdb12e2c86f00583ba657b4cc30cd2ed1844a376`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 11.0 MB (11004787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8c4d99d0b4ac79ec1c072a97573c8c136aec200774122b4079ff8324f4a20`  
		Last Modified: Tue, 03 Sep 2024 18:56:24 GMT  
		Size: 129.9 MB (129947407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f986638b11a6dad670940fea7ec0acaa931484a35e4db24346f8c3560e1d733`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604db00cf059cd7006c6a52a0104fa5aabb467a403a8d246efbd3ad3f1080a15`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf1474b54c3a3c1de8eeee623d4ec201febb0621ba123200759229335ecf4e`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7627560b067e8dd4cb7f7d33d3a225d1e740c7a9a990fcd33dda302b675bd0a`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a76eff9a04aa7356ff1d90699e3548bb3198edff2696a6bf451afb0f325983`  
		Last Modified: Tue, 03 Sep 2024 18:56:22 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:2a04ba0226fbf57e52e302183aecc9c49ad8a80aaf9731a2e1557387ef9b7fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5008056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006c44c873be46223a9c2bf2153ffd1106c25a38db0739e7bb446863f6e475d`

```dockerfile
```

-	Layers:
	-	`sha256:20cf0deaef4e64a560f10a0b09a65104f859293a772dcc1a49ef352990170fc0`  
		Last Modified: Tue, 03 Sep 2024 18:56:21 GMT  
		Size: 5.0 MB (4984968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e3e8a3b5e3cce26ff8be054e6106f2d385032eb94c897f308b66c682a5e1ab`  
		Last Modified: Tue, 03 Sep 2024 18:56:20 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ada3a785df3184535936f2d291760d7fe11adb7fe53c2ef24bc58a83b9b4b1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209826702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350fb2808b3f32adeb1686aa35c76526af9ccc352f0c16828250ca4e57da0b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Wed, 28 Aug 2024 08:18:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.2.tar.gz.asc crate-5.8.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.2.tar.gz.asc     && tar -xf crate-5.8.2.tar.gz -C /crate --strip-components=1     && rm crate-5.8.2.tar.gz # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 08:18:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 28 Aug 2024 08:18:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
VOLUME [/data]
# Wed, 28 Aug 2024 08:18:09 GMT
WORKDIR /data
# Wed, 28 Aug 2024 08:18:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-08-28T08:18:09.229386 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.2
# Wed, 28 Aug 2024 08:18:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 28 Aug 2024 08:18:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Aug 2024 08:18:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa294afffab8bdcb14f5214fc333a4ae44343feec8f7f66bed9f59d023e43bc`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 11.0 MB (10983569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6bf9b04354dd7abc15df8def94e43ac7ed9823eca503002ca8c16be40113a3`  
		Last Modified: Tue, 03 Sep 2024 18:56:35 GMT  
		Size: 129.4 MB (129394149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eb27f1e4469b424e1e5d26aa2feebca3e2d317383ac88d845e836fe633c13e`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9d77f15601af40e8fec8cd77ec5b887a279bc6587fb011af5f500a92ee16f2`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974070880e7089ac652a55dc3040ff5d23fd76578c53f720ad035b2ec199118e`  
		Last Modified: Tue, 03 Sep 2024 18:56:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1df34388bed7df29f7d05d7cbc6727ce6f3c9f20cdb3601baf0e73bb615f26`  
		Last Modified: Tue, 03 Sep 2024 18:56:33 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e4756e5fe28339a30f37746322be25609b3e2e5848d28192a11d5388e34b6`  
		Last Modified: Tue, 03 Sep 2024 18:56:34 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:9293454546faf29ed12843f3c06c207f21881c721d57376104c9b0afff78331a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5006358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aa266183fd792e8c4d2e2ee60d86d07f3a5e87cabf7863ba05c2c17fce4e00`

```dockerfile
```

-	Layers:
	-	`sha256:99ffb3fc5fc191f16a431ebf7694ca86695a5fab46cbd9420b060992daa95bf1`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 5.0 MB (4982897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b47ae05cbc4ea797101d3d21325f3bd2f3440abdfdab63dc3ac156b57d97329`  
		Last Modified: Tue, 03 Sep 2024 18:56:32 GMT  
		Size: 23.5 KB (23461 bytes)  
		MIME: application/vnd.in-toto+json
