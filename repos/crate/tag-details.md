<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.4`](#crate54)
-	[`crate:5.4.8`](#crate548)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.4`](#crate554)
-	[`crate:5.5.5`](#crate555)
-	[`crate:5.6`](#crate56)
-	[`crate:5.6.5`](#crate565)
-	[`crate:5.7`](#crate57)
-	[`crate:5.7.2`](#crate572)
-	[`crate:latest`](#cratelatest)

## `crate:5.4`

```console
$ docker pull crate@sha256:6294de85a3646706431c55baf84243af5ac702c853b3640d482614479d06cf9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:ff0d0b37f87fdddfbff441e7e2103c7250e3e2bca335f713a448a8d4aae8ad38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300104193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a0f94a0e3140735469d8ad54f2d1c4de14f5770e40c1b3cb0f4c3c09e3d476`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 17:48:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 17:48:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 17:48:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 17:48:09 GMT
WORKDIR /data
# Mon, 29 Jan 2024 17:48:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 29 Jan 2024 17:48:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983fe712a32d6626785ce081df64b142533bf70fd9424a212eb7e438cedeeb09`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38158d15d3f84a9f79a338ee7c05a8866886620455095a8111f6b1387069313`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 229.6 MB (229566926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88304503e965a69b6793e2fbcedae377df0316b3832b86929838d41a1303117e`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 1.9 MB (1939590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc9ab6a6a1c02603ad0ea5f15fc95dfb5713b52e8cc9300d09a2332e3220e84`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ab0263b0b935ce849c9a08e87763abf56100c0f52c071e151723b9f023b3a`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f666c496e27f9bffded1a89ac412bd83d05b8dfcb32acb62c8b1e38b7294bbd`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3361efcd650e796ef99dac91bfbc36c6970ad31ebcc393e2db29d98ea011a`  
		Last Modified: Fri, 21 Jun 2024 01:03:26 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4` - unknown; unknown

```console
$ docker pull crate@sha256:ed2c3a8dfbc5b19a3dba18d51a6727bafc4275769ee600f2622c6a896feecbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3517c9d48f70e255670b353040158019f3e17fae80c04a274cb3b06e5e42b6`

```dockerfile
```

-	Layers:
	-	`sha256:343321a606fed522ce0deded11f70a3ab5563328698ab61e61f367e640ce509e`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 4.9 MB (4906445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5af403c31131fb4ae81ca2d1b9e571452f5184f5b1f40c86945a2d61a62369f`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6c9b7895617d0424415799dcb50f9c99acfd121bd751a9fba791381986641fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297346447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653536eab918527beb4cd5d94519a9acc6268edafc327b87a2e2e88f6ae5086f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 17:48:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 17:48:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 17:48:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 17:48:09 GMT
WORKDIR /data
# Mon, 29 Jan 2024 17:48:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 29 Jan 2024 17:48:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6197b7d94066d9434963e5d862459d95fc96e465759d5974476e628bb6784f96`  
		Last Modified: Fri, 21 Jun 2024 07:15:53 GMT  
		Size: 227.9 MB (227888369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebdd398c5f62408e07fd1b4503e918957aae716fdf3c012f97bab1a67d253c`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 1.9 MB (1939586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d6e6d954fc425734a6a7e5ade0d7ea05cff9ea2480bcde86dd24ed5ab51ec`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5b7f8a5e79d509effe21136be1608abb8e06dca996870c58903464f73a1e1`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3c6240b70ba1e90b760be6f0aba3b7470870ffee6f68c58481a0ad09a952ff`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fc2cd5c71d584d12610118e8bee099663cf206c003eefdbf9b3a63b661341`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4` - unknown; unknown

```console
$ docker pull crate@sha256:9deaf5ce0827b672c6d8cb1c7cb1368c5e67f88b6593bb5f979137bab4a4222c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d6c2a3654a7de137e89190a343cf8d6ead2f519c7ec4f9c0dc6d398e95cf3`

```dockerfile
```

-	Layers:
	-	`sha256:43bcb2cb5ee6980e0d9b1aa1842a62ce75fcebf8ebebea818c5ab9e606dd4978`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 4.9 MB (4904362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3c68611bcffdfc437084ad5b0ac94a373b6718806feda36b63e14f371078f8`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.4.8`

```console
$ docker pull crate@sha256:6294de85a3646706431c55baf84243af5ac702c853b3640d482614479d06cf9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:ff0d0b37f87fdddfbff441e7e2103c7250e3e2bca335f713a448a8d4aae8ad38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300104193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a0f94a0e3140735469d8ad54f2d1c4de14f5770e40c1b3cb0f4c3c09e3d476`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 17:48:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 17:48:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 17:48:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 17:48:09 GMT
WORKDIR /data
# Mon, 29 Jan 2024 17:48:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 29 Jan 2024 17:48:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983fe712a32d6626785ce081df64b142533bf70fd9424a212eb7e438cedeeb09`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38158d15d3f84a9f79a338ee7c05a8866886620455095a8111f6b1387069313`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 229.6 MB (229566926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88304503e965a69b6793e2fbcedae377df0316b3832b86929838d41a1303117e`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 1.9 MB (1939590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc9ab6a6a1c02603ad0ea5f15fc95dfb5713b52e8cc9300d09a2332e3220e84`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ab0263b0b935ce849c9a08e87763abf56100c0f52c071e151723b9f023b3a`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f666c496e27f9bffded1a89ac412bd83d05b8dfcb32acb62c8b1e38b7294bbd`  
		Last Modified: Fri, 21 Jun 2024 01:03:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e3361efcd650e796ef99dac91bfbc36c6970ad31ebcc393e2db29d98ea011a`  
		Last Modified: Fri, 21 Jun 2024 01:03:26 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4.8` - unknown; unknown

```console
$ docker pull crate@sha256:ed2c3a8dfbc5b19a3dba18d51a6727bafc4275769ee600f2622c6a896feecbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3517c9d48f70e255670b353040158019f3e17fae80c04a274cb3b06e5e42b6`

```dockerfile
```

-	Layers:
	-	`sha256:343321a606fed522ce0deded11f70a3ab5563328698ab61e61f367e640ce509e`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 4.9 MB (4906445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5af403c31131fb4ae81ca2d1b9e571452f5184f5b1f40c86945a2d61a62369f`  
		Last Modified: Fri, 21 Jun 2024 01:03:24 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6c9b7895617d0424415799dcb50f9c99acfd121bd751a9fba791381986641fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297346447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653536eab918527beb4cd5d94519a9acc6268edafc327b87a2e2e88f6ae5086f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 17:48:09 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 17:48:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 29 Jan 2024 17:48:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
VOLUME [/data]
# Mon, 29 Jan 2024 17:48:09 GMT
WORKDIR /data
# Mon, 29 Jan 2024 17:48:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 29 Jan 2024 17:48:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Jan 2024 17:48:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Jan 2024 17:48:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6197b7d94066d9434963e5d862459d95fc96e465759d5974476e628bb6784f96`  
		Last Modified: Fri, 21 Jun 2024 07:15:53 GMT  
		Size: 227.9 MB (227888369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebdd398c5f62408e07fd1b4503e918957aae716fdf3c012f97bab1a67d253c`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 1.9 MB (1939586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d6e6d954fc425734a6a7e5ade0d7ea05cff9ea2480bcde86dd24ed5ab51ec`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5b7f8a5e79d509effe21136be1608abb8e06dca996870c58903464f73a1e1`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3c6240b70ba1e90b760be6f0aba3b7470870ffee6f68c58481a0ad09a952ff`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fc2cd5c71d584d12610118e8bee099663cf206c003eefdbf9b3a63b661341`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4.8` - unknown; unknown

```console
$ docker pull crate@sha256:9deaf5ce0827b672c6d8cb1c7cb1368c5e67f88b6593bb5f979137bab4a4222c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d6c2a3654a7de137e89190a343cf8d6ead2f519c7ec4f9c0dc6d398e95cf3`

```dockerfile
```

-	Layers:
	-	`sha256:43bcb2cb5ee6980e0d9b1aa1842a62ce75fcebf8ebebea818c5ab9e606dd4978`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 4.9 MB (4904362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3c68611bcffdfc437084ad5b0ac94a373b6718806feda36b63e14f371078f8`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5`

```console
$ docker pull crate@sha256:8448bc153124d1ef42018c6c8132c83361d64b68d67dd89ef9101cdf0cd68388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:76e0ab5927522b4236f1c5ca1cde83b1c00d2da61116c4d734f466c4930c4061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187305361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4a7ffc3b03979bf6e968c708a43156bc88f3ef17f80cb0acc730e231b5c91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
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
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3bef5ab60f2604a3bbfc7c672841461a8df8be5b794414c3261031c3e18423`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d80520282580445c31bd3c7e3b47caccdedeacd3d3901bdb3f4f885e25a75b`  
		Last Modified: Fri, 21 Jun 2024 01:02:56 GMT  
		Size: 116.8 MB (116768093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6cb95b7d42bd4124030a50f9f11c4fec801de594daec467789c96182cb05d`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781f08f624fe748e947f6e60de0a0bf6e1fda30c9edd04ce00408f1b33f094e0`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e5b35fe2a8a7abc626a4e014fe0e454acebce6aef79d55148787f86399dec1`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11a982858577e27c22275d8b425084e3fb47eac448131a0cef83e2b4d98ae6`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782355a7d5768cc676f43e7e203594d094dbaf064020f5fc11d5626106e548ac`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:60e198c3e27218c8dc744f518fe4836aa5302e2ae7e0599d273d143a609db199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9c04d02a42f0212a7f66cb946a3e2d61fcea6aa865d50e28b0f88b61bcef38`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f99304d723b2666c1dcdb17cd5920ad0125bd878b95e795fb73a41de9585a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4909925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f896220d64b7fb37b3fc9016d7ab09f18c89a414fcd77f8312917c3dea2eaaf8`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.4`

```console
$ docker pull crate@sha256:8448bc153124d1ef42018c6c8132c83361d64b68d67dd89ef9101cdf0cd68388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:76e0ab5927522b4236f1c5ca1cde83b1c00d2da61116c4d734f466c4930c4061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187305361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4a7ffc3b03979bf6e968c708a43156bc88f3ef17f80cb0acc730e231b5c91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
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
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3bef5ab60f2604a3bbfc7c672841461a8df8be5b794414c3261031c3e18423`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d80520282580445c31bd3c7e3b47caccdedeacd3d3901bdb3f4f885e25a75b`  
		Last Modified: Fri, 21 Jun 2024 01:02:56 GMT  
		Size: 116.8 MB (116768093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6cb95b7d42bd4124030a50f9f11c4fec801de594daec467789c96182cb05d`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781f08f624fe748e947f6e60de0a0bf6e1fda30c9edd04ce00408f1b33f094e0`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e5b35fe2a8a7abc626a4e014fe0e454acebce6aef79d55148787f86399dec1`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11a982858577e27c22275d8b425084e3fb47eac448131a0cef83e2b4d98ae6`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782355a7d5768cc676f43e7e203594d094dbaf064020f5fc11d5626106e548ac`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:60e198c3e27218c8dc744f518fe4836aa5302e2ae7e0599d273d143a609db199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9c04d02a42f0212a7f66cb946a3e2d61fcea6aa865d50e28b0f88b61bcef38`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f99304d723b2666c1dcdb17cd5920ad0125bd878b95e795fb73a41de9585a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4909925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f896220d64b7fb37b3fc9016d7ab09f18c89a414fcd77f8312917c3dea2eaaf8`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.5`

```console
$ docker pull crate@sha256:8448bc153124d1ef42018c6c8132c83361d64b68d67dd89ef9101cdf0cd68388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:76e0ab5927522b4236f1c5ca1cde83b1c00d2da61116c4d734f466c4930c4061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187305361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4a7ffc3b03979bf6e968c708a43156bc88f3ef17f80cb0acc730e231b5c91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
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
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3bef5ab60f2604a3bbfc7c672841461a8df8be5b794414c3261031c3e18423`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d80520282580445c31bd3c7e3b47caccdedeacd3d3901bdb3f4f885e25a75b`  
		Last Modified: Fri, 21 Jun 2024 01:02:56 GMT  
		Size: 116.8 MB (116768093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6cb95b7d42bd4124030a50f9f11c4fec801de594daec467789c96182cb05d`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781f08f624fe748e947f6e60de0a0bf6e1fda30c9edd04ce00408f1b33f094e0`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e5b35fe2a8a7abc626a4e014fe0e454acebce6aef79d55148787f86399dec1`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11a982858577e27c22275d8b425084e3fb47eac448131a0cef83e2b4d98ae6`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782355a7d5768cc676f43e7e203594d094dbaf064020f5fc11d5626106e548ac`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:60e198c3e27218c8dc744f518fe4836aa5302e2ae7e0599d273d143a609db199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9c04d02a42f0212a7f66cb946a3e2d61fcea6aa865d50e28b0f88b61bcef38`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f99304d723b2666c1dcdb17cd5920ad0125bd878b95e795fb73a41de9585a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4909925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f896220d64b7fb37b3fc9016d7ab09f18c89a414fcd77f8312917c3dea2eaaf8`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6`

```console
$ docker pull crate@sha256:099081f4af08c8fcfab2480bab3b6c9550ac4f99b07d396265aa90eadf3248a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:aa10313e7b9dd492cb120426b5ba85d3d4e88eb139f70a461416494e75c4f986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188454537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98762b9d189f40da0d05d6b16cde82218ceea23a6bee6a5494f5d661bd86ea47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
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
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad152cf6ec9b6817d247c50dc89c5e43b4a4bd6dbad61cad2670ad4bc71381`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 17.6 KB (17612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1df3f1e111d4332ff5630692c064f20f490c9ef36afed0cdb6ce5dba59fd061`  
		Last Modified: Fri, 21 Jun 2024 01:03:15 GMT  
		Size: 117.9 MB (117916227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac39f9b461f0830a28886a8079115cfbc60a083e302612234885a176f561066`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 1.9 MB (1940636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39807056d681733b95572024287e5ba551d7a746a13d3f36a9451ffda34dc7`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e09da796b522d502287aac8690382d1068a775f1f5ddf966d13c2932be5ae5`  
		Last Modified: Fri, 21 Jun 2024 01:03:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89064cf381dbce48df4a302a05ca1a3e78f987950580753f760d607efc78331`  
		Last Modified: Fri, 21 Jun 2024 01:03:13 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4dc8dc6feb93b671d3c1ec9f2d4d7e5a049fbee2bdd9d5d061b13163c7c55e`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:1859b50ae8ea18c72bf68f9e6ac1f1672c8ffd4cea4f3019ca39c7368a354857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a68a747aa6edf80ab6df7255f0bac601af292d87bf7b02861ac3e83dfa1bce`

```dockerfile
```

-	Layers:
	-	`sha256:e941a600db96c7aec114c8653f314ff0b455b08558e10122e1767230412df483`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.9 MB (4909658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acb2ee03b08316ec0198d2a02bdeca5083ad10af03cf75c8b17330507f977b3`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ca7b0adc7a9ae7675625ebb5157bd9f6a932777586586ffd1907d0a8d0690629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186885776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b306af9b11b2a4ca8d8d5ae70fa01314022fc4e83fde59eea6aeabbb2278bbb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497854d6ecf796d164cfd72f6ab25d5b8b87510a455668c71a02ef8fd3a5cfe7`  
		Last Modified: Fri, 21 Jun 2024 07:13:58 GMT  
		Size: 117.4 MB (117426650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54deb0e70b569452bdb4ca1236e0941d6ca005271583d14634acafca167f0f`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebf456af4786a8ba19e6bc2963d4901233960c2ddd0e2c46735adf326a8e69`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64152a91245b85b9f7b92f8f0198b673c8ebcba1dfd5cd69b8676f01044d026`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73300b322cf7777ec0ddac485e316de893cbf556dce957035a653e252769c93c`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff357aeb7705f9e10a6a29e1b040f766f73c3674011ce52037c045efa1d7bc94`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:000c64b9eb1b47b9b6e252db978882e14302329ff4dfbb368ed36e2c785841d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c19ae11b4e13629837b9ad93fbd716e851f669aa597bf40f4db463ad16da40`

```dockerfile
```

-	Layers:
	-	`sha256:a3914984236a06cc63c6b2936b14b462c4e11f145d69045eadd3d767fbe0f6ec`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826c98aa6ee51897a4efb972d746fa82c9847539c5e99220c199429bc8e4caf1`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6.5`

```console
$ docker pull crate@sha256:099081f4af08c8fcfab2480bab3b6c9550ac4f99b07d396265aa90eadf3248a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:aa10313e7b9dd492cb120426b5ba85d3d4e88eb139f70a461416494e75c4f986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188454537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98762b9d189f40da0d05d6b16cde82218ceea23a6bee6a5494f5d661bd86ea47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
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
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad152cf6ec9b6817d247c50dc89c5e43b4a4bd6dbad61cad2670ad4bc71381`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 17.6 KB (17612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1df3f1e111d4332ff5630692c064f20f490c9ef36afed0cdb6ce5dba59fd061`  
		Last Modified: Fri, 21 Jun 2024 01:03:15 GMT  
		Size: 117.9 MB (117916227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac39f9b461f0830a28886a8079115cfbc60a083e302612234885a176f561066`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 1.9 MB (1940636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39807056d681733b95572024287e5ba551d7a746a13d3f36a9451ffda34dc7`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e09da796b522d502287aac8690382d1068a775f1f5ddf966d13c2932be5ae5`  
		Last Modified: Fri, 21 Jun 2024 01:03:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89064cf381dbce48df4a302a05ca1a3e78f987950580753f760d607efc78331`  
		Last Modified: Fri, 21 Jun 2024 01:03:13 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4dc8dc6feb93b671d3c1ec9f2d4d7e5a049fbee2bdd9d5d061b13163c7c55e`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:1859b50ae8ea18c72bf68f9e6ac1f1672c8ffd4cea4f3019ca39c7368a354857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a68a747aa6edf80ab6df7255f0bac601af292d87bf7b02861ac3e83dfa1bce`

```dockerfile
```

-	Layers:
	-	`sha256:e941a600db96c7aec114c8653f314ff0b455b08558e10122e1767230412df483`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.9 MB (4909658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acb2ee03b08316ec0198d2a02bdeca5083ad10af03cf75c8b17330507f977b3`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ca7b0adc7a9ae7675625ebb5157bd9f6a932777586586ffd1907d0a8d0690629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186885776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b306af9b11b2a4ca8d8d5ae70fa01314022fc4e83fde59eea6aeabbb2278bbb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497854d6ecf796d164cfd72f6ab25d5b8b87510a455668c71a02ef8fd3a5cfe7`  
		Last Modified: Fri, 21 Jun 2024 07:13:58 GMT  
		Size: 117.4 MB (117426650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54deb0e70b569452bdb4ca1236e0941d6ca005271583d14634acafca167f0f`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebf456af4786a8ba19e6bc2963d4901233960c2ddd0e2c46735adf326a8e69`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64152a91245b85b9f7b92f8f0198b673c8ebcba1dfd5cd69b8676f01044d026`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73300b322cf7777ec0ddac485e316de893cbf556dce957035a653e252769c93c`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff357aeb7705f9e10a6a29e1b040f766f73c3674011ce52037c045efa1d7bc94`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:000c64b9eb1b47b9b6e252db978882e14302329ff4dfbb368ed36e2c785841d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c19ae11b4e13629837b9ad93fbd716e851f669aa597bf40f4db463ad16da40`

```dockerfile
```

-	Layers:
	-	`sha256:a3914984236a06cc63c6b2936b14b462c4e11f145d69045eadd3d767fbe0f6ec`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826c98aa6ee51897a4efb972d746fa82c9847539c5e99220c199429bc8e4caf1`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:40bbe28ea61c0374ebc24893a7ff40481ce6829bfb71e7557d7bea2a6efcc343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:c9e395861f0a229f26fa2826faa2832fd0d22fc2106d6482f877a5c32412df80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198189181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bb2770ca008a01438afd621ad1b9d2b8f01d55722b10d30b7f65d59ef7be03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f282573885649262fb9b4e0b6c346329ea4892e45f55f7a903728bccda1ad69`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c6ef00641b72c8b0ba8e11e671739fd4de83c992dacabc7a2215c2601d8148`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 127.6 MB (127647869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdefdb0f0bc3944bd0746bd7c5f979f71e15f119ef1644615ee1c62ee3f79a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca655399a56fd4ceed0e2e0c79fe2872f1199d2d12af6f721d50a90011166c71`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614aaae0c614008391cdb5e00fa4ce6588f5f40a931faa94c4127481a3695699`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ed697249cd2fd2c2cfe9244283ce72e7f6529ef3629317df21ff8c968cacc`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc07682a755e8fffd2a00ee15c9e84098d6505c3c641455b3e43d31980100ce`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:b6044da2e80947ef83e55f3a8842a3348623ef869654c486ec33ed5d76337847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97beef97edc7cb022ecc82873a952ace090859cf2f08b79d5ebf95ef3c716cc9`

```dockerfile
```

-	Layers:
	-	`sha256:25b17f4a39298d3085a6860b1f9667c5f133f39fd1ce8485c619eaf27254f885`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4947789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67e01d8f2b2222864e81ce69baaaeac78fc6afe597b5cc8e033d281f2c4ebb0`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22895 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.2`

```console
$ docker pull crate@sha256:40bbe28ea61c0374ebc24893a7ff40481ce6829bfb71e7557d7bea2a6efcc343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.2` - linux; amd64

```console
$ docker pull crate@sha256:c9e395861f0a229f26fa2826faa2832fd0d22fc2106d6482f877a5c32412df80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198189181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bb2770ca008a01438afd621ad1b9d2b8f01d55722b10d30b7f65d59ef7be03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f282573885649262fb9b4e0b6c346329ea4892e45f55f7a903728bccda1ad69`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c6ef00641b72c8b0ba8e11e671739fd4de83c992dacabc7a2215c2601d8148`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 127.6 MB (127647869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdefdb0f0bc3944bd0746bd7c5f979f71e15f119ef1644615ee1c62ee3f79a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca655399a56fd4ceed0e2e0c79fe2872f1199d2d12af6f721d50a90011166c71`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614aaae0c614008391cdb5e00fa4ce6588f5f40a931faa94c4127481a3695699`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ed697249cd2fd2c2cfe9244283ce72e7f6529ef3629317df21ff8c968cacc`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc07682a755e8fffd2a00ee15c9e84098d6505c3c641455b3e43d31980100ce`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.2` - unknown; unknown

```console
$ docker pull crate@sha256:b6044da2e80947ef83e55f3a8842a3348623ef869654c486ec33ed5d76337847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97beef97edc7cb022ecc82873a952ace090859cf2f08b79d5ebf95ef3c716cc9`

```dockerfile
```

-	Layers:
	-	`sha256:25b17f4a39298d3085a6860b1f9667c5f133f39fd1ce8485c619eaf27254f885`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4947789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67e01d8f2b2222864e81ce69baaaeac78fc6afe597b5cc8e033d281f2c4ebb0`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22895 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.2` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:40bbe28ea61c0374ebc24893a7ff40481ce6829bfb71e7557d7bea2a6efcc343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:c9e395861f0a229f26fa2826faa2832fd0d22fc2106d6482f877a5c32412df80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198189181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bb2770ca008a01438afd621ad1b9d2b8f01d55722b10d30b7f65d59ef7be03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f282573885649262fb9b4e0b6c346329ea4892e45f55f7a903728bccda1ad69`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c6ef00641b72c8b0ba8e11e671739fd4de83c992dacabc7a2215c2601d8148`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 127.6 MB (127647869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdefdb0f0bc3944bd0746bd7c5f979f71e15f119ef1644615ee1c62ee3f79a`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca655399a56fd4ceed0e2e0c79fe2872f1199d2d12af6f721d50a90011166c71`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614aaae0c614008391cdb5e00fa4ce6588f5f40a931faa94c4127481a3695699`  
		Last Modified: Fri, 21 Jun 2024 01:02:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ed697249cd2fd2c2cfe9244283ce72e7f6529ef3629317df21ff8c968cacc`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc07682a755e8fffd2a00ee15c9e84098d6505c3c641455b3e43d31980100ce`  
		Last Modified: Fri, 21 Jun 2024 01:02:55 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b6044da2e80947ef83e55f3a8842a3348623ef869654c486ec33ed5d76337847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97beef97edc7cb022ecc82873a952ace090859cf2f08b79d5ebf95ef3c716cc9`

```dockerfile
```

-	Layers:
	-	`sha256:25b17f4a39298d3085a6860b1f9667c5f133f39fd1ce8485c619eaf27254f885`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 4.9 MB (4947789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67e01d8f2b2222864e81ce69baaaeac78fc6afe597b5cc8e033d281f2c4ebb0`  
		Last Modified: Fri, 21 Jun 2024 01:02:53 GMT  
		Size: 22.9 KB (22895 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 14:05:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 14:05:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Jun 2024 14:05:02 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
VOLUME [/data]
# Wed, 12 Jun 2024 14:05:02 GMT
WORKDIR /data
# Wed, 12 Jun 2024 14:05:02 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Wed, 12 Jun 2024 14:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 14:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 14:05:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json
