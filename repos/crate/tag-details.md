<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.11`](#crate51011)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:c8cf99ba641468db1fb727e984644b609dc91bff23fdd91feb5c568c363b4895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:efd25c4bc5ab6b357ac9eade9165f667ad810f2a497bc0d3b2f6eeb83fa5aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233819120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c98aba8018ab9ed3bfa541991c9c5d7482466327c76d592eb406ae7a17a179`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2bd009c0ba042fdee2efd106f4cd26fcd9d5d0376f1dcdd87abac6f6f9ac271f`  
		Last Modified: Mon, 04 Aug 2025 20:27:11 GMT  
		Size: 67.3 MB (67325559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b03f9c9c232c0d8964625cdae65a2a1d45fec862311cf58d261a1ea2fe9a327`  
		Last Modified: Mon, 04 Aug 2025 20:37:39 GMT  
		Size: 14.9 MB (14879148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d7fd4a3090465cf45961ef1f3fb8b25ce103241d7604af6ae5e9baa3312d24`  
		Last Modified: Mon, 04 Aug 2025 23:38:54 GMT  
		Size: 149.7 MB (149668904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edac569bba357de431aaf677659c1fb6e720e17849ce63ec08c8393c7e5dcee`  
		Last Modified: Mon, 04 Aug 2025 20:37:38 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e497a75392638745bac4658935c502ea308324edcfb5a2f1a11c92ee0f4067e0`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d8ee4c0c5b4eace4baf012a111885ff2d43d41f85ac4288ffe73450b5d129`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f697deae8e4362b7e0137cac592f197d6214ebe319b97e8d54c4cd0a59b909`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171aa52df391c9dd8973251203ea4152b032f088772e4b2e0a0d2ba31cc616c`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:b59e926be488c8176932278a60fe4c5eafae29a42feaa90d9f3614176c9ba000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97f2fd286ecde8973d058688889d20e538bb9e70ba5b15cfb10c1c5fc33cfdd`

```dockerfile
```

-	Layers:
	-	`sha256:aa39d49b5423d35dcf1e9884056af5cf4056204d2cd525417c376e48fbca00a0`  
		Last Modified: Mon, 04 Aug 2025 23:38:17 GMT  
		Size: 5.2 MB (5184036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94127999eb58bd4172495f37b773e493b0924e7dce7830dfc280741caf0853c`  
		Last Modified: Mon, 04 Aug 2025 23:38:18 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:026cd114ac35276a37e9b55cb77099da4b5d91a934a1aad6616be783cefee9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233005372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a439e09ef01d01f6a101a883c2245e7c5edefcf148bbb89dd75f9abd649f620f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ec2409fac64365a1b8f0c910292b06848eba5a4497d68a9db1b99cb357a673d1`  
		Last Modified: Tue, 05 Aug 2025 00:08:53 GMT  
		Size: 65.8 MB (65793060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa71995eeb906ac5d9dab02471b3b7d1b62f44940ace6be94f67ea4af9e20a7`  
		Last Modified: Tue, 05 Aug 2025 07:27:48 GMT  
		Size: 14.9 MB (14921126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af9531b0b1ce954ecc5fee1e6c809ed6a4ebcc708b98e0732a1c48260ceb111`  
		Last Modified: Tue, 05 Aug 2025 08:50:20 GMT  
		Size: 150.3 MB (150345681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9158445951b0351e68b3cb49975b3f7498c895484e93d505029a18f5f51ffe77`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850549a52a81278f895cee958431b31bcae6c8a5bdcde0d9ee4f21feda8e68e`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7ed1eb053543b04ba2b849bfa4e32089f737e8e6653e5fcdcaedea568ec6b`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e13567a4d10e97dee09a98e41c159f7608fff655d53a0c3be2fd9b65e3eac9a`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8179e3c3195fc0ae2ef5183406ba8f694caf7c0f393f5f5e457db90377e4d`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:145ac956a173c2acea9e75d031d4d14ae11aac0e480154d983108c9f8a27d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4ed578569824c88423589b3a3d0c9806359e0e930aa98005d50095f230bc6c`

```dockerfile
```

-	Layers:
	-	`sha256:4d37ba7741ffcffd8a03c34de5b351956b5fd2fd82ef578a7e7c5e170c02084a`  
		Last Modified: Tue, 05 Aug 2025 08:38:21 GMT  
		Size: 5.2 MB (5181344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a01c45825b9b8f9cc83af93c8efcb7944c2636615ce37ee62b8a7dcfb364fdc`  
		Last Modified: Tue, 05 Aug 2025 08:38:22 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.11`

```console
$ docker pull crate@sha256:c8cf99ba641468db1fb727e984644b609dc91bff23fdd91feb5c568c363b4895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.11` - linux; amd64

```console
$ docker pull crate@sha256:efd25c4bc5ab6b357ac9eade9165f667ad810f2a497bc0d3b2f6eeb83fa5aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233819120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c98aba8018ab9ed3bfa541991c9c5d7482466327c76d592eb406ae7a17a179`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2bd009c0ba042fdee2efd106f4cd26fcd9d5d0376f1dcdd87abac6f6f9ac271f`  
		Last Modified: Mon, 04 Aug 2025 20:27:11 GMT  
		Size: 67.3 MB (67325559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b03f9c9c232c0d8964625cdae65a2a1d45fec862311cf58d261a1ea2fe9a327`  
		Last Modified: Mon, 04 Aug 2025 20:37:39 GMT  
		Size: 14.9 MB (14879148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d7fd4a3090465cf45961ef1f3fb8b25ce103241d7604af6ae5e9baa3312d24`  
		Last Modified: Mon, 04 Aug 2025 23:38:54 GMT  
		Size: 149.7 MB (149668904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edac569bba357de431aaf677659c1fb6e720e17849ce63ec08c8393c7e5dcee`  
		Last Modified: Mon, 04 Aug 2025 20:37:38 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e497a75392638745bac4658935c502ea308324edcfb5a2f1a11c92ee0f4067e0`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d8ee4c0c5b4eace4baf012a111885ff2d43d41f85ac4288ffe73450b5d129`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f697deae8e4362b7e0137cac592f197d6214ebe319b97e8d54c4cd0a59b909`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171aa52df391c9dd8973251203ea4152b032f088772e4b2e0a0d2ba31cc616c`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:b59e926be488c8176932278a60fe4c5eafae29a42feaa90d9f3614176c9ba000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97f2fd286ecde8973d058688889d20e538bb9e70ba5b15cfb10c1c5fc33cfdd`

```dockerfile
```

-	Layers:
	-	`sha256:aa39d49b5423d35dcf1e9884056af5cf4056204d2cd525417c376e48fbca00a0`  
		Last Modified: Mon, 04 Aug 2025 23:38:17 GMT  
		Size: 5.2 MB (5184036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94127999eb58bd4172495f37b773e493b0924e7dce7830dfc280741caf0853c`  
		Last Modified: Mon, 04 Aug 2025 23:38:18 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.11` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:026cd114ac35276a37e9b55cb77099da4b5d91a934a1aad6616be783cefee9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233005372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a439e09ef01d01f6a101a883c2245e7c5edefcf148bbb89dd75f9abd649f620f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ec2409fac64365a1b8f0c910292b06848eba5a4497d68a9db1b99cb357a673d1`  
		Last Modified: Tue, 05 Aug 2025 00:08:53 GMT  
		Size: 65.8 MB (65793060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa71995eeb906ac5d9dab02471b3b7d1b62f44940ace6be94f67ea4af9e20a7`  
		Last Modified: Tue, 05 Aug 2025 07:27:48 GMT  
		Size: 14.9 MB (14921126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af9531b0b1ce954ecc5fee1e6c809ed6a4ebcc708b98e0732a1c48260ceb111`  
		Last Modified: Tue, 05 Aug 2025 08:50:20 GMT  
		Size: 150.3 MB (150345681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9158445951b0351e68b3cb49975b3f7498c895484e93d505029a18f5f51ffe77`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850549a52a81278f895cee958431b31bcae6c8a5bdcde0d9ee4f21feda8e68e`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7ed1eb053543b04ba2b849bfa4e32089f737e8e6653e5fcdcaedea568ec6b`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e13567a4d10e97dee09a98e41c159f7608fff655d53a0c3be2fd9b65e3eac9a`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8179e3c3195fc0ae2ef5183406ba8f694caf7c0f393f5f5e457db90377e4d`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:145ac956a173c2acea9e75d031d4d14ae11aac0e480154d983108c9f8a27d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4ed578569824c88423589b3a3d0c9806359e0e930aa98005d50095f230bc6c`

```dockerfile
```

-	Layers:
	-	`sha256:4d37ba7741ffcffd8a03c34de5b351956b5fd2fd82ef578a7e7c5e170c02084a`  
		Last Modified: Tue, 05 Aug 2025 08:38:21 GMT  
		Size: 5.2 MB (5181344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a01c45825b9b8f9cc83af93c8efcb7944c2636615ce37ee62b8a7dcfb364fdc`  
		Last Modified: Tue, 05 Aug 2025 08:38:22 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:7e3e91a10a250302652aaab0b1ba60809c6959cb4ce8794baf9d8aa27b288586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:3b61c373e661355799ec6c42ec1f78f2f2aca90f9bbfb437550cd5ae493b534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233160068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a01cc8efd74bd0e42e54752faf667976735e9fb3a739382d5b9406fd9b80e6e`
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
	-	`sha256:2bd009c0ba042fdee2efd106f4cd26fcd9d5d0376f1dcdd87abac6f6f9ac271f`  
		Last Modified: Mon, 04 Aug 2025 20:27:11 GMT  
		Size: 67.3 MB (67325559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe2b01854ec561c70f77b4ec601a6470d590221e6f4f35cc9dacc7fdb1cc170`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 14.9 MB (14879380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df059f641d62e45f02dc79e48eab8ffa114a640b623ed62224535cf10368d4e0`  
		Last Modified: Tue, 05 Aug 2025 03:09:44 GMT  
		Size: 149.0 MB (149009622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1dd411a3dcec10d59797cbb8e02a4ab9bfd41bb404b9e7313a61c22c416880`  
		Last Modified: Mon, 04 Aug 2025 20:37:47 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b9b0961e5a593def93b6df82386d5819d3291ae7bbad9b8a0a94690dd9f7e1`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4380c6d584dbc2f8b897f9b01f2953a0a8476c85d6b941f7879886513bbfbb32`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697240c61579f64a6b27ec48227fee1b7e7bb76dc4981648777d968ccec5de0`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171aa52df391c9dd8973251203ea4152b032f088772e4b2e0a0d2ba31cc616c`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:a32ececfc14234cefa98c158061cf1136388149543f1a5bf91d1a11da77fe7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8221211fbee76f017237b758c44430043f3810cf719caef1f8f5c802c6caf94`

```dockerfile
```

-	Layers:
	-	`sha256:2a1d0e7fb8ef37e018bc1aa1784a7ece4e16f4533447bffe37910679aeaba430`  
		Last Modified: Mon, 04 Aug 2025 23:38:25 GMT  
		Size: 5.2 MB (5182101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7708e16addb333fe2c6e606cd0bae7028dca15cb11805071ea83e2cfb7f595`  
		Last Modified: Mon, 04 Aug 2025 23:38:26 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:18c15751254a9f45a87a1463603337ee5ae31082023f34f551d3e2cff7d3fce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520e4a19d4f4c3e85a9faecb354e36583720d8156d4afabcb9995e5944f72054`
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
	-	`sha256:ec2409fac64365a1b8f0c910292b06848eba5a4497d68a9db1b99cb357a673d1`  
		Last Modified: Tue, 05 Aug 2025 00:08:53 GMT  
		Size: 65.8 MB (65793060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa71995eeb906ac5d9dab02471b3b7d1b62f44940ace6be94f67ea4af9e20a7`  
		Last Modified: Tue, 05 Aug 2025 07:27:48 GMT  
		Size: 14.9 MB (14921126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55115cb237213fb6a8c9004a571a8f7e8ab4b70984df1c6db30fa2775d677aa2`  
		Last Modified: Thu, 07 Aug 2025 07:43:17 GMT  
		Size: 149.7 MB (149708522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1833b34b82c2339e816aaf1ddc3a19f487091be46b9a29213505f269c95b3`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d967ccc8d46cd066f6131639966da6f3fe0475f163f1c1211cf666c379166f`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e9a0f3b21f49c638a413c38da54dd5dc7bd88a14dc4955788dcc03a010ef5`  
		Last Modified: Tue, 05 Aug 2025 07:28:39 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b7ec00de64cd0dd285dd558272f07587b40f98ca874e3251a67357a115ddc7`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a1538f8935a8e7732c0e5be932749cdb23db277f225399e39ee87186cb4bd`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:eea87502511a462418c71e7ac10f60e58b4b1630c45821ef35e2af7952e49211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aff34501ec5938bad3e9c36c0177534c288d1c3003df168c0da96be54ae01fd`

```dockerfile
```

-	Layers:
	-	`sha256:4810f9da25ba18520bd32c2f010b35a8fb3fa177d46c6e79fea944220293bc06`  
		Last Modified: Tue, 05 Aug 2025 08:38:27 GMT  
		Size: 5.2 MB (5179397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e511906d8dbe734cce6231d533206e3c12ba779e26a4507ea39ecd126ad108fb`  
		Last Modified: Tue, 05 Aug 2025 08:38:27 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:7e3e91a10a250302652aaab0b1ba60809c6959cb4ce8794baf9d8aa27b288586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:3b61c373e661355799ec6c42ec1f78f2f2aca90f9bbfb437550cd5ae493b534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233160068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a01cc8efd74bd0e42e54752faf667976735e9fb3a739382d5b9406fd9b80e6e`
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
	-	`sha256:2bd009c0ba042fdee2efd106f4cd26fcd9d5d0376f1dcdd87abac6f6f9ac271f`  
		Last Modified: Mon, 04 Aug 2025 20:27:11 GMT  
		Size: 67.3 MB (67325559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe2b01854ec561c70f77b4ec601a6470d590221e6f4f35cc9dacc7fdb1cc170`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 14.9 MB (14879380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df059f641d62e45f02dc79e48eab8ffa114a640b623ed62224535cf10368d4e0`  
		Last Modified: Tue, 05 Aug 2025 03:09:44 GMT  
		Size: 149.0 MB (149009622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1dd411a3dcec10d59797cbb8e02a4ab9bfd41bb404b9e7313a61c22c416880`  
		Last Modified: Mon, 04 Aug 2025 20:37:47 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b9b0961e5a593def93b6df82386d5819d3291ae7bbad9b8a0a94690dd9f7e1`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4380c6d584dbc2f8b897f9b01f2953a0a8476c85d6b941f7879886513bbfbb32`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697240c61579f64a6b27ec48227fee1b7e7bb76dc4981648777d968ccec5de0`  
		Last Modified: Mon, 04 Aug 2025 20:37:45 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171aa52df391c9dd8973251203ea4152b032f088772e4b2e0a0d2ba31cc616c`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:a32ececfc14234cefa98c158061cf1136388149543f1a5bf91d1a11da77fe7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8221211fbee76f017237b758c44430043f3810cf719caef1f8f5c802c6caf94`

```dockerfile
```

-	Layers:
	-	`sha256:2a1d0e7fb8ef37e018bc1aa1784a7ece4e16f4533447bffe37910679aeaba430`  
		Last Modified: Mon, 04 Aug 2025 23:38:25 GMT  
		Size: 5.2 MB (5182101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7708e16addb333fe2c6e606cd0bae7028dca15cb11805071ea83e2cfb7f595`  
		Last Modified: Mon, 04 Aug 2025 23:38:26 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:18c15751254a9f45a87a1463603337ee5ae31082023f34f551d3e2cff7d3fce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520e4a19d4f4c3e85a9faecb354e36583720d8156d4afabcb9995e5944f72054`
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
	-	`sha256:ec2409fac64365a1b8f0c910292b06848eba5a4497d68a9db1b99cb357a673d1`  
		Last Modified: Tue, 05 Aug 2025 00:08:53 GMT  
		Size: 65.8 MB (65793060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa71995eeb906ac5d9dab02471b3b7d1b62f44940ace6be94f67ea4af9e20a7`  
		Last Modified: Tue, 05 Aug 2025 07:27:48 GMT  
		Size: 14.9 MB (14921126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55115cb237213fb6a8c9004a571a8f7e8ab4b70984df1c6db30fa2775d677aa2`  
		Last Modified: Thu, 07 Aug 2025 07:43:17 GMT  
		Size: 149.7 MB (149708522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1833b34b82c2339e816aaf1ddc3a19f487091be46b9a29213505f269c95b3`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d967ccc8d46cd066f6131639966da6f3fe0475f163f1c1211cf666c379166f`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e9a0f3b21f49c638a413c38da54dd5dc7bd88a14dc4955788dcc03a010ef5`  
		Last Modified: Tue, 05 Aug 2025 07:28:39 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b7ec00de64cd0dd285dd558272f07587b40f98ca874e3251a67357a115ddc7`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a1538f8935a8e7732c0e5be932749cdb23db277f225399e39ee87186cb4bd`  
		Last Modified: Tue, 05 Aug 2025 07:28:38 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:eea87502511a462418c71e7ac10f60e58b4b1630c45821ef35e2af7952e49211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aff34501ec5938bad3e9c36c0177534c288d1c3003df168c0da96be54ae01fd`

```dockerfile
```

-	Layers:
	-	`sha256:4810f9da25ba18520bd32c2f010b35a8fb3fa177d46c6e79fea944220293bc06`  
		Last Modified: Tue, 05 Aug 2025 08:38:27 GMT  
		Size: 5.2 MB (5179397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e511906d8dbe734cce6231d533206e3c12ba779e26a4507ea39ecd126ad108fb`  
		Last Modified: Tue, 05 Aug 2025 08:38:27 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:c8cf99ba641468db1fb727e984644b609dc91bff23fdd91feb5c568c363b4895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:efd25c4bc5ab6b357ac9eade9165f667ad810f2a497bc0d3b2f6eeb83fa5aaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233819120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c98aba8018ab9ed3bfa541991c9c5d7482466327c76d592eb406ae7a17a179`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2bd009c0ba042fdee2efd106f4cd26fcd9d5d0376f1dcdd87abac6f6f9ac271f`  
		Last Modified: Mon, 04 Aug 2025 20:27:11 GMT  
		Size: 67.3 MB (67325559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b03f9c9c232c0d8964625cdae65a2a1d45fec862311cf58d261a1ea2fe9a327`  
		Last Modified: Mon, 04 Aug 2025 20:37:39 GMT  
		Size: 14.9 MB (14879148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d7fd4a3090465cf45961ef1f3fb8b25ce103241d7604af6ae5e9baa3312d24`  
		Last Modified: Mon, 04 Aug 2025 23:38:54 GMT  
		Size: 149.7 MB (149668904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edac569bba357de431aaf677659c1fb6e720e17849ce63ec08c8393c7e5dcee`  
		Last Modified: Mon, 04 Aug 2025 20:37:38 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e497a75392638745bac4658935c502ea308324edcfb5a2f1a11c92ee0f4067e0`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d8ee4c0c5b4eace4baf012a111885ff2d43d41f85ac4288ffe73450b5d129`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f697deae8e4362b7e0137cac592f197d6214ebe319b97e8d54c4cd0a59b909`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171aa52df391c9dd8973251203ea4152b032f088772e4b2e0a0d2ba31cc616c`  
		Last Modified: Mon, 04 Aug 2025 20:37:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b59e926be488c8176932278a60fe4c5eafae29a42feaa90d9f3614176c9ba000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97f2fd286ecde8973d058688889d20e538bb9e70ba5b15cfb10c1c5fc33cfdd`

```dockerfile
```

-	Layers:
	-	`sha256:aa39d49b5423d35dcf1e9884056af5cf4056204d2cd525417c376e48fbca00a0`  
		Last Modified: Mon, 04 Aug 2025 23:38:17 GMT  
		Size: 5.2 MB (5184036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94127999eb58bd4172495f37b773e493b0924e7dce7830dfc280741caf0853c`  
		Last Modified: Mon, 04 Aug 2025 23:38:18 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:026cd114ac35276a37e9b55cb77099da4b5d91a934a1aad6616be783cefee9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233005372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a439e09ef01d01f6a101a883c2245e7c5edefcf148bbb89dd75f9abd649f620f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ec2409fac64365a1b8f0c910292b06848eba5a4497d68a9db1b99cb357a673d1`  
		Last Modified: Tue, 05 Aug 2025 00:08:53 GMT  
		Size: 65.8 MB (65793060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa71995eeb906ac5d9dab02471b3b7d1b62f44940ace6be94f67ea4af9e20a7`  
		Last Modified: Tue, 05 Aug 2025 07:27:48 GMT  
		Size: 14.9 MB (14921126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af9531b0b1ce954ecc5fee1e6c809ed6a4ebcc708b98e0732a1c48260ceb111`  
		Last Modified: Tue, 05 Aug 2025 08:50:20 GMT  
		Size: 150.3 MB (150345681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9158445951b0351e68b3cb49975b3f7498c895484e93d505029a18f5f51ffe77`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850549a52a81278f895cee958431b31bcae6c8a5bdcde0d9ee4f21feda8e68e`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7ed1eb053543b04ba2b849bfa4e32089f737e8e6653e5fcdcaedea568ec6b`  
		Last Modified: Tue, 05 Aug 2025 07:27:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e13567a4d10e97dee09a98e41c159f7608fff655d53a0c3be2fd9b65e3eac9a`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8179e3c3195fc0ae2ef5183406ba8f694caf7c0f393f5f5e457db90377e4d`  
		Last Modified: Tue, 05 Aug 2025 07:27:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:145ac956a173c2acea9e75d031d4d14ae11aac0e480154d983108c9f8a27d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4ed578569824c88423589b3a3d0c9806359e0e930aa98005d50095f230bc6c`

```dockerfile
```

-	Layers:
	-	`sha256:4d37ba7741ffcffd8a03c34de5b351956b5fd2fd82ef578a7e7c5e170c02084a`  
		Last Modified: Tue, 05 Aug 2025 08:38:21 GMT  
		Size: 5.2 MB (5181344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a01c45825b9b8f9cc83af93c8efcb7944c2636615ce37ee62b8a7dcfb364fdc`  
		Last Modified: Tue, 05 Aug 2025 08:38:22 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json
