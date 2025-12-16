<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.16`](#crate51016)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.5`](#crate605)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.2`](#crate612)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:a78c25fed2dc52d0897f4ded252c8abec823ad66c781856a22f3ecd2fd0929b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:341e9883c1e113e27a525fc963738a88b53ed3e23c8b0a233f8e2e276b24ed4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233637825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deb5758706503875840a430b6de3859870e2d00be7b5e75e9eb95b048a19825`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f81a2a4849e42a3768bacdad9aa432168367c45ceb617685022812c2099054d`  
		Last Modified: Mon, 15 Dec 2025 19:30:28 GMT  
		Size: 149.7 MB (149721713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c906cc62c53415e98a2f2fe4df8ee1ccf188844390072912c6251508aaf1174`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bde33a34fe9590ae1eca3017adb7dfe936ff3a87e24943074af345b2b302b`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fbd4344b20d37010a5d01ae13c441a6da8b705e302a80cd6f5f1737d295e1`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fec063b5fe7df37f5736438207b6e34e593e079651eab638aa2fdc145a7dec`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:1b8884b41aef254e412193245ebf25d10bd918184e0874fd22a0c542cad6ba0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7b1eecc5b8bfa6a780b19004b570d29727986918db8c788aa7fc433320c0f7`

```dockerfile
```

-	Layers:
	-	`sha256:179ac3c30eeb6c2bb0cf8f2fb1a8cbd7e1074053979347cc0490d5e7352057a2`  
		Last Modified: Mon, 15 Dec 2025 21:38:23 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35213ccced9cf1a2cb537ad9011c3e9cc74a21a31aac4e96c55bb44331f53ec7`  
		Last Modified: Mon, 15 Dec 2025 21:38:24 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e3989455aaa4981cdac61d69f6a37e89f3899b0fd6ac5a77e8d245e9e2bc047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232858591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80cb233e7f39eba91b62589b03943e1356e1951bdc33196c1180692e24e0653`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f89f2bf29b60cd8d45c680bce299f02ae74959214ad9343bc21f5501217fd`  
		Last Modified: Mon, 15 Dec 2025 19:30:33 GMT  
		Size: 150.4 MB (150402353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb8fc022e91eb6459e10811809ff8ff16887ab5ab34255121511328a34253d`  
		Last Modified: Mon, 15 Dec 2025 19:30:20 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91dfc4e182b1686814f6e0e4fb31857df1609bc9adbb3f503a0f713c85aa37`  
		Last Modified: Mon, 15 Dec 2025 19:30:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fff6400a7fb12bcffb3094416f6b5847f0798a23a8417b4fb8b9ee135e2e31`  
		Last Modified: Mon, 15 Dec 2025 19:30:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8131d027a1fd2315b3c0cfb4fea1db04a18c04ae7af421a25ce8858d772f1940`  
		Last Modified: Mon, 15 Dec 2025 19:30:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:180fa32cad26b621a8952bf5f6b3aaacbc0ce18525e15a0218bd4b2f9fcec169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1e21b209cb6ce63a0efe22bec0a091a0f99a6a7ee55b8ceddcd60a2fb1a5b1`

```dockerfile
```

-	Layers:
	-	`sha256:06f29a76d0d93c3181b609b6a29513c3f75199410d30a5880dcf14c726868bc7`  
		Last Modified: Mon, 15 Dec 2025 21:38:29 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e9cbcb2f4c8144c7c9d3fe84d80c8689a7703701cb2dcd5d2ea7e02771d63f`  
		Last Modified: Mon, 15 Dec 2025 21:38:33 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.16`

```console
$ docker pull crate@sha256:a78c25fed2dc52d0897f4ded252c8abec823ad66c781856a22f3ecd2fd0929b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.16` - linux; amd64

```console
$ docker pull crate@sha256:341e9883c1e113e27a525fc963738a88b53ed3e23c8b0a233f8e2e276b24ed4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233637825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deb5758706503875840a430b6de3859870e2d00be7b5e75e9eb95b048a19825`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f81a2a4849e42a3768bacdad9aa432168367c45ceb617685022812c2099054d`  
		Last Modified: Mon, 15 Dec 2025 19:30:28 GMT  
		Size: 149.7 MB (149721713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c906cc62c53415e98a2f2fe4df8ee1ccf188844390072912c6251508aaf1174`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bde33a34fe9590ae1eca3017adb7dfe936ff3a87e24943074af345b2b302b`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fbd4344b20d37010a5d01ae13c441a6da8b705e302a80cd6f5f1737d295e1`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fec063b5fe7df37f5736438207b6e34e593e079651eab638aa2fdc145a7dec`  
		Last Modified: Mon, 15 Dec 2025 19:30:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:1b8884b41aef254e412193245ebf25d10bd918184e0874fd22a0c542cad6ba0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7b1eecc5b8bfa6a780b19004b570d29727986918db8c788aa7fc433320c0f7`

```dockerfile
```

-	Layers:
	-	`sha256:179ac3c30eeb6c2bb0cf8f2fb1a8cbd7e1074053979347cc0490d5e7352057a2`  
		Last Modified: Mon, 15 Dec 2025 21:38:23 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35213ccced9cf1a2cb537ad9011c3e9cc74a21a31aac4e96c55bb44331f53ec7`  
		Last Modified: Mon, 15 Dec 2025 21:38:24 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.16` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e3989455aaa4981cdac61d69f6a37e89f3899b0fd6ac5a77e8d245e9e2bc047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232858591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80cb233e7f39eba91b62589b03943e1356e1951bdc33196c1180692e24e0653`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f89f2bf29b60cd8d45c680bce299f02ae74959214ad9343bc21f5501217fd`  
		Last Modified: Mon, 15 Dec 2025 19:30:33 GMT  
		Size: 150.4 MB (150402353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb8fc022e91eb6459e10811809ff8ff16887ab5ab34255121511328a34253d`  
		Last Modified: Mon, 15 Dec 2025 19:30:20 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91dfc4e182b1686814f6e0e4fb31857df1609bc9adbb3f503a0f713c85aa37`  
		Last Modified: Mon, 15 Dec 2025 19:30:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fff6400a7fb12bcffb3094416f6b5847f0798a23a8417b4fb8b9ee135e2e31`  
		Last Modified: Mon, 15 Dec 2025 19:30:22 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8131d027a1fd2315b3c0cfb4fea1db04a18c04ae7af421a25ce8858d772f1940`  
		Last Modified: Mon, 15 Dec 2025 19:30:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:180fa32cad26b621a8952bf5f6b3aaacbc0ce18525e15a0218bd4b2f9fcec169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1e21b209cb6ce63a0efe22bec0a091a0f99a6a7ee55b8ceddcd60a2fb1a5b1`

```dockerfile
```

-	Layers:
	-	`sha256:06f29a76d0d93c3181b609b6a29513c3f75199410d30a5880dcf14c726868bc7`  
		Last Modified: Mon, 15 Dec 2025 21:38:29 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e9cbcb2f4c8144c7c9d3fe84d80c8689a7703701cb2dcd5d2ea7e02771d63f`  
		Last Modified: Mon, 15 Dec 2025 21:38:33 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:99f63ed1f088d9b94da7e8c4ae802adfa9b82f3f6fe81a68bf9cbba5294bdd2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:b654d4e2299defd542d0d633537b0690f33845505aa22436655949cce947ccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232944879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74b6a8d2032db29b2196b03645f14a7a3bcd0d88b7ee2c3fac5612482382069`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:29:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:30:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:30:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:30:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:30:01 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:30:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:30:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 15 Dec 2025 19:30:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:30:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b687cfaf8538cf9f96da38fd84f0859fdb497c31e1be7bb3655035a4ad2e1d`  
		Last Modified: Mon, 15 Dec 2025 19:30:35 GMT  
		Size: 14.5 MB (14512767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd950f508bbe6b631cfe010e996db829480aa53edd23064a07ad977c0310322`  
		Last Modified: Mon, 15 Dec 2025 19:30:42 GMT  
		Size: 149.0 MB (149028828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345d4bb330c2cf7116599637ab0995d36d8aae2b69b44efc2e016199b4b88624`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8545622da4de6958b108fdb06de46592727a6a801acae1ca5bc0eb591ffdf834`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732f7332ba602f81a7ec4bb6a2792888c4e2f011bc7737372f9cee9d41af2524`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293052585459cfb8cbc11071477aff48b184198f1c2ba7cf809e810999eb45f`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc974acd5c2bdfcc3ff5c8216eaf0e1728c40f3310ba2c87f90a96c83cfe04`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:bc1f389bda06c378607543ae1afe77f1f44171ba61e581ee4d67af21e326cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dac7ac8fac2c64f29c903a75e5e7ad6092f4013bd8c665070c0587e2fb2724`

```dockerfile
```

-	Layers:
	-	`sha256:d19e9150d828f0bc3ad9efdc4f26c28c0637134f1079641d12751c089bcf5bc3`  
		Last Modified: Mon, 15 Dec 2025 21:38:34 GMT  
		Size: 5.2 MB (5191984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4adb92f6c0d3e62fcd7226f9dea5432650e2d859eada735555f4d72a778e03`  
		Last Modified: Mon, 15 Dec 2025 21:38:35 GMT  
		Size: 22.8 KB (22843 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:99f9edf61147db915c3cc04586b6eba041a92acad7d795f1d583eaf9a1be301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232172409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea1bb063b58e4847dd71cc238f53f8a3cd51fe14312249b23ec85f7311f7f42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:29:26 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f918ce551f17a6c732d557fa88aa72d27f0b6105f02c5a4697337601d796a3`  
		Last Modified: Mon, 15 Dec 2025 19:30:21 GMT  
		Size: 14.6 MB (14567770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331afa561fbcf598281990e14f08ce267128bfb8b04364687ad48178b6ce14fa`  
		Last Modified: Mon, 15 Dec 2025 19:30:33 GMT  
		Size: 149.7 MB (149716138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2a12ad3ec11588abf100a9b76539be0b04a45aed675246269cc093db0b89d`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6bb8f439df55bd5c6a7438045c973ea609406265781704703f64198e2e219a`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee5d5bfb962cbb0db67643386d15860f01961df5992e34379d5eab91addc0`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54849dffd3c7a97cfe77ab37a8af21202f6ac6a7df17e02f4bec4b5da90f8bf5`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:d1bdfcaf9e1e9ae27e7a648a2f8044d12357aa7cdccf3983d0a7189a02c8c3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc1f07de849d15d3a74d07cb7663e894959355e6cfaae16a8a8499413a0e77b`

```dockerfile
```

-	Layers:
	-	`sha256:c2ef4b250646b406d03e911327c46b65113aa8c2f919ec71082051f3d9b6f6d4`  
		Last Modified: Mon, 15 Dec 2025 21:38:39 GMT  
		Size: 5.2 MB (5189891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759c98bf39dbcc3c973efc05446abc339be1b9d2a22a9f6c5711edb7666139e2`  
		Last Modified: Mon, 15 Dec 2025 21:38:40 GMT  
		Size: 23.0 KB (22968 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.5`

```console
$ docker pull crate@sha256:99f63ed1f088d9b94da7e8c4ae802adfa9b82f3f6fe81a68bf9cbba5294bdd2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.5` - linux; amd64

```console
$ docker pull crate@sha256:b654d4e2299defd542d0d633537b0690f33845505aa22436655949cce947ccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232944879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74b6a8d2032db29b2196b03645f14a7a3bcd0d88b7ee2c3fac5612482382069`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:29:47 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:30:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:30:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:30:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:30:01 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:30:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:30:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 15 Dec 2025 19:30:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:30:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:30:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b687cfaf8538cf9f96da38fd84f0859fdb497c31e1be7bb3655035a4ad2e1d`  
		Last Modified: Mon, 15 Dec 2025 19:30:35 GMT  
		Size: 14.5 MB (14512767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd950f508bbe6b631cfe010e996db829480aa53edd23064a07ad977c0310322`  
		Last Modified: Mon, 15 Dec 2025 19:30:42 GMT  
		Size: 149.0 MB (149028828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345d4bb330c2cf7116599637ab0995d36d8aae2b69b44efc2e016199b4b88624`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8545622da4de6958b108fdb06de46592727a6a801acae1ca5bc0eb591ffdf834`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732f7332ba602f81a7ec4bb6a2792888c4e2f011bc7737372f9cee9d41af2524`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293052585459cfb8cbc11071477aff48b184198f1c2ba7cf809e810999eb45f`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc974acd5c2bdfcc3ff5c8216eaf0e1728c40f3310ba2c87f90a96c83cfe04`  
		Last Modified: Mon, 15 Dec 2025 19:30:31 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:bc1f389bda06c378607543ae1afe77f1f44171ba61e581ee4d67af21e326cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dac7ac8fac2c64f29c903a75e5e7ad6092f4013bd8c665070c0587e2fb2724`

```dockerfile
```

-	Layers:
	-	`sha256:d19e9150d828f0bc3ad9efdc4f26c28c0637134f1079641d12751c089bcf5bc3`  
		Last Modified: Mon, 15 Dec 2025 21:38:34 GMT  
		Size: 5.2 MB (5191984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4adb92f6c0d3e62fcd7226f9dea5432650e2d859eada735555f4d72a778e03`  
		Last Modified: Mon, 15 Dec 2025 21:38:35 GMT  
		Size: 22.8 KB (22843 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:99f9edf61147db915c3cc04586b6eba041a92acad7d795f1d583eaf9a1be301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232172409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea1bb063b58e4847dd71cc238f53f8a3cd51fe14312249b23ec85f7311f7f42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:29:26 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:29:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:29:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:29:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:29:40 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:29:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Mon, 15 Dec 2025 19:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:29:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f918ce551f17a6c732d557fa88aa72d27f0b6105f02c5a4697337601d796a3`  
		Last Modified: Mon, 15 Dec 2025 19:30:21 GMT  
		Size: 14.6 MB (14567770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331afa561fbcf598281990e14f08ce267128bfb8b04364687ad48178b6ce14fa`  
		Last Modified: Mon, 15 Dec 2025 19:30:33 GMT  
		Size: 149.7 MB (149716138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2a12ad3ec11588abf100a9b76539be0b04a45aed675246269cc093db0b89d`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1979bc0dfaaa1a842472135b61eb9a84c0d4b1326e7b2f579aeee9ee04cafde`  
		Last Modified: Mon, 15 Dec 2025 19:30:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6bb8f439df55bd5c6a7438045c973ea609406265781704703f64198e2e219a`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee5d5bfb962cbb0db67643386d15860f01961df5992e34379d5eab91addc0`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54849dffd3c7a97cfe77ab37a8af21202f6ac6a7df17e02f4bec4b5da90f8bf5`  
		Last Modified: Mon, 15 Dec 2025 19:30:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:d1bdfcaf9e1e9ae27e7a648a2f8044d12357aa7cdccf3983d0a7189a02c8c3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc1f07de849d15d3a74d07cb7663e894959355e6cfaae16a8a8499413a0e77b`

```dockerfile
```

-	Layers:
	-	`sha256:c2ef4b250646b406d03e911327c46b65113aa8c2f919ec71082051f3d9b6f6d4`  
		Last Modified: Mon, 15 Dec 2025 21:38:39 GMT  
		Size: 5.2 MB (5189891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759c98bf39dbcc3c973efc05446abc339be1b9d2a22a9f6c5711edb7666139e2`  
		Last Modified: Mon, 15 Dec 2025 21:38:40 GMT  
		Size: 23.0 KB (22968 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:68d1430b4f7edf386dcaeb01d52b18d92d595da2a3012cb5a80b2e56579b1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:03755e49eb92ae8eb1d7acc49092a05b6502092caedb5339174b22f67f35709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5242d7e52462d870dd44bc64aa0d685a59bfe7c86e5145e0e634dd198a5aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:57 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ced334c44f4de2a971bd22e1992bd6b0c842659e52fc9e255fd46337df525`  
		Last Modified: Mon, 15 Dec 2025 21:39:33 GMT  
		Size: 149.1 MB (149133517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7111a74856498548b678c9cb798ca45fbec416115cb9472774d5cb902a1cd1`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666a64ebf108b2bbfd8f845c7510d51aa7b19993cd83bcf5d3c7288ad3982d5`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d862f94a754e253e94e266b073be3fe868359c5fb4e3671943799233a67d11`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c1baaaba5c1a5127f7301c826ffb775362c6a3b3f9b611dda2fad16ed28ec`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150126d40904960df7e55865dc704e4f7ab9b1435a671f51840b9a8373e9748c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:acbb49761e5d8ba0a18936d9b890cab96742b70ef486ac924cfe2eb50163923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056c1346f8a30d4061ef1f68698acfe20196c9a24ab4903c071318a960a9d07`

```dockerfile
```

-	Layers:
	-	`sha256:839de76bcc0825cd1a263ccae664ae2da6cc19324fd5bb0909f66319014847fe`  
		Last Modified: Mon, 15 Dec 2025 21:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e89c8b5fd1284ead2b63564ba79b930853662954d8dc82bfe01da7e1989113f`  
		Last Modified: Mon, 15 Dec 2025 21:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e49af2c974ad83ad55b4b44edbceb941a8356738af0c661bf44ec20b3f68c4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386e1b9355b4ee549be27edab692905aba2e5643739a3962fe5541973efd8b92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:56 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263b2b1d6e00611a009470a5e6c157ed0f005dead6fdc5343d40c17a5c89989a`  
		Last Modified: Mon, 15 Dec 2025 19:29:47 GMT  
		Size: 149.8 MB (149821981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82ce11b8ab22af2550cfd8dd0bda0535a9b282c189088e2b53ef8ae91d7e35`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ac1a82b7183428d26f4c85130380e6f813ad98d42c649345b6012616bbd0a`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e193941b5b441906dc3bc62458716e36d7e2d87656b0f221499cab4acccf00`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327eef58bc79a5f8ef34349f4a48f02bf17d3de10b2ebfc9fc7c580eea1c89`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a563353501f74fb1e5911728c89d06ce1cf70169b156bddcd288278092ea66c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:8dd3f419410d61586f8040128d81cac4c4e5bea6416df22b2db77cad724f8213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e8f0df4aed567043ecef4c2f04a3927975d93f92aec3d006333ce3de04e0d5`

```dockerfile
```

-	Layers:
	-	`sha256:b627ca132cfd98bd44a00d1c7f926fe11c029a623b007adc63cba8c2def09cb4`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaea1d0720139b2b23b37c4dad6ef4b068aa322a0f5171aa266b7a37422c92a`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.2`

```console
$ docker pull crate@sha256:68d1430b4f7edf386dcaeb01d52b18d92d595da2a3012cb5a80b2e56579b1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.2` - linux; amd64

```console
$ docker pull crate@sha256:03755e49eb92ae8eb1d7acc49092a05b6502092caedb5339174b22f67f35709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5242d7e52462d870dd44bc64aa0d685a59bfe7c86e5145e0e634dd198a5aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:57 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ced334c44f4de2a971bd22e1992bd6b0c842659e52fc9e255fd46337df525`  
		Last Modified: Mon, 15 Dec 2025 21:39:33 GMT  
		Size: 149.1 MB (149133517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7111a74856498548b678c9cb798ca45fbec416115cb9472774d5cb902a1cd1`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666a64ebf108b2bbfd8f845c7510d51aa7b19993cd83bcf5d3c7288ad3982d5`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d862f94a754e253e94e266b073be3fe868359c5fb4e3671943799233a67d11`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c1baaaba5c1a5127f7301c826ffb775362c6a3b3f9b611dda2fad16ed28ec`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150126d40904960df7e55865dc704e4f7ab9b1435a671f51840b9a8373e9748c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.2` - unknown; unknown

```console
$ docker pull crate@sha256:acbb49761e5d8ba0a18936d9b890cab96742b70ef486ac924cfe2eb50163923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056c1346f8a30d4061ef1f68698acfe20196c9a24ab4903c071318a960a9d07`

```dockerfile
```

-	Layers:
	-	`sha256:839de76bcc0825cd1a263ccae664ae2da6cc19324fd5bb0909f66319014847fe`  
		Last Modified: Mon, 15 Dec 2025 21:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e89c8b5fd1284ead2b63564ba79b930853662954d8dc82bfe01da7e1989113f`  
		Last Modified: Mon, 15 Dec 2025 21:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e49af2c974ad83ad55b4b44edbceb941a8356738af0c661bf44ec20b3f68c4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386e1b9355b4ee549be27edab692905aba2e5643739a3962fe5541973efd8b92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:56 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263b2b1d6e00611a009470a5e6c157ed0f005dead6fdc5343d40c17a5c89989a`  
		Last Modified: Mon, 15 Dec 2025 19:29:47 GMT  
		Size: 149.8 MB (149821981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82ce11b8ab22af2550cfd8dd0bda0535a9b282c189088e2b53ef8ae91d7e35`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ac1a82b7183428d26f4c85130380e6f813ad98d42c649345b6012616bbd0a`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e193941b5b441906dc3bc62458716e36d7e2d87656b0f221499cab4acccf00`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327eef58bc79a5f8ef34349f4a48f02bf17d3de10b2ebfc9fc7c580eea1c89`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a563353501f74fb1e5911728c89d06ce1cf70169b156bddcd288278092ea66c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.2` - unknown; unknown

```console
$ docker pull crate@sha256:8dd3f419410d61586f8040128d81cac4c4e5bea6416df22b2db77cad724f8213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e8f0df4aed567043ecef4c2f04a3927975d93f92aec3d006333ce3de04e0d5`

```dockerfile
```

-	Layers:
	-	`sha256:b627ca132cfd98bd44a00d1c7f926fe11c029a623b007adc63cba8c2def09cb4`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaea1d0720139b2b23b37c4dad6ef4b068aa322a0f5171aa266b7a37422c92a`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:68d1430b4f7edf386dcaeb01d52b18d92d595da2a3012cb5a80b2e56579b1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:03755e49eb92ae8eb1d7acc49092a05b6502092caedb5339174b22f67f35709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5242d7e52462d870dd44bc64aa0d685a59bfe7c86e5145e0e634dd198a5aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:57 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ced334c44f4de2a971bd22e1992bd6b0c842659e52fc9e255fd46337df525`  
		Last Modified: Mon, 15 Dec 2025 21:39:33 GMT  
		Size: 149.1 MB (149133517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7111a74856498548b678c9cb798ca45fbec416115cb9472774d5cb902a1cd1`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666a64ebf108b2bbfd8f845c7510d51aa7b19993cd83bcf5d3c7288ad3982d5`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d862f94a754e253e94e266b073be3fe868359c5fb4e3671943799233a67d11`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c1baaaba5c1a5127f7301c826ffb775362c6a3b3f9b611dda2fad16ed28ec`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150126d40904960df7e55865dc704e4f7ab9b1435a671f51840b9a8373e9748c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:acbb49761e5d8ba0a18936d9b890cab96742b70ef486ac924cfe2eb50163923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056c1346f8a30d4061ef1f68698acfe20196c9a24ab4903c071318a960a9d07`

```dockerfile
```

-	Layers:
	-	`sha256:839de76bcc0825cd1a263ccae664ae2da6cc19324fd5bb0909f66319014847fe`  
		Last Modified: Mon, 15 Dec 2025 21:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e89c8b5fd1284ead2b63564ba79b930853662954d8dc82bfe01da7e1989113f`  
		Last Modified: Mon, 15 Dec 2025 21:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e49af2c974ad83ad55b4b44edbceb941a8356738af0c661bf44ec20b3f68c4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386e1b9355b4ee549be27edab692905aba2e5643739a3962fe5541973efd8b92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:56 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263b2b1d6e00611a009470a5e6c157ed0f005dead6fdc5343d40c17a5c89989a`  
		Last Modified: Mon, 15 Dec 2025 19:29:47 GMT  
		Size: 149.8 MB (149821981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82ce11b8ab22af2550cfd8dd0bda0535a9b282c189088e2b53ef8ae91d7e35`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ac1a82b7183428d26f4c85130380e6f813ad98d42c649345b6012616bbd0a`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e193941b5b441906dc3bc62458716e36d7e2d87656b0f221499cab4acccf00`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327eef58bc79a5f8ef34349f4a48f02bf17d3de10b2ebfc9fc7c580eea1c89`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a563353501f74fb1e5911728c89d06ce1cf70169b156bddcd288278092ea66c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:8dd3f419410d61586f8040128d81cac4c4e5bea6416df22b2db77cad724f8213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e8f0df4aed567043ecef4c2f04a3927975d93f92aec3d006333ce3de04e0d5`

```dockerfile
```

-	Layers:
	-	`sha256:b627ca132cfd98bd44a00d1c7f926fe11c029a623b007adc63cba8c2def09cb4`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaea1d0720139b2b23b37c4dad6ef4b068aa322a0f5171aa266b7a37422c92a`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
