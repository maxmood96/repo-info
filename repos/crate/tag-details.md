<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.5`](#crate55)
-	[`crate:5.5.4`](#crate554)
-	[`crate:5.5.5`](#crate555)
-	[`crate:5.6`](#crate56)
-	[`crate:5.6.5`](#crate565)
-	[`crate:5.7`](#crate57)
-	[`crate:5.7.3`](#crate573)
-	[`crate:latest`](#cratelatest)

## `crate:5.5`

```console
$ docker pull crate@sha256:b15deb8140a5a3ea31926fae5ebc7f5113ccf6590ceaeda00c174c36c940971f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:5e2f459d789a286aba7b3b01d64dd8128eb50435f4219731f74a0f6530585924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187316410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5579f68cb3dc326c972c76a81f4d69c6ddc0caa7fba689d11f9c01efea9fa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44c323ce9b92cf90d4698a141c0004ff5860bf1f5eae1f9b38d76a1e392f4b9`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 17.6 KB (17637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649b7e120dbb4b77c637c97aeba5345e561533c417539ef60712d31bdfc501a`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 116.8 MB (116768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebe7b013d44817fbb849765bb50f881e33afc664098fe42edbb928f1a0be27`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 1.9 MB (1939585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39e91b03ff6e70911238fd98c9840dd9ecbb3ddf3519627f6e0bb7c69355579`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4a478ef45cf6b024249987a140362ec38df5d8fa60a5ddb22bf2be5eff02e`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5b3670f8661da632ade69cbb2250c32cc8f7de2a1ffedacbace897358b8e85`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b074be2d83a2ca3c116cf60f2b96386d3740ef7b2692b4e9ea98676f118de9bc`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:7a1a141a137a84050a4e52d587f9b6c5d583fd0f47cb150c27f87eddd92acdc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd36a9d07a57b1b9d019a5e83d6cbb57d1221a4e9f082f8eed5dbf58cd01ac9`

```dockerfile
```

-	Layers:
	-	`sha256:0a7d5370f524f092d1415cb68e6b70ffea9a3effd1517a326b38f87a71e83d4c`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 4.9 MB (4949216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ed2455a81810b0658b8c86cb267e88bc8eedd6c38c783898cc9769afd50ab0`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 23.1 KB (23062 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:05109d17d8845344443081758afad2a1b399d70e733b76c03bc48cc4e0400794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185764950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2228ff5699c3757145db0fd5bd30f29d65334b9731ed0176ab9c6d2783f5d747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
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
	-	`sha256:d734c7a47293cefe26711aaad454da5e203082a99a294d1b1a8258685f569711`  
		Last Modified: Wed, 24 Jul 2024 16:33:37 GMT  
		Size: 116.3 MB (116302312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03254ef1b94b4468f3d63c1e7d5cb439d452947fcdb202617b8c503a62485a61`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac7d8cecafd6be328739f5ef2ab29a114b293c9dd49425d49ba8d396d5c50f`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea46f75facffcbbebd35b7d805977b297f77943ec17a3eb87e369c8aeb13746`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e66cfca4b07c088f6b31450cd67c02492f31074874a62a574b5d817cd3773e`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6762d13d918af911af0c43a82243051ba7b13e55fff9ad9f571eaa96970a90ba`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:a6e17ec7371ff3a4064960f5baf3eb1a3f32b7a21b8ecc6b312d5a44d26adf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a87f1a844d986a6ab047a0a58b9fc7333b9cdf1a4e8482972bf7b3fa71debe1`

```dockerfile
```

-	Layers:
	-	`sha256:c53c0a6fb0f53468a28c0295e29f021795534849491878c1072eec93455e21bc`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 4.9 MB (4947145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8cbc9a62523295245c1ce491c99f35eb658d3999b5a025321db639157f6a78`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.4`

```console
$ docker pull crate@sha256:b15deb8140a5a3ea31926fae5ebc7f5113ccf6590ceaeda00c174c36c940971f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:5e2f459d789a286aba7b3b01d64dd8128eb50435f4219731f74a0f6530585924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187316410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5579f68cb3dc326c972c76a81f4d69c6ddc0caa7fba689d11f9c01efea9fa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44c323ce9b92cf90d4698a141c0004ff5860bf1f5eae1f9b38d76a1e392f4b9`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 17.6 KB (17637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649b7e120dbb4b77c637c97aeba5345e561533c417539ef60712d31bdfc501a`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 116.8 MB (116768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebe7b013d44817fbb849765bb50f881e33afc664098fe42edbb928f1a0be27`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 1.9 MB (1939585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39e91b03ff6e70911238fd98c9840dd9ecbb3ddf3519627f6e0bb7c69355579`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4a478ef45cf6b024249987a140362ec38df5d8fa60a5ddb22bf2be5eff02e`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5b3670f8661da632ade69cbb2250c32cc8f7de2a1ffedacbace897358b8e85`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b074be2d83a2ca3c116cf60f2b96386d3740ef7b2692b4e9ea98676f118de9bc`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:7a1a141a137a84050a4e52d587f9b6c5d583fd0f47cb150c27f87eddd92acdc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd36a9d07a57b1b9d019a5e83d6cbb57d1221a4e9f082f8eed5dbf58cd01ac9`

```dockerfile
```

-	Layers:
	-	`sha256:0a7d5370f524f092d1415cb68e6b70ffea9a3effd1517a326b38f87a71e83d4c`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 4.9 MB (4949216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ed2455a81810b0658b8c86cb267e88bc8eedd6c38c783898cc9769afd50ab0`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 23.1 KB (23062 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:05109d17d8845344443081758afad2a1b399d70e733b76c03bc48cc4e0400794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185764950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2228ff5699c3757145db0fd5bd30f29d65334b9731ed0176ab9c6d2783f5d747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
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
	-	`sha256:d734c7a47293cefe26711aaad454da5e203082a99a294d1b1a8258685f569711`  
		Last Modified: Wed, 24 Jul 2024 16:33:37 GMT  
		Size: 116.3 MB (116302312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03254ef1b94b4468f3d63c1e7d5cb439d452947fcdb202617b8c503a62485a61`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac7d8cecafd6be328739f5ef2ab29a114b293c9dd49425d49ba8d396d5c50f`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea46f75facffcbbebd35b7d805977b297f77943ec17a3eb87e369c8aeb13746`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e66cfca4b07c088f6b31450cd67c02492f31074874a62a574b5d817cd3773e`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6762d13d918af911af0c43a82243051ba7b13e55fff9ad9f571eaa96970a90ba`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:a6e17ec7371ff3a4064960f5baf3eb1a3f32b7a21b8ecc6b312d5a44d26adf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a87f1a844d986a6ab047a0a58b9fc7333b9cdf1a4e8482972bf7b3fa71debe1`

```dockerfile
```

-	Layers:
	-	`sha256:c53c0a6fb0f53468a28c0295e29f021795534849491878c1072eec93455e21bc`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 4.9 MB (4947145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8cbc9a62523295245c1ce491c99f35eb658d3999b5a025321db639157f6a78`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.5`

```console
$ docker pull crate@sha256:b15deb8140a5a3ea31926fae5ebc7f5113ccf6590ceaeda00c174c36c940971f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:5e2f459d789a286aba7b3b01d64dd8128eb50435f4219731f74a0f6530585924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187316410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5579f68cb3dc326c972c76a81f4d69c6ddc0caa7fba689d11f9c01efea9fa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44c323ce9b92cf90d4698a141c0004ff5860bf1f5eae1f9b38d76a1e392f4b9`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 17.6 KB (17637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649b7e120dbb4b77c637c97aeba5345e561533c417539ef60712d31bdfc501a`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 116.8 MB (116768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebe7b013d44817fbb849765bb50f881e33afc664098fe42edbb928f1a0be27`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 1.9 MB (1939585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39e91b03ff6e70911238fd98c9840dd9ecbb3ddf3519627f6e0bb7c69355579`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4a478ef45cf6b024249987a140362ec38df5d8fa60a5ddb22bf2be5eff02e`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5b3670f8661da632ade69cbb2250c32cc8f7de2a1ffedacbace897358b8e85`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b074be2d83a2ca3c116cf60f2b96386d3740ef7b2692b4e9ea98676f118de9bc`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:7a1a141a137a84050a4e52d587f9b6c5d583fd0f47cb150c27f87eddd92acdc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd36a9d07a57b1b9d019a5e83d6cbb57d1221a4e9f082f8eed5dbf58cd01ac9`

```dockerfile
```

-	Layers:
	-	`sha256:0a7d5370f524f092d1415cb68e6b70ffea9a3effd1517a326b38f87a71e83d4c`  
		Last Modified: Tue, 23 Jul 2024 18:13:53 GMT  
		Size: 4.9 MB (4949216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ed2455a81810b0658b8c86cb267e88bc8eedd6c38c783898cc9769afd50ab0`  
		Last Modified: Tue, 23 Jul 2024 18:13:52 GMT  
		Size: 23.1 KB (23062 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:05109d17d8845344443081758afad2a1b399d70e733b76c03bc48cc4e0400794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185764950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2228ff5699c3757145db0fd5bd30f29d65334b9731ed0176ab9c6d2783f5d747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 18:39:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 18:39:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 18:39:32 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 18:39:32 GMT
WORKDIR /data
# Mon, 29 Jan 2024 18:39:32 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 29 Jan 2024 18:39:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 18:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 18:39:32 GMT
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
	-	`sha256:d734c7a47293cefe26711aaad454da5e203082a99a294d1b1a8258685f569711`  
		Last Modified: Wed, 24 Jul 2024 16:33:37 GMT  
		Size: 116.3 MB (116302312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03254ef1b94b4468f3d63c1e7d5cb439d452947fcdb202617b8c503a62485a61`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac7d8cecafd6be328739f5ef2ab29a114b293c9dd49425d49ba8d396d5c50f`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea46f75facffcbbebd35b7d805977b297f77943ec17a3eb87e369c8aeb13746`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e66cfca4b07c088f6b31450cd67c02492f31074874a62a574b5d817cd3773e`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6762d13d918af911af0c43a82243051ba7b13e55fff9ad9f571eaa96970a90ba`  
		Last Modified: Wed, 24 Jul 2024 16:33:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:a6e17ec7371ff3a4064960f5baf3eb1a3f32b7a21b8ecc6b312d5a44d26adf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a87f1a844d986a6ab047a0a58b9fc7333b9cdf1a4e8482972bf7b3fa71debe1`

```dockerfile
```

-	Layers:
	-	`sha256:c53c0a6fb0f53468a28c0295e29f021795534849491878c1072eec93455e21bc`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 4.9 MB (4947145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8cbc9a62523295245c1ce491c99f35eb658d3999b5a025321db639157f6a78`  
		Last Modified: Wed, 24 Jul 2024 16:33:34 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6`

```console
$ docker pull crate@sha256:cd93f2366487a8aa7954a375cab0e3ec9dc6b50a57a32deff051f5e76e38a641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:699974c5510ac40aaca3ab9b035f9a33d39f6162eeb4b52ffc958e05f155a742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188465566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a1c2b9592f8e64c9b90f30bf2784ef5daf82a62a285e5ff41b95563e9f53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 12:27:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 12:27:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 May 2024 12:27:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 May 2024 12:27:16 GMT
VOLUME [/data]
# Thu, 02 May 2024 12:27:16 GMT
WORKDIR /data
# Thu, 02 May 2024 12:27:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 May 2024 12:27:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 02 May 2024 12:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 12:27:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fc518319ed0d6b4634d143f0fecb77491438a83a0a84ebd9a0dcdc28b79fa`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 17.7 KB (17674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051ddce80e0a561054d2b9988c0b0c86ad3b2a007bf05c7e099afb3631ef9cd`  
		Last Modified: Tue, 23 Jul 2024 18:13:58 GMT  
		Size: 117.9 MB (117916119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554537e996b496b7cec5fde48a0d815ff05c9964c3510bdbb0afd06660e67df8`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 1.9 MB (1940633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7163958b4e4b3766252cb00d72d74f966bc11fac36cf85db508e7145c8bd0c`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ba1141317df4640a860d371cd5a87a2904254ea1ccac9ccfcd98ad0b083a8`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8afd2104abfe86359d7decf17db40101456caaaa45fad771fc4b30f9e940a`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa50509895613f8ccfba77c2f5fa7d201f434b5711dda44876e2189b7b3f38c`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:b7eec128cd98ff9152d34bf4b592b1bf2bb01bd59baf3b76c62a9dd362032269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101728fe914e185bdcbc6d00cfed758281f236fbdb7efb603e2c421b69551726`

```dockerfile
```

-	Layers:
	-	`sha256:c45b76f4d9e133f0263f4143402251c026c88843d70ab0152680edc677ce9616`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 4.9 MB (4948949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9372d78146a88eba9808bcf62f6c39af4733085d54edcd69d3ae18b0d884d99`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 22.8 KB (22767 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2f2226f05cd2f5607d7c297bc25635cbfada27c562df968f9d1fbae308d0989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197815608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8933c5e3d65274cdbab7fb19bb9b3dce1498396800af02f28458dc6b23efa73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 12:27:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 12:27:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 May 2024 12:27:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 May 2024 12:27:16 GMT
VOLUME [/data]
# Thu, 02 May 2024 12:27:16 GMT
WORKDIR /data
# Thu, 02 May 2024 12:27:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 May 2024 12:27:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 02 May 2024 12:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 12:27:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c147e32867f7ecf704c6d4ea1e98ec0418ec22a5719abba183fbe604e9a5fbc`  
		Last Modified: Thu, 27 Jun 2024 05:51:25 GMT  
		Size: 117.4 MB (117426632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae227b193d9e655491e494172db7f39244948b14fcdd790f3c419fb719b3fa`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6974e9beee1e6b359108ee8adcdc4f31b52b762b3226e63aff37339aa1925`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6729cab256dc7741d2ee1ecb23510335d68da7fe275affd2a81813a72d1fc`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d4582e3b169050999ed4db0a0a01f99ef62a51a564352c7bf7f5660e51afb`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcea5d9dc1273ae352e94632eeea1d3b0cabab2c88eb2e62efde1994ff167e1c`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:6977a21a32ee12ac7b5e36dc647da05451f849596393d8ed616bede821abd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1539afccbf63d331a2dd685b6ac3276994c6b41495664ba79b2eea90186216`

```dockerfile
```

-	Layers:
	-	`sha256:039948e1b38b873f6c28877fcf79806b5cf48249324066c2cf126df6694baa72`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 4.9 MB (4907599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c60cb2021b90a881173a65a90b6f90340430f560262d775c5e6fab338e3d8c4`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6.5`

```console
$ docker pull crate@sha256:cd93f2366487a8aa7954a375cab0e3ec9dc6b50a57a32deff051f5e76e38a641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:699974c5510ac40aaca3ab9b035f9a33d39f6162eeb4b52ffc958e05f155a742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188465566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a1c2b9592f8e64c9b90f30bf2784ef5daf82a62a285e5ff41b95563e9f53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 12:27:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 12:27:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 May 2024 12:27:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 May 2024 12:27:16 GMT
VOLUME [/data]
# Thu, 02 May 2024 12:27:16 GMT
WORKDIR /data
# Thu, 02 May 2024 12:27:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 May 2024 12:27:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 02 May 2024 12:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 12:27:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fc518319ed0d6b4634d143f0fecb77491438a83a0a84ebd9a0dcdc28b79fa`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 17.7 KB (17674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051ddce80e0a561054d2b9988c0b0c86ad3b2a007bf05c7e099afb3631ef9cd`  
		Last Modified: Tue, 23 Jul 2024 18:13:58 GMT  
		Size: 117.9 MB (117916119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554537e996b496b7cec5fde48a0d815ff05c9964c3510bdbb0afd06660e67df8`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 1.9 MB (1940633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7163958b4e4b3766252cb00d72d74f966bc11fac36cf85db508e7145c8bd0c`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ba1141317df4640a860d371cd5a87a2904254ea1ccac9ccfcd98ad0b083a8`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8afd2104abfe86359d7decf17db40101456caaaa45fad771fc4b30f9e940a`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa50509895613f8ccfba77c2f5fa7d201f434b5711dda44876e2189b7b3f38c`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:b7eec128cd98ff9152d34bf4b592b1bf2bb01bd59baf3b76c62a9dd362032269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101728fe914e185bdcbc6d00cfed758281f236fbdb7efb603e2c421b69551726`

```dockerfile
```

-	Layers:
	-	`sha256:c45b76f4d9e133f0263f4143402251c026c88843d70ab0152680edc677ce9616`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 4.9 MB (4948949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9372d78146a88eba9808bcf62f6c39af4733085d54edcd69d3ae18b0d884d99`  
		Last Modified: Tue, 23 Jul 2024 18:13:54 GMT  
		Size: 22.8 KB (22767 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2f2226f05cd2f5607d7c297bc25635cbfada27c562df968f9d1fbae308d0989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197815608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8933c5e3d65274cdbab7fb19bb9b3dce1498396800af02f28458dc6b23efa73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 12:27:16 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz # buildkit
# Thu, 02 May 2024 12:27:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 12:27:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 02 May 2024 12:27:16 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 02 May 2024 12:27:16 GMT
VOLUME [/data]
# Thu, 02 May 2024 12:27:16 GMT
WORKDIR /data
# Thu, 02 May 2024 12:27:16 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 02 May 2024 12:27:16 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 02 May 2024 12:27:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 02 May 2024 12:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 02 May 2024 12:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 12:27:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c147e32867f7ecf704c6d4ea1e98ec0418ec22a5719abba183fbe604e9a5fbc`  
		Last Modified: Thu, 27 Jun 2024 05:51:25 GMT  
		Size: 117.4 MB (117426632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae227b193d9e655491e494172db7f39244948b14fcdd790f3c419fb719b3fa`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6974e9beee1e6b359108ee8adcdc4f31b52b762b3226e63aff37339aa1925`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6729cab256dc7741d2ee1ecb23510335d68da7fe275affd2a81813a72d1fc`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d4582e3b169050999ed4db0a0a01f99ef62a51a564352c7bf7f5660e51afb`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcea5d9dc1273ae352e94632eeea1d3b0cabab2c88eb2e62efde1994ff167e1c`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:6977a21a32ee12ac7b5e36dc647da05451f849596393d8ed616bede821abd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1539afccbf63d331a2dd685b6ac3276994c6b41495664ba79b2eea90186216`

```dockerfile
```

-	Layers:
	-	`sha256:039948e1b38b873f6c28877fcf79806b5cf48249324066c2cf126df6694baa72`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 4.9 MB (4907599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c60cb2021b90a881173a65a90b6f90340430f560262d775c5e6fab338e3d8c4`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:03dea39e712207344ad6140eb41b80e3c45308d5481f0d705ed8c630181e0a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:e7bd41b2f35907ac4eff6f9000547514794ebc3031a9f7efb44f0f4ff4c03623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198201934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d02d94a2169e03eb50d192d0607ba87b16ddac5c62d3bf3e5137c8f5ebb858`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292528a5fb9d24fb81d28f0a1e92a3772ba0b057dd905a95ed718453229d2771`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1abd5273fb7fa9c45e23f27e7cb5d6c18bfa3cf8f8957aa22710ccb0d72cbd0`  
		Last Modified: Tue, 23 Jul 2024 18:13:41 GMT  
		Size: 127.6 MB (127649526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fda4d4d7da149288530257fba31f307d1496a9c315d3950a8b2f6fbae2d956`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0d3f3e4c6df2979d9c91bafd19eb2018bb2352a6998d68a534debac0dceb2`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa710ecd63d7ae07251756f1d2385e06c29897c14065d274329d6bb8d9acd`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc6ed209681a3fef927af1ff61981229265e2fc330f47ddb674e1a65f4efa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2eb6310e5c8710c691bbd5473714bfc004eeb26a2624dd6be7c4d26cee717`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:18e7cebb8aa7c5e9d36c187a332e9e5bf5edf93a1a6be832b73bd64d8fa44b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5015292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169e61c4f2b46d410e089aa9e39ad96ddf888f2197701d1bc0bcd0ad92abe2f6`

```dockerfile
```

-	Layers:
	-	`sha256:da1500427c08f41e3fd57bc6b65bf6b4eaa6ec0f67ee9750d9511234c960ba5c`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 5.0 MB (4992228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f8846511931e478b89a607f3175998086913589dc34b122175af579ddc0aa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aff25b90636105ff7b103d639f633d1c2d34d7233984e897ef623b9e249df55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196622215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24df1d7dceee6665a236e5905c319dd35ccff86a572f24b68ae4245a030b523`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
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
	-	`sha256:9c209f2a7f0784e86ac03d724a851481cfdec3e2becaaebe189d4de84fa5e529`  
		Last Modified: Wed, 24 Jul 2024 16:32:27 GMT  
		Size: 127.2 MB (127155534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896f01bd58d9a018fbccb654521850bb2c504030406b700b38d16ad952b2768`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8eb15e2b85292c168d6a153e3904c1cabb8addc1f16a4ffcacf303cfc3641f`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ac7312b2501f67b158ce48ca9a717b90a9130b9bf2f100920eb29951b7f02`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4aed19f298923c17355272d4158be5063f3fec84dbec82c62f784996bf156`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291f50ffe5dc2bbc0cbeb5526be5c6ae85e4be42f58723cf24b5e13b4bb318d`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:b37f7261e8922b5733087b392cb5043972e2cc20a626467252733481d4e291dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496360eca0f4bd578ddb5dfa3d9eb5b12b62f893b5965ec385f9d2f9fcddffc2`

```dockerfile
```

-	Layers:
	-	`sha256:f03eacb6ddc1175a9ffee49b977686f303ff41725499f43afc2822b228531115`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 5.0 MB (4990157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc26f883fd312a663b5cd93e8d5d4f3295596d2433d09aa9a1e8874e798efa`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.3`

```console
$ docker pull crate@sha256:03dea39e712207344ad6140eb41b80e3c45308d5481f0d705ed8c630181e0a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.3` - linux; amd64

```console
$ docker pull crate@sha256:e7bd41b2f35907ac4eff6f9000547514794ebc3031a9f7efb44f0f4ff4c03623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198201934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d02d94a2169e03eb50d192d0607ba87b16ddac5c62d3bf3e5137c8f5ebb858`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292528a5fb9d24fb81d28f0a1e92a3772ba0b057dd905a95ed718453229d2771`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1abd5273fb7fa9c45e23f27e7cb5d6c18bfa3cf8f8957aa22710ccb0d72cbd0`  
		Last Modified: Tue, 23 Jul 2024 18:13:41 GMT  
		Size: 127.6 MB (127649526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fda4d4d7da149288530257fba31f307d1496a9c315d3950a8b2f6fbae2d956`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0d3f3e4c6df2979d9c91bafd19eb2018bb2352a6998d68a534debac0dceb2`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa710ecd63d7ae07251756f1d2385e06c29897c14065d274329d6bb8d9acd`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc6ed209681a3fef927af1ff61981229265e2fc330f47ddb674e1a65f4efa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2eb6310e5c8710c691bbd5473714bfc004eeb26a2624dd6be7c4d26cee717`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.3` - unknown; unknown

```console
$ docker pull crate@sha256:18e7cebb8aa7c5e9d36c187a332e9e5bf5edf93a1a6be832b73bd64d8fa44b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5015292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169e61c4f2b46d410e089aa9e39ad96ddf888f2197701d1bc0bcd0ad92abe2f6`

```dockerfile
```

-	Layers:
	-	`sha256:da1500427c08f41e3fd57bc6b65bf6b4eaa6ec0f67ee9750d9511234c960ba5c`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 5.0 MB (4992228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f8846511931e478b89a607f3175998086913589dc34b122175af579ddc0aa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aff25b90636105ff7b103d639f633d1c2d34d7233984e897ef623b9e249df55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196622215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24df1d7dceee6665a236e5905c319dd35ccff86a572f24b68ae4245a030b523`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
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
	-	`sha256:9c209f2a7f0784e86ac03d724a851481cfdec3e2becaaebe189d4de84fa5e529`  
		Last Modified: Wed, 24 Jul 2024 16:32:27 GMT  
		Size: 127.2 MB (127155534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896f01bd58d9a018fbccb654521850bb2c504030406b700b38d16ad952b2768`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8eb15e2b85292c168d6a153e3904c1cabb8addc1f16a4ffcacf303cfc3641f`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ac7312b2501f67b158ce48ca9a717b90a9130b9bf2f100920eb29951b7f02`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4aed19f298923c17355272d4158be5063f3fec84dbec82c62f784996bf156`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291f50ffe5dc2bbc0cbeb5526be5c6ae85e4be42f58723cf24b5e13b4bb318d`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.3` - unknown; unknown

```console
$ docker pull crate@sha256:b37f7261e8922b5733087b392cb5043972e2cc20a626467252733481d4e291dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496360eca0f4bd578ddb5dfa3d9eb5b12b62f893b5965ec385f9d2f9fcddffc2`

```dockerfile
```

-	Layers:
	-	`sha256:f03eacb6ddc1175a9ffee49b977686f303ff41725499f43afc2822b228531115`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 5.0 MB (4990157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc26f883fd312a663b5cd93e8d5d4f3295596d2433d09aa9a1e8874e798efa`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:03dea39e712207344ad6140eb41b80e3c45308d5481f0d705ed8c630181e0a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e7bd41b2f35907ac4eff6f9000547514794ebc3031a9f7efb44f0f4ff4c03623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198201934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d02d94a2169e03eb50d192d0607ba87b16ddac5c62d3bf3e5137c8f5ebb858`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292528a5fb9d24fb81d28f0a1e92a3772ba0b057dd905a95ed718453229d2771`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1abd5273fb7fa9c45e23f27e7cb5d6c18bfa3cf8f8957aa22710ccb0d72cbd0`  
		Last Modified: Tue, 23 Jul 2024 18:13:41 GMT  
		Size: 127.6 MB (127649526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fda4d4d7da149288530257fba31f307d1496a9c315d3950a8b2f6fbae2d956`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0d3f3e4c6df2979d9c91bafd19eb2018bb2352a6998d68a534debac0dceb2`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa710ecd63d7ae07251756f1d2385e06c29897c14065d274329d6bb8d9acd`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc6ed209681a3fef927af1ff61981229265e2fc330f47ddb674e1a65f4efa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2eb6310e5c8710c691bbd5473714bfc004eeb26a2624dd6be7c4d26cee717`  
		Last Modified: Tue, 23 Jul 2024 18:13:40 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:18e7cebb8aa7c5e9d36c187a332e9e5bf5edf93a1a6be832b73bd64d8fa44b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5015292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169e61c4f2b46d410e089aa9e39ad96ddf888f2197701d1bc0bcd0ad92abe2f6`

```dockerfile
```

-	Layers:
	-	`sha256:da1500427c08f41e3fd57bc6b65bf6b4eaa6ec0f67ee9750d9511234c960ba5c`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 5.0 MB (4992228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f8846511931e478b89a607f3175998086913589dc34b122175af579ddc0aa8`  
		Last Modified: Tue, 23 Jul 2024 18:13:39 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:aff25b90636105ff7b103d639f633d1c2d34d7233984e897ef623b9e249df55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196622215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24df1d7dceee6665a236e5905c319dd35ccff86a572f24b68ae4245a030b523`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 10 Jul 2024 14:21:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
CMD ["/bin/bash"]
# Wed, 10 Jul 2024 14:21:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.3.tar.gz.asc crate-5.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.3.tar.gz.asc     && tar -xf crate-5.7.3.tar.gz -C /crate --strip-components=1     && rm crate-5.7.3.tar.gz # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 14:21:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 10 Jul 2024 14:21:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
VOLUME [/data]
# Wed, 10 Jul 2024 14:21:21 GMT
WORKDIR /data
# Wed, 10 Jul 2024 14:21:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-10T14:21:21.369800 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.3
# Wed, 10 Jul 2024 14:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Jul 2024 14:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jul 2024 14:21:21 GMT
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
	-	`sha256:9c209f2a7f0784e86ac03d724a851481cfdec3e2becaaebe189d4de84fa5e529`  
		Last Modified: Wed, 24 Jul 2024 16:32:27 GMT  
		Size: 127.2 MB (127155534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896f01bd58d9a018fbccb654521850bb2c504030406b700b38d16ad952b2768`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8eb15e2b85292c168d6a153e3904c1cabb8addc1f16a4ffcacf303cfc3641f`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ac7312b2501f67b158ce48ca9a717b90a9130b9bf2f100920eb29951b7f02`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4aed19f298923c17355272d4158be5063f3fec84dbec82c62f784996bf156`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1291f50ffe5dc2bbc0cbeb5526be5c6ae85e4be42f58723cf24b5e13b4bb318d`  
		Last Modified: Wed, 24 Jul 2024 16:32:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b37f7261e8922b5733087b392cb5043972e2cc20a626467252733481d4e291dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496360eca0f4bd578ddb5dfa3d9eb5b12b62f893b5965ec385f9d2f9fcddffc2`

```dockerfile
```

-	Layers:
	-	`sha256:f03eacb6ddc1175a9ffee49b977686f303ff41725499f43afc2822b228531115`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 5.0 MB (4990157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc26f883fd312a663b5cd93e8d5d4f3295596d2433d09aa9a1e8874e798efa`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 23.4 KB (23435 bytes)  
		MIME: application/vnd.in-toto+json
