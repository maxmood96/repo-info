<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.3`](#crate53)
-	[`crate:5.3.9`](#crate539)
-	[`crate:5.4`](#crate54)
-	[`crate:5.4.8`](#crate548)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.5`](#crate555)
-	[`crate:5.6`](#crate56)
-	[`crate:5.6.4`](#crate564)
-	[`crate:latest`](#cratelatest)

## `crate:5.3`

```console
$ docker pull crate@sha256:8e547d125ddffcdd4ac4d3243edc3d67af441f743cf6d5e73641e1a1547a74f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:ba0f6b18191316a89e7157bebe00e3100d0ba6ec26049b481602c1852628e3f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297908088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa8f5108aef981010505705a027af12110438f1899af7ce14656e2c97e98c67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:42:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 12 Apr 2024 01:42:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:42:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:42:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:42:07 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:42:07 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:42:08 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:42:08 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:42:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:42:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:42:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 12 Apr 2024 01:42:08 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:42:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce9850d7c31a0cfe68e41f1ffe83d330757024bf52995af9cc96b3e7a4cf2d`  
		Last Modified: Fri, 12 Apr 2024 01:43:47 GMT  
		Size: 227.3 MB (227342932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b223cc5fe639de264ddf5b2ddb4110d66c4bd87a30e4069d8a339fb15e2b3f5`  
		Last Modified: Fri, 12 Apr 2024 01:43:30 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cec6cdde8f9807b44fff854a7ec84e620cd36c03a72b9ad6de3ead5997b9bd5`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70df5879521c071964187fdcd5e30f4c1efbae401c33c83ea39917eb4976d6a5`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c363865e48bb6552c2a7d92501c6f6f46a22c2566be5b9634e90905f98ccd95`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53662c20931d42a955b24d261081a38709868e04aa02def050e71ff7b8b1c417`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0c29c3e17566fadf09d35b8d5f4ecf9410dafcb0e80aea3e48810375cabdae5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295536528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb0ad923d19a2647a002b8ce21fb25cac8786c7c841bccf4454c349acda22d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:41:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 02 Feb 2024 19:41:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:41:13 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:41:13 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:41:14 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:41:14 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:41:14 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:41:14 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:41:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 02 Feb 2024 19:41:14 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:41:15 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008b21a36f59421aa34b5133880f8db55f991c3c0c17010304f230f8e2d80a3`  
		Last Modified: Fri, 02 Feb 2024 19:42:57 GMT  
		Size: 226.1 MB (226079639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0649b35fe65ab29e8b2bdcfd5d93751391fee7cbffc92fdc42e4a5dd1585e6e4`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18d454ce9a92375340eab0386c1429deb281023c7d51acf41a0f9046ff3903`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996563eac46296a062dc9296c1aa1c86dc89618a53e0b2827244270cc33fdff8`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebc3e2f14052597c0e820b9029163e938225645f4938d83f90cb3db500eabba`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70acc361644181c57fefbabfa6a3c2d7ca1f9495fd82516f53db8aca79116b45`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.9`

```console
$ docker pull crate@sha256:8e547d125ddffcdd4ac4d3243edc3d67af441f743cf6d5e73641e1a1547a74f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.9` - linux; amd64

```console
$ docker pull crate@sha256:ba0f6b18191316a89e7157bebe00e3100d0ba6ec26049b481602c1852628e3f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297908088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa8f5108aef981010505705a027af12110438f1899af7ce14656e2c97e98c67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:42:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 12 Apr 2024 01:42:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:42:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:42:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:42:07 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:42:07 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:42:08 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:42:08 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:42:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:42:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:42:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 12 Apr 2024 01:42:08 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:42:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce9850d7c31a0cfe68e41f1ffe83d330757024bf52995af9cc96b3e7a4cf2d`  
		Last Modified: Fri, 12 Apr 2024 01:43:47 GMT  
		Size: 227.3 MB (227342932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b223cc5fe639de264ddf5b2ddb4110d66c4bd87a30e4069d8a339fb15e2b3f5`  
		Last Modified: Fri, 12 Apr 2024 01:43:30 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cec6cdde8f9807b44fff854a7ec84e620cd36c03a72b9ad6de3ead5997b9bd5`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70df5879521c071964187fdcd5e30f4c1efbae401c33c83ea39917eb4976d6a5`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c363865e48bb6552c2a7d92501c6f6f46a22c2566be5b9634e90905f98ccd95`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53662c20931d42a955b24d261081a38709868e04aa02def050e71ff7b8b1c417`  
		Last Modified: Fri, 12 Apr 2024 01:43:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0c29c3e17566fadf09d35b8d5f4ecf9410dafcb0e80aea3e48810375cabdae5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295536528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb0ad923d19a2647a002b8ce21fb25cac8786c7c841bccf4454c349acda22d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:41:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 02 Feb 2024 19:41:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:41:13 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:41:13 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:41:14 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:41:14 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:41:14 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:41:14 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:41:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 02 Feb 2024 19:41:14 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:41:15 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008b21a36f59421aa34b5133880f8db55f991c3c0c17010304f230f8e2d80a3`  
		Last Modified: Fri, 02 Feb 2024 19:42:57 GMT  
		Size: 226.1 MB (226079639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0649b35fe65ab29e8b2bdcfd5d93751391fee7cbffc92fdc42e4a5dd1585e6e4`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18d454ce9a92375340eab0386c1429deb281023c7d51acf41a0f9046ff3903`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996563eac46296a062dc9296c1aa1c86dc89618a53e0b2827244270cc33fdff8`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebc3e2f14052597c0e820b9029163e938225645f4938d83f90cb3db500eabba`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70acc361644181c57fefbabfa6a3c2d7ca1f9495fd82516f53db8aca79116b45`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:5c1951ff4681865316489a49ad799e3d5d3b8e0ae5493649a30471a106b02a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:20a3901fe168de221e72559e32aed47a0b8f2a0722a153803b026cb3ac4f926b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300131619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e550cf5cd08dd82850f8c5c4b517cec2f91898721df8812c0ada798b7b6900`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:41:30 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 12 Apr 2024 01:41:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:41:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:41:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:41:33 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:41:33 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:41:34 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:41:34 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:41:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:41:34 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:41:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 12 Apr 2024 01:41:34 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:41:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:41:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830ebd5d0b8b5c70f3fdffceaceac4a33b3acd4cb616c5ef2f410438b629f88`  
		Last Modified: Fri, 12 Apr 2024 01:43:20 GMT  
		Size: 229.6 MB (229566466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079e073787715b5f0b16b083b434f23d5807878af5e0885d788aed84aa5f1571`  
		Last Modified: Fri, 12 Apr 2024 01:43:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd736fdb04364af1b104cbf1c996586213377ebe55413b891fbec956321c55`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc717e09a9fdb0a7c273a02f138c621d81a07639a8e6e8e0c51dfa73cc4cbf`  
		Last Modified: Fri, 12 Apr 2024 01:43:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8969d8c9083c7cb384fc476df039293460a2f4ba4f2931e2326534e6e9c0f84`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f392e91703479b52b9d242b85022ee91181685912a75ef111050cfb59965134`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d656c986391c85c05aff68cf1198367c555f91116fd4bd16e807103d42bbfc6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297345377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf3aea2585b5a7a1ae7cc979cd7645a8e022492d3ea863a728853130a07f392`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 02 Feb 2024 19:40:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:40 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:41 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:41 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:41 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 02 Feb 2024 19:40:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e68902d7118bd0caf3a08e52244bb28722abc67a641cad543fb4fddc629c84b`  
		Last Modified: Fri, 02 Feb 2024 19:42:31 GMT  
		Size: 227.9 MB (227888484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26063e3be7e402998d414a768e4b0c3e99888b581600a175f8119a409d1af422`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3562c2eff4166f9dceb602d682d97d03e0a789da6e2fbf568b5df7e227e44c80`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a4ff9f5ac4c419037c9b3bf868889cf4f518f70a090e0497a2946025e4907b`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0d01738270dd5442d8f1ae77834531c8594f37b5fe4970f4e90dba00d62eff`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab623f974e09f711c789fdde33ca0037c53c22ed52e6fdea011b836cdd3d5b5c`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:5c1951ff4681865316489a49ad799e3d5d3b8e0ae5493649a30471a106b02a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:20a3901fe168de221e72559e32aed47a0b8f2a0722a153803b026cb3ac4f926b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300131619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e550cf5cd08dd82850f8c5c4b517cec2f91898721df8812c0ada798b7b6900`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:41:30 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 12 Apr 2024 01:41:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:41:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:41:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:41:33 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:41:33 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:41:34 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:41:34 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:41:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:41:34 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:41:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 12 Apr 2024 01:41:34 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:41:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:41:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830ebd5d0b8b5c70f3fdffceaceac4a33b3acd4cb616c5ef2f410438b629f88`  
		Last Modified: Fri, 12 Apr 2024 01:43:20 GMT  
		Size: 229.6 MB (229566466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079e073787715b5f0b16b083b434f23d5807878af5e0885d788aed84aa5f1571`  
		Last Modified: Fri, 12 Apr 2024 01:43:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd736fdb04364af1b104cbf1c996586213377ebe55413b891fbec956321c55`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc717e09a9fdb0a7c273a02f138c621d81a07639a8e6e8e0c51dfa73cc4cbf`  
		Last Modified: Fri, 12 Apr 2024 01:43:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8969d8c9083c7cb384fc476df039293460a2f4ba4f2931e2326534e6e9c0f84`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f392e91703479b52b9d242b85022ee91181685912a75ef111050cfb59965134`  
		Last Modified: Fri, 12 Apr 2024 01:43:01 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d656c986391c85c05aff68cf1198367c555f91116fd4bd16e807103d42bbfc6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297345377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf3aea2585b5a7a1ae7cc979cd7645a8e022492d3ea863a728853130a07f392`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 02 Feb 2024 19:40:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:40 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:41 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:41 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:41 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 02 Feb 2024 19:40:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e68902d7118bd0caf3a08e52244bb28722abc67a641cad543fb4fddc629c84b`  
		Last Modified: Fri, 02 Feb 2024 19:42:31 GMT  
		Size: 227.9 MB (227888484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26063e3be7e402998d414a768e4b0c3e99888b581600a175f8119a409d1af422`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3562c2eff4166f9dceb602d682d97d03e0a789da6e2fbf568b5df7e227e44c80`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a4ff9f5ac4c419037c9b3bf868889cf4f518f70a090e0497a2946025e4907b`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0d01738270dd5442d8f1ae77834531c8594f37b5fe4970f4e90dba00d62eff`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab623f974e09f711c789fdde33ca0037c53c22ed52e6fdea011b836cdd3d5b5c`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:d4bf9ffd719b796e5cb0c4ee1b38a1602a1389bf89f4e2d70ecb608d12b9ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:d47d73fb726f6cd9b8af1cd948c3df5ac4923dfc3f7ff3dc96afbf948d7088e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187332583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcba06883cdbdd67f69109bbc0b4f55eae790fbb13d3b53e69111f7179046be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 12 Apr 2024 01:41:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:41:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:41:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:41:02 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:41:02 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:41:02 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:41:02 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:41:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:41:02 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:41:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 12 Apr 2024 01:41:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:41:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:41:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae62fb68576ab55133309c9b282ab1f266bb4a9846c9b7e39e0f2f4804ce9`  
		Last Modified: Fri, 12 Apr 2024 01:42:54 GMT  
		Size: 116.8 MB (116767430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47fa7b3de1110e48561dbdf26830cc9c279855217e146055daa79a0a7a821f`  
		Last Modified: Fri, 12 Apr 2024 01:42:43 GMT  
		Size: 1.9 MB (1939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff542b0ce5fa41a4b2e003088226e7adc1aa0285750c7881a0f459065639ca56`  
		Last Modified: Fri, 12 Apr 2024 01:42:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa6e1b01bad363afa65e513af70164e32bc15507292dd66e91c38780480cfb4`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8991ace4c46a0bf4901f7cc3109b821cda07fec994f18f4aafcf29624ebf43`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450fe1859b6158e24b7831807b07dcd34321096541cc9b5f19ea8c9cbbf278a2`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:daa7929307eb30cbd91bf1b3b8b2f6cd47385c99fa34848ac73d1a0e866d3227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185758997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581ce29672c6cf7e735526aaf89c0fe9993a1ceaae2598e05a22172d4c64cb16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 02 Feb 2024 19:40:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:10 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:10 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:10 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:10 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 02 Feb 2024 19:40:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13154c493272245f778cf8550a7c76270148717b85acdfe67ff871933c516993`  
		Last Modified: Fri, 02 Feb 2024 19:42:06 GMT  
		Size: 116.3 MB (116302111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec45476da2cb4472f6b7ca93036e8647cec694600ef202a826cc4a1a2a57707`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7bdbff0a05616a0adb5914af746c0fd2d2f3054b466ca8f7ed59e3bf099bd6`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3592b40a987409a1cef456ec698ddf5c1042a6d6dd602ca0ddba3c0a615fc10`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f77e3b6f35959c33068168534f681e498c05aa44b1e6de9e90935e24c77dcc`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624cb721018ea071f6f8f31caf19caae4d71f6d1e87298a5487113bbe08362c1`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:d4bf9ffd719b796e5cb0c4ee1b38a1602a1389bf89f4e2d70ecb608d12b9ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:d47d73fb726f6cd9b8af1cd948c3df5ac4923dfc3f7ff3dc96afbf948d7088e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187332583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcba06883cdbdd67f69109bbc0b4f55eae790fbb13d3b53e69111f7179046be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 12 Apr 2024 01:41:01 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:41:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:41:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:41:02 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:41:02 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:41:02 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:41:02 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:41:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:41:02 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:41:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 12 Apr 2024 01:41:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:41:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:41:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae62fb68576ab55133309c9b282ab1f266bb4a9846c9b7e39e0f2f4804ce9`  
		Last Modified: Fri, 12 Apr 2024 01:42:54 GMT  
		Size: 116.8 MB (116767430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47fa7b3de1110e48561dbdf26830cc9c279855217e146055daa79a0a7a821f`  
		Last Modified: Fri, 12 Apr 2024 01:42:43 GMT  
		Size: 1.9 MB (1939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff542b0ce5fa41a4b2e003088226e7adc1aa0285750c7881a0f459065639ca56`  
		Last Modified: Fri, 12 Apr 2024 01:42:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa6e1b01bad363afa65e513af70164e32bc15507292dd66e91c38780480cfb4`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8991ace4c46a0bf4901f7cc3109b821cda07fec994f18f4aafcf29624ebf43`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450fe1859b6158e24b7831807b07dcd34321096541cc9b5f19ea8c9cbbf278a2`  
		Last Modified: Fri, 12 Apr 2024 01:42:42 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:daa7929307eb30cbd91bf1b3b8b2f6cd47385c99fa34848ac73d1a0e866d3227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185758997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581ce29672c6cf7e735526aaf89c0fe9993a1ceaae2598e05a22172d4c64cb16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 02 Feb 2024 19:40:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:10 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:10 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:10 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:10 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 02 Feb 2024 19:40:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13154c493272245f778cf8550a7c76270148717b85acdfe67ff871933c516993`  
		Last Modified: Fri, 02 Feb 2024 19:42:06 GMT  
		Size: 116.3 MB (116302111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec45476da2cb4472f6b7ca93036e8647cec694600ef202a826cc4a1a2a57707`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7bdbff0a05616a0adb5914af746c0fd2d2f3054b466ca8f7ed59e3bf099bd6`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3592b40a987409a1cef456ec698ddf5c1042a6d6dd602ca0ddba3c0a615fc10`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f77e3b6f35959c33068168534f681e498c05aa44b1e6de9e90935e24c77dcc`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624cb721018ea071f6f8f31caf19caae4d71f6d1e87298a5487113bbe08362c1`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:6870def05f3709b094c8645b0e369cb6cc0ff0c381394d4e4fe077f2404bfb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:e7565d09dd1793409875f1a38e086e7a22fb79f97db5f307061a8dc7469d43ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189001890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d9390ea0c9353669cf94f2a91fa3822666ef3639817087de9b94467040330`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 01:40:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:40:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:40:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:40:38 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:40:38 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:40:38 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:40:38 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:40:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 01:40:39 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:40:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:40:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124713450165b300a5564c7e7f867872efc20dcadcab0da7fefc54e38b26aa8f`  
		Last Modified: Fri, 12 Apr 2024 01:42:32 GMT  
		Size: 118.4 MB (118435699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33edd3abd1664a7ce0a32840f9984b5f7840358dbc7c1511e62420c42761380f`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 1.9 MB (1940654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a5daffa9b99902422d73fce700aa264995b940f35f6f2083de4b2213e54cac`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8081fd96df3d797219535bd2b24584437920b18d3fe62d3d24167cde96f166c`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d03402f6f939c724589ce530ebf44ba1046be714b06c83100fdff412eb565`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204840cd1dee42c195853f6537f7b20ee5881aa86fe55263592c76296dfead3`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:de1ff6ed2a98601e38f62c743f33a27d169cd9c1f15035ea910c1a60d475e941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187431393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfc031a9c2b52669bd47835d557c375c4b5360db0efd90f324976e415d7399`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 08 Apr 2024 20:05:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Mon, 08 Apr 2024 20:05:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 08 Apr 2024 20:05:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Apr 2024 20:05:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 08 Apr 2024 20:05:19 GMT
RUN mkdir -p /data/data /data/log
# Mon, 08 Apr 2024 20:05:19 GMT
VOLUME [/data]
# Mon, 08 Apr 2024 20:05:20 GMT
WORKDIR /data
# Mon, 08 Apr 2024 20:05:20 GMT
EXPOSE 4200 4300 5432
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 08 Apr 2024 20:05:20 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Mon, 08 Apr 2024 20:05:20 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 08 Apr 2024 20:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Apr 2024 20:05:20 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dee5275671aaa8bdf1898e77a728be2ea2873f94d2a55c963faf525e036fab`  
		Last Modified: Mon, 08 Apr 2024 20:05:49 GMT  
		Size: 118.0 MB (117973469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf1e040a1d7ddacecfa83cd4cc9a92dc9c4d74f159378e642118cb008a1e7bb`  
		Last Modified: Mon, 08 Apr 2024 20:05:40 GMT  
		Size: 1.9 MB (1940653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760dc81db632110ab8451a1c6c46336f90566a991d4357f947102f27d93b9b`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d2c01e11a2cf2bbc091943dab987292d4c921ff2876be9a86a1b40fe150a1`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e2a3a62a0c81a986c51f9ee82518d8db7b9fa28372a685febd15f03303741`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a952bb6db9283db3c5c64966db65d2e7765683cf7c0fbfa916e196b8e087d`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.4`

```console
$ docker pull crate@sha256:6870def05f3709b094c8645b0e369cb6cc0ff0c381394d4e4fe077f2404bfb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6.4` - linux; amd64

```console
$ docker pull crate@sha256:e7565d09dd1793409875f1a38e086e7a22fb79f97db5f307061a8dc7469d43ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189001890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d9390ea0c9353669cf94f2a91fa3822666ef3639817087de9b94467040330`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 01:40:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:40:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:40:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:40:38 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:40:38 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:40:38 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:40:38 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:40:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 01:40:39 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:40:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:40:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124713450165b300a5564c7e7f867872efc20dcadcab0da7fefc54e38b26aa8f`  
		Last Modified: Fri, 12 Apr 2024 01:42:32 GMT  
		Size: 118.4 MB (118435699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33edd3abd1664a7ce0a32840f9984b5f7840358dbc7c1511e62420c42761380f`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 1.9 MB (1940654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a5daffa9b99902422d73fce700aa264995b940f35f6f2083de4b2213e54cac`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8081fd96df3d797219535bd2b24584437920b18d3fe62d3d24167cde96f166c`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d03402f6f939c724589ce530ebf44ba1046be714b06c83100fdff412eb565`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204840cd1dee42c195853f6537f7b20ee5881aa86fe55263592c76296dfead3`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:de1ff6ed2a98601e38f62c743f33a27d169cd9c1f15035ea910c1a60d475e941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187431393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfc031a9c2b52669bd47835d557c375c4b5360db0efd90f324976e415d7399`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 08 Apr 2024 20:05:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Mon, 08 Apr 2024 20:05:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 08 Apr 2024 20:05:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Apr 2024 20:05:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 08 Apr 2024 20:05:19 GMT
RUN mkdir -p /data/data /data/log
# Mon, 08 Apr 2024 20:05:19 GMT
VOLUME [/data]
# Mon, 08 Apr 2024 20:05:20 GMT
WORKDIR /data
# Mon, 08 Apr 2024 20:05:20 GMT
EXPOSE 4200 4300 5432
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 08 Apr 2024 20:05:20 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Mon, 08 Apr 2024 20:05:20 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 08 Apr 2024 20:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Apr 2024 20:05:20 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dee5275671aaa8bdf1898e77a728be2ea2873f94d2a55c963faf525e036fab`  
		Last Modified: Mon, 08 Apr 2024 20:05:49 GMT  
		Size: 118.0 MB (117973469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf1e040a1d7ddacecfa83cd4cc9a92dc9c4d74f159378e642118cb008a1e7bb`  
		Last Modified: Mon, 08 Apr 2024 20:05:40 GMT  
		Size: 1.9 MB (1940653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760dc81db632110ab8451a1c6c46336f90566a991d4357f947102f27d93b9b`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d2c01e11a2cf2bbc091943dab987292d4c921ff2876be9a86a1b40fe150a1`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e2a3a62a0c81a986c51f9ee82518d8db7b9fa28372a685febd15f03303741`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a952bb6db9283db3c5c64966db65d2e7765683cf7c0fbfa916e196b8e087d`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:6870def05f3709b094c8645b0e369cb6cc0ff0c381394d4e4fe077f2404bfb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e7565d09dd1793409875f1a38e086e7a22fb79f97db5f307061a8dc7469d43ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189001890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d9390ea0c9353669cf94f2a91fa3822666ef3639817087de9b94467040330`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 01:40:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:40:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:40:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:40:38 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:40:38 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:40:38 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:40:38 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:40:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 01:40:39 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:40:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:40:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124713450165b300a5564c7e7f867872efc20dcadcab0da7fefc54e38b26aa8f`  
		Last Modified: Fri, 12 Apr 2024 01:42:32 GMT  
		Size: 118.4 MB (118435699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33edd3abd1664a7ce0a32840f9984b5f7840358dbc7c1511e62420c42761380f`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 1.9 MB (1940654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a5daffa9b99902422d73fce700aa264995b940f35f6f2083de4b2213e54cac`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8081fd96df3d797219535bd2b24584437920b18d3fe62d3d24167cde96f166c`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d03402f6f939c724589ce530ebf44ba1046be714b06c83100fdff412eb565`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204840cd1dee42c195853f6537f7b20ee5881aa86fe55263592c76296dfead3`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:de1ff6ed2a98601e38f62c743f33a27d169cd9c1f15035ea910c1a60d475e941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187431393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfc031a9c2b52669bd47835d557c375c4b5360db0efd90f324976e415d7399`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 08 Apr 2024 20:05:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Mon, 08 Apr 2024 20:05:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 08 Apr 2024 20:05:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Apr 2024 20:05:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 08 Apr 2024 20:05:19 GMT
RUN mkdir -p /data/data /data/log
# Mon, 08 Apr 2024 20:05:19 GMT
VOLUME [/data]
# Mon, 08 Apr 2024 20:05:20 GMT
WORKDIR /data
# Mon, 08 Apr 2024 20:05:20 GMT
EXPOSE 4200 4300 5432
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 08 Apr 2024 20:05:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 08 Apr 2024 20:05:20 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Mon, 08 Apr 2024 20:05:20 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 08 Apr 2024 20:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Apr 2024 20:05:20 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dee5275671aaa8bdf1898e77a728be2ea2873f94d2a55c963faf525e036fab`  
		Last Modified: Mon, 08 Apr 2024 20:05:49 GMT  
		Size: 118.0 MB (117973469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf1e040a1d7ddacecfa83cd4cc9a92dc9c4d74f159378e642118cb008a1e7bb`  
		Last Modified: Mon, 08 Apr 2024 20:05:40 GMT  
		Size: 1.9 MB (1940653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760dc81db632110ab8451a1c6c46336f90566a991d4357f947102f27d93b9b`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d2c01e11a2cf2bbc091943dab987292d4c921ff2876be9a86a1b40fe150a1`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e2a3a62a0c81a986c51f9ee82518d8db7b9fa28372a685febd15f03303741`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a952bb6db9283db3c5c64966db65d2e7765683cf7c0fbfa916e196b8e087d`  
		Last Modified: Mon, 08 Apr 2024 20:05:39 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
