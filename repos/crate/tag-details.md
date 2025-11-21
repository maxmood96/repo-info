<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.14`](#crate51014)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.3`](#crate603)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:fe9443a823bbbd6bca96cf7e93ea100a1c37029d7c0738d3dc6f56c6fa2a5bd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:a093b06933961ae606c8646a004db56a312a31a661728dc7a11e03743c73e5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233636695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086bf090eafa84cd7f5b78b8fc8966859088fcbe9f402542f7172709f0a0dd4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:11:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:11:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:11:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:11:19 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:11:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:11:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Mon, 17 Nov 2025 19:11:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:11:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d431e5a1208e4a4d55025827a18385d229fba1de9ca5802bc99409ed1bf24d`  
		Last Modified: Mon, 17 Nov 2025 21:39:31 GMT  
		Size: 149.7 MB (149720625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb86f56f90f2f6cc6f7d4f9acd006bb2f66cc30b7d223173e70fa4a2cdf10f7`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4763118e649bba894e25c4c95198e2bd3b4356c3603bd7d6894f2562ec4bd`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5f302feb36696cafef3616088591776b106c995df683194a15bdf62c5f74d`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fd07fb19fb39744e9789cbd8e1082ee87a49ff009e5d8fddb22b6b81f2a0ae`  
		Last Modified: Mon, 17 Nov 2025 19:11:50 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9bdaaaaf92ed2640bc1065d288f144fcd9097ac2c48ed13436ede7bfcf28a`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:1f4a41955de01b668f559375ffa533435e1bc15aba943b9b7c3cf0fd07d0cda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09406a7737f0321202bc90bb8dbd4e782efa4c0e8ce7bf0724d22355e03a80e`

```dockerfile
```

-	Layers:
	-	`sha256:3087ff85f96db3a9c5161f35fd9a26b5b64c891de689d97f2e6b1dbcbdddff68`  
		Last Modified: Mon, 17 Nov 2025 21:38:21 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2603201765956a5cdbc52b1ce6569c58e8ee44db7a143410d80889dfabe223`  
		Last Modified: Mon, 17 Nov 2025 21:38:22 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8df8545b90c3ec848682ea3f394711eacb4fdb06666448d20d9414b4fa26340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232855007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24e8b6998d10e271304bb515c1fb9ab93ab2476bbdd0ef38b31622b295bb809`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:11:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:11:25 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:11:25 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:11:25 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:11:25 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:11:25 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Mon, 17 Nov 2025 19:11:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:11:25 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a89b253b90b5a2b57339f07ffc6eac099b405c2e938af71d8e407cfc41eb3`  
		Last Modified: Fri, 21 Nov 2025 09:32:40 GMT  
		Size: 150.4 MB (150398713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89cc9907b8e6af55341512031192eb4fca15af0c2ec88b1bed67b112efaad6c`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843491b9551753c44d7ea91cfe8c5af9298663c76293c2512faaf8449da98d8`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277dc1829fa0c160fad68db262a66137718a09cd9e294338538eb5222bc77e9`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5648be81fb4957590457c0a3cb27cc063d4e95791ca28fe6350443383da24`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1bc638fbe2595b138d4c681437e316c38ea2d1841d8dd00585723d19364511`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:c662a7e04364c47593702c451a4eccba70e8dee86f565d1932bd767154425623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4a4e802d243893877f4a5889cfab684d957e72dbdfb536ff2702abc681152`

```dockerfile
```

-	Layers:
	-	`sha256:6c606791ec1a822d8111f99fa85057f12d470138638b315c2574e88554da6b02`  
		Last Modified: Mon, 17 Nov 2025 21:38:27 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfed2d6df38f392cd62ec1ebec3aba54d87184b966de2ead3f086a4153c8ec61`  
		Last Modified: Mon, 17 Nov 2025 21:38:28 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.14`

```console
$ docker pull crate@sha256:fe9443a823bbbd6bca96cf7e93ea100a1c37029d7c0738d3dc6f56c6fa2a5bd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.14` - linux; amd64

```console
$ docker pull crate@sha256:a093b06933961ae606c8646a004db56a312a31a661728dc7a11e03743c73e5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233636695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086bf090eafa84cd7f5b78b8fc8966859088fcbe9f402542f7172709f0a0dd4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:11:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:11:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:11:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:11:19 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:11:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:11:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Mon, 17 Nov 2025 19:11:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:11:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:11:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d431e5a1208e4a4d55025827a18385d229fba1de9ca5802bc99409ed1bf24d`  
		Last Modified: Mon, 17 Nov 2025 21:39:31 GMT  
		Size: 149.7 MB (149720625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb86f56f90f2f6cc6f7d4f9acd006bb2f66cc30b7d223173e70fa4a2cdf10f7`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4763118e649bba894e25c4c95198e2bd3b4356c3603bd7d6894f2562ec4bd`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5f302feb36696cafef3616088591776b106c995df683194a15bdf62c5f74d`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fd07fb19fb39744e9789cbd8e1082ee87a49ff009e5d8fddb22b6b81f2a0ae`  
		Last Modified: Mon, 17 Nov 2025 19:11:50 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9bdaaaaf92ed2640bc1065d288f144fcd9097ac2c48ed13436ede7bfcf28a`  
		Last Modified: Mon, 17 Nov 2025 19:11:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.14` - unknown; unknown

```console
$ docker pull crate@sha256:1f4a41955de01b668f559375ffa533435e1bc15aba943b9b7c3cf0fd07d0cda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09406a7737f0321202bc90bb8dbd4e782efa4c0e8ce7bf0724d22355e03a80e`

```dockerfile
```

-	Layers:
	-	`sha256:3087ff85f96db3a9c5161f35fd9a26b5b64c891de689d97f2e6b1dbcbdddff68`  
		Last Modified: Mon, 17 Nov 2025 21:38:21 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2603201765956a5cdbc52b1ce6569c58e8ee44db7a143410d80889dfabe223`  
		Last Modified: Mon, 17 Nov 2025 21:38:22 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.14` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8df8545b90c3ec848682ea3f394711eacb4fdb06666448d20d9414b4fa26340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232855007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24e8b6998d10e271304bb515c1fb9ab93ab2476bbdd0ef38b31622b295bb809`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:11:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.14.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.14.tar.gz.asc crate-5.10.14.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.14.tar.gz.asc     && tar -xf crate-5.10.14.tar.gz -C /crate --strip-components=1     && rm crate-5.10.14.tar.gz # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:11:25 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:11:25 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:11:25 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:11:25 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:11:25 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-03T09:56:23.454876 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.14
# Mon, 17 Nov 2025 19:11:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:11:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:11:25 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a89b253b90b5a2b57339f07ffc6eac099b405c2e938af71d8e407cfc41eb3`  
		Last Modified: Fri, 21 Nov 2025 09:32:40 GMT  
		Size: 150.4 MB (150398713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89cc9907b8e6af55341512031192eb4fca15af0c2ec88b1bed67b112efaad6c`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843491b9551753c44d7ea91cfe8c5af9298663c76293c2512faaf8449da98d8`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277dc1829fa0c160fad68db262a66137718a09cd9e294338538eb5222bc77e9`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5648be81fb4957590457c0a3cb27cc063d4e95791ca28fe6350443383da24`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1bc638fbe2595b138d4c681437e316c38ea2d1841d8dd00585723d19364511`  
		Last Modified: Mon, 17 Nov 2025 19:11:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.14` - unknown; unknown

```console
$ docker pull crate@sha256:c662a7e04364c47593702c451a4eccba70e8dee86f565d1932bd767154425623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4a4e802d243893877f4a5889cfab684d957e72dbdfb536ff2702abc681152`

```dockerfile
```

-	Layers:
	-	`sha256:6c606791ec1a822d8111f99fa85057f12d470138638b315c2574e88554da6b02`  
		Last Modified: Mon, 17 Nov 2025 21:38:27 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfed2d6df38f392cd62ec1ebec3aba54d87184b966de2ead3f086a4153c8ec61`  
		Last Modified: Mon, 17 Nov 2025 21:38:28 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:f9817ce5321f7bebb8cedb7173c0695b25ab87c97f1b0d656627f9f3bf440602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:0bdf38da9b5ed5fbad8334f56b4d9cbf97cbf742b6e8cb9bcffb720ea11ec534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232941747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a3c9f8388d4e955fdcd316eb96d7b9b78fd9583a960071a6da21497fe1b5ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:33 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:33 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:33 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c276eb189c1af5d3bf0fd0cefd24a060d8a6550383d13462b6fb3e6fa0d5ae`  
		Last Modified: Mon, 17 Nov 2025 21:38:51 GMT  
		Size: 149.0 MB (149025676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b05b562a6fd9228ae7d82b2e7793a76011314b3a356341edac73b85ca5afd6`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095ebb24b8d759dd20faba6a5b334ad4e6bfe298152724494ede8d5bd299260`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331a5bb2bce80dd171a3b04d2fe75436c16570c57c282614ca56fbea6e5fa05`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6867a1b2a95053b959557200f693b34c8e0bae64ee6eb93b5d4619f335fb373f`  
		Last Modified: Mon, 17 Nov 2025 19:11:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c9bea6e2e15503cf1339ebbec6faec7884bb9904f0baab6fe40f337cac67c`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:1abc8a49d2ef58112da1c9c5684873939b91fc44bd6258482d3b19a5b2db1ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc34abb05d97eb36ff501a71807fb80d4b232cf97dee06032a688a3a0963b8`

```dockerfile
```

-	Layers:
	-	`sha256:199b497c6f7f19f6a77f20290d79fdb58bcaffdbc750adb69e69547acdd19df2`  
		Last Modified: Mon, 17 Nov 2025 21:38:32 GMT  
		Size: 5.2 MB (5192280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bd724ee2ae808d82272bf96baad7d5358c4bfc0c12289fb6aa0253e93b02b4`  
		Last Modified: Mon, 17 Nov 2025 21:38:33 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b99c41fe836ddbdf065725bccfc1f19b94b8c6bdc8e306025695fbeda84761a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232170117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f13a65e9e5abe5adf2921c3ce056d19c89c37130024bb5fe0ef06c3331b300b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:42 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94961dd5362a0f3f453e4e58213c94de87c8795dfa95d6086f5fa5375edaa5`  
		Last Modified: Mon, 17 Nov 2025 21:49:09 GMT  
		Size: 149.7 MB (149713818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeed2533dfd110495dcfa1b70a91a18966271bdc0bcc32c212dec68f85d94e`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1092f6284b549a5a6965163d3672be80cee960a64632d7664f66921b503b4`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b08be77882453720be84648d36927bdf4bc975f54017e0671ab578f2b15fb`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c2d3cb43bf253ec906622b1938ec4baf68119a8e372df4e780b0e4494fe0d`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f485f0a96ae712069ab1cba0a1c6cf8b7524477011ac9dd448bf88cbebbe4e6`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:7512135d603bf980beee0e1e18f7bec5766d157bdfc9c48660c3d0d5fc9c959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6ecdeefed9c7c057dc6a6bb9246306761a979754487230215941c91513a2e6`

```dockerfile
```

-	Layers:
	-	`sha256:daafe8ffaba6b98b107ddcac59b468b6ee6592312ae2e776fb164be9db2d6040`  
		Last Modified: Mon, 17 Nov 2025 21:38:38 GMT  
		Size: 5.2 MB (5190199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9f2f0bf59a880c080ac68e721bd9a6643b38a5a093f16d5f2ebad1d808e555`  
		Last Modified: Mon, 17 Nov 2025 21:38:39 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.3`

```console
$ docker pull crate@sha256:f9817ce5321f7bebb8cedb7173c0695b25ab87c97f1b0d656627f9f3bf440602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.3` - linux; amd64

```console
$ docker pull crate@sha256:0bdf38da9b5ed5fbad8334f56b4d9cbf97cbf742b6e8cb9bcffb720ea11ec534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232941747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a3c9f8388d4e955fdcd316eb96d7b9b78fd9583a960071a6da21497fe1b5ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:33 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:33 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:33 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c276eb189c1af5d3bf0fd0cefd24a060d8a6550383d13462b6fb3e6fa0d5ae`  
		Last Modified: Mon, 17 Nov 2025 21:38:51 GMT  
		Size: 149.0 MB (149025676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b05b562a6fd9228ae7d82b2e7793a76011314b3a356341edac73b85ca5afd6`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095ebb24b8d759dd20faba6a5b334ad4e6bfe298152724494ede8d5bd299260`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331a5bb2bce80dd171a3b04d2fe75436c16570c57c282614ca56fbea6e5fa05`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6867a1b2a95053b959557200f693b34c8e0bae64ee6eb93b5d4619f335fb373f`  
		Last Modified: Mon, 17 Nov 2025 19:11:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c9bea6e2e15503cf1339ebbec6faec7884bb9904f0baab6fe40f337cac67c`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.3` - unknown; unknown

```console
$ docker pull crate@sha256:1abc8a49d2ef58112da1c9c5684873939b91fc44bd6258482d3b19a5b2db1ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc34abb05d97eb36ff501a71807fb80d4b232cf97dee06032a688a3a0963b8`

```dockerfile
```

-	Layers:
	-	`sha256:199b497c6f7f19f6a77f20290d79fdb58bcaffdbc750adb69e69547acdd19df2`  
		Last Modified: Mon, 17 Nov 2025 21:38:32 GMT  
		Size: 5.2 MB (5192280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bd724ee2ae808d82272bf96baad7d5358c4bfc0c12289fb6aa0253e93b02b4`  
		Last Modified: Mon, 17 Nov 2025 21:38:33 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b99c41fe836ddbdf065725bccfc1f19b94b8c6bdc8e306025695fbeda84761a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232170117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f13a65e9e5abe5adf2921c3ce056d19c89c37130024bb5fe0ef06c3331b300b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:42 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94961dd5362a0f3f453e4e58213c94de87c8795dfa95d6086f5fa5375edaa5`  
		Last Modified: Mon, 17 Nov 2025 21:49:09 GMT  
		Size: 149.7 MB (149713818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeed2533dfd110495dcfa1b70a91a18966271bdc0bcc32c212dec68f85d94e`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1092f6284b549a5a6965163d3672be80cee960a64632d7664f66921b503b4`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b08be77882453720be84648d36927bdf4bc975f54017e0671ab578f2b15fb`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c2d3cb43bf253ec906622b1938ec4baf68119a8e372df4e780b0e4494fe0d`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f485f0a96ae712069ab1cba0a1c6cf8b7524477011ac9dd448bf88cbebbe4e6`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.3` - unknown; unknown

```console
$ docker pull crate@sha256:7512135d603bf980beee0e1e18f7bec5766d157bdfc9c48660c3d0d5fc9c959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6ecdeefed9c7c057dc6a6bb9246306761a979754487230215941c91513a2e6`

```dockerfile
```

-	Layers:
	-	`sha256:daafe8ffaba6b98b107ddcac59b468b6ee6592312ae2e776fb164be9db2d6040`  
		Last Modified: Mon, 17 Nov 2025 21:38:38 GMT  
		Size: 5.2 MB (5190199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9f2f0bf59a880c080ac68e721bd9a6643b38a5a093f16d5f2ebad1d808e555`  
		Last Modified: Mon, 17 Nov 2025 21:38:39 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:f9817ce5321f7bebb8cedb7173c0695b25ab87c97f1b0d656627f9f3bf440602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:0bdf38da9b5ed5fbad8334f56b4d9cbf97cbf742b6e8cb9bcffb720ea11ec534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232941747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a3c9f8388d4e955fdcd316eb96d7b9b78fd9583a960071a6da21497fe1b5ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:33 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:33 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:33 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c276eb189c1af5d3bf0fd0cefd24a060d8a6550383d13462b6fb3e6fa0d5ae`  
		Last Modified: Mon, 17 Nov 2025 21:38:51 GMT  
		Size: 149.0 MB (149025676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b05b562a6fd9228ae7d82b2e7793a76011314b3a356341edac73b85ca5afd6`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095ebb24b8d759dd20faba6a5b334ad4e6bfe298152724494ede8d5bd299260`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331a5bb2bce80dd171a3b04d2fe75436c16570c57c282614ca56fbea6e5fa05`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6867a1b2a95053b959557200f693b34c8e0bae64ee6eb93b5d4619f335fb373f`  
		Last Modified: Mon, 17 Nov 2025 19:11:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c9bea6e2e15503cf1339ebbec6faec7884bb9904f0baab6fe40f337cac67c`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:1abc8a49d2ef58112da1c9c5684873939b91fc44bd6258482d3b19a5b2db1ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc34abb05d97eb36ff501a71807fb80d4b232cf97dee06032a688a3a0963b8`

```dockerfile
```

-	Layers:
	-	`sha256:199b497c6f7f19f6a77f20290d79fdb58bcaffdbc750adb69e69547acdd19df2`  
		Last Modified: Mon, 17 Nov 2025 21:38:32 GMT  
		Size: 5.2 MB (5192280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bd724ee2ae808d82272bf96baad7d5358c4bfc0c12289fb6aa0253e93b02b4`  
		Last Modified: Mon, 17 Nov 2025 21:38:33 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b99c41fe836ddbdf065725bccfc1f19b94b8c6bdc8e306025695fbeda84761a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232170117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f13a65e9e5abe5adf2921c3ce056d19c89c37130024bb5fe0ef06c3331b300b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:42 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94961dd5362a0f3f453e4e58213c94de87c8795dfa95d6086f5fa5375edaa5`  
		Last Modified: Mon, 17 Nov 2025 21:49:09 GMT  
		Size: 149.7 MB (149713818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeed2533dfd110495dcfa1b70a91a18966271bdc0bcc32c212dec68f85d94e`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1092f6284b549a5a6965163d3672be80cee960a64632d7664f66921b503b4`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b08be77882453720be84648d36927bdf4bc975f54017e0671ab578f2b15fb`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c2d3cb43bf253ec906622b1938ec4baf68119a8e372df4e780b0e4494fe0d`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f485f0a96ae712069ab1cba0a1c6cf8b7524477011ac9dd448bf88cbebbe4e6`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7512135d603bf980beee0e1e18f7bec5766d157bdfc9c48660c3d0d5fc9c959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6ecdeefed9c7c057dc6a6bb9246306761a979754487230215941c91513a2e6`

```dockerfile
```

-	Layers:
	-	`sha256:daafe8ffaba6b98b107ddcac59b468b6ee6592312ae2e776fb164be9db2d6040`  
		Last Modified: Mon, 17 Nov 2025 21:38:38 GMT  
		Size: 5.2 MB (5190199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9f2f0bf59a880c080ac68e721bd9a6643b38a5a093f16d5f2ebad1d808e555`  
		Last Modified: Mon, 17 Nov 2025 21:38:39 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
