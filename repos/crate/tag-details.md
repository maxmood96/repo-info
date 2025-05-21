<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.6`](#crate5106)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:6097d30d99941e1087accc84108a5cb4dac3115e59bc7dca0d8eba59ea2ad714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:ffb2493c0c7b89e957b7b7d396fcdac0433833408a179c6b9c33577d5ba31a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234245464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea2a7f6b4153266f5f29252794e4158a19bbe985d36fa85f5f8ff3907d0345d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 20 May 2025 21:32:46 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a42acb3d1a0256b4a4f8d6599b7a6143067a190b88602571ada485b22ddd24`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 15.4 MB (15420984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca355a328eb2ba93a5b1c0f4a215c8085ecc1482eec1ff945dacc2aef4dcc19`  
		Last Modified: Tue, 20 May 2025 21:35:45 GMT  
		Size: 149.7 MB (149657248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92edb8dff1c59b0283c412946d70ca5061b4f088765528d9199860f88eef101c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e29d60eecdebd69fb367f4ab72b4db2416ad944e6ec558f5945ebb26ebda3c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c130e3b8b0b89d86e9d0adaa508a5545b67451687f8e3c67f13e959ff94580c`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019652859fac596dce7fe5725ccb1b365bb8ef228daf46628f40ceb5b77bef8e`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d444a7486e55051011dd4dbf9009e0578913582f5d472222467359334d1545`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:7bc1515a316efcae62367353b1cbac4a36444b4b93ead18c68672f96e21e857a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e43e28f513bf20527705d15a46e777d4c1fb2dbab55aab4c7acee9b93dc32`

```dockerfile
```

-	Layers:
	-	`sha256:8f9d2f7a206374570f8cf07c707667f8cf6443d3e2418a6e0d44d0ea994550a8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f31547aa389aee1352f21201c0a2ea2c5b5ba1a7a4b78da5aaf81e318990f8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d773496596414583673311f950d4078010abe57a229c5b37d185ad72f1c5017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233497587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30322475da1d7f51706eb60cb65fad8d9dc8b60bb1f695c56089ede75d7c5bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 20 May 2025 21:32:17 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4f20e404ef12944afecbdd171a5128436996c16ca7e55ca77f977ff2bceb3`  
		Last Modified: Tue, 20 May 2025 21:35:23 GMT  
		Size: 150.3 MB (150335302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bbffb882b7cf7e114fda95f97a07c87062d180c38f6620f0376ec19fc289d`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a73619aef8b150db6a3c18fa8d985a6e07deb2237f1d13a75282c7a83a2655`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e2a82054604ad437b6b2a322e1725ce7bd486830173d08ce09ed94c9720f0`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2eb0ef16ac2a8173e917ec46f21dcce867625c32519d60febfb8586a25b97`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534f1a61767ddc55c022bbf91ff90368d6f2bc5bd6635551122fc10184d6baf`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:0dffe38989b3c15df689805bbccb7417e42c7e72d58822cb938a8571c897ef43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5784f1dfdaf7abe90205c30971885e07bc9486c17b1e1b99c760fa0449cc27dc`

```dockerfile
```

-	Layers:
	-	`sha256:fe2d501461a820339ac37623ba3fadf7dc4c69de5717e6d31a9f3d491aed4ce2`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c524803b09ee81d2edcd2464d4c17512136e0b6b7d824aa891ddf93a700700f`  
		Last Modified: Tue, 20 May 2025 21:35:17 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.6`

```console
$ docker pull crate@sha256:6097d30d99941e1087accc84108a5cb4dac3115e59bc7dca0d8eba59ea2ad714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.6` - linux; amd64

```console
$ docker pull crate@sha256:ffb2493c0c7b89e957b7b7d396fcdac0433833408a179c6b9c33577d5ba31a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234245464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea2a7f6b4153266f5f29252794e4158a19bbe985d36fa85f5f8ff3907d0345d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 20 May 2025 21:32:46 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a42acb3d1a0256b4a4f8d6599b7a6143067a190b88602571ada485b22ddd24`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 15.4 MB (15420984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca355a328eb2ba93a5b1c0f4a215c8085ecc1482eec1ff945dacc2aef4dcc19`  
		Last Modified: Tue, 20 May 2025 21:35:45 GMT  
		Size: 149.7 MB (149657248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92edb8dff1c59b0283c412946d70ca5061b4f088765528d9199860f88eef101c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e29d60eecdebd69fb367f4ab72b4db2416ad944e6ec558f5945ebb26ebda3c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c130e3b8b0b89d86e9d0adaa508a5545b67451687f8e3c67f13e959ff94580c`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019652859fac596dce7fe5725ccb1b365bb8ef228daf46628f40ceb5b77bef8e`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d444a7486e55051011dd4dbf9009e0578913582f5d472222467359334d1545`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.6` - unknown; unknown

```console
$ docker pull crate@sha256:7bc1515a316efcae62367353b1cbac4a36444b4b93ead18c68672f96e21e857a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e43e28f513bf20527705d15a46e777d4c1fb2dbab55aab4c7acee9b93dc32`

```dockerfile
```

-	Layers:
	-	`sha256:8f9d2f7a206374570f8cf07c707667f8cf6443d3e2418a6e0d44d0ea994550a8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f31547aa389aee1352f21201c0a2ea2c5b5ba1a7a4b78da5aaf81e318990f8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d773496596414583673311f950d4078010abe57a229c5b37d185ad72f1c5017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233497587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30322475da1d7f51706eb60cb65fad8d9dc8b60bb1f695c56089ede75d7c5bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 20 May 2025 21:32:17 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4f20e404ef12944afecbdd171a5128436996c16ca7e55ca77f977ff2bceb3`  
		Last Modified: Tue, 20 May 2025 21:35:23 GMT  
		Size: 150.3 MB (150335302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bbffb882b7cf7e114fda95f97a07c87062d180c38f6620f0376ec19fc289d`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a73619aef8b150db6a3c18fa8d985a6e07deb2237f1d13a75282c7a83a2655`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e2a82054604ad437b6b2a322e1725ce7bd486830173d08ce09ed94c9720f0`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2eb0ef16ac2a8173e917ec46f21dcce867625c32519d60febfb8586a25b97`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534f1a61767ddc55c022bbf91ff90368d6f2bc5bd6635551122fc10184d6baf`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.6` - unknown; unknown

```console
$ docker pull crate@sha256:0dffe38989b3c15df689805bbccb7417e42c7e72d58822cb938a8571c897ef43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5784f1dfdaf7abe90205c30971885e07bc9486c17b1e1b99c760fa0449cc27dc`

```dockerfile
```

-	Layers:
	-	`sha256:fe2d501461a820339ac37623ba3fadf7dc4c69de5717e6d31a9f3d491aed4ce2`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c524803b09ee81d2edcd2464d4c17512136e0b6b7d824aa891ddf93a700700f`  
		Last Modified: Tue, 20 May 2025 21:35:17 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:ae26ed73e2c4936fae3796160dbef7d09a66c3ca8cee148235d95a0121631e61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:084a04c51e5d125a3e12143854575e5e9ed6096436fc76489f37a3d8f75c840f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233598122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c116f493891f09c1e6ed04348a35b6f1de4330ca3a9f2a82a26b4deacc29c2f`
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 20 May 2025 21:32:46 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0bf3fca5b5cc6ca367287374cec091954893be167b0e058b557fb9c8cada0`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 15.4 MB (15421182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ebde60ec227c951cb7f500c7b33114a77c068572ed97259beb4ba68e7a0690`  
		Last Modified: Tue, 20 May 2025 21:36:20 GMT  
		Size: 149.0 MB (149009708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e7dfb2c65caf1a63cfbfff27c15147d5d77fce970166d44c325b3437c91d8`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2486ae9b744af5cbd0a2548d1e975f6c9236999a1f499c1a5fb31f5d9ddc2b`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488da3fd806f4aeb510977b15cf933f8cafe576457eceb262671b7346a2b74a`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a4ca7bc0363fde84883ac9c06f69a0f20789af443af9a66ae87ae2d0c89a3`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b5f2398c0016e43b99037d2131ead2af52542cc6cb5ecfa023386fede11973`  
		Last Modified: Tue, 20 May 2025 21:36:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:cf1aaeb402a4ba66648bbf9760f1e02a53a9db39735db472619270246f053a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97595934d167d66b46d961c6dc4f10468872c8c19d94ad22a11591edc3902bcd`

```dockerfile
```

-	Layers:
	-	`sha256:d12a80722e38c1e7de23a581902bd56f41e8ba2cc4fe1c8200c168d61b7fc312`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 5.2 MB (5178426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25169c71ab59d7452bafca4aca1d8272877f72a138a29a30d272c8074c5dc36b`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:240133e4dfb02cd9ac38033f4bf455f8e4c7335974bd90a2c6b0c54607667768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232870865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea976b5623f273f89347063c796b298e0c72e9ddf3287fb1d8c6055d9d21c73`
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
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 20 May 2025 21:32:17 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e25f1665ae5c3fce08cbaa86a27dbd468087c2e48e4b1d3f50316265d8aa6`  
		Last Modified: Tue, 20 May 2025 21:36:02 GMT  
		Size: 149.7 MB (149708577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d5e2d0f8f9da3244218732c75a2dca1be6cbdb9d7ad9166540bcac87373454`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9071465ca3719ad9937260bc70fde031fd45ad5b2f4f3f8fe6b87bf5474760b`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88279d887e62c03cbe416998e82c03f3416dbb14edec74a732a633120df730`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe376dd8d1ceaddea988006e242601369ff886914d3da06fbf41517d44b544b2`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea881fae8579feb45d6ac18970f3e5002ab453b5f8359d5f000ea39062dfa7`  
		Last Modified: Tue, 20 May 2025 21:36:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:38f3064444f672e50bc8730f55369de836e25d9b737843d01f7d7315f899b82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5fcd8719594ca1341547510a352936435bc34ebb6266aecd017eccf9917813`

```dockerfile
```

-	Layers:
	-	`sha256:123d34466579c123f0a9d090ce68afd61e19d2d28e550c72dc8ad8d675941e0c`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:ae26ed73e2c4936fae3796160dbef7d09a66c3ca8cee148235d95a0121631e61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:084a04c51e5d125a3e12143854575e5e9ed6096436fc76489f37a3d8f75c840f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233598122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c116f493891f09c1e6ed04348a35b6f1de4330ca3a9f2a82a26b4deacc29c2f`
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
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 20 May 2025 21:32:46 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0bf3fca5b5cc6ca367287374cec091954893be167b0e058b557fb9c8cada0`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 15.4 MB (15421182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ebde60ec227c951cb7f500c7b33114a77c068572ed97259beb4ba68e7a0690`  
		Last Modified: Tue, 20 May 2025 21:36:20 GMT  
		Size: 149.0 MB (149009708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e7dfb2c65caf1a63cfbfff27c15147d5d77fce970166d44c325b3437c91d8`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2486ae9b744af5cbd0a2548d1e975f6c9236999a1f499c1a5fb31f5d9ddc2b`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488da3fd806f4aeb510977b15cf933f8cafe576457eceb262671b7346a2b74a`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a4ca7bc0363fde84883ac9c06f69a0f20789af443af9a66ae87ae2d0c89a3`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b5f2398c0016e43b99037d2131ead2af52542cc6cb5ecfa023386fede11973`  
		Last Modified: Tue, 20 May 2025 21:36:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:cf1aaeb402a4ba66648bbf9760f1e02a53a9db39735db472619270246f053a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97595934d167d66b46d961c6dc4f10468872c8c19d94ad22a11591edc3902bcd`

```dockerfile
```

-	Layers:
	-	`sha256:d12a80722e38c1e7de23a581902bd56f41e8ba2cc4fe1c8200c168d61b7fc312`  
		Last Modified: Tue, 20 May 2025 21:36:18 GMT  
		Size: 5.2 MB (5178426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25169c71ab59d7452bafca4aca1d8272877f72a138a29a30d272c8074c5dc36b`  
		Last Modified: Tue, 20 May 2025 21:36:17 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:240133e4dfb02cd9ac38033f4bf455f8e4c7335974bd90a2c6b0c54607667768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232870865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea976b5623f273f89347063c796b298e0c72e9ddf3287fb1d8c6055d9d21c73`
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
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 20 May 2025 21:32:17 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e25f1665ae5c3fce08cbaa86a27dbd468087c2e48e4b1d3f50316265d8aa6`  
		Last Modified: Tue, 20 May 2025 21:36:02 GMT  
		Size: 149.7 MB (149708577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d5e2d0f8f9da3244218732c75a2dca1be6cbdb9d7ad9166540bcac87373454`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9071465ca3719ad9937260bc70fde031fd45ad5b2f4f3f8fe6b87bf5474760b`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88279d887e62c03cbe416998e82c03f3416dbb14edec74a732a633120df730`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe376dd8d1ceaddea988006e242601369ff886914d3da06fbf41517d44b544b2`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea881fae8579feb45d6ac18970f3e5002ab453b5f8359d5f000ea39062dfa7`  
		Last Modified: Tue, 20 May 2025 21:36:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:38f3064444f672e50bc8730f55369de836e25d9b737843d01f7d7315f899b82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5fcd8719594ca1341547510a352936435bc34ebb6266aecd017eccf9917813`

```dockerfile
```

-	Layers:
	-	`sha256:123d34466579c123f0a9d090ce68afd61e19d2d28e550c72dc8ad8d675941e0c`  
		Last Modified: Tue, 20 May 2025 21:35:59 GMT  
		Size: 5.2 MB (5175722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b859065f6e1d85040bec7891b5fa41e203cfc586d5cfb9397330c57a869185d`  
		Last Modified: Tue, 20 May 2025 21:35:58 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:6097d30d99941e1087accc84108a5cb4dac3115e59bc7dca0d8eba59ea2ad714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:ffb2493c0c7b89e957b7b7d396fcdac0433833408a179c6b9c33577d5ba31a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234245464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea2a7f6b4153266f5f29252794e4158a19bbe985d36fa85f5f8ff3907d0345d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a816d8f0e1d0a3745e447d97948db913506747f5e3653ff3ffaa027f62088489`  
		Last Modified: Tue, 20 May 2025 21:32:46 GMT  
		Size: 67.2 MB (67221727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a42acb3d1a0256b4a4f8d6599b7a6143067a190b88602571ada485b22ddd24`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 15.4 MB (15420984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca355a328eb2ba93a5b1c0f4a215c8085ecc1482eec1ff945dacc2aef4dcc19`  
		Last Modified: Tue, 20 May 2025 21:35:45 GMT  
		Size: 149.7 MB (149657248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92edb8dff1c59b0283c412946d70ca5061b4f088765528d9199860f88eef101c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e29d60eecdebd69fb367f4ab72b4db2416ad944e6ec558f5945ebb26ebda3c`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c130e3b8b0b89d86e9d0adaa508a5545b67451687f8e3c67f13e959ff94580c`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019652859fac596dce7fe5725ccb1b365bb8ef228daf46628f40ceb5b77bef8e`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d444a7486e55051011dd4dbf9009e0578913582f5d472222467359334d1545`  
		Last Modified: Tue, 20 May 2025 21:35:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7bc1515a316efcae62367353b1cbac4a36444b4b93ead18c68672f96e21e857a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e43e28f513bf20527705d15a46e777d4c1fb2dbab55aab4c7acee9b93dc32`

```dockerfile
```

-	Layers:
	-	`sha256:8f9d2f7a206374570f8cf07c707667f8cf6443d3e2418a6e0d44d0ea994550a8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 5.2 MB (5180293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f31547aa389aee1352f21201c0a2ea2c5b5ba1a7a4b78da5aaf81e318990f8`  
		Last Modified: Tue, 20 May 2025 21:35:43 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d773496596414583673311f950d4078010abe57a229c5b37d185ad72f1c5017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233497587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30322475da1d7f51706eb60cb65fad8d9dc8b60bb1f695c56089ede75d7c5bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 12 May 2025 12:44:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d65646c8deafed7b3b2cf9c8de289d8dd4e8bd5905bf7effebaa26de74599d6`  
		Last Modified: Tue, 20 May 2025 21:32:17 GMT  
		Size: 65.7 MB (65741766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918bffde4d7340529b99c143a7dc82ebed45d4002d0426777a49fe295e45b1`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 15.5 MB (15475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4f20e404ef12944afecbdd171a5128436996c16ca7e55ca77f977ff2bceb3`  
		Last Modified: Tue, 20 May 2025 21:35:23 GMT  
		Size: 150.3 MB (150335302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bbffb882b7cf7e114fda95f97a07c87062d180c38f6620f0376ec19fc289d`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a73619aef8b150db6a3c18fa8d985a6e07deb2237f1d13a75282c7a83a2655`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e2a82054604ad437b6b2a322e1725ce7bd486830173d08ce09ed94c9720f0`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2eb0ef16ac2a8173e917ec46f21dcce867625c32519d60febfb8586a25b97`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534f1a61767ddc55c022bbf91ff90368d6f2bc5bd6635551122fc10184d6baf`  
		Last Modified: Tue, 20 May 2025 21:35:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:0dffe38989b3c15df689805bbccb7417e42c7e72d58822cb938a8571c897ef43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5784f1dfdaf7abe90205c30971885e07bc9486c17b1e1b99c760fa0449cc27dc`

```dockerfile
```

-	Layers:
	-	`sha256:fe2d501461a820339ac37623ba3fadf7dc4c69de5717e6d31a9f3d491aed4ce2`  
		Last Modified: Tue, 20 May 2025 21:35:18 GMT  
		Size: 5.2 MB (5177601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c524803b09ee81d2edcd2464d4c17512136e0b6b7d824aa891ddf93a700700f`  
		Last Modified: Tue, 20 May 2025 21:35:17 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
