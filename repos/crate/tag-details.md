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
$ docker pull crate@sha256:7fa87317733575b796ef0896d0507adeec916d3a8ca6f4885e0cb1c256f869ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:35031e812994186924463c9e959e2fbf806e507453d6e0ee36fd3f1a19a324f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297752208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5cae1c023b51573ef5d0e93d93208c3e0e83a6a0de1dec1f96f138eb10f8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:49:53 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:53 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:53 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:53 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:53 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:53 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:53 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:49:54 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf636b5c8162cd8fd6b069dac68f24b7d61292ac58898180f0077cf7f7fddb`  
		Last Modified: Thu, 30 May 2024 20:51:25 GMT  
		Size: 227.9 MB (227888420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ecc3ac145619784c69d92d47a988fc8f49e365e9e9e79a92ab337e87bbbb43`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 1.9 MB (1939612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081a3f2a8dfe4289368272ad96fa21a491e719600aead0c0c20867efc1fc938`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46329c8169bfa356ac1be46c6e376349c5f70f7203c85ba6ea5d76cf0177323`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85daad9bfee4be0793638b05eae7bd3ea6e2afb1a92118f81c48ef01b788de49`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe53944723f0059ac353184ef1c887e6c4175134d96b7b375ec64b17c6c012`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:7fa87317733575b796ef0896d0507adeec916d3a8ca6f4885e0cb1c256f869ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:35031e812994186924463c9e959e2fbf806e507453d6e0ee36fd3f1a19a324f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297752208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5cae1c023b51573ef5d0e93d93208c3e0e83a6a0de1dec1f96f138eb10f8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:49:53 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:53 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:53 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:53 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:53 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:53 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:53 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:49:54 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf636b5c8162cd8fd6b069dac68f24b7d61292ac58898180f0077cf7f7fddb`  
		Last Modified: Thu, 30 May 2024 20:51:25 GMT  
		Size: 227.9 MB (227888420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ecc3ac145619784c69d92d47a988fc8f49e365e9e9e79a92ab337e87bbbb43`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 1.9 MB (1939612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081a3f2a8dfe4289368272ad96fa21a491e719600aead0c0c20867efc1fc938`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46329c8169bfa356ac1be46c6e376349c5f70f7203c85ba6ea5d76cf0177323`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85daad9bfee4be0793638b05eae7bd3ea6e2afb1a92118f81c48ef01b788de49`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe53944723f0059ac353184ef1c887e6c4175134d96b7b375ec64b17c6c012`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:d96cf2e7fb8f68eb1aa4a1054df8d23d6c28588789943f789285eebec8409e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.4`

```console
$ docker pull crate@sha256:d96cf2e7fb8f68eb1aa4a1054df8d23d6c28588789943f789285eebec8409e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:d96cf2e7fb8f68eb1aa4a1054df8d23d6c28588789943f789285eebec8409e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:222b7b7f9508df0d55bc84dc36c888fdf83edbf0cfe647aa3fa40da566068eb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:6a27f74dfc318043ccf8b02390511a884f6a6902f6bb84b3ae0d4db06b5a17e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187291851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059addbbe35ba3a6d4573c5b45c22262a5d1dc40acbac0720e04fa1a76c4a021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:01 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:49:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:04 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:04 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:04 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:04 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:49:05 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c499c532cbb6ff39a98b87d56d1d02b62c24b51a4be7d41440f680706a378f`  
		Last Modified: Thu, 30 May 2024 20:50:41 GMT  
		Size: 117.4 MB (117427024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666298ed1cdec8c65865b36765d1c5972876c94f9c09b84955d3ee0413c0ea3e`  
		Last Modified: Thu, 30 May 2024 20:50:32 GMT  
		Size: 1.9 MB (1940644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e2649e57debc1e956c9b4ac0dc744e19f2ae8844ac94f4d87221f7b4924d5`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2e644ce4d5a8be47aac40902d62b049fde4b4de32d153a24d29f5b97da75f4`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2c11b626940e12fee215ef74940a4545917633e8c7ed40ee5352afba8dc69a`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b0bc1cab79db268163c990f48396f90222d15cf81c5f2ad84a59bd2d17dc49`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.5`

```console
$ docker pull crate@sha256:222b7b7f9508df0d55bc84dc36c888fdf83edbf0cfe647aa3fa40da566068eb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:6a27f74dfc318043ccf8b02390511a884f6a6902f6bb84b3ae0d4db06b5a17e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187291851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059addbbe35ba3a6d4573c5b45c22262a5d1dc40acbac0720e04fa1a76c4a021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:01 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:49:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:04 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:04 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:04 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:04 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:49:05 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c499c532cbb6ff39a98b87d56d1d02b62c24b51a4be7d41440f680706a378f`  
		Last Modified: Thu, 30 May 2024 20:50:41 GMT  
		Size: 117.4 MB (117427024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666298ed1cdec8c65865b36765d1c5972876c94f9c09b84955d3ee0413c0ea3e`  
		Last Modified: Thu, 30 May 2024 20:50:32 GMT  
		Size: 1.9 MB (1940644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e2649e57debc1e956c9b4ac0dc744e19f2ae8844ac94f4d87221f7b4924d5`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2e644ce4d5a8be47aac40902d62b049fde4b4de32d153a24d29f5b97da75f4`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2c11b626940e12fee215ef74940a4545917633e8c7ed40ee5352afba8dc69a`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b0bc1cab79db268163c990f48396f90222d15cf81c5f2ad84a59bd2d17dc49`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7`

```console
$ docker pull crate@sha256:3e1a66879ec02ebf24ae4a9e189da7184e5d0d6839fc031cf1e6b936a3d436cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:18baddfcad25311e36616193c98bfe868405df519a47d70b7a83f0878d6be173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197027069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6275c5a30d1ba403047b40dde0ccdb53a0211e2353372a1987502355ad9eb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 14 Jun 2024 17:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz
# Fri, 14 Jun 2024 17:39:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 14 Jun 2024 17:39:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Jun 2024 17:39:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 14 Jun 2024 17:39:45 GMT
RUN mkdir -p /data/data /data/log
# Fri, 14 Jun 2024 17:39:45 GMT
VOLUME [/data]
# Fri, 14 Jun 2024 17:39:45 GMT
WORKDIR /data
# Fri, 14 Jun 2024 17:39:45 GMT
EXPOSE 4200 4300 5432
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 14 Jun 2024 17:39:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Fri, 14 Jun 2024 17:39:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 14 Jun 2024 17:39:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 17:39:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026d664468395d78a36fb20b5b4dc75fccdf756dbb7fcfdc76a7bc8bf1f8bfb3`  
		Last Modified: Fri, 14 Jun 2024 17:40:10 GMT  
		Size: 127.2 MB (127159270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59de24e59cd271a5982e01e5b51c45eda1f949068c21cecbff2fe20c005026b`  
		Last Modified: Fri, 14 Jun 2024 17:40:01 GMT  
		Size: 1.9 MB (1943654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a488b0ace67fa99deafd0127d93b45da0c59ca96afe3ac5902b3d0b7a314f914`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b7093760e34306a855bf5018b42e063a7c5eba392f752d22ca786e8ebaf36a`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd41d307e5f5f417dceb0885c60afc315a8311e036f2981ae54e4f21573bb52`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163abee6a8a1784b5a51275982de462e35090ed37ab6bc12e0a28547d6379dd`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7.2`

```console
$ docker pull crate@sha256:3e1a66879ec02ebf24ae4a9e189da7184e5d0d6839fc031cf1e6b936a3d436cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:18baddfcad25311e36616193c98bfe868405df519a47d70b7a83f0878d6be173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197027069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6275c5a30d1ba403047b40dde0ccdb53a0211e2353372a1987502355ad9eb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 14 Jun 2024 17:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz
# Fri, 14 Jun 2024 17:39:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 14 Jun 2024 17:39:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Jun 2024 17:39:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 14 Jun 2024 17:39:45 GMT
RUN mkdir -p /data/data /data/log
# Fri, 14 Jun 2024 17:39:45 GMT
VOLUME [/data]
# Fri, 14 Jun 2024 17:39:45 GMT
WORKDIR /data
# Fri, 14 Jun 2024 17:39:45 GMT
EXPOSE 4200 4300 5432
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 14 Jun 2024 17:39:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Fri, 14 Jun 2024 17:39:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 14 Jun 2024 17:39:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 17:39:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026d664468395d78a36fb20b5b4dc75fccdf756dbb7fcfdc76a7bc8bf1f8bfb3`  
		Last Modified: Fri, 14 Jun 2024 17:40:10 GMT  
		Size: 127.2 MB (127159270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59de24e59cd271a5982e01e5b51c45eda1f949068c21cecbff2fe20c005026b`  
		Last Modified: Fri, 14 Jun 2024 17:40:01 GMT  
		Size: 1.9 MB (1943654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a488b0ace67fa99deafd0127d93b45da0c59ca96afe3ac5902b3d0b7a314f914`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b7093760e34306a855bf5018b42e063a7c5eba392f752d22ca786e8ebaf36a`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd41d307e5f5f417dceb0885c60afc315a8311e036f2981ae54e4f21573bb52`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163abee6a8a1784b5a51275982de462e35090ed37ab6bc12e0a28547d6379dd`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:3e1a66879ec02ebf24ae4a9e189da7184e5d0d6839fc031cf1e6b936a3d436cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

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
$ docker pull crate@sha256:18baddfcad25311e36616193c98bfe868405df519a47d70b7a83f0878d6be173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197027069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6275c5a30d1ba403047b40dde0ccdb53a0211e2353372a1987502355ad9eb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 14 Jun 2024 17:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.2.tar.gz.asc crate-5.7.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.2.tar.gz.asc     && tar -xf crate-5.7.2.tar.gz -C /crate --strip-components=1     && rm crate-5.7.2.tar.gz
# Fri, 14 Jun 2024 17:39:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 14 Jun 2024 17:39:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Jun 2024 17:39:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 14 Jun 2024 17:39:45 GMT
RUN mkdir -p /data/data /data/log
# Fri, 14 Jun 2024 17:39:45 GMT
VOLUME [/data]
# Fri, 14 Jun 2024 17:39:45 GMT
WORKDIR /data
# Fri, 14 Jun 2024 17:39:45 GMT
EXPOSE 4200 4300 5432
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 14 Jun 2024 17:39:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 14 Jun 2024 17:39:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-06-12T14:05:02.557343 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.2
# Fri, 14 Jun 2024 17:39:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 14 Jun 2024 17:39:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 17:39:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026d664468395d78a36fb20b5b4dc75fccdf756dbb7fcfdc76a7bc8bf1f8bfb3`  
		Last Modified: Fri, 14 Jun 2024 17:40:10 GMT  
		Size: 127.2 MB (127159270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59de24e59cd271a5982e01e5b51c45eda1f949068c21cecbff2fe20c005026b`  
		Last Modified: Fri, 14 Jun 2024 17:40:01 GMT  
		Size: 1.9 MB (1943654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a488b0ace67fa99deafd0127d93b45da0c59ca96afe3ac5902b3d0b7a314f914`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b7093760e34306a855bf5018b42e063a7c5eba392f752d22ca786e8ebaf36a`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd41d307e5f5f417dceb0885c60afc315a8311e036f2981ae54e4f21573bb52`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163abee6a8a1784b5a51275982de462e35090ed37ab6bc12e0a28547d6379dd`  
		Last Modified: Fri, 14 Jun 2024 17:40:00 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
