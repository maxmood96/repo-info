<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.8`](#crate58)
-	[`crate:5.8.5`](#crate585)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.4`](#crate594)
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
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:06:14 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:05:18 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:05:19 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:06:14 GMT  
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
		Last Modified: Mon, 18 Nov 2024 22:06:11 GMT  
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
$ docker pull crate@sha256:d58e7284912c162ad8dacb1c9530d252d06640711ba1c927009ad4da38494d9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:a89642e060029a285c91b497663053e209be785093b641de00557be75a731268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228250979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44873ce76a85976dda9d9a650698eeb09c7816a37cd4fe32717c8a4d4c1999a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e10c5a86c6df5834dfc02b5204cc668ea8a19b2bb92e303d80dc3be452c31`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087270977aaceb6dd093a86303914774d2a531f2f5112cb7849780b23ffd418`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 147.2 MB (147208274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a725d9ec79b90daa2288e2a494da93bf05b4d56f5b1920e6e5537e068abff`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e24803cb814e9af3d043769e7a116c841994390845327c09a25e6228bc1d`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ea685949016929b829f855087eef9d1a79c8e8f4ef264594940fff3816d0c`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38518dbc4b434353a9b8bac25facc7498905467440ac0d4779c1226bc03f1aa`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3bacf1c1849e3e75bb5e56790cddee73478586305273db041a1f4269b51ff`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:ac99f800bf41f90b91d9d0ec22fbf9a7e8dbdd8863d3c1b9f46b3af19662afdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6354145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5fdffd84d632ad93482efe41f73e38d09b92324f7b3e90bb8929d4c797ff4b`

```dockerfile
```

-	Layers:
	-	`sha256:132c77371d7f1d92fa7bfd58bdca838f9125965e0ef27107cb444cc0b8c15ffb`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 6.3 MB (6331047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e161d3e31addf0f999d2d2be880c45e36b792ffdb522804333cffefef1c96`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8334e1c848a403ec9e2d7d84efd3deb51f15173675b51134e37e35b3bab67e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228326504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a8e7c1e12817d7555a63b50d4e6d24e00f84a3faeaa4f64865e354c498a05f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
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
	-	`sha256:742b565b332edcf304d8ed3b024367144d670464c8e762a1036d9269aa9fd710`  
		Last Modified: Mon, 02 Dec 2024 20:24:33 GMT  
		Size: 148.4 MB (148373945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12e1cbb625234467c0c85072b64cbce54698366ed6347641de14a13d988f82`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e000a722018046fdeb6eaca440528c298c33f144dd5bfe8909035d4560ef97b`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc5821e18f7dfcb7205257a8154205c6607f6edefee0f267eaebc376410847`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff94c925090de1bb65adedb6fe034a5d9775904296f91eef55375b2b4109bcb`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477163ec3bf9761cbe66638d5fb90a8a8f0440ff7188cb489a7ede1dababb7b9`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:94f6cf48c4594267d4bc01df1ac8f26509ffbe83729389f5dab9f49e5cb325de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1916bb94d6b92f05852fa3a7cb44c331f277bde8b2b6e2154b48d9ede7b6b57`

```dockerfile
```

-	Layers:
	-	`sha256:f35dc8a43e255a04b630f90f716600ff22623b0bcb937157157e96676e601833`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 6.3 MB (6327751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ce03a67932aec45fb926725e776a8328cd1265b5b74fa1c653ec7328c0fedf`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.4`

```console
$ docker pull crate@sha256:d58e7284912c162ad8dacb1c9530d252d06640711ba1c927009ad4da38494d9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.4` - linux; amd64

```console
$ docker pull crate@sha256:a89642e060029a285c91b497663053e209be785093b641de00557be75a731268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228250979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44873ce76a85976dda9d9a650698eeb09c7816a37cd4fe32717c8a4d4c1999a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e10c5a86c6df5834dfc02b5204cc668ea8a19b2bb92e303d80dc3be452c31`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087270977aaceb6dd093a86303914774d2a531f2f5112cb7849780b23ffd418`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 147.2 MB (147208274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a725d9ec79b90daa2288e2a494da93bf05b4d56f5b1920e6e5537e068abff`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e24803cb814e9af3d043769e7a116c841994390845327c09a25e6228bc1d`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ea685949016929b829f855087eef9d1a79c8e8f4ef264594940fff3816d0c`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38518dbc4b434353a9b8bac25facc7498905467440ac0d4779c1226bc03f1aa`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3bacf1c1849e3e75bb5e56790cddee73478586305273db041a1f4269b51ff`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.4` - unknown; unknown

```console
$ docker pull crate@sha256:ac99f800bf41f90b91d9d0ec22fbf9a7e8dbdd8863d3c1b9f46b3af19662afdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6354145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5fdffd84d632ad93482efe41f73e38d09b92324f7b3e90bb8929d4c797ff4b`

```dockerfile
```

-	Layers:
	-	`sha256:132c77371d7f1d92fa7bfd58bdca838f9125965e0ef27107cb444cc0b8c15ffb`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 6.3 MB (6331047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e161d3e31addf0f999d2d2be880c45e36b792ffdb522804333cffefef1c96`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8334e1c848a403ec9e2d7d84efd3deb51f15173675b51134e37e35b3bab67e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228326504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a8e7c1e12817d7555a63b50d4e6d24e00f84a3faeaa4f64865e354c498a05f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
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
	-	`sha256:742b565b332edcf304d8ed3b024367144d670464c8e762a1036d9269aa9fd710`  
		Last Modified: Mon, 02 Dec 2024 20:24:33 GMT  
		Size: 148.4 MB (148373945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12e1cbb625234467c0c85072b64cbce54698366ed6347641de14a13d988f82`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e000a722018046fdeb6eaca440528c298c33f144dd5bfe8909035d4560ef97b`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc5821e18f7dfcb7205257a8154205c6607f6edefee0f267eaebc376410847`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff94c925090de1bb65adedb6fe034a5d9775904296f91eef55375b2b4109bcb`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477163ec3bf9761cbe66638d5fb90a8a8f0440ff7188cb489a7ede1dababb7b9`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.4` - unknown; unknown

```console
$ docker pull crate@sha256:94f6cf48c4594267d4bc01df1ac8f26509ffbe83729389f5dab9f49e5cb325de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1916bb94d6b92f05852fa3a7cb44c331f277bde8b2b6e2154b48d9ede7b6b57`

```dockerfile
```

-	Layers:
	-	`sha256:f35dc8a43e255a04b630f90f716600ff22623b0bcb937157157e96676e601833`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 6.3 MB (6327751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ce03a67932aec45fb926725e776a8328cd1265b5b74fa1c653ec7328c0fedf`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:d58e7284912c162ad8dacb1c9530d252d06640711ba1c927009ad4da38494d9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:a89642e060029a285c91b497663053e209be785093b641de00557be75a731268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228250979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44873ce76a85976dda9d9a650698eeb09c7816a37cd4fe32717c8a4d4c1999a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e10c5a86c6df5834dfc02b5204cc668ea8a19b2bb92e303d80dc3be452c31`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087270977aaceb6dd093a86303914774d2a531f2f5112cb7849780b23ffd418`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 147.2 MB (147208274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a725d9ec79b90daa2288e2a494da93bf05b4d56f5b1920e6e5537e068abff`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e24803cb814e9af3d043769e7a116c841994390845327c09a25e6228bc1d`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ea685949016929b829f855087eef9d1a79c8e8f4ef264594940fff3816d0c`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38518dbc4b434353a9b8bac25facc7498905467440ac0d4779c1226bc03f1aa`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3bacf1c1849e3e75bb5e56790cddee73478586305273db041a1f4269b51ff`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:ac99f800bf41f90b91d9d0ec22fbf9a7e8dbdd8863d3c1b9f46b3af19662afdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6354145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5fdffd84d632ad93482efe41f73e38d09b92324f7b3e90bb8929d4c797ff4b`

```dockerfile
```

-	Layers:
	-	`sha256:132c77371d7f1d92fa7bfd58bdca838f9125965e0ef27107cb444cc0b8c15ffb`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 6.3 MB (6331047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21e161d3e31addf0f999d2d2be880c45e36b792ffdb522804333cffefef1c96`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8334e1c848a403ec9e2d7d84efd3deb51f15173675b51134e37e35b3bab67e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228326504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a8e7c1e12817d7555a63b50d4e6d24e00f84a3faeaa4f64865e354c498a05f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2024 14:37:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.4.tar.gz.asc crate-5.9.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.4.tar.gz.asc     && tar -xf crate-5.9.4.tar.gz -C /crate --strip-components=1     && rm crate-5.9.4.tar.gz # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 14:37:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 27 Nov 2024 14:37:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
VOLUME [/data]
# Wed, 27 Nov 2024 14:37:47 GMT
WORKDIR /data
# Wed, 27 Nov 2024 14:37:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-27T14:37:47.959903 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.4
# Wed, 27 Nov 2024 14:37:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 27 Nov 2024 14:37:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Nov 2024 14:37:47 GMT
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
	-	`sha256:742b565b332edcf304d8ed3b024367144d670464c8e762a1036d9269aa9fd710`  
		Last Modified: Mon, 02 Dec 2024 20:24:33 GMT  
		Size: 148.4 MB (148373945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12e1cbb625234467c0c85072b64cbce54698366ed6347641de14a13d988f82`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e000a722018046fdeb6eaca440528c298c33f144dd5bfe8909035d4560ef97b`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc5821e18f7dfcb7205257a8154205c6607f6edefee0f267eaebc376410847`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff94c925090de1bb65adedb6fe034a5d9775904296f91eef55375b2b4109bcb`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477163ec3bf9761cbe66638d5fb90a8a8f0440ff7188cb489a7ede1dababb7b9`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:94f6cf48c4594267d4bc01df1ac8f26509ffbe83729389f5dab9f49e5cb325de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1916bb94d6b92f05852fa3a7cb44c331f277bde8b2b6e2154b48d9ede7b6b57`

```dockerfile
```

-	Layers:
	-	`sha256:f35dc8a43e255a04b630f90f716600ff22623b0bcb937157157e96676e601833`  
		Last Modified: Mon, 02 Dec 2024 20:24:29 GMT  
		Size: 6.3 MB (6327751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ce03a67932aec45fb926725e776a8328cd1265b5b74fa1c653ec7328c0fedf`  
		Last Modified: Mon, 02 Dec 2024 20:24:28 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json
