<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.10`](#crate51010)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:7a37f7e9d935fe3358eb13c28786b49ffe2d127c670a9ed23b1d2fe9f3c52cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:333b3f90a231353299bfa1e915355d046c4db4846c63753380d4a6454f73efc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248796756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a389f1091350b104351da6d068b460a1a5df6dd6d6cf0009450d7044955715`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbefc1b3c83b1eed47be6effef121de219aa7f871a61eec2d481243cc5a87e`  
		Last Modified: Thu, 03 Jul 2025 17:06:36 GMT  
		Size: 30.0 MB (29999646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84919f910b975da140d85593f10a376f10af669ac0a12f53fcae988ae3b55374`  
		Last Modified: Thu, 03 Jul 2025 17:38:48 GMT  
		Size: 149.7 MB (149663686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97debf30635ff0b882cd93991b31b46edf46c2ab98224b32dd6dbd188a4aaa3f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d30f57a57c5f46f3f178c0c039c27ce4c9db88d8b79f30115a06ab216d826`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70631fb0770f8490a11be2bb561aae60e3b36b93c209fcbe3e230f2bba21a20`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f290b9389732f45ab816b6c5bcf5c592c6966fb344b4eb164a2c9eeb139449`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a0eae17fc27a4fa577a88066c369f0237aaef007948fbc99d297e3679d052f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:7f1ee390e37c89f3252ce0290f53b8285134090098850e7be1894456e0857e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03a6671e44d0d2b7b3b50304d7ef87ccc5cb6fee25bbdbc9d73d2bd23d9cfc9`

```dockerfile
```

-	Layers:
	-	`sha256:253353588e613cb075ce59a0d299602f428fe89fe2de6e4880bb94cc9e49cc3c`  
		Last Modified: Thu, 03 Jul 2025 17:38:28 GMT  
		Size: 5.2 MB (5183363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2482da364c40603417897c3c2e41281f92a52caa1ac29755ef2a0f6cb7a69331`  
		Last Modified: Thu, 03 Jul 2025 17:38:29 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7483b6e44ad2191151e4c7de32561fc35a9db26f9c53b48a640d2c0683a4fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247892902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ae7e866ad4453077b0c2eaef1505d02d5a2d33065a168f76d2ad7e5cc2cf62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80cd61bc344866c4903c5a7f545345395c84fc8917e69db3b3453001f0029f0`  
		Last Modified: Thu, 03 Jul 2025 17:07:03 GMT  
		Size: 29.9 MB (29916701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b76622ef14d61c8fcff142b2d44658520af51e3c3240f988fb8c32fba4079cc`  
		Last Modified: Thu, 03 Jul 2025 17:48:22 GMT  
		Size: 150.3 MB (150342641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830140196d08c00d404fa6e61fb8e8c3792c6a158f287e54a795734d3fb6c06f`  
		Last Modified: Thu, 03 Jul 2025 17:07:01 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d86b20f30b04f7a9317899d2b8c4037862c492da4714860edb1453ec068d23`  
		Last Modified: Thu, 03 Jul 2025 17:06:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ed9f2f87a0966dfbde5bab30c8cd5a95f1b1eef48885e1b87cfba5367c54fc`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24329342bc814e8258471d6509ca1af57c276b334a6235c9dfafbf0256735d`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79372075131c730531f7461495c68e8f18d09f880eace493c92d074fc0bd38`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:2aba2f9526d4995fec35badf2f95993e8dd9760715633d29b971f9e76c8e6a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2dea44252452fc90db573f87b664bed454699b17c3c5f1b53fa6d518cba49b`

```dockerfile
```

-	Layers:
	-	`sha256:93642ea138b26917e7fb964765bec99ecfd72a022602f46af7744872d446dce9`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 5.2 MB (5180671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43889f53c219e627f7df7849f70025d5a20d392d6d2c7f414d7f66c92c3052de`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.10`

```console
$ docker pull crate@sha256:7a37f7e9d935fe3358eb13c28786b49ffe2d127c670a9ed23b1d2fe9f3c52cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.10` - linux; amd64

```console
$ docker pull crate@sha256:333b3f90a231353299bfa1e915355d046c4db4846c63753380d4a6454f73efc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248796756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a389f1091350b104351da6d068b460a1a5df6dd6d6cf0009450d7044955715`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbefc1b3c83b1eed47be6effef121de219aa7f871a61eec2d481243cc5a87e`  
		Last Modified: Thu, 03 Jul 2025 17:06:36 GMT  
		Size: 30.0 MB (29999646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84919f910b975da140d85593f10a376f10af669ac0a12f53fcae988ae3b55374`  
		Last Modified: Thu, 03 Jul 2025 17:38:48 GMT  
		Size: 149.7 MB (149663686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97debf30635ff0b882cd93991b31b46edf46c2ab98224b32dd6dbd188a4aaa3f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d30f57a57c5f46f3f178c0c039c27ce4c9db88d8b79f30115a06ab216d826`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70631fb0770f8490a11be2bb561aae60e3b36b93c209fcbe3e230f2bba21a20`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f290b9389732f45ab816b6c5bcf5c592c6966fb344b4eb164a2c9eeb139449`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a0eae17fc27a4fa577a88066c369f0237aaef007948fbc99d297e3679d052f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.10` - unknown; unknown

```console
$ docker pull crate@sha256:7f1ee390e37c89f3252ce0290f53b8285134090098850e7be1894456e0857e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03a6671e44d0d2b7b3b50304d7ef87ccc5cb6fee25bbdbc9d73d2bd23d9cfc9`

```dockerfile
```

-	Layers:
	-	`sha256:253353588e613cb075ce59a0d299602f428fe89fe2de6e4880bb94cc9e49cc3c`  
		Last Modified: Thu, 03 Jul 2025 17:38:28 GMT  
		Size: 5.2 MB (5183363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2482da364c40603417897c3c2e41281f92a52caa1ac29755ef2a0f6cb7a69331`  
		Last Modified: Thu, 03 Jul 2025 17:38:29 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7483b6e44ad2191151e4c7de32561fc35a9db26f9c53b48a640d2c0683a4fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247892902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ae7e866ad4453077b0c2eaef1505d02d5a2d33065a168f76d2ad7e5cc2cf62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80cd61bc344866c4903c5a7f545345395c84fc8917e69db3b3453001f0029f0`  
		Last Modified: Thu, 03 Jul 2025 17:07:03 GMT  
		Size: 29.9 MB (29916701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b76622ef14d61c8fcff142b2d44658520af51e3c3240f988fb8c32fba4079cc`  
		Last Modified: Thu, 03 Jul 2025 17:48:22 GMT  
		Size: 150.3 MB (150342641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830140196d08c00d404fa6e61fb8e8c3792c6a158f287e54a795734d3fb6c06f`  
		Last Modified: Thu, 03 Jul 2025 17:07:01 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d86b20f30b04f7a9317899d2b8c4037862c492da4714860edb1453ec068d23`  
		Last Modified: Thu, 03 Jul 2025 17:06:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ed9f2f87a0966dfbde5bab30c8cd5a95f1b1eef48885e1b87cfba5367c54fc`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24329342bc814e8258471d6509ca1af57c276b334a6235c9dfafbf0256735d`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79372075131c730531f7461495c68e8f18d09f880eace493c92d074fc0bd38`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.10` - unknown; unknown

```console
$ docker pull crate@sha256:2aba2f9526d4995fec35badf2f95993e8dd9760715633d29b971f9e76c8e6a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2dea44252452fc90db573f87b664bed454699b17c3c5f1b53fa6d518cba49b`

```dockerfile
```

-	Layers:
	-	`sha256:93642ea138b26917e7fb964765bec99ecfd72a022602f46af7744872d446dce9`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 5.2 MB (5180671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43889f53c219e627f7df7849f70025d5a20d392d6d2c7f414d7f66c92c3052de`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:0c51896428e789e297c0c9d8ae0d086ba62d8408730bf2862bf55620b2ac47fa
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
		Last Modified: Wed, 11 Jun 2025 23:19:32 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 23:19:41 GMT  
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
$ docker pull crate@sha256:f45218332b08e96de0d23e578191189c92b7940316f59e9d46de5b1c1330dd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232751340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f6769cad003fb88285496c6585887754137d6be13201f4a0af51d99fa099c`
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
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0df37ad3bbae4b3e1e8b5a5faa0300948774d6478f9a52187bf62c30f54a04`  
		Last Modified: Thu, 12 Jun 2025 12:18:24 GMT  
		Size: 149.7 MB (149708538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edab8c2f093adc381d09a5b1148cba34b8ec89f24722402115da93555984ad`  
		Last Modified: Thu, 12 Jun 2025 04:55:32 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fb1e67e41a5024490ce8019d771cad63228d8072b69ebecb114031e2854cc`  
		Last Modified: Thu, 12 Jun 2025 04:55:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9865901db5cba0d95c8876983a6dcf0d269ee74547e1b3314e3df030e6346`  
		Last Modified: Thu, 12 Jun 2025 04:55:58 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfd3e2584488c3f049cabfadaee99b20ec04bd4f4953c4f829ca1dc44baa4a1`  
		Last Modified: Thu, 12 Jun 2025 04:56:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea497212c9651e773522151c6c295025f34d2c09fc5691e089c07a8778a6ee`  
		Last Modified: Thu, 12 Jun 2025 04:56:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:e3798d1e8aa55fc98021754792789818d986325f74568e49f50e8b39dbe2010f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790b0660c3d88429a02b2847814e61ed26dc9d11e0b882e1727be9ad1e6e37c`

```dockerfile
```

-	Layers:
	-	`sha256:6d6d22f6af5777b254cb12620f7e4775513b114a31ae1bc0da288ce52627623a`  
		Last Modified: Thu, 12 Jun 2025 05:38:28 GMT  
		Size: 5.2 MB (5178724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce501395edc091051025a9100df132186c10868694956548f4cec682b45b301`  
		Last Modified: Thu, 12 Jun 2025 05:38:29 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:0c51896428e789e297c0c9d8ae0d086ba62d8408730bf2862bf55620b2ac47fa
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
		Last Modified: Wed, 11 Jun 2025 23:19:32 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 23:19:41 GMT  
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
$ docker pull crate@sha256:f45218332b08e96de0d23e578191189c92b7940316f59e9d46de5b1c1330dd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232751340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f6769cad003fb88285496c6585887754137d6be13201f4a0af51d99fa099c`
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
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0df37ad3bbae4b3e1e8b5a5faa0300948774d6478f9a52187bf62c30f54a04`  
		Last Modified: Thu, 12 Jun 2025 12:18:24 GMT  
		Size: 149.7 MB (149708538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edab8c2f093adc381d09a5b1148cba34b8ec89f24722402115da93555984ad`  
		Last Modified: Thu, 12 Jun 2025 04:55:32 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fb1e67e41a5024490ce8019d771cad63228d8072b69ebecb114031e2854cc`  
		Last Modified: Thu, 12 Jun 2025 04:55:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9865901db5cba0d95c8876983a6dcf0d269ee74547e1b3314e3df030e6346`  
		Last Modified: Thu, 12 Jun 2025 04:55:58 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfd3e2584488c3f049cabfadaee99b20ec04bd4f4953c4f829ca1dc44baa4a1`  
		Last Modified: Thu, 12 Jun 2025 04:56:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea497212c9651e773522151c6c295025f34d2c09fc5691e089c07a8778a6ee`  
		Last Modified: Thu, 12 Jun 2025 04:56:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:e3798d1e8aa55fc98021754792789818d986325f74568e49f50e8b39dbe2010f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790b0660c3d88429a02b2847814e61ed26dc9d11e0b882e1727be9ad1e6e37c`

```dockerfile
```

-	Layers:
	-	`sha256:6d6d22f6af5777b254cb12620f7e4775513b114a31ae1bc0da288ce52627623a`  
		Last Modified: Thu, 12 Jun 2025 05:38:28 GMT  
		Size: 5.2 MB (5178724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce501395edc091051025a9100df132186c10868694956548f4cec682b45b301`  
		Last Modified: Thu, 12 Jun 2025 05:38:29 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:7a37f7e9d935fe3358eb13c28786b49ffe2d127c670a9ed23b1d2fe9f3c52cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:333b3f90a231353299bfa1e915355d046c4db4846c63753380d4a6454f73efc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248796756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a389f1091350b104351da6d068b460a1a5df6dd6d6cf0009450d7044955715`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbefc1b3c83b1eed47be6effef121de219aa7f871a61eec2d481243cc5a87e`  
		Last Modified: Thu, 03 Jul 2025 17:06:36 GMT  
		Size: 30.0 MB (29999646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84919f910b975da140d85593f10a376f10af669ac0a12f53fcae988ae3b55374`  
		Last Modified: Thu, 03 Jul 2025 17:38:48 GMT  
		Size: 149.7 MB (149663686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97debf30635ff0b882cd93991b31b46edf46c2ab98224b32dd6dbd188a4aaa3f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d30f57a57c5f46f3f178c0c039c27ce4c9db88d8b79f30115a06ab216d826`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70631fb0770f8490a11be2bb561aae60e3b36b93c209fcbe3e230f2bba21a20`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f290b9389732f45ab816b6c5bcf5c592c6966fb344b4eb164a2c9eeb139449`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a0eae17fc27a4fa577a88066c369f0237aaef007948fbc99d297e3679d052f`  
		Last Modified: Thu, 03 Jul 2025 17:06:33 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7f1ee390e37c89f3252ce0290f53b8285134090098850e7be1894456e0857e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03a6671e44d0d2b7b3b50304d7ef87ccc5cb6fee25bbdbc9d73d2bd23d9cfc9`

```dockerfile
```

-	Layers:
	-	`sha256:253353588e613cb075ce59a0d299602f428fe89fe2de6e4880bb94cc9e49cc3c`  
		Last Modified: Thu, 03 Jul 2025 17:38:28 GMT  
		Size: 5.2 MB (5183363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2482da364c40603417897c3c2e41281f92a52caa1ac29755ef2a0f6cb7a69331`  
		Last Modified: Thu, 03 Jul 2025 17:38:29 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7483b6e44ad2191151e4c7de32561fc35a9db26f9c53b48a640d2c0683a4fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247892902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ae7e866ad4453077b0c2eaef1505d02d5a2d33065a168f76d2ad7e5cc2cf62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 11 Jun 2025 13:41:30 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Wed, 11 Jun 2025 13:41:30 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80cd61bc344866c4903c5a7f545345395c84fc8917e69db3b3453001f0029f0`  
		Last Modified: Thu, 03 Jul 2025 17:07:03 GMT  
		Size: 29.9 MB (29916701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b76622ef14d61c8fcff142b2d44658520af51e3c3240f988fb8c32fba4079cc`  
		Last Modified: Thu, 03 Jul 2025 17:48:22 GMT  
		Size: 150.3 MB (150342641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830140196d08c00d404fa6e61fb8e8c3792c6a158f287e54a795734d3fb6c06f`  
		Last Modified: Thu, 03 Jul 2025 17:07:01 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d86b20f30b04f7a9317899d2b8c4037862c492da4714860edb1453ec068d23`  
		Last Modified: Thu, 03 Jul 2025 17:06:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ed9f2f87a0966dfbde5bab30c8cd5a95f1b1eef48885e1b87cfba5367c54fc`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24329342bc814e8258471d6509ca1af57c276b334a6235c9dfafbf0256735d`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79372075131c730531f7461495c68e8f18d09f880eace493c92d074fc0bd38`  
		Last Modified: Thu, 03 Jul 2025 17:07:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:2aba2f9526d4995fec35badf2f95993e8dd9760715633d29b971f9e76c8e6a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2dea44252452fc90db573f87b664bed454699b17c3c5f1b53fa6d518cba49b`

```dockerfile
```

-	Layers:
	-	`sha256:93642ea138b26917e7fb964765bec99ecfd72a022602f46af7744872d446dce9`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 5.2 MB (5180671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43889f53c219e627f7df7849f70025d5a20d392d6d2c7f414d7f66c92c3052de`  
		Last Modified: Thu, 03 Jul 2025 17:38:39 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json
