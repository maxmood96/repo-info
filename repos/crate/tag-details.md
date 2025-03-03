<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.2`](#crate5102)
-	[`crate:5.7`](#crate57)
-	[`crate:5.7.6`](#crate576)
-	[`crate:5.8`](#crate58)
-	[`crate:5.8.7`](#crate587)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.11`](#crate5911)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:5512de3efc4321a9705ddc363edae5bfb028c5b5dc34a2d50fc6aa0eef03a83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:3e2f617b76d574dd1747534ce06ea1634bd40bb79893207dc3de45663de200fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249159175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48d7b3cb548514fdf798e5b82b0c2d2ab00669d2a73435cb26c3bf539ba503`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2122572b38204c69a5ee6fea31d16a5c543dff059ed1ea1eeb2d3527bd23e5f1`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 31.6 MB (31556971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250b59418d9b257b5e6d89f60f34c2972751848996920ca62751cb734adee3f`  
		Last Modified: Mon, 03 Mar 2025 21:07:18 GMT  
		Size: 149.7 MB (149652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619e33933e97e76c8db6119ce7e98f9b2fadaed8a7d9e9999e273dac426d886a`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a3e22501f970101a3f32a7e7494560ad554ccdf0eef61f133303509011bb8c`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb48f8153e2d3061b77448ad9ea90bf88fe70e5bdcc6e995db3525233f14a68`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4cfdd5097a0395be8f5b096a3f7ba88491fe1e51083ad0f2cd2ce7eb9d5e4a`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29625f6eecd8eeae4ee326a53536405b8ced93a1e4889b4c24b7ac950922de37`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:fc67c32aa5b4a3660a28e2d53134b7c7c8d0f53c405ff39afcfaaf4425f45f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6cd87946b29b5b9b00bd75f3f072c59db43a7bcd6b2190672312634d1416c9`

```dockerfile
```

-	Layers:
	-	`sha256:e3623c2727f799d136aab49b05e15e341e16b25777d2d3180e6fb6e29da6fc79`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 5.2 MB (5155083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e628578550d141466d03ffdfc2df77239c502d9c914980832416c80aaddf0e03`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6487449caa5d8b7de5734191b633bc6bb3c43ab68f2603822e7f137d918925e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248393514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ee8c3953a1c18b271eaf5d41009184c155216b45fafc67db57a44a9b6a46aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf212e0d8278f31a6cedad8e6d878dbbfaca1e5576d6cc007d50ab5eb4d149`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 31.5 MB (31471348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f100132c5a2664ec59f6103255bc83d6db2d47f64092482209a82f56a502062f`  
		Last Modified: Mon, 03 Mar 2025 21:06:59 GMT  
		Size: 150.3 MB (150333818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec7e23e9af3bd4748577c67989d02487d52ebaef8239bcc2f9d3113f0c5261`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f4da468adea6ba9df6c13a6203706b61cc0d8ac5db20ef4ac77c7f21a38dcb`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428f78a33b077cb7b8b63ca5564e5473c54a99d3bbe7c593539b862015a77a6`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739ee82a3362143e76da6d07d0b49715268941f53ceae1e7900c17be42f0df3`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ab8b9762a14a808d3cf55155f236ac53fcdab209fc18780cbb360dab5b4a2`  
		Last Modified: Mon, 03 Mar 2025 21:06:58 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:ae25cb13a400f96a6533733875bfc45b7544c166210adf3f36ac9cb0abbf7a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dada7153fec957e527eba573a7f5d71e22999f6f6ddb75be242f9f3e415c154`

```dockerfile
```

-	Layers:
	-	`sha256:275d351dcd18b836cb3d7520c276fb29d9506e412eb54847b50de5bc461d19c1`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 5.2 MB (5152391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00922077fb04571b58ba690f6e605cd25e56f75549f4012cb28e0e9479efa9a`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.2`

```console
$ docker pull crate@sha256:5512de3efc4321a9705ddc363edae5bfb028c5b5dc34a2d50fc6aa0eef03a83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.2` - linux; amd64

```console
$ docker pull crate@sha256:3e2f617b76d574dd1747534ce06ea1634bd40bb79893207dc3de45663de200fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249159175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48d7b3cb548514fdf798e5b82b0c2d2ab00669d2a73435cb26c3bf539ba503`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2122572b38204c69a5ee6fea31d16a5c543dff059ed1ea1eeb2d3527bd23e5f1`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 31.6 MB (31556971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250b59418d9b257b5e6d89f60f34c2972751848996920ca62751cb734adee3f`  
		Last Modified: Mon, 03 Mar 2025 21:07:18 GMT  
		Size: 149.7 MB (149652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619e33933e97e76c8db6119ce7e98f9b2fadaed8a7d9e9999e273dac426d886a`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a3e22501f970101a3f32a7e7494560ad554ccdf0eef61f133303509011bb8c`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb48f8153e2d3061b77448ad9ea90bf88fe70e5bdcc6e995db3525233f14a68`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4cfdd5097a0395be8f5b096a3f7ba88491fe1e51083ad0f2cd2ce7eb9d5e4a`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29625f6eecd8eeae4ee326a53536405b8ced93a1e4889b4c24b7ac950922de37`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.2` - unknown; unknown

```console
$ docker pull crate@sha256:fc67c32aa5b4a3660a28e2d53134b7c7c8d0f53c405ff39afcfaaf4425f45f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6cd87946b29b5b9b00bd75f3f072c59db43a7bcd6b2190672312634d1416c9`

```dockerfile
```

-	Layers:
	-	`sha256:e3623c2727f799d136aab49b05e15e341e16b25777d2d3180e6fb6e29da6fc79`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 5.2 MB (5155083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e628578550d141466d03ffdfc2df77239c502d9c914980832416c80aaddf0e03`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6487449caa5d8b7de5734191b633bc6bb3c43ab68f2603822e7f137d918925e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248393514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ee8c3953a1c18b271eaf5d41009184c155216b45fafc67db57a44a9b6a46aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf212e0d8278f31a6cedad8e6d878dbbfaca1e5576d6cc007d50ab5eb4d149`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 31.5 MB (31471348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f100132c5a2664ec59f6103255bc83d6db2d47f64092482209a82f56a502062f`  
		Last Modified: Mon, 03 Mar 2025 21:06:59 GMT  
		Size: 150.3 MB (150333818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec7e23e9af3bd4748577c67989d02487d52ebaef8239bcc2f9d3113f0c5261`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f4da468adea6ba9df6c13a6203706b61cc0d8ac5db20ef4ac77c7f21a38dcb`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428f78a33b077cb7b8b63ca5564e5473c54a99d3bbe7c593539b862015a77a6`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739ee82a3362143e76da6d07d0b49715268941f53ceae1e7900c17be42f0df3`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ab8b9762a14a808d3cf55155f236ac53fcdab209fc18780cbb360dab5b4a2`  
		Last Modified: Mon, 03 Mar 2025 21:06:58 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.2` - unknown; unknown

```console
$ docker pull crate@sha256:ae25cb13a400f96a6533733875bfc45b7544c166210adf3f36ac9cb0abbf7a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dada7153fec957e527eba573a7f5d71e22999f6f6ddb75be242f9f3e415c154`

```dockerfile
```

-	Layers:
	-	`sha256:275d351dcd18b836cb3d7520c276fb29d9506e412eb54847b50de5bc461d19c1`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 5.2 MB (5152391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00922077fb04571b58ba690f6e605cd25e56f75549f4012cb28e0e9479efa9a`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:43616811da15804be5a5134a4a67b235f2661aca4da18d74b367db74e815cf02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:18ed0795fd515536aedc431a2e4fd595e2e8903fdced32995be7c8179564ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222473692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3380feb3474142b276669d506057975611857f6603cec8f9f112dfd5d876c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:4f1aee1457eef2e84cf605d2d7bbb7a62f69df337350b2df6fa9ad3a6502b739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e1b8ab92e2d8a0e804f48728361cba944de2688406eb24436658f19a3a9eb`

```dockerfile
```

-	Layers:
	-	`sha256:79ad35a1f957ff0cdb355dac65c0999a2269d4bf812595fd54583913d8c082dc`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 6.3 MB (6307614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63707574a469fb5256260de2b08956303124c0611a371df45ff210c37227bcfd`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:56df24803f48b69ef67afe35a3e93d8d2041a328b9b2bb1dcdd24aa015726d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220990509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae41fa9c6d6c159723a120b03cfd2d47ea4d5589ea4e5d79b726e90a7d6704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Mon, 03 Feb 2025 22:29:15 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:8546dae2b9393070cf5de782664e55fc4d8d5043d82ae5f373f2dbff969423bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6328485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88a57d6771cd6148eca809c037130a0eee707592f2ba9d6cc2248fb9e56c32f`

```dockerfile
```

-	Layers:
	-	`sha256:65a92c74cb9153eecbe3aee799b45ec390bb40474b07477f19e87749b15460dc`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 6.3 MB (6305534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fbee603b6fc8414e65a4bada522e097094dab0f15da087b2465240aa196110`  
		Last Modified: Mon, 03 Feb 2025 22:29:11 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.6`

```console
$ docker pull crate@sha256:43616811da15804be5a5134a4a67b235f2661aca4da18d74b367db74e815cf02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.6` - linux; amd64

```console
$ docker pull crate@sha256:18ed0795fd515536aedc431a2e4fd595e2e8903fdced32995be7c8179564ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222473692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3380feb3474142b276669d506057975611857f6603cec8f9f112dfd5d876c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.6` - unknown; unknown

```console
$ docker pull crate@sha256:4f1aee1457eef2e84cf605d2d7bbb7a62f69df337350b2df6fa9ad3a6502b739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e1b8ab92e2d8a0e804f48728361cba944de2688406eb24436658f19a3a9eb`

```dockerfile
```

-	Layers:
	-	`sha256:79ad35a1f957ff0cdb355dac65c0999a2269d4bf812595fd54583913d8c082dc`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 6.3 MB (6307614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63707574a469fb5256260de2b08956303124c0611a371df45ff210c37227bcfd`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:56df24803f48b69ef67afe35a3e93d8d2041a328b9b2bb1dcdd24aa015726d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220990509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae41fa9c6d6c159723a120b03cfd2d47ea4d5589ea4e5d79b726e90a7d6704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Mon, 03 Feb 2025 22:29:15 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.6` - unknown; unknown

```console
$ docker pull crate@sha256:8546dae2b9393070cf5de782664e55fc4d8d5043d82ae5f373f2dbff969423bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6328485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88a57d6771cd6148eca809c037130a0eee707592f2ba9d6cc2248fb9e56c32f`

```dockerfile
```

-	Layers:
	-	`sha256:65a92c74cb9153eecbe3aee799b45ec390bb40474b07477f19e87749b15460dc`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 6.3 MB (6305534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fbee603b6fc8414e65a4bada522e097094dab0f15da087b2465240aa196110`  
		Last Modified: Mon, 03 Feb 2025 22:29:11 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8`

```console
$ docker pull crate@sha256:9a3e42c1360080086c3730090011fa96448376ea2b42eac7bff441916db5e2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8` - linux; amd64

```console
$ docker pull crate@sha256:0c4e697dfc9f0910b913d2d2ad62959eb7abb173e0e5db3ebd434893c9550082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229471940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b54ccbcce4cb17b805634136a01b74651a4425ea7a0b51e7f1d6c50a03da42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 13:30:07 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.7.tar.gz.asc crate-5.8.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.7.tar.gz.asc     && tar -xf crate-5.8.7.tar.gz -C /crate --strip-components=1     && rm crate-5.8.7.tar.gz # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 13:30:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 13:30:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 13:30:07 GMT
WORKDIR /data
# Thu, 27 Feb 2025 13:30:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 13:30:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T13:30:07.740047 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.7
# Thu, 27 Feb 2025 13:30:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 13:30:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ce43b97bd59095eae16fb5ad7e238d0130c406b7af64e0970eb76582e9cc1d`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 31.6 MB (31556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda485b4f6330224657ecab33ea17b7c9aeb5e07745eacae8daafaea3fe0ed2`  
		Last Modified: Mon, 03 Mar 2025 21:07:28 GMT  
		Size: 130.0 MB (129965112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bda8d8fc01679ef7b0203c6d80c0f49a388a6cf56c11e75d053edeb76e05`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76d9a5f6a4d2f7293892d3087891ea867aa6810b7a2875415ba5ee7fe7712`  
		Last Modified: Mon, 03 Mar 2025 21:07:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff51cccc186e4aaa7761df7161a9278428cf0582463b9065cdddc94dd53289`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1c2ed30c4237378103de9d6a5dbf48c4caf271c9366f5d34d471e77aeefa9f`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ef517e48f46691f6ffc49b6991acf605f02d646c9be04990f3063d75eb8165`  
		Last Modified: Mon, 03 Mar 2025 21:07:27 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:53070857e4916fe0e1b45226f12102260e89f76476b50fd39c121527c75ab5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a869c2fbea7a9f122ebb75bcd3f0e4aa9718fc55e93585116440fee5c13644d4`

```dockerfile
```

-	Layers:
	-	`sha256:6b00900136341fd9a9af2fb6679274e57360503fdb86519db9f7ebfa016eb545`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 5.1 MB (5136653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41602bdaa1b0a517d58fdd4411568a42e8c3560cf82efd92aebd7b337546a4b`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 22.9 KB (22887 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bfdc8a8faf6e4ecbd04f4f395f208a7e430b454b06df52eb67e60f8801440861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223540739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5added6112601e5abfb14d1b73567dec272004ee864ffeca4dd9f7572fad518f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 16:42:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.6.tar.gz.asc crate-5.8.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.6.tar.gz.asc     && tar -xf crate-5.8.6.tar.gz -C /crate --strip-components=1     && rm crate-5.8.6.tar.gz # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 16:42:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 16:42:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 16:42:57 GMT
WORKDIR /data
# Thu, 30 Jan 2025 16:42:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T16:42:57.310116 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.6
# Thu, 30 Jan 2025 16:42:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 16:42:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925575c4ad696b0392b1e5623678226cf327e83ef5dd77249f56efb83e08db7f`  
		Last Modified: Mon, 03 Feb 2025 22:28:22 GMT  
		Size: 129.4 MB (129412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f56b72c56eaef6be6c960e2edbdd52131ca0d785fe2814fd0cc98c348a0842`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17da6553dd1a472e3daefd9753b66f5290c055c25008fa3b9d21847fdebeb16`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bb6ba7c924dd6d4374c154c75f42b420500db97f26e46ad78a44d93dacac6`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da709d79ed5b345bf3ae95fab349ffc4f3ee6f5a0af717d96c5e95b6e3cf81`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86115430a3330e27af6bbd3793fa03f403720f84d0ec347f31d85d18709094`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:39334effa5723f5c5be9daefd89e6285099626ac85b61aefb52c7bf510bf3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a988c18880d0246452e33bbb744595b2e8362d60f9739529c93965bb47805563`

```dockerfile
```

-	Layers:
	-	`sha256:f6e9fb7c38563db8dc6d44f6c25d5135bd18ac7eab9a4383b1ca816179a845d7`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 6.3 MB (6297784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18b938e7f03ecd9760265c48521b957dc7cad62f0dc5761077a4337ece73322`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8.7`

```console
$ docker pull crate@sha256:ad809025f572a17ab80d04a22d43b1b850fa2420ce52379d6d845bf6561ac762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `crate:5.8.7` - linux; amd64

```console
$ docker pull crate@sha256:0c4e697dfc9f0910b913d2d2ad62959eb7abb173e0e5db3ebd434893c9550082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229471940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b54ccbcce4cb17b805634136a01b74651a4425ea7a0b51e7f1d6c50a03da42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 13:30:07 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.7.tar.gz.asc crate-5.8.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.7.tar.gz.asc     && tar -xf crate-5.8.7.tar.gz -C /crate --strip-components=1     && rm crate-5.8.7.tar.gz # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 13:30:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 13:30:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 13:30:07 GMT
WORKDIR /data
# Thu, 27 Feb 2025 13:30:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 13:30:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T13:30:07.740047 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.7
# Thu, 27 Feb 2025 13:30:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 13:30:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 13:30:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ce43b97bd59095eae16fb5ad7e238d0130c406b7af64e0970eb76582e9cc1d`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 31.6 MB (31556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda485b4f6330224657ecab33ea17b7c9aeb5e07745eacae8daafaea3fe0ed2`  
		Last Modified: Mon, 03 Mar 2025 21:07:28 GMT  
		Size: 130.0 MB (129965112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bda8d8fc01679ef7b0203c6d80c0f49a388a6cf56c11e75d053edeb76e05`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76d9a5f6a4d2f7293892d3087891ea867aa6810b7a2875415ba5ee7fe7712`  
		Last Modified: Mon, 03 Mar 2025 21:07:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff51cccc186e4aaa7761df7161a9278428cf0582463b9065cdddc94dd53289`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1c2ed30c4237378103de9d6a5dbf48c4caf271c9366f5d34d471e77aeefa9f`  
		Last Modified: Mon, 03 Mar 2025 21:07:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ef517e48f46691f6ffc49b6991acf605f02d646c9be04990f3063d75eb8165`  
		Last Modified: Mon, 03 Mar 2025 21:07:27 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.7` - unknown; unknown

```console
$ docker pull crate@sha256:53070857e4916fe0e1b45226f12102260e89f76476b50fd39c121527c75ab5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a869c2fbea7a9f122ebb75bcd3f0e4aa9718fc55e93585116440fee5c13644d4`

```dockerfile
```

-	Layers:
	-	`sha256:6b00900136341fd9a9af2fb6679274e57360503fdb86519db9f7ebfa016eb545`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 5.1 MB (5136653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41602bdaa1b0a517d58fdd4411568a42e8c3560cf82efd92aebd7b337546a4b`  
		Last Modified: Mon, 03 Mar 2025 21:07:25 GMT  
		Size: 22.9 KB (22887 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:971eb21de3019a6628302ef1e7b1fb2f48a9931690f4576c32dc2f9a99c5b3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:ed86d0d6d5ce7cc9bd52cfe51067492120c8698ffa2e06b568cf017ba9afb99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248513084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee573a0c7a5847624d922b5c2a48ac4de0eaefe88ee6e2fa70174955fff2be4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 15:04:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.11.tar.gz.asc crate-5.9.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.11.tar.gz.asc     && tar -xf crate-5.9.11.tar.gz -C /crate --strip-components=1     && rm crate-5.9.11.tar.gz # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 15:04:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 15:04:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 15:04:32 GMT
WORKDIR /data
# Thu, 27 Feb 2025 15:04:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T15:04:32.414992 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.11
# Thu, 27 Feb 2025 15:04:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 15:04:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d311c45f4eb3b1707a77f02940f55c21ebb89b07826a9aeeaeb8698e6d165`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 31.6 MB (31556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a816863a571cf69472e7f9525f4e95f7525ee3b607fae364a635c5c19e905f1`  
		Last Modified: Mon, 03 Mar 2025 21:07:12 GMT  
		Size: 149.0 MB (149006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741bb9f51e02be06671d77481e03b244bf16765eb0e89913dc85a638470cd236`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69fa6984e51554b7f533247a2eca9c0233d998fa65275d4f719ae3de65ba74`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9f4cfa2bb970b2b91b1559b6019405dcdeb841910a518f91aa237d3bd46c2`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7faf23982562187cb8c1bdd52621c3a6810e533efad647f21e2dd62cdd13ed`  
		Last Modified: Mon, 03 Mar 2025 21:07:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846efd8e41597ecf619dabc29b617f7e13f3fe1abe3b97f229b66e3525cbd0dd`  
		Last Modified: Mon, 03 Mar 2025 21:07:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:5ce2e0c9ea42116d30d3c1fcbf0698fb514eda1484d82a59bf4b95da034cbdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f12bb33f540b70740a1d0dab304caab15b566085b3de847fb2c5df09d203ab`

```dockerfile
```

-	Layers:
	-	`sha256:3fe6b9f7da2f2a3e59a89772ae7d35b5dbbc2400cac62295a43cec360648ce8d`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 5.2 MB (5152911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bbcd006683cab933c712e957603f5858d89b0325924805b8b044682c04c1b9`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bee1d69443f831b19ec7de7626405fb44f43525cb63624b2e62168b6425759bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247764414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653362c56d4e935eea7ecd8df214094f51cd1bac7a712bb5eba58ec0493dc066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 15:04:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.11.tar.gz.asc crate-5.9.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.11.tar.gz.asc     && tar -xf crate-5.9.11.tar.gz -C /crate --strip-components=1     && rm crate-5.9.11.tar.gz # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 15:04:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 15:04:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 15:04:32 GMT
WORKDIR /data
# Thu, 27 Feb 2025 15:04:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T15:04:32.414992 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.11
# Thu, 27 Feb 2025 15:04:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 15:04:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf212e0d8278f31a6cedad8e6d878dbbfaca1e5576d6cc007d50ab5eb4d149`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 31.5 MB (31471348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abdfaa1bd689c3b79a73edd7b200ca4dc06311284fb10b274b1d940aeb86bf0`  
		Last Modified: Mon, 03 Mar 2025 21:10:10 GMT  
		Size: 149.7 MB (149704720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98836c77271214a7e5984b796c4ca6960b9a05f24980f3d44b2a12bbbc5a6962`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129ed946cded32559147c893de019c8054a69bc05b7b594f381d9950752c73d`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fe5414d8768e6030cc5d6d0118b14863fa412d6b03919d9e1f778c8a2f21e0`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40f5cd554874b26262ace372738a38585008ea2d3ab9439abe40a733b9092a`  
		Last Modified: Mon, 03 Mar 2025 21:10:07 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118f75dee1103875fd39234e8b5337499466120b01dd870607e3d6955a71270`  
		Last Modified: Mon, 03 Mar 2025 21:10:07 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:a014adbabbd3a1f6a86dd30cf8ea501d1982fa769fde7c48eb68ff8672cda064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d8d751a7483ae57e3d5879ae64c93d3a11957e106fe415de84366ddcb26dfa`

```dockerfile
```

-	Layers:
	-	`sha256:b02db13777337f30bd76aa1ade1758c7c7e1c64a7814670fac1f48fe3e963df7`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 5.2 MB (5150207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fedcf4e52b923cc8d7eaf8c728f620b427ebab01fc77b252cf428edab79cd4`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.11`

```console
$ docker pull crate@sha256:971eb21de3019a6628302ef1e7b1fb2f48a9931690f4576c32dc2f9a99c5b3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.11` - linux; amd64

```console
$ docker pull crate@sha256:ed86d0d6d5ce7cc9bd52cfe51067492120c8698ffa2e06b568cf017ba9afb99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248513084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee573a0c7a5847624d922b5c2a48ac4de0eaefe88ee6e2fa70174955fff2be4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 15:04:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.11.tar.gz.asc crate-5.9.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.11.tar.gz.asc     && tar -xf crate-5.9.11.tar.gz -C /crate --strip-components=1     && rm crate-5.9.11.tar.gz # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 15:04:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 15:04:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 15:04:32 GMT
WORKDIR /data
# Thu, 27 Feb 2025 15:04:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T15:04:32.414992 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.11
# Thu, 27 Feb 2025 15:04:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 15:04:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d311c45f4eb3b1707a77f02940f55c21ebb89b07826a9aeeaeb8698e6d165`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 31.6 MB (31556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a816863a571cf69472e7f9525f4e95f7525ee3b607fae364a635c5c19e905f1`  
		Last Modified: Mon, 03 Mar 2025 21:07:12 GMT  
		Size: 149.0 MB (149006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741bb9f51e02be06671d77481e03b244bf16765eb0e89913dc85a638470cd236`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69fa6984e51554b7f533247a2eca9c0233d998fa65275d4f719ae3de65ba74`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9f4cfa2bb970b2b91b1559b6019405dcdeb841910a518f91aa237d3bd46c2`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7faf23982562187cb8c1bdd52621c3a6810e533efad647f21e2dd62cdd13ed`  
		Last Modified: Mon, 03 Mar 2025 21:07:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846efd8e41597ecf619dabc29b617f7e13f3fe1abe3b97f229b66e3525cbd0dd`  
		Last Modified: Mon, 03 Mar 2025 21:07:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.11` - unknown; unknown

```console
$ docker pull crate@sha256:5ce2e0c9ea42116d30d3c1fcbf0698fb514eda1484d82a59bf4b95da034cbdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f12bb33f540b70740a1d0dab304caab15b566085b3de847fb2c5df09d203ab`

```dockerfile
```

-	Layers:
	-	`sha256:3fe6b9f7da2f2a3e59a89772ae7d35b5dbbc2400cac62295a43cec360648ce8d`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 5.2 MB (5152911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bbcd006683cab933c712e957603f5858d89b0325924805b8b044682c04c1b9`  
		Last Modified: Mon, 03 Mar 2025 21:07:10 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.11` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bee1d69443f831b19ec7de7626405fb44f43525cb63624b2e62168b6425759bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247764414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653362c56d4e935eea7ecd8df214094f51cd1bac7a712bb5eba58ec0493dc066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 15:04:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.11.tar.gz.asc crate-5.9.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.11.tar.gz.asc     && tar -xf crate-5.9.11.tar.gz -C /crate --strip-components=1     && rm crate-5.9.11.tar.gz # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 15:04:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 27 Feb 2025 15:04:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
VOLUME [/data]
# Thu, 27 Feb 2025 15:04:32 GMT
WORKDIR /data
# Thu, 27 Feb 2025 15:04:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-27T15:04:32.414992 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.11
# Thu, 27 Feb 2025 15:04:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 27 Feb 2025 15:04:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 15:04:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf212e0d8278f31a6cedad8e6d878dbbfaca1e5576d6cc007d50ab5eb4d149`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 31.5 MB (31471348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abdfaa1bd689c3b79a73edd7b200ca4dc06311284fb10b274b1d940aeb86bf0`  
		Last Modified: Mon, 03 Mar 2025 21:10:10 GMT  
		Size: 149.7 MB (149704720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98836c77271214a7e5984b796c4ca6960b9a05f24980f3d44b2a12bbbc5a6962`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129ed946cded32559147c893de019c8054a69bc05b7b594f381d9950752c73d`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fe5414d8768e6030cc5d6d0118b14863fa412d6b03919d9e1f778c8a2f21e0`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40f5cd554874b26262ace372738a38585008ea2d3ab9439abe40a733b9092a`  
		Last Modified: Mon, 03 Mar 2025 21:10:07 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118f75dee1103875fd39234e8b5337499466120b01dd870607e3d6955a71270`  
		Last Modified: Mon, 03 Mar 2025 21:10:07 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.11` - unknown; unknown

```console
$ docker pull crate@sha256:a014adbabbd3a1f6a86dd30cf8ea501d1982fa769fde7c48eb68ff8672cda064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d8d751a7483ae57e3d5879ae64c93d3a11957e106fe415de84366ddcb26dfa`

```dockerfile
```

-	Layers:
	-	`sha256:b02db13777337f30bd76aa1ade1758c7c7e1c64a7814670fac1f48fe3e963df7`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 5.2 MB (5150207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fedcf4e52b923cc8d7eaf8c728f620b427ebab01fc77b252cf428edab79cd4`  
		Last Modified: Mon, 03 Mar 2025 21:10:06 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:5512de3efc4321a9705ddc363edae5bfb028c5b5dc34a2d50fc6aa0eef03a83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:3e2f617b76d574dd1747534ce06ea1634bd40bb79893207dc3de45663de200fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249159175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48d7b3cb548514fdf798e5b82b0c2d2ab00669d2a73435cb26c3bf539ba503`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2122572b38204c69a5ee6fea31d16a5c543dff059ed1ea1eeb2d3527bd23e5f1`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 31.6 MB (31556971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250b59418d9b257b5e6d89f60f34c2972751848996920ca62751cb734adee3f`  
		Last Modified: Mon, 03 Mar 2025 21:07:18 GMT  
		Size: 149.7 MB (149652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619e33933e97e76c8db6119ce7e98f9b2fadaed8a7d9e9999e273dac426d886a`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a3e22501f970101a3f32a7e7494560ad554ccdf0eef61f133303509011bb8c`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb48f8153e2d3061b77448ad9ea90bf88fe70e5bdcc6e995db3525233f14a68`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4cfdd5097a0395be8f5b096a3f7ba88491fe1e51083ad0f2cd2ce7eb9d5e4a`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29625f6eecd8eeae4ee326a53536405b8ced93a1e4889b4c24b7ac950922de37`  
		Last Modified: Mon, 03 Mar 2025 21:07:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:fc67c32aa5b4a3660a28e2d53134b7c7c8d0f53c405ff39afcfaaf4425f45f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6cd87946b29b5b9b00bd75f3f072c59db43a7bcd6b2190672312634d1416c9`

```dockerfile
```

-	Layers:
	-	`sha256:e3623c2727f799d136aab49b05e15e341e16b25777d2d3180e6fb6e29da6fc79`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 5.2 MB (5155083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e628578550d141466d03ffdfc2df77239c502d9c914980832416c80aaddf0e03`  
		Last Modified: Mon, 03 Mar 2025 21:07:16 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6487449caa5d8b7de5734191b633bc6bb3c43ab68f2603822e7f137d918925e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248393514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ee8c3953a1c18b271eaf5d41009184c155216b45fafc67db57a44a9b6a46aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 11:37:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.2.tar.gz.asc crate-5.10.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.2.tar.gz.asc     && tar -xf crate-5.10.2.tar.gz -C /crate --strip-components=1     && rm crate-5.10.2.tar.gz # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 11:37:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 28 Feb 2025 11:37:51 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
VOLUME [/data]
# Fri, 28 Feb 2025 11:37:51 GMT
WORKDIR /data
# Fri, 28 Feb 2025 11:37:51 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-28T11:37:51.589079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.2
# Fri, 28 Feb 2025 11:37:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 28 Feb 2025 11:37:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2025 11:37:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf212e0d8278f31a6cedad8e6d878dbbfaca1e5576d6cc007d50ab5eb4d149`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 31.5 MB (31471348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f100132c5a2664ec59f6103255bc83d6db2d47f64092482209a82f56a502062f`  
		Last Modified: Mon, 03 Mar 2025 21:06:59 GMT  
		Size: 150.3 MB (150333818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec7e23e9af3bd4748577c67989d02487d52ebaef8239bcc2f9d3113f0c5261`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f4da468adea6ba9df6c13a6203706b61cc0d8ac5db20ef4ac77c7f21a38dcb`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428f78a33b077cb7b8b63ca5564e5473c54a99d3bbe7c593539b862015a77a6`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739ee82a3362143e76da6d07d0b49715268941f53ceae1e7900c17be42f0df3`  
		Last Modified: Mon, 03 Mar 2025 21:06:57 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ab8b9762a14a808d3cf55155f236ac53fcdab209fc18780cbb360dab5b4a2`  
		Last Modified: Mon, 03 Mar 2025 21:06:58 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:ae25cb13a400f96a6533733875bfc45b7544c166210adf3f36ac9cb0abbf7a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dada7153fec957e527eba573a7f5d71e22999f6f6ddb75be242f9f3e415c154`

```dockerfile
```

-	Layers:
	-	`sha256:275d351dcd18b836cb3d7520c276fb29d9506e412eb54847b50de5bc461d19c1`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 5.2 MB (5152391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00922077fb04571b58ba690f6e605cd25e56f75549f4012cb28e0e9479efa9a`  
		Last Modified: Mon, 03 Mar 2025 21:06:56 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
