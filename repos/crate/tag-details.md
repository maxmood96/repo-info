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
-	[`crate:5.7.1`](#crate571)
-	[`crate:latest`](#cratelatest)

## `crate:5.4`

```console
$ docker pull crate@sha256:503f0f2f356bed160625925f37329afd9dff4ed48ff59cf5225f8e72bdbc7eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:bbefdf4ba06c24030bf051534475e1dfecbc7f489930a10ff26289a27c5f58e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300446036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0072fef66c22b253821d79867e1398eb16383c574f944d96677be8539d11ede7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 18:39:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:43 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:43 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 18:39:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d26ddb93039dcc46edf76bce535731e479f81e3a6c127590d47ede874ffaa`  
		Last Modified: Mon, 06 May 2024 18:41:20 GMT  
		Size: 229.6 MB (229566553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994d76ddcb7e66f097f41facfc438a1c1c1a734f664b80191aa34960f22748bc`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e413eb84a0a784d0984bdb9d65e49a77961028e8d1b1c4cbff3246c772d56762`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6094c69e5e56b3ea58dc87a35c23cbf1bd2c5d34668c217801d902c2de26cd`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f337136039046a41bbfe342aa28e2e43b24451992b18c3e1b32bd4539df39100`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431eba8c4925bc231f3439488a4c242d876061688f2ae91ed1a66224482bfaa5`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c57f6b8e1f46e2354900fe1d6c244879c6bb0ff143c6d0f5a12698038c8702e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297338574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55f1f7305ae3b466f3b25d99a74d3b6bf08c18b9683590193947a6bf1c563fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:13:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 12 Apr 2024 02:13:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:13:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:13:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:13:41 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:13:41 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:13:41 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:13:41 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:13:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:13:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:13:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 12 Apr 2024 02:13:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:13:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:13:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd44257adf171087eb42fe4c5b40f9d25b401db906a7f8200ca05fe07b7f27`  
		Last Modified: Fri, 12 Apr 2024 02:15:27 GMT  
		Size: 227.9 MB (227888520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd5811e28a5fb9b4f7161fd6f4a9271c3c1485a4f109115c6a3e000a54f1a5d`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2594ec5d866322efefb23d57ee4dc060f234d952d939aa0784341a76e3be3eea`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07350fda87bbdf2f91bd6eb7a5759bd27ccf4f76f32e4a92780d83de1720d77`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0189ecc03467feb832542a1602960a61dd5fcfb13afa2d6b52b09d382386ab`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d180a78d85b0240189d585285cef4d09cb8fc578292fbd22788e8e9184891f3`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:503f0f2f356bed160625925f37329afd9dff4ed48ff59cf5225f8e72bdbc7eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:bbefdf4ba06c24030bf051534475e1dfecbc7f489930a10ff26289a27c5f58e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300446036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0072fef66c22b253821d79867e1398eb16383c574f944d96677be8539d11ede7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 18:39:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:43 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:43 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 18:39:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d26ddb93039dcc46edf76bce535731e479f81e3a6c127590d47ede874ffaa`  
		Last Modified: Mon, 06 May 2024 18:41:20 GMT  
		Size: 229.6 MB (229566553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994d76ddcb7e66f097f41facfc438a1c1c1a734f664b80191aa34960f22748bc`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e413eb84a0a784d0984bdb9d65e49a77961028e8d1b1c4cbff3246c772d56762`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6094c69e5e56b3ea58dc87a35c23cbf1bd2c5d34668c217801d902c2de26cd`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f337136039046a41bbfe342aa28e2e43b24451992b18c3e1b32bd4539df39100`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431eba8c4925bc231f3439488a4c242d876061688f2ae91ed1a66224482bfaa5`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c57f6b8e1f46e2354900fe1d6c244879c6bb0ff143c6d0f5a12698038c8702e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297338574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55f1f7305ae3b466f3b25d99a74d3b6bf08c18b9683590193947a6bf1c563fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:13:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 12 Apr 2024 02:13:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:13:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:13:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:13:41 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:13:41 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:13:41 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:13:41 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:13:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:13:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:13:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 12 Apr 2024 02:13:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:13:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:13:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd44257adf171087eb42fe4c5b40f9d25b401db906a7f8200ca05fe07b7f27`  
		Last Modified: Fri, 12 Apr 2024 02:15:27 GMT  
		Size: 227.9 MB (227888520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd5811e28a5fb9b4f7161fd6f4a9271c3c1485a4f109115c6a3e000a54f1a5d`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2594ec5d866322efefb23d57ee4dc060f234d952d939aa0784341a76e3be3eea`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07350fda87bbdf2f91bd6eb7a5759bd27ccf4f76f32e4a92780d83de1720d77`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0189ecc03467feb832542a1602960a61dd5fcfb13afa2d6b52b09d382386ab`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d180a78d85b0240189d585285cef4d09cb8fc578292fbd22788e8e9184891f3`  
		Last Modified: Fri, 12 Apr 2024 02:15:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:efab050f105f58fec53dbceca6c3a4f98e10486c7a2e6a44247b1a42b617b092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1c7d34306a5609ed8906ef7983cf6d683756c0fb174521855022eba2f082f0cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185752368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04921b8b6e6ddf875cb82ad7b7593094d2eaec1d86c14ead1f0ae657f819b7dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:13:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 12 Apr 2024 02:13:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:13:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:13:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:13:11 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:13:11 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:13:11 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:13:12 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:13:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 12 Apr 2024 02:13:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:13:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:13:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63129be0f2b1aa9201867f1486ab2ec8607f4eaeb8b63f525973228342c9d91f`  
		Last Modified: Fri, 12 Apr 2024 02:15:00 GMT  
		Size: 116.3 MB (116302311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f19b12a1785097dcb091f945a1273dad0b9462783e98b45037295727bed6`  
		Last Modified: Fri, 12 Apr 2024 02:14:52 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f240b8a722997f79e72817f408dac89c137f35a1861c170b8eef74856c5d593b`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125670c4abd7ac812a7231e59737bcc136799b6f2c06adff6aced0dd0765d6a`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a996f2eeef75e792572c81dd4feca8cc2a3499959482fcc8dee3b138b5a117`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cf236df8f146db874e4ab00b6607bc37ce59347159f2749fdc72b43f011b4`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.4`

```console
$ docker pull crate@sha256:efab050f105f58fec53dbceca6c3a4f98e10486c7a2e6a44247b1a42b617b092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1c7d34306a5609ed8906ef7983cf6d683756c0fb174521855022eba2f082f0cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185752368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04921b8b6e6ddf875cb82ad7b7593094d2eaec1d86c14ead1f0ae657f819b7dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:13:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 12 Apr 2024 02:13:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:13:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:13:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:13:11 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:13:11 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:13:11 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:13:12 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:13:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 12 Apr 2024 02:13:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:13:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:13:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63129be0f2b1aa9201867f1486ab2ec8607f4eaeb8b63f525973228342c9d91f`  
		Last Modified: Fri, 12 Apr 2024 02:15:00 GMT  
		Size: 116.3 MB (116302311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f19b12a1785097dcb091f945a1273dad0b9462783e98b45037295727bed6`  
		Last Modified: Fri, 12 Apr 2024 02:14:52 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f240b8a722997f79e72817f408dac89c137f35a1861c170b8eef74856c5d593b`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125670c4abd7ac812a7231e59737bcc136799b6f2c06adff6aced0dd0765d6a`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a996f2eeef75e792572c81dd4feca8cc2a3499959482fcc8dee3b138b5a117`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cf236df8f146db874e4ab00b6607bc37ce59347159f2749fdc72b43f011b4`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:efab050f105f58fec53dbceca6c3a4f98e10486c7a2e6a44247b1a42b617b092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1c7d34306a5609ed8906ef7983cf6d683756c0fb174521855022eba2f082f0cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185752368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04921b8b6e6ddf875cb82ad7b7593094d2eaec1d86c14ead1f0ae657f819b7dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:13:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 12 Apr 2024 02:13:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:13:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:13:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:13:11 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:13:11 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:13:11 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:13:12 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:13:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:13:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 12 Apr 2024 02:13:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:13:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:13:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63129be0f2b1aa9201867f1486ab2ec8607f4eaeb8b63f525973228342c9d91f`  
		Last Modified: Fri, 12 Apr 2024 02:15:00 GMT  
		Size: 116.3 MB (116302311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f19b12a1785097dcb091f945a1273dad0b9462783e98b45037295727bed6`  
		Last Modified: Fri, 12 Apr 2024 02:14:52 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f240b8a722997f79e72817f408dac89c137f35a1861c170b8eef74856c5d593b`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125670c4abd7ac812a7231e59737bcc136799b6f2c06adff6aced0dd0765d6a`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a996f2eeef75e792572c81dd4feca8cc2a3499959482fcc8dee3b138b5a117`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cf236df8f146db874e4ab00b6607bc37ce59347159f2749fdc72b43f011b4`  
		Last Modified: Fri, 12 Apr 2024 02:14:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:bd3cc325d54f1fcdbf8f864c4e39dbedbee61e4317846e56b05b684e39be0308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:3f84b5d0d960756eb662a2b96030bb168d1b24f1ecd99dc94ec44469b318dcae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188797435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555285bc5a8c9bb5ad1a81315430bddf1f14ffd4c023c29532890aeb949c6b89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 18:38:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:49 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:49 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:49 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:49 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 18:38:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7929982749cf81ce40be549b5d6960bc59a4013ba224a4f611c48f2ad01f673`  
		Last Modified: Mon, 06 May 2024 18:40:31 GMT  
		Size: 117.9 MB (117916907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f891f5354b59ee2d35bb762fcc6ea2f1a6e40841b13c3a804f243d718b380e10`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c80fb2eb604a92656588693e6d63358f8811319ba52ad9b8a85be702114e73b`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a05359db030c1e7f0afcfaa2a9b31f5fa205ce1289f8b1c1c4a79556b660b4`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a37d04b4905fcf45b457566bbfff92b8cfd4d319d960e5b42c4c710b204e0e`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314a0cbaa07e760507b8b29bce57e036d67bcc0b253227712bd6c54846630e02`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:be222d5c95546a9eba0ed2c5aa3553fc53028d1bec4a43d7589b3c6e7207f7af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187424511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388fcbf2fc56dc7d70ac20ee60a958bd4543dede538a3b7c5681e76e754a120e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:12:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 02:12:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:12:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:12:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:12:49 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:12:49 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:12:49 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:12:49 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:12:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:12:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:12:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 02:12:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:12:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1686b4bb65d3e8d847fea26425b0c8a7b9f29053a586e39f950013d9e5dde5`  
		Last Modified: Fri, 12 Apr 2024 02:14:40 GMT  
		Size: 118.0 MB (117973419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e844ed34289eda813289d0b228073384424a5d1ab9247d869c7304656a7091`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 1.9 MB (1940656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6574ba80367b745d5cb4a42612babbc0c334a5409046da6ee8953ddb7bc0d`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a756271070466b99015a49a29240cd60e260d271dfcf8e0c8c1629e2bceca6`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb926faadc2da675147b97e4305a15d48d49ce12450072a81dbbdc881debfd27`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3e50353b130bfe837910c7cd483af7a736ab39efa98d4cf16e6386cf97a0e`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.5`

```console
$ docker pull crate@sha256:b2d09539e220feb5fcdc1aca22196229f474609e8778987240151da21defa1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:3f84b5d0d960756eb662a2b96030bb168d1b24f1ecd99dc94ec44469b318dcae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188797435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555285bc5a8c9bb5ad1a81315430bddf1f14ffd4c023c29532890aeb949c6b89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 18:38:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:49 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:49 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:49 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:49 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 18:38:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7929982749cf81ce40be549b5d6960bc59a4013ba224a4f611c48f2ad01f673`  
		Last Modified: Mon, 06 May 2024 18:40:31 GMT  
		Size: 117.9 MB (117916907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f891f5354b59ee2d35bb762fcc6ea2f1a6e40841b13c3a804f243d718b380e10`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c80fb2eb604a92656588693e6d63358f8811319ba52ad9b8a85be702114e73b`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a05359db030c1e7f0afcfaa2a9b31f5fa205ce1289f8b1c1c4a79556b660b4`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a37d04b4905fcf45b457566bbfff92b8cfd4d319d960e5b42c4c710b204e0e`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314a0cbaa07e760507b8b29bce57e036d67bcc0b253227712bd6c54846630e02`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7`

```console
$ docker pull crate@sha256:d099d30c9debf65c232b328c7ad697448b645bbe1c0fae9181800e16b064e772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f2b3ef4fd2d1d64a89be48c387b1c09e0a8115020001302aa1767e2cadebe833
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197147416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b76d289222f8b2f4468ba0652031574c43dff82c9e5ebbce17704808baa8816`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Wed, 24 Apr 2024 17:46:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.0.tar.gz.asc crate-5.7.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.0.tar.gz.asc     && tar -xf crate-5.7.0.tar.gz -C /crate --strip-components=1     && rm crate-5.7.0.tar.gz
# Wed, 24 Apr 2024 17:46:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 24 Apr 2024 17:46:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 17:46:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Apr 2024 17:46:19 GMT
RUN mkdir -p /data/data /data/log
# Wed, 24 Apr 2024 17:46:19 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 17:46:19 GMT
WORKDIR /data
# Wed, 24 Apr 2024 17:46:19 GMT
EXPOSE 4200 4300 5432
# Wed, 24 Apr 2024 17:46:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 24 Apr 2024 17:46:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 24 Apr 2024 17:46:20 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T13:52:59.820951 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.0
# Wed, 24 Apr 2024 17:46:20 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 24 Apr 2024 17:46:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 17:46:20 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa2f10751b0ac7c8a7c01db70a97f4d9f7a3fbb9e755613d5d34b53183adf1`  
		Last Modified: Wed, 24 Apr 2024 17:46:46 GMT  
		Size: 127.7 MB (127696326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3556aaa60dbfb28179caa24a6d5422e19afe0ce1873d7c220b50ca36d7be3`  
		Last Modified: Wed, 24 Apr 2024 17:46:37 GMT  
		Size: 1.9 MB (1940649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846b486be3ffefdc054a456273029832851d05e29bea263afa1e08cf1b2c208`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d99eabe2f67add0759c8477bc4fd37a146ac01198bc1da8439ad1a3a66df9dc`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef8415a4479e098423276404fbeb115e1eef87c4cc681aacc4a9def849b162`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b34e77a8db6d715ccfb0ffd77732ccd3cc98e3c64ce20ccf3a98f0d20a33874`  
		Last Modified: Wed, 24 Apr 2024 17:46:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7.1`

```console
$ docker pull crate@sha256:c78c70f940bdd450900f628c31575fd530da40ba50aec590319adeb8bbbc7d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `crate:5.7.1` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:d099d30c9debf65c232b328c7ad697448b645bbe1c0fae9181800e16b064e772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f2b3ef4fd2d1d64a89be48c387b1c09e0a8115020001302aa1767e2cadebe833
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197147416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b76d289222f8b2f4468ba0652031574c43dff82c9e5ebbce17704808baa8816`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Wed, 24 Apr 2024 17:46:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.0.tar.gz.asc crate-5.7.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.0.tar.gz.asc     && tar -xf crate-5.7.0.tar.gz -C /crate --strip-components=1     && rm crate-5.7.0.tar.gz
# Wed, 24 Apr 2024 17:46:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 24 Apr 2024 17:46:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 17:46:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Apr 2024 17:46:19 GMT
RUN mkdir -p /data/data /data/log
# Wed, 24 Apr 2024 17:46:19 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 17:46:19 GMT
WORKDIR /data
# Wed, 24 Apr 2024 17:46:19 GMT
EXPOSE 4200 4300 5432
# Wed, 24 Apr 2024 17:46:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 24 Apr 2024 17:46:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 24 Apr 2024 17:46:20 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T13:52:59.820951 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.0
# Wed, 24 Apr 2024 17:46:20 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 24 Apr 2024 17:46:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 17:46:20 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa2f10751b0ac7c8a7c01db70a97f4d9f7a3fbb9e755613d5d34b53183adf1`  
		Last Modified: Wed, 24 Apr 2024 17:46:46 GMT  
		Size: 127.7 MB (127696326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3556aaa60dbfb28179caa24a6d5422e19afe0ce1873d7c220b50ca36d7be3`  
		Last Modified: Wed, 24 Apr 2024 17:46:37 GMT  
		Size: 1.9 MB (1940649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b846b486be3ffefdc054a456273029832851d05e29bea263afa1e08cf1b2c208`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d99eabe2f67add0759c8477bc4fd37a146ac01198bc1da8439ad1a3a66df9dc`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef8415a4479e098423276404fbeb115e1eef87c4cc681aacc4a9def849b162`  
		Last Modified: Wed, 24 Apr 2024 17:46:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b34e77a8db6d715ccfb0ffd77732ccd3cc98e3c64ce20ccf3a98f0d20a33874`  
		Last Modified: Wed, 24 Apr 2024 17:46:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
