## `crate:latest`

```console
$ docker pull crate@sha256:f9d72d76c78836f3bb9c9ad423f065bb4df683b6bb6eed9a160beea4e6ac3255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:df824933c4be1d912229786ab34c92719d4b924abf4e1c0e9144e0e2f7544dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245938958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eea202967fd6810dd8966c97b3c1f91c81f270330f0fc8ba471ebab2a2d5af5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:01:21 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:01:21 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:25:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:25:37 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:25:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:25:40 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:25:40 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:25:40 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:25:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:25:40 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:df6cec240bd2d043c7a684d78ecbba543cf1e8d7b30df15e7534a37c94c8ea28`  
		Last Modified: Tue, 28 Apr 2026 00:01:38 GMT  
		Size: 68.6 MB (68552440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50537d3e35d5db283eea8a2e0650d49f4045de9041e7fb9574e8e7d749c0a5`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 18.4 MB (18367506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119834775cb5dab48b3e2c3ac7ca2a1df3b548546b30b7654c6e1b5d7439a18`  
		Last Modified: Thu, 30 Apr 2026 23:26:03 GMT  
		Size: 151.3 MB (151317597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f521aac87aa3fb6f908eb00e514c4d15c451ea21ed7fa6b53796123fcbecf1d`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 7.7 MB (7699535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6f793a004d96b30d2309cebabd4d689355975301f9d3c795ef5d5a24d25eb`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e449a28970ee3ec5483dce75c08f8e24ed220c62dad40d2fecef58bad31da5`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310ea6165f6bf994ef651fa9d8baf5b61de593e8507b20c92efbf1309c5e7ff`  
		Last Modified: Thu, 30 Apr 2026 23:26:01 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cb11a9d82750eb52f895edb7281c15be9782c1c3f9f1d9380423ad8d2706d`  
		Last Modified: Thu, 30 Apr 2026 23:26:02 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:03ea6a7f6f388bde09db4802b45dd6633acfb61f47cd80ddaf868b2deebd9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4c48fd29935747a8e0739d37fdc5f01e3b5e0981132b6b0a3ec1db7353d13c`

```dockerfile
```

-	Layers:
	-	`sha256:5bf06b0c62586a51ed4f06cd6c52775b0cb19310a80d5c98716e04a41a14efb4`  
		Last Modified: Thu, 30 Apr 2026 23:26:00 GMT  
		Size: 6.7 MB (6656883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7457cfe3bbdf651b75584d9f44a905a19e5311cbe24d74bc068d1071d1e5ad3`  
		Last Modified: Thu, 30 Apr 2026 23:25:59 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1e42ebb83d303420863d862142cb0c7692b2cac278aa434d7e8daa1f7ad91c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242536163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde23c10d541527a8290cb623fadbdeb597ca144bbdec9a73539fe19455d8b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Apr 2026 00:02:02 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 28 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Apr 2026 23:26:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Apr 2026 23:26:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
VOLUME [/data]
# Thu, 30 Apr 2026 23:26:22 GMT
WORKDIR /data
# Thu, 30 Apr 2026 23:26:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Thu, 30 Apr 2026 23:26:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Apr 2026 23:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:82db57c44d8fa677f613b9d3d1a50032dbc9033d14583e1766667f999fa3dc48`  
		Last Modified: Tue, 28 Apr 2026 00:02:21 GMT  
		Size: 67.1 MB (67138087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e79055875104e491b1adaa789299c82fcc794fd3b0495f5b51ca807812d2d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 18.4 MB (18416446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e091587ec4dc15bdd40ff5c61a1060f08f8a3f72575ddd13becf423a86ec3648`  
		Last Modified: Thu, 30 Apr 2026 23:26:48 GMT  
		Size: 149.3 MB (149282817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ea96a8025503f892c67b0a96e651ac3c26be6236f7b25b171da0cdba59db30`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 7.7 MB (7696932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e57c29095ed18fe8a10de33548b6f3e2673f80954a32bd4a58ac1e9a7fce1`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a0bd00aab25109bfb071eb55234565307272e71f45338ed1aa1535154dc4e`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce01436e258c79187258e4970fec0062061030e17305af6f604b81d4696d36`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42064fcf1b7c6a2ea1a881d5782b11c87ad1655601236bcb7522de8a3b77e06`  
		Last Modified: Thu, 30 Apr 2026 23:26:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:486f0d0b1d300757b2d88cec3f6330325a1c9b44d8e64d12da3639e70ba15b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a428e8d8b417170fb8c135d9f4524a5db5fd71818ef330049d2011da61afac`

```dockerfile
```

-	Layers:
	-	`sha256:2d6e9995c4dd26d0a352584ff180fa467bc70e05b1a147cc8df6642f82020e76`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 6.7 MB (6654807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce6f847c0415d626da65c7195c89c4471634b94720d3426c883089188821587`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 21.8 KB (21776 bytes)  
		MIME: application/vnd.in-toto+json
