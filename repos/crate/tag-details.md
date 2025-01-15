<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.8`](#crate58)
-	[`crate:5.8.5`](#crate585)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.6`](#crate596)
-	[`crate:latest`](#cratelatest)

## `crate:5.8`

```console
$ docker pull crate@sha256:c42ba0bb2e9a298dc9fa8fdd96189d384e176307df605d9b0f99b77dac761211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8` - linux; amd64

```console
$ docker pull crate@sha256:777621802efb2333c3567292a5c042abda846a65eab17ce21dd287b0722d8a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211008963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746c6e012ba7f3e55d6b5eb71833d6c1c37634e2b5c3b3750d08a518ee5a8ca8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 28 Oct 2024 13:54:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ee68434703fc490d721476608b9e34aee6b4a7ca2b9892599ddfe761db0a99`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a3fc9dcc1bcfdad62ee6d3158e5fe6556798c9796758ce70ba313e5e287d7`  
		Last Modified: Mon, 18 Nov 2024 22:05:20 GMT  
		Size: 130.0 MB (129966263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bf409aa2276efd18fa37ad553999932167ba867b040aa5933a164f96f03c41`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bded23721afaeac40ae5c513bfaa6e6af2a9f9cc4003ae40108ffe081e574b85`  
		Last Modified: Tue, 17 Dec 2024 06:15:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13498f55f845c2554c8397cc8b91b2fa83da950a3451d0925877e6dea003565`  
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eea8cc5913bd485e232c0ee4619734448ab0c237d23c9a27bdfe1fc1aa30b2`  
		Last Modified: Tue, 17 Dec 2024 06:15:35 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931921550a8e6ebb8ec70856456770ea1d6a2623b85b9fccb967312a9c9a188`  
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:1ea0359b2e02ee9b17c2a4b394049451400f6f1d364f10f7e3fb1a8ccab45fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0076cc7c95ad3ff9b3e0a0bdae59ee78fbd0d2c1833797c061ae5c47e00fd5ae`

```dockerfile
```

-	Layers:
	-	`sha256:0b7caadd48f351a77160d5674b11e97ded7c220684555892a9ed6e8375622d8d`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 6.3 MB (6314647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9b10506babba20f271076efd5627353fd64459e43e373a3bbdf4b507cff8fa`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 22.8 KB (22802 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8ed22dc9e2f6229f93dbefa7830e7f5780190b7002810da29787c3efab5bff5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209364536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759acc6d869676e9a239874cc8db47e282ee6a62ae0f828a5f9b875e23b57f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 28 Oct 2024 13:54:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560cf44776d8c069d97c29bd19342141d384ef1f7f854fb33c9089e367943340`  
		Last Modified: Mon, 18 Nov 2024 22:04:59 GMT  
		Size: 18.3 KB (18273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e658f481fcdb2b77c1c993244908333fc5665e401b02ab906fe00d2528286100`  
		Last Modified: Mon, 06 Jan 2025 17:29:39 GMT  
		Size: 129.4 MB (129411988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a982ddb3bd60d4efe1ef896f2502da0dc976dd1a71ec3082539db78e972ea7`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea0d2b7847d97f61b6ad3521cce15ae5fb2c0f7b6f522f38535e6c0befddab4`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c808276ea36308c3b8164bac1ca12b80df46ba0116b3396500a603d376526bdf`  
		Last Modified: Wed, 08 Jan 2025 01:29:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527018106ba150a65895d2e9d1988bca7a5299f2d59774997b3e3bcab43cbdb9`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4c34eb128571eec7c207460247e7bde8f2b6409c85571e6eccd1329be10e89`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:5b017a7ebc75e97bdad032a72d7678b3f679a6c4d5102252876ede32e68768bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb1a57a969c1374539f2e4c09d71fa60f3b23e6a9c890456746b9363b4a33c9`

```dockerfile
```

-	Layers:
	-	`sha256:1bbfdada00908b120262029bb0dce6bc2683e0a244ad24ea7c729edc7ca950c9`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 6.3 MB (6311949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db05ea3efbb5da06cf449a37319efc1ca2548005c7389aa08bd3542d8a226d6`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 22.9 KB (22927 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8.5`

```console
$ docker pull crate@sha256:c42ba0bb2e9a298dc9fa8fdd96189d384e176307df605d9b0f99b77dac761211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8.5` - linux; amd64

```console
$ docker pull crate@sha256:777621802efb2333c3567292a5c042abda846a65eab17ce21dd287b0722d8a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211008963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746c6e012ba7f3e55d6b5eb71833d6c1c37634e2b5c3b3750d08a518ee5a8ca8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 28 Oct 2024 13:54:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ee68434703fc490d721476608b9e34aee6b4a7ca2b9892599ddfe761db0a99`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a3fc9dcc1bcfdad62ee6d3158e5fe6556798c9796758ce70ba313e5e287d7`  
		Last Modified: Mon, 18 Nov 2024 22:05:20 GMT  
		Size: 130.0 MB (129966263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bf409aa2276efd18fa37ad553999932167ba867b040aa5933a164f96f03c41`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bded23721afaeac40ae5c513bfaa6e6af2a9f9cc4003ae40108ffe081e574b85`  
		Last Modified: Tue, 17 Dec 2024 06:15:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13498f55f845c2554c8397cc8b91b2fa83da950a3451d0925877e6dea003565`  
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eea8cc5913bd485e232c0ee4619734448ab0c237d23c9a27bdfe1fc1aa30b2`  
		Last Modified: Tue, 17 Dec 2024 06:15:35 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931921550a8e6ebb8ec70856456770ea1d6a2623b85b9fccb967312a9c9a188`  
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.5` - unknown; unknown

```console
$ docker pull crate@sha256:1ea0359b2e02ee9b17c2a4b394049451400f6f1d364f10f7e3fb1a8ccab45fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0076cc7c95ad3ff9b3e0a0bdae59ee78fbd0d2c1833797c061ae5c47e00fd5ae`

```dockerfile
```

-	Layers:
	-	`sha256:0b7caadd48f351a77160d5674b11e97ded7c220684555892a9ed6e8375622d8d`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 6.3 MB (6314647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9b10506babba20f271076efd5627353fd64459e43e373a3bbdf4b507cff8fa`  
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
		Size: 22.8 KB (22802 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8ed22dc9e2f6229f93dbefa7830e7f5780190b7002810da29787c3efab5bff5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209364536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759acc6d869676e9a239874cc8db47e282ee6a62ae0f828a5f9b875e23b57f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 28 Oct 2024 13:54:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560cf44776d8c069d97c29bd19342141d384ef1f7f854fb33c9089e367943340`  
		Last Modified: Mon, 18 Nov 2024 22:04:59 GMT  
		Size: 18.3 KB (18273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e658f481fcdb2b77c1c993244908333fc5665e401b02ab906fe00d2528286100`  
		Last Modified: Mon, 06 Jan 2025 17:29:39 GMT  
		Size: 129.4 MB (129411988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a982ddb3bd60d4efe1ef896f2502da0dc976dd1a71ec3082539db78e972ea7`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea0d2b7847d97f61b6ad3521cce15ae5fb2c0f7b6f522f38535e6c0befddab4`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c808276ea36308c3b8164bac1ca12b80df46ba0116b3396500a603d376526bdf`  
		Last Modified: Wed, 08 Jan 2025 01:29:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527018106ba150a65895d2e9d1988bca7a5299f2d59774997b3e3bcab43cbdb9`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4c34eb128571eec7c207460247e7bde8f2b6409c85571e6eccd1329be10e89`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.5` - unknown; unknown

```console
$ docker pull crate@sha256:5b017a7ebc75e97bdad032a72d7678b3f679a6c4d5102252876ede32e68768bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb1a57a969c1374539f2e4c09d71fa60f3b23e6a9c890456746b9363b4a33c9`

```dockerfile
```

-	Layers:
	-	`sha256:1bbfdada00908b120262029bb0dce6bc2683e0a244ad24ea7c729edc7ca950c9`  
		Last Modified: Mon, 18 Nov 2024 22:06:12 GMT  
		Size: 6.3 MB (6311949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db05ea3efbb5da06cf449a37319efc1ca2548005c7389aa08bd3542d8a226d6`  
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
		Size: 22.9 KB (22927 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:4a64b31b6840341aa39399b88741ae925c341582f11ecd73eacc33cddc87ef2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:226c51f49ecc6a69b77a453192966374b1ef555540753377963bfbe33e6ee628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242388761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d93cf3c690755ef1c2dbc4d500930dde85368f706f2a3b84ac2fbc22495bf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 09:51:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.6.tar.gz.asc crate-5.9.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.6.tar.gz.asc     && tar -xf crate-5.9.6.tar.gz -C /crate --strip-components=1     && rm crate-5.9.6.tar.gz # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2025 09:51:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 09 Jan 2025 09:51:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
VOLUME [/data]
# Thu, 09 Jan 2025 09:51:54 GMT
WORKDIR /data
# Thu, 09 Jan 2025 09:51:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-09T09:51:54.945195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.6
# Thu, 09 Jan 2025 09:51:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Jan 2025 09:51:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3dd3c1b43a094a57c82f7c759e85dfd0f0d11c22757bf9d66f39b8e6473324`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 14.1 MB (14148844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482f67ddb8a7b3d7a84e40719de1c9e941390bd028ff957fdddbc23451f3bb20`  
		Last Modified: Tue, 14 Jan 2025 19:28:22 GMT  
		Size: 147.2 MB (147215424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3fc86289e6e8ebb83dfd994802ca96d5e3d914683cb5911159985438ae6da`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cdbfc93a57c32d59db0a675ba6d988a3f50b7018b56323528567fdd0dd95e`  
		Last Modified: Tue, 14 Jan 2025 21:38:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04ce584b69bb42ca4276462807c5e3ed21605e7393a8c572474c440bcc792a`  
		Last Modified: Tue, 14 Jan 2025 21:38:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e295e350f57f4e6b0bb10f153233b44e5ca75c3e4469f88f5fbeb2fc7e9d2`  
		Last Modified: Tue, 14 Jan 2025 21:38:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74c1dfcca3b21a5e74e91a095b205f966a45c6ca09954e11e301451fc1a8bd0`  
		Last Modified: Tue, 14 Jan 2025 19:28:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:79eb120af451887579bf6515acc29cf2ec35881d82f5afc41db98410df827d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9600d8173123bbbbca9b93d2801f835653fb2e7c82af77edb202ab21df0439`

```dockerfile
```

-	Layers:
	-	`sha256:7534b7fd988c1da09755b678a4fcbbc4f69641cff79dceccac1576090e37ad39`  
		Last Modified: Tue, 14 Jan 2025 21:38:22 GMT  
		Size: 6.3 MB (6316984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947cef4af6a5e3e0836cce96333e75a58c26087374980cba36905aa26fb5758a`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:631edf26dbc222e38eadea02a51fd7f45637812c5da2b03f3989a50c5a0b8553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2e63d1c9955a1f63d0a5e77654904553ee260bfd92dec147b9e0931b9f3cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Tue, 10 Dec 2024 16:21:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.5.tar.gz.asc crate-5.9.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.5.tar.gz.asc     && tar -xf crate-5.9.5.tar.gz -C /crate --strip-components=1     && rm crate-5.9.5.tar.gz # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Dec 2024 16:21:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 10 Dec 2024 16:21:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
VOLUME [/data]
# Tue, 10 Dec 2024 16:21:56 GMT
WORKDIR /data
# Tue, 10 Dec 2024 16:21:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-12-10T16:21:56.023234 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.5
# Tue, 10 Dec 2024 16:21:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Dec 2024 16:21:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eeccda12ed247fc86af9756eed85b9493924d0e5654243889a076103dba020`  
		Last Modified: Sat, 14 Dec 2024 18:11:31 GMT  
		Size: 13.5 MB (13537879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1e6977d7c6274d2809b4c27d1e41a2b9519f487a53b741263dd04bca7dac8b`  
		Last Modified: Sat, 14 Dec 2024 18:11:38 GMT  
		Size: 148.4 MB (148375948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298f0d0860c7d87c45abc13dd98458d6f6aaaffc41f61973f23de9e7da30493`  
		Last Modified: Sat, 14 Dec 2024 18:11:33 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5390f2f5edde014145aa39036356876d9045e93796c8af41f4de3f71dfd9f`  
		Last Modified: Fri, 13 Dec 2024 20:28:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fdf3527e264dc2003068e61b266a4b9ee395d3d153a57a7058014ac80ddbd6`  
		Last Modified: Fri, 13 Dec 2024 20:28:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf88d03d210975a6da59c0047af95728c1f90f1608754b2a2d81fee08f48f104`  
		Last Modified: Sat, 14 Dec 2024 18:10:28 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ae2da509d2a624303fe3b492d1fc6f1f49114065d73181123b41c3f3a6c9ff`  
		Last Modified: Fri, 13 Dec 2024 20:28:15 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:51c6206ce4d37e8fa7f927139e42061f862ec183a8590194a033e7f08dc5697a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9291f3cb2fa49d1ee7ba0bcea78940880bfafcb9cd823e7f0656f5df7eb99cb3`

```dockerfile
```

-	Layers:
	-	`sha256:9a37744ec313b2f7e8f033eaa064ba70ae9340eac85a59af74ac84ed1bb4598a`  
		Last Modified: Mon, 16 Dec 2024 19:09:09 GMT  
		Size: 6.3 MB (6327739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a505c2a4fac5bac8830a37aedf1b0540c2fa6604c6499f774f7bdfabe7910dfb`  
		Last Modified: Sun, 15 Dec 2024 05:36:14 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.6`

```console
$ docker pull crate@sha256:461fa7b704d2a6104f76d015171736266da29200494a3ac7a68933f21da04d46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `crate:5.9.6` - linux; amd64

```console
$ docker pull crate@sha256:226c51f49ecc6a69b77a453192966374b1ef555540753377963bfbe33e6ee628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242388761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d93cf3c690755ef1c2dbc4d500930dde85368f706f2a3b84ac2fbc22495bf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 09:51:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.6.tar.gz.asc crate-5.9.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.6.tar.gz.asc     && tar -xf crate-5.9.6.tar.gz -C /crate --strip-components=1     && rm crate-5.9.6.tar.gz # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2025 09:51:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 09 Jan 2025 09:51:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
VOLUME [/data]
# Thu, 09 Jan 2025 09:51:54 GMT
WORKDIR /data
# Thu, 09 Jan 2025 09:51:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-09T09:51:54.945195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.6
# Thu, 09 Jan 2025 09:51:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Jan 2025 09:51:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3dd3c1b43a094a57c82f7c759e85dfd0f0d11c22757bf9d66f39b8e6473324`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 14.1 MB (14148844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482f67ddb8a7b3d7a84e40719de1c9e941390bd028ff957fdddbc23451f3bb20`  
		Last Modified: Tue, 14 Jan 2025 19:28:22 GMT  
		Size: 147.2 MB (147215424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3fc86289e6e8ebb83dfd994802ca96d5e3d914683cb5911159985438ae6da`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cdbfc93a57c32d59db0a675ba6d988a3f50b7018b56323528567fdd0dd95e`  
		Last Modified: Tue, 14 Jan 2025 21:38:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04ce584b69bb42ca4276462807c5e3ed21605e7393a8c572474c440bcc792a`  
		Last Modified: Tue, 14 Jan 2025 21:38:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e295e350f57f4e6b0bb10f153233b44e5ca75c3e4469f88f5fbeb2fc7e9d2`  
		Last Modified: Tue, 14 Jan 2025 21:38:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74c1dfcca3b21a5e74e91a095b205f966a45c6ca09954e11e301451fc1a8bd0`  
		Last Modified: Tue, 14 Jan 2025 19:28:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.6` - unknown; unknown

```console
$ docker pull crate@sha256:79eb120af451887579bf6515acc29cf2ec35881d82f5afc41db98410df827d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9600d8173123bbbbca9b93d2801f835653fb2e7c82af77edb202ab21df0439`

```dockerfile
```

-	Layers:
	-	`sha256:7534b7fd988c1da09755b678a4fcbbc4f69641cff79dceccac1576090e37ad39`  
		Last Modified: Tue, 14 Jan 2025 21:38:22 GMT  
		Size: 6.3 MB (6316984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947cef4af6a5e3e0836cce96333e75a58c26087374980cba36905aa26fb5758a`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:4a64b31b6840341aa39399b88741ae925c341582f11ecd73eacc33cddc87ef2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:226c51f49ecc6a69b77a453192966374b1ef555540753377963bfbe33e6ee628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242388761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d93cf3c690755ef1c2dbc4d500930dde85368f706f2a3b84ac2fbc22495bf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 09:51:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.6.tar.gz.asc crate-5.9.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.6.tar.gz.asc     && tar -xf crate-5.9.6.tar.gz -C /crate --strip-components=1     && rm crate-5.9.6.tar.gz # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2025 09:51:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 09 Jan 2025 09:51:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
VOLUME [/data]
# Thu, 09 Jan 2025 09:51:54 GMT
WORKDIR /data
# Thu, 09 Jan 2025 09:51:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-09T09:51:54.945195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.6
# Thu, 09 Jan 2025 09:51:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Jan 2025 09:51:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3dd3c1b43a094a57c82f7c759e85dfd0f0d11c22757bf9d66f39b8e6473324`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 14.1 MB (14148844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482f67ddb8a7b3d7a84e40719de1c9e941390bd028ff957fdddbc23451f3bb20`  
		Last Modified: Tue, 14 Jan 2025 19:28:22 GMT  
		Size: 147.2 MB (147215424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3fc86289e6e8ebb83dfd994802ca96d5e3d914683cb5911159985438ae6da`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cdbfc93a57c32d59db0a675ba6d988a3f50b7018b56323528567fdd0dd95e`  
		Last Modified: Tue, 14 Jan 2025 21:38:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04ce584b69bb42ca4276462807c5e3ed21605e7393a8c572474c440bcc792a`  
		Last Modified: Tue, 14 Jan 2025 21:38:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e295e350f57f4e6b0bb10f153233b44e5ca75c3e4469f88f5fbeb2fc7e9d2`  
		Last Modified: Tue, 14 Jan 2025 21:38:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74c1dfcca3b21a5e74e91a095b205f966a45c6ca09954e11e301451fc1a8bd0`  
		Last Modified: Tue, 14 Jan 2025 19:28:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:79eb120af451887579bf6515acc29cf2ec35881d82f5afc41db98410df827d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9600d8173123bbbbca9b93d2801f835653fb2e7c82af77edb202ab21df0439`

```dockerfile
```

-	Layers:
	-	`sha256:7534b7fd988c1da09755b678a4fcbbc4f69641cff79dceccac1576090e37ad39`  
		Last Modified: Tue, 14 Jan 2025 21:38:22 GMT  
		Size: 6.3 MB (6316984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947cef4af6a5e3e0836cce96333e75a58c26087374980cba36905aa26fb5758a`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:631edf26dbc222e38eadea02a51fd7f45637812c5da2b03f3989a50c5a0b8553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2e63d1c9955a1f63d0a5e77654904553ee260bfd92dec147b9e0931b9f3cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Tue, 10 Dec 2024 16:21:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.5.tar.gz.asc crate-5.9.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.5.tar.gz.asc     && tar -xf crate-5.9.5.tar.gz -C /crate --strip-components=1     && rm crate-5.9.5.tar.gz # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Dec 2024 16:21:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 10 Dec 2024 16:21:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
VOLUME [/data]
# Tue, 10 Dec 2024 16:21:56 GMT
WORKDIR /data
# Tue, 10 Dec 2024 16:21:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-12-10T16:21:56.023234 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.5
# Tue, 10 Dec 2024 16:21:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Dec 2024 16:21:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eeccda12ed247fc86af9756eed85b9493924d0e5654243889a076103dba020`  
		Last Modified: Sat, 14 Dec 2024 18:11:31 GMT  
		Size: 13.5 MB (13537879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1e6977d7c6274d2809b4c27d1e41a2b9519f487a53b741263dd04bca7dac8b`  
		Last Modified: Sat, 14 Dec 2024 18:11:38 GMT  
		Size: 148.4 MB (148375948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298f0d0860c7d87c45abc13dd98458d6f6aaaffc41f61973f23de9e7da30493`  
		Last Modified: Sat, 14 Dec 2024 18:11:33 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5390f2f5edde014145aa39036356876d9045e93796c8af41f4de3f71dfd9f`  
		Last Modified: Fri, 13 Dec 2024 20:28:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fdf3527e264dc2003068e61b266a4b9ee395d3d153a57a7058014ac80ddbd6`  
		Last Modified: Fri, 13 Dec 2024 20:28:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf88d03d210975a6da59c0047af95728c1f90f1608754b2a2d81fee08f48f104`  
		Last Modified: Sat, 14 Dec 2024 18:10:28 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ae2da509d2a624303fe3b492d1fc6f1f49114065d73181123b41c3f3a6c9ff`  
		Last Modified: Fri, 13 Dec 2024 20:28:15 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:51c6206ce4d37e8fa7f927139e42061f862ec183a8590194a033e7f08dc5697a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9291f3cb2fa49d1ee7ba0bcea78940880bfafcb9cd823e7f0656f5df7eb99cb3`

```dockerfile
```

-	Layers:
	-	`sha256:9a37744ec313b2f7e8f033eaa064ba70ae9340eac85a59af74ac84ed1bb4598a`  
		Last Modified: Mon, 16 Dec 2024 19:09:09 GMT  
		Size: 6.3 MB (6327739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a505c2a4fac5bac8830a37aedf1b0540c2fa6604c6499f774f7bdfabe7910dfb`  
		Last Modified: Sun, 15 Dec 2024 05:36:14 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json
