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
