<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.8`](#crate628)
-	[`crate:6.3`](#crate63)
-	[`crate:6.3.2`](#crate632)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:0834bdf6f525436b6d19a9fe452857b8bd53cab7eb6f3c293c1bc9e89a8f2a50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:f0501dbd19852b4c56d00668f8a70c63b8b104569bb72f91b2cebd6d82429fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243721167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a335f38eabcb6833c06fdc33a10da6858847ab13e366641770b6d8592c2cbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 26 May 2026 19:17:44 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:44 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:44 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 26 May 2026 19:17:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a1e89e949a813c5781787d099a6ea62513aa5693d48927afda3faa9fcdc82b`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 18.4 MB (18373255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad989cfd5b334ef2fca35ff3aed95c10bc97e5057141adbb21c6954b916ad475`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 149.0 MB (149020580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245671380f319851f3821b22c2f7108accdf669a8e44c8a328998722ea687aa0`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 7.8 MB (7762502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74448aabf566e8a6f825d5e60d192afe8aef925f5ea844190d8c3ce251c0b3f`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81adb8040763daa4f683ae9076e183e32025c941e36155a1d121b51b66f0c0a`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e097c799e6f69ccca3ed2928e8b389023288030e01b86faeda89e0442b02e51`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e19f1108bdff41878450bf0d4a1715556c3511b826c1fb78b90fe4fa8c9552`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:4865ac917d6389aaf9e419ed13be6c2755a4725dd4ea044ffe6ac3914d902b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca757ece09d6c59a513010ff783e6f493086f1ec14ba7c57052daf5bee8823b`

```dockerfile
```

-	Layers:
	-	`sha256:e16c2c07e823997f440e7758977f0aa73e48661498b602b8f46cec76c0fcc313`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 6.7 MB (6652289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7565c98dfb1e6c4ac8c4007f5baea109bc3a3641d993bfdc6012852ee54556c`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a58ec6264ed554ef36f61640e1e493d5dee78679f228bece2b2b277f23b5d492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243034617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e2fad09634768cd49f403987838d1589a9e653d2ba34d659ff0e3ac02a759`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 26 May 2026 19:17:49 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:49 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:49 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:49 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:49 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:49 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:49 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 26 May 2026 19:17:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0045ba538d58aa99a78a57759c6542381d8f308f4f0aeccf9f2a0adfc9709c5`  
		Last Modified: Tue, 26 May 2026 19:18:09 GMT  
		Size: 18.4 MB (18426583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48877024d8c9f2ffe7bc4b6ecb82cd942622470b07abf955bb54f944bdf88a6`  
		Last Modified: Tue, 26 May 2026 19:18:12 GMT  
		Size: 149.7 MB (149712727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea175ab64ef60dcd6e38d6742976b85897a48f8192a644f8f793d235c4002f`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 7.8 MB (7759262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f1271baf7d81451f55188669c76ba03fde1c3f7c0782ddf5cd2bdc527439cf`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd12cffb985311843780ed3474b67ff57ef0ea7ca071c66b8650b8cdaa8c0869`  
		Last Modified: Tue, 26 May 2026 19:18:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db3dc5b44257de52fcc822d14ffbdbd88c872bee42f9d406df1a13bc58b286`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce622046d023556bdc4a0b843ff22735f0e242383dd40f23f2f059523ba7cc`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:8851349c4e08851a28f419d26c3889a829fdeb4c27dd623fed3c0119c904368c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76c131825e70c7e8c51bbf9911b466b13ff9c21014e98a341e4028ff223c4a5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf8c2cd6772fde555e79e989613c87d469dc8bc425bcf3ad8a003d09e9b0008`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 6.7 MB (6650201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd4fcdc0da5939b3df357789958c1f17ad22ca5675e3ad91569141d2db6e286`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:0834bdf6f525436b6d19a9fe452857b8bd53cab7eb6f3c293c1bc9e89a8f2a50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:f0501dbd19852b4c56d00668f8a70c63b8b104569bb72f91b2cebd6d82429fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243721167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a335f38eabcb6833c06fdc33a10da6858847ab13e366641770b6d8592c2cbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 26 May 2026 19:17:44 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:44 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:44 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 26 May 2026 19:17:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a1e89e949a813c5781787d099a6ea62513aa5693d48927afda3faa9fcdc82b`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 18.4 MB (18373255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad989cfd5b334ef2fca35ff3aed95c10bc97e5057141adbb21c6954b916ad475`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 149.0 MB (149020580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245671380f319851f3821b22c2f7108accdf669a8e44c8a328998722ea687aa0`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 7.8 MB (7762502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74448aabf566e8a6f825d5e60d192afe8aef925f5ea844190d8c3ce251c0b3f`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81adb8040763daa4f683ae9076e183e32025c941e36155a1d121b51b66f0c0a`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e097c799e6f69ccca3ed2928e8b389023288030e01b86faeda89e0442b02e51`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e19f1108bdff41878450bf0d4a1715556c3511b826c1fb78b90fe4fa8c9552`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:4865ac917d6389aaf9e419ed13be6c2755a4725dd4ea044ffe6ac3914d902b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca757ece09d6c59a513010ff783e6f493086f1ec14ba7c57052daf5bee8823b`

```dockerfile
```

-	Layers:
	-	`sha256:e16c2c07e823997f440e7758977f0aa73e48661498b602b8f46cec76c0fcc313`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 6.7 MB (6652289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7565c98dfb1e6c4ac8c4007f5baea109bc3a3641d993bfdc6012852ee54556c`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a58ec6264ed554ef36f61640e1e493d5dee78679f228bece2b2b277f23b5d492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243034617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e2fad09634768cd49f403987838d1589a9e653d2ba34d659ff0e3ac02a759`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Tue, 26 May 2026 19:17:49 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:49 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:49 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:49 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:49 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:49 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:49 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Tue, 26 May 2026 19:17:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0045ba538d58aa99a78a57759c6542381d8f308f4f0aeccf9f2a0adfc9709c5`  
		Last Modified: Tue, 26 May 2026 19:18:09 GMT  
		Size: 18.4 MB (18426583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48877024d8c9f2ffe7bc4b6ecb82cd942622470b07abf955bb54f944bdf88a6`  
		Last Modified: Tue, 26 May 2026 19:18:12 GMT  
		Size: 149.7 MB (149712727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea175ab64ef60dcd6e38d6742976b85897a48f8192a644f8f793d235c4002f`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 7.8 MB (7759262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f1271baf7d81451f55188669c76ba03fde1c3f7c0782ddf5cd2bdc527439cf`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd12cffb985311843780ed3474b67ff57ef0ea7ca071c66b8650b8cdaa8c0869`  
		Last Modified: Tue, 26 May 2026 19:18:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db3dc5b44257de52fcc822d14ffbdbd88c872bee42f9d406df1a13bc58b286`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce622046d023556bdc4a0b843ff22735f0e242383dd40f23f2f059523ba7cc`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:8851349c4e08851a28f419d26c3889a829fdeb4c27dd623fed3c0119c904368c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76c131825e70c7e8c51bbf9911b466b13ff9c21014e98a341e4028ff223c4a5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf8c2cd6772fde555e79e989613c87d469dc8bc425bcf3ad8a003d09e9b0008`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 6.7 MB (6650201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd4fcdc0da5939b3df357789958c1f17ad22ca5675e3ad91569141d2db6e286`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:96765fff1d2477d096976adb021a7982ef5b7772bbcb78961aac71ef29b33a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:d88f164927f526e5761d0e62f268ef28c75efa06683d45ddaca45857db7ea667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c931aec8a113dbca0573c6933bd62b900b84d7555fad4eafa6f07f7631aa21b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 26 May 2026 19:17:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:42 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:42 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 26 May 2026 19:17:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156cf5bab2132d1229bf089507c6d737f383fd4cb73d5693e2136ff70f023fb8`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 18.4 MB (18373021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedca9446faf71b50417b75490550632b92192c7017d744056ce6776a16b2f00`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 149.1 MB (149148230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1840182e876e5b023eff2c25d6cf67641600d3bda608b22f629c2f2990d7673d`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 7.8 MB (7762934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a3b5b56aa88593291b59d090ecf125b339679db8e24f4d851fcfa6649a0be`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07dcafc5352e24d0a31f054dd871e590262b74951ab11c05930f5b22067861`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48f8d52de0300a4c1c34d8441284b6e5daa0faf5176c0ad58335e2cffce1a95`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a54491521fe3e9cbebd58148bf2350e0bc3633f6c44fe6a9f46fd7393b4baf`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:cbbfb3b5bc7c34b7a5860a3ad66773cca7fdbf74755a03107d0c6487932d5228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54fee6519d2250dbf37e2d17084e892edafde19b9aa9d6e9c32a5fcd84991d2`

```dockerfile
```

-	Layers:
	-	`sha256:74851ce41167c9c71b6bf5f576caa5de6c045983c3740a4e8bc0796f788b78a9`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 6.7 MB (6651073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8387b8fc0fb9bab8b822d3e95b3454b8b32d76640a93edb994deb53b2ef33d07`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8a79ab1a878276c3794db3ff31c9730626d9bde635f1b117fae3ca8738720ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243160408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d230304e0aa7bb266b243c5eb2fd528ad4653f5d05519781633be05f993a07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 26 May 2026 19:17:48 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:48 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:48 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:48 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:48 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:48 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:48 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 26 May 2026 19:17:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ddcb678f5a24722c4249c5e7f6648559c502171ae45e6502b3d4ff42c741e0`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 18.4 MB (18426461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d63d0f317fbfa72e1f536dc12dd0f1dbf4da7c94ecb76015b7ec5b70c5af2d1`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 149.8 MB (149838606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bc8be21b83d4ce4eea5b9149cd25a10fbe73d9c6c146807042eabb71acdbd`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 7.8 MB (7759290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a234610ee68350317800078d0332a72975c58a5b85de6260673fac687768e0`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7257d14d6cb9dbdfd3ac2d889d5fa607287cb3090f2538c2055bf9c06e9da7a6`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a319ab035936534103af246d581d0b06b7c36c55c10c6883b2b375a586b6255d`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e19f1108bdff41878450bf0d4a1715556c3511b826c1fb78b90fe4fa8c9552`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:2d8c9853f68314ba8c93065980c65bfddbdc4bde39d0235137dd6a42138b75c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0293b230611067ef013be185045f01690bbb799c64be48b61ada7a260ad6a2a2`

```dockerfile
```

-	Layers:
	-	`sha256:6d0d5451839feea3524bcae77df96d6a1e1b022784ea039a763438d80a72419b`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 6.6 MB (6648985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea8a82396f0ea5106aacb9e18e1ffcd8be874f103d14240a197986cad45ddcf5`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:96765fff1d2477d096976adb021a7982ef5b7772bbcb78961aac71ef29b33a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:d88f164927f526e5761d0e62f268ef28c75efa06683d45ddaca45857db7ea667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243849013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c931aec8a113dbca0573c6933bd62b900b84d7555fad4eafa6f07f7631aa21b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 26 May 2026 19:17:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:42 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:42 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 26 May 2026 19:17:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156cf5bab2132d1229bf089507c6d737f383fd4cb73d5693e2136ff70f023fb8`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 18.4 MB (18373021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedca9446faf71b50417b75490550632b92192c7017d744056ce6776a16b2f00`  
		Last Modified: Tue, 26 May 2026 19:18:03 GMT  
		Size: 149.1 MB (149148230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1840182e876e5b023eff2c25d6cf67641600d3bda608b22f629c2f2990d7673d`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 7.8 MB (7762934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a3b5b56aa88593291b59d090ecf125b339679db8e24f4d851fcfa6649a0be`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07dcafc5352e24d0a31f054dd871e590262b74951ab11c05930f5b22067861`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48f8d52de0300a4c1c34d8441284b6e5daa0faf5176c0ad58335e2cffce1a95`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a54491521fe3e9cbebd58148bf2350e0bc3633f6c44fe6a9f46fd7393b4baf`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:cbbfb3b5bc7c34b7a5860a3ad66773cca7fdbf74755a03107d0c6487932d5228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54fee6519d2250dbf37e2d17084e892edafde19b9aa9d6e9c32a5fcd84991d2`

```dockerfile
```

-	Layers:
	-	`sha256:74851ce41167c9c71b6bf5f576caa5de6c045983c3740a4e8bc0796f788b78a9`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 6.7 MB (6651073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8387b8fc0fb9bab8b822d3e95b3454b8b32d76640a93edb994deb53b2ef33d07`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8a79ab1a878276c3794db3ff31c9730626d9bde635f1b117fae3ca8738720ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243160408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d230304e0aa7bb266b243c5eb2fd528ad4653f5d05519781633be05f993a07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 26 May 2026 19:17:48 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:48 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:48 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:48 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:48 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:48 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:48 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 26 May 2026 19:17:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ddcb678f5a24722c4249c5e7f6648559c502171ae45e6502b3d4ff42c741e0`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 18.4 MB (18426461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d63d0f317fbfa72e1f536dc12dd0f1dbf4da7c94ecb76015b7ec5b70c5af2d1`  
		Last Modified: Tue, 26 May 2026 19:18:10 GMT  
		Size: 149.8 MB (149838606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bc8be21b83d4ce4eea5b9149cd25a10fbe73d9c6c146807042eabb71acdbd`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 7.8 MB (7759290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a234610ee68350317800078d0332a72975c58a5b85de6260673fac687768e0`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7257d14d6cb9dbdfd3ac2d889d5fa607287cb3090f2538c2055bf9c06e9da7a6`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a319ab035936534103af246d581d0b06b7c36c55c10c6883b2b375a586b6255d`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e19f1108bdff41878450bf0d4a1715556c3511b826c1fb78b90fe4fa8c9552`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:2d8c9853f68314ba8c93065980c65bfddbdc4bde39d0235137dd6a42138b75c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0293b230611067ef013be185045f01690bbb799c64be48b61ada7a260ad6a2a2`

```dockerfile
```

-	Layers:
	-	`sha256:6d0d5451839feea3524bcae77df96d6a1e1b022784ea039a763438d80a72419b`  
		Last Modified: Tue, 26 May 2026 19:18:07 GMT  
		Size: 6.6 MB (6648985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea8a82396f0ea5106aacb9e18e1ffcd8be874f103d14240a197986cad45ddcf5`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:a7c711b09c9f0dde17ce7c2a9b04b99b05f0dc4e59f971967976f09fd0aef2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:0a2bfbbb969b6840111f8a4991d387b293d26f954cbec06a3471d02048970481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246032889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c9178cdeca91d0509487b23f7667c8d3bf32e8d24c62deaa5da3d5187b33e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 26 May 2026 19:17:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:39 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:39 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 26 May 2026 19:17:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc606b4862266f09baba7f1b583e1c3f929ed21bc3d256e53fa7582ab37c820`  
		Last Modified: Tue, 26 May 2026 19:17:59 GMT  
		Size: 18.4 MB (18373260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eabec8e18e3128afa2f1da9f8880cba409f4143bc4df2b018c4016dc1d4223`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 151.3 MB (151332032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b582dfc4bf1f2c0c506722ccd94c0d6fc465dfe1277632628b0953334477e20`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 7.8 MB (7762767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e258d1728109b75e2544540abe0c3478e9d749461b86e6d11d7e7f5ddc40f3`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3316c85b644b8d60b4f5c3e1e07c5d4c06d42be9ba4cdff6c87db71bea196d`  
		Last Modified: Tue, 26 May 2026 19:17:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f721e72c4c8c6818e1711a3360b741f9ab338b46314a197d48f3f983f90a1`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e65e642bd5c3c8fe8c984f4fbeb9e452c4ea6a22d818a12be6511af8e6e9fa9`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:90b0f71f49055c48b089205c2eec1aa0f070f56aa45bb8ad172300308249ceb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d826424bf09dd0778dd9f61a1ef3a056c27a6b399a599eafd4d69a4218c0f1`

```dockerfile
```

-	Layers:
	-	`sha256:ce98be5b69ffd6b4e7b809a76f0debda17f21227a1ef511e51347d601ac35964`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 6.7 MB (6656601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12788f4ed6329d3e41c7ed35374e82583c4ac75a600dd4c4c2fb7d1256152725`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2ebd6517c1c91845737ccb0a488b12bdaf532ee9312789efcbe909c1eb2a7478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242622103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936a8e8eb0ff7d05f384a8aa4f313d9b5ec37d053fc8a63a8ff5f194b626d741`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:28 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 26 May 2026 19:17:45 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:45 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:45 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 26 May 2026 19:17:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade0badc9383ae2084e4d6df3ec39bfaecfad2148a930770f886221b4aea6906`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 18.4 MB (18426523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8199b12d2c62306152f2f8241ecea3078c2e4224a1f255a3c43cf58d5292bf58`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 149.3 MB (149300268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584ddf90724a2bbdfc9124f580ec2830bcdb2f707aeca16141e104cd7e7f4c4e`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 7.8 MB (7759262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097f5a64a13fa63b1d8fd9ed9a851ea61626a7b27832d9b384daf20fcf3aca4`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8688c379ca27c32111b45090bb27a204cf9962101527052ad165f7feaa988ed5`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c736f325f8e7fa8ef606fac53245470620e363ea29406a98939872d5172c15af`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a54491521fe3e9cbebd58148bf2350e0bc3633f6c44fe6a9f46fd7393b4baf`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:164a217575a2e0be823472c71a15cbd78e5e1feba8a9208e461cca68970085a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949bcf33cd5e189682a582eef70cc82bf7433f2dfa7798b9c19703ecc94cd667`

```dockerfile
```

-	Layers:
	-	`sha256:d875235a85119bec5bffab122c461ffe9aba4d45e305cbe46509b28a4fd8165a`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 6.7 MB (6654513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e271bb05258fa6ba8b364efe25f605064620471bf672bafc60cebb23985ad65`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.8`

```console
$ docker pull crate@sha256:a7c711b09c9f0dde17ce7c2a9b04b99b05f0dc4e59f971967976f09fd0aef2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.8` - linux; amd64

```console
$ docker pull crate@sha256:0a2bfbbb969b6840111f8a4991d387b293d26f954cbec06a3471d02048970481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246032889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c9178cdeca91d0509487b23f7667c8d3bf32e8d24c62deaa5da3d5187b33e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 26 May 2026 19:17:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:39 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:39 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 26 May 2026 19:17:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc606b4862266f09baba7f1b583e1c3f929ed21bc3d256e53fa7582ab37c820`  
		Last Modified: Tue, 26 May 2026 19:17:59 GMT  
		Size: 18.4 MB (18373260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eabec8e18e3128afa2f1da9f8880cba409f4143bc4df2b018c4016dc1d4223`  
		Last Modified: Tue, 26 May 2026 19:18:01 GMT  
		Size: 151.3 MB (151332032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b582dfc4bf1f2c0c506722ccd94c0d6fc465dfe1277632628b0953334477e20`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 7.8 MB (7762767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e258d1728109b75e2544540abe0c3478e9d749461b86e6d11d7e7f5ddc40f3`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3316c85b644b8d60b4f5c3e1e07c5d4c06d42be9ba4cdff6c87db71bea196d`  
		Last Modified: Tue, 26 May 2026 19:17:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f721e72c4c8c6818e1711a3360b741f9ab338b46314a197d48f3f983f90a1`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e65e642bd5c3c8fe8c984f4fbeb9e452c4ea6a22d818a12be6511af8e6e9fa9`  
		Last Modified: Tue, 26 May 2026 19:18:00 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:90b0f71f49055c48b089205c2eec1aa0f070f56aa45bb8ad172300308249ceb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d826424bf09dd0778dd9f61a1ef3a056c27a6b399a599eafd4d69a4218c0f1`

```dockerfile
```

-	Layers:
	-	`sha256:ce98be5b69ffd6b4e7b809a76f0debda17f21227a1ef511e51347d601ac35964`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 6.7 MB (6656601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12788f4ed6329d3e41c7ed35374e82583c4ac75a600dd4c4c2fb7d1256152725`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2ebd6517c1c91845737ccb0a488b12bdaf532ee9312789efcbe909c1eb2a7478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242622103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936a8e8eb0ff7d05f384a8aa4f313d9b5ec37d053fc8a63a8ff5f194b626d741`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:28 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.8.tar.gz.asc crate-6.2.8.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.8.tar.gz.asc     && tar -xf crate-6.2.8.tar.gz -C /crate --strip-components=1     && rm crate-6.2.8.tar.gz # buildkit
# Tue, 26 May 2026 19:17:45 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:45 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:45 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:03:44.554696+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.8
# Tue, 26 May 2026 19:17:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade0badc9383ae2084e4d6df3ec39bfaecfad2148a930770f886221b4aea6906`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 18.4 MB (18426523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8199b12d2c62306152f2f8241ecea3078c2e4224a1f255a3c43cf58d5292bf58`  
		Last Modified: Tue, 26 May 2026 19:18:08 GMT  
		Size: 149.3 MB (149300268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584ddf90724a2bbdfc9124f580ec2830bcdb2f707aeca16141e104cd7e7f4c4e`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 7.8 MB (7759262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097f5a64a13fa63b1d8fd9ed9a851ea61626a7b27832d9b384daf20fcf3aca4`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8688c379ca27c32111b45090bb27a204cf9962101527052ad165f7feaa988ed5`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c736f325f8e7fa8ef606fac53245470620e363ea29406a98939872d5172c15af`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a54491521fe3e9cbebd58148bf2350e0bc3633f6c44fe6a9f46fd7393b4baf`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.8` - unknown; unknown

```console
$ docker pull crate@sha256:164a217575a2e0be823472c71a15cbd78e5e1feba8a9208e461cca68970085a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949bcf33cd5e189682a582eef70cc82bf7433f2dfa7798b9c19703ecc94cd667`

```dockerfile
```

-	Layers:
	-	`sha256:d875235a85119bec5bffab122c461ffe9aba4d45e305cbe46509b28a4fd8165a`  
		Last Modified: Tue, 26 May 2026 19:18:05 GMT  
		Size: 6.7 MB (6654513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e271bb05258fa6ba8b364efe25f605064620471bf672bafc60cebb23985ad65`  
		Last Modified: Tue, 26 May 2026 19:18:04 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3`

```console
$ docker pull crate@sha256:5fa05ec7b3f533f75a9529dd12ad2b6f7b8a13c9f394c044c6945d868a4f3605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3` - linux; amd64

```console
$ docker pull crate@sha256:dc8ce9b18d9746387afb8a9e85b3067e5bc0666a5a703fff40d4a843c62b816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ef19c41831b5143d1460d7d3362d7eb8e36d3a3e0feaa96fc6ef09009a870a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:26 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:27 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:27 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c3b6246f20b9a925dc87e934c9cf64c0c44010f77ff19511188cef2b2c0fb`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 18.4 MB (18373082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfba3c79962856a1e54c0451a888bbd72cdc56d39113497c5122a6bacdf5d6`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 139.1 MB (139069153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b23ac2eb4d969f240217e147a30312cad9c3a7c2a2b2d2879d638eea0e0ed0`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 7.8 MB (7763063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be65eec188df7e0de0cc2b3b5bd7c3426e31b5ebee20eede07291da9ecc18238`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684e42778e98a899e4642aa85982a554ff579c919faa689a0ae976e03fcef8d`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dcbd6619b8f7f19901b4ca519a535fda4ced674fcff6d1561d634bdc4e02f4`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29365e98f1d9c54259e9868bef2078fd5e1d186808a5849fce5142616fff1688`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:d11618d4795ebca54f1248ff72a25d44a3c2dd2271774e89b25480689679c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fce6930bdb4ca1a6d109bd30726b7d3c5192a5b236b9bc4df4709c2b0006d45`

```dockerfile
```

-	Layers:
	-	`sha256:27e049d1a72565d90641210798de34acd23fc4fcebbe61a2565986f39096c40b`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b052e0a388755bee67dc90b89240b22fdbc198c98e798c30a70b1bc21473757c`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:53c3dc19d76e2038859d2581497ad614a0f472190c80d951f70e34c2ffb33a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230348745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03adb1f17743c41e0d8fa123e2ff28c04b44b649ace81291f87980ce36533bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:37 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:37 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ceb39908fa0916b55c1c5fe25d6bcd599da6bfea3b0ff6784403960fede1f`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 18.4 MB (18426634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d685f87a033ed8a0d40ceae6e41e7371f31cb46fee7591a7b0978001f3088`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 137.0 MB (137026793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06f03bfaf4751fb824c3110cdf8450ae4ac48f80ad4b2d6b3b7527f785b0907`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 7.8 MB (7759273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d25aad35dc3ad69b8550d33c494253c2fa843098728f64f876a5580709a68`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e780bc235567c7eacd93b2e4de0dd3bd68719be2b1b94568d02b59814ed8a01`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72283ff895861ddf517071d1be26211f55ed97c744a9fc77ea1d71a943589a8b`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0a0e7416b07e74ca20a4fac603cb172ea2f7031c2ebfc16a39d4ef7e1fd29`  
		Last Modified: Tue, 26 May 2026 19:17:57 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:b2dd7888f58360dfb132bbc951711b82224eec40d1778976a460b77f45fdd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b707dc1ed84ad8256cc6ce6a7f51a4a0075f5b986d49d809b342536f2ef70079`

```dockerfile
```

-	Layers:
	-	`sha256:4fb64da8749ab6cb4d64ea706935ff1ffbd1923a6a1fa1b57d269b137fd9bbcc`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb513657ce155379bf96b49dceedb36c21d28ed214fa70fb66f1414e7d3e883`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3.2`

```console
$ docker pull crate@sha256:5fa05ec7b3f533f75a9529dd12ad2b6f7b8a13c9f394c044c6945d868a4f3605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3.2` - linux; amd64

```console
$ docker pull crate@sha256:dc8ce9b18d9746387afb8a9e85b3067e5bc0666a5a703fff40d4a843c62b816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ef19c41831b5143d1460d7d3362d7eb8e36d3a3e0feaa96fc6ef09009a870a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:26 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:27 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:27 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c3b6246f20b9a925dc87e934c9cf64c0c44010f77ff19511188cef2b2c0fb`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 18.4 MB (18373082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfba3c79962856a1e54c0451a888bbd72cdc56d39113497c5122a6bacdf5d6`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 139.1 MB (139069153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b23ac2eb4d969f240217e147a30312cad9c3a7c2a2b2d2879d638eea0e0ed0`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 7.8 MB (7763063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be65eec188df7e0de0cc2b3b5bd7c3426e31b5ebee20eede07291da9ecc18238`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684e42778e98a899e4642aa85982a554ff579c919faa689a0ae976e03fcef8d`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dcbd6619b8f7f19901b4ca519a535fda4ced674fcff6d1561d634bdc4e02f4`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29365e98f1d9c54259e9868bef2078fd5e1d186808a5849fce5142616fff1688`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:d11618d4795ebca54f1248ff72a25d44a3c2dd2271774e89b25480689679c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fce6930bdb4ca1a6d109bd30726b7d3c5192a5b236b9bc4df4709c2b0006d45`

```dockerfile
```

-	Layers:
	-	`sha256:27e049d1a72565d90641210798de34acd23fc4fcebbe61a2565986f39096c40b`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b052e0a388755bee67dc90b89240b22fdbc198c98e798c30a70b1bc21473757c`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:53c3dc19d76e2038859d2581497ad614a0f472190c80d951f70e34c2ffb33a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230348745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03adb1f17743c41e0d8fa123e2ff28c04b44b649ace81291f87980ce36533bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:37 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:37 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ceb39908fa0916b55c1c5fe25d6bcd599da6bfea3b0ff6784403960fede1f`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 18.4 MB (18426634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d685f87a033ed8a0d40ceae6e41e7371f31cb46fee7591a7b0978001f3088`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 137.0 MB (137026793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06f03bfaf4751fb824c3110cdf8450ae4ac48f80ad4b2d6b3b7527f785b0907`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 7.8 MB (7759273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d25aad35dc3ad69b8550d33c494253c2fa843098728f64f876a5580709a68`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e780bc235567c7eacd93b2e4de0dd3bd68719be2b1b94568d02b59814ed8a01`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72283ff895861ddf517071d1be26211f55ed97c744a9fc77ea1d71a943589a8b`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0a0e7416b07e74ca20a4fac603cb172ea2f7031c2ebfc16a39d4ef7e1fd29`  
		Last Modified: Tue, 26 May 2026 19:17:57 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.2` - unknown; unknown

```console
$ docker pull crate@sha256:b2dd7888f58360dfb132bbc951711b82224eec40d1778976a460b77f45fdd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b707dc1ed84ad8256cc6ce6a7f51a4a0075f5b986d49d809b342536f2ef70079`

```dockerfile
```

-	Layers:
	-	`sha256:4fb64da8749ab6cb4d64ea706935ff1ffbd1923a6a1fa1b57d269b137fd9bbcc`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb513657ce155379bf96b49dceedb36c21d28ed214fa70fb66f1414e7d3e883`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:5fa05ec7b3f533f75a9529dd12ad2b6f7b8a13c9f394c044c6945d868a4f3605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:dc8ce9b18d9746387afb8a9e85b3067e5bc0666a5a703fff40d4a843c62b816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ef19c41831b5143d1460d7d3362d7eb8e36d3a3e0feaa96fc6ef09009a870a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:26 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:27 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:27 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c3b6246f20b9a925dc87e934c9cf64c0c44010f77ff19511188cef2b2c0fb`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 18.4 MB (18373082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfba3c79962856a1e54c0451a888bbd72cdc56d39113497c5122a6bacdf5d6`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 139.1 MB (139069153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b23ac2eb4d969f240217e147a30312cad9c3a7c2a2b2d2879d638eea0e0ed0`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 7.8 MB (7763063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be65eec188df7e0de0cc2b3b5bd7c3426e31b5ebee20eede07291da9ecc18238`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684e42778e98a899e4642aa85982a554ff579c919faa689a0ae976e03fcef8d`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dcbd6619b8f7f19901b4ca519a535fda4ced674fcff6d1561d634bdc4e02f4`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29365e98f1d9c54259e9868bef2078fd5e1d186808a5849fce5142616fff1688`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d11618d4795ebca54f1248ff72a25d44a3c2dd2271774e89b25480689679c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fce6930bdb4ca1a6d109bd30726b7d3c5192a5b236b9bc4df4709c2b0006d45`

```dockerfile
```

-	Layers:
	-	`sha256:27e049d1a72565d90641210798de34acd23fc4fcebbe61a2565986f39096c40b`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b052e0a388755bee67dc90b89240b22fdbc198c98e798c30a70b1bc21473757c`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:53c3dc19d76e2038859d2581497ad614a0f472190c80d951f70e34c2ffb33a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230348745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03adb1f17743c41e0d8fa123e2ff28c04b44b649ace81291f87980ce36533bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:37 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:37 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ceb39908fa0916b55c1c5fe25d6bcd599da6bfea3b0ff6784403960fede1f`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 18.4 MB (18426634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d685f87a033ed8a0d40ceae6e41e7371f31cb46fee7591a7b0978001f3088`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 137.0 MB (137026793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06f03bfaf4751fb824c3110cdf8450ae4ac48f80ad4b2d6b3b7527f785b0907`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 7.8 MB (7759273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d25aad35dc3ad69b8550d33c494253c2fa843098728f64f876a5580709a68`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e780bc235567c7eacd93b2e4de0dd3bd68719be2b1b94568d02b59814ed8a01`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72283ff895861ddf517071d1be26211f55ed97c744a9fc77ea1d71a943589a8b`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0a0e7416b07e74ca20a4fac603cb172ea2f7031c2ebfc16a39d4ef7e1fd29`  
		Last Modified: Tue, 26 May 2026 19:17:57 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b2dd7888f58360dfb132bbc951711b82224eec40d1778976a460b77f45fdd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b707dc1ed84ad8256cc6ce6a7f51a4a0075f5b986d49d809b342536f2ef70079`

```dockerfile
```

-	Layers:
	-	`sha256:4fb64da8749ab6cb4d64ea706935ff1ffbd1923a6a1fa1b57d269b137fd9bbcc`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb513657ce155379bf96b49dceedb36c21d28ed214fa70fb66f1414e7d3e883`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
