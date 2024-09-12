<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.7`](#crate57)
-	[`crate:5.7.5`](#crate575)
-	[`crate:5.8`](#crate58)
-	[`crate:5.8.2`](#crate582)
-	[`crate:latest`](#cratelatest)

## `crate:5.7`

```console
$ docker pull crate@sha256:2261d36456c62f36e6409fe52a2958fd827f4d02e3f5c29f56047111dfe3790c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:d8f2b26528e5a2389e4e063755fdf2b88b74ba01d3a2445d65377502913b9dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209188125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5f34d3fc7fb31e2c762614066f63b5e4941cbd8b9f87d58f860eb3140f09c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 07:51:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.4.tar.gz.asc crate-5.7.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.4.tar.gz.asc     && tar -xf crate-5.7.4.tar.gz -C /crate --strip-components=1     && rm crate-5.7.4.tar.gz # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 07:51:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 26 Jul 2024 07:51:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
VOLUME [/data]
# Fri, 26 Jul 2024 07:51:44 GMT
WORKDIR /data
# Fri, 26 Jul 2024 07:51:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 26 Jul 2024 07:51:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-26T07:51:44.117532 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.4
# Fri, 26 Jul 2024 07:51:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 07:51:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc07f3fc0f5ab76d0eef4acdc5d46ec369c50a68ea9d17cf91247eee191e2186`  
		Last Modified: Mon, 29 Jul 2024 18:56:29 GMT  
		Size: 11.0 MB (10967458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f696bfbfde1420dc986aa7fc3bd7826ae85ad4d0773ddebd7de86cfb204f46f`  
		Last Modified: Mon, 29 Jul 2024 18:56:30 GMT  
		Size: 127.7 MB (127685896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e416b64660e8b040c0fcbd445df07e1fa0ab20fd7734e2a6efa96702692a2d`  
		Last Modified: Mon, 29 Jul 2024 18:56:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b16de96a13d836544331930b88f17241d3bc9f2614783a599c82a409042cc8`  
		Last Modified: Mon, 29 Jul 2024 18:56:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4d58c9d4ccd9b9bed6d543cfadf67c2b4d45749024d02f8612ea3076c44812`  
		Last Modified: Mon, 29 Jul 2024 18:56:29 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04475e3843c3f7e2fbc155591a25f52b3f882314bf98075b1348a62eb85f757`  
		Last Modified: Mon, 29 Jul 2024 18:56:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34001f19152a919674a673464a103c432eaad2033ec4559ff98c3ad5d58706`  
		Last Modified: Mon, 29 Jul 2024 18:56:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:43dae7b80ec9516836541ec00a56dd2a6e933778f3f6f6496030f157c7fc9aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5015316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc63a23452b8ea487746e2da0fb9f81ca1792461ea362a99fa01820411c7c1a`

```dockerfile
```

-	Layers:
	-	`sha256:b7bfc060b36f0c4f4c97ba0bcef249a16c4f485ff8953773149262a0e94eb7d3`  
		Last Modified: Mon, 29 Jul 2024 18:56:28 GMT  
		Size: 5.0 MB (4992228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8922179e72b8ec1a9c6ca96f57552ed3e2b3c8c5bae8290f289e9ac0185054`  
		Last Modified: Mon, 29 Jul 2024 18:56:28 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:82bcef9ee1e3ffa87eafda8a2158e38dabb91b30c1c8a6b7b58724cbf945b730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196671855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2818739b4a7797a8ec4ed9e1b43835eecba9a281cb542838eacaf3528c6e0bd8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 07:51:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.4.tar.gz.asc crate-5.7.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.4.tar.gz.asc     && tar -xf crate-5.7.4.tar.gz -C /crate --strip-components=1     && rm crate-5.7.4.tar.gz # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 07:51:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 26 Jul 2024 07:51:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
VOLUME [/data]
# Fri, 26 Jul 2024 07:51:44 GMT
WORKDIR /data
# Fri, 26 Jul 2024 07:51:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 26 Jul 2024 07:51:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-26T07:51:44.117532 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.4
# Fri, 26 Jul 2024 07:51:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 07:51:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 07:51:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b65453f3a6d5a9e154e45c80ebf228e6940e0950bcc9202980afe28bd552fc`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 17.7 KB (17698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e190259b7e6123c4cff0f6034a8397e53ad3d7b31495fcfa48bc020eb0de2c14`  
		Last Modified: Mon, 29 Jul 2024 18:56:14 GMT  
		Size: 127.2 MB (127205176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbf925818a4215db31647f9850350081e5e0338c746e18cbe1cf1b1fdb2e80`  
		Last Modified: Mon, 29 Jul 2024 18:56:11 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49318588277cff736232304b582ef4d3bff3f2e1d3adf7515555e31dcef93638`  
		Last Modified: Mon, 29 Jul 2024 18:56:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca04fde7870c6f6ae18ad5eddc54347189b30a3de0979ef4393efda8d25fa2ea`  
		Last Modified: Mon, 29 Jul 2024 18:56:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22a40c687f50061f3563680509c1cb8e0fa2650732535ab245e8015d34e9cd1`  
		Last Modified: Mon, 29 Jul 2024 18:56:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8d8a9eb80f1fc191d1e2153237023371e44d1158bb8f052e397af0330e0ebe`  
		Last Modified: Mon, 29 Jul 2024 18:56:11 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:af4977e599af358f8ab6bb85c22e517c75e3bc269f2673064152916a227d3be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730ab226aa5a45c39616bdacf206bc84ab0cdaa97c65bb6fb9e1a5f29ee1e4a5`

```dockerfile
```

-	Layers:
	-	`sha256:98693205061902d2b9f8531baf658872dfc039d8498391af70ae042d5a79692b`  
		Last Modified: Mon, 29 Jul 2024 18:56:11 GMT  
		Size: 5.0 MB (4990157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8664afb7ad95217223c1955332d4dd0bad346f577ebbe3386143eee61c59fb75`  
		Last Modified: Mon, 29 Jul 2024 18:56:10 GMT  
		Size: 23.4 KB (23437 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.5`

**does not exist** (yet?)

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

## `crate:5.8.2`

```console
$ docker pull crate@sha256:ab3c0f2aa656433ae354f6f0569a9597f0e6efea929091c023f6d49a21881c99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8.2` - linux; amd64

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

### `crate:5.8.2` - unknown; unknown

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

### `crate:5.8.2` - linux; arm64 variant v8

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

### `crate:5.8.2` - unknown; unknown

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
