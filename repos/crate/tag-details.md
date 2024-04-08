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
$ docker pull crate@sha256:2caa3c491957f1a8bb6b8d9e12f72e5851d4a367e7edc06b22a0b4041b312a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:fb84d19b5e9d960ff9a4d93c0ffddc9a371eb448c2cb771ef4e9eacc63cb2306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297920934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ef386d8d51c8d6289e1981f2b0cc687292b65620ff5cc46e7d9d320dec128`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:28:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Sat, 03 Feb 2024 02:28:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:28:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:28:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:28:42 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:28:42 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:28:42 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:28:42 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:28:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:28:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:28:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Sat, 03 Feb 2024 02:28:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:28:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:28:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba6f83beb93e1bb56bb58fe308b7710d62da171305d61c33c146afb8461aa46`  
		Last Modified: Sat, 03 Feb 2024 02:30:32 GMT  
		Size: 227.3 MB (227342918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeaaf1e1f3879d21b279c40814ddac5c546f76ac0b96b9001acff268527837d`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9174c19cc0da2813d937677fe585d937a3838955d687de28c449af49e89c30cb`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292437de10d787d087f888d8b4d74066840de45f1f95df96debddc6075ded52e`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23240c554c5035b9d0ac7caf81e8c74d757a6f67a56f09dc6f523fe86e706870`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2666e272c4599be5cec55c2de101d3cf01038f07775d960c8c22af8f8834fab2`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 505.0 B  
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
$ docker pull crate@sha256:2caa3c491957f1a8bb6b8d9e12f72e5851d4a367e7edc06b22a0b4041b312a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.9` - linux; amd64

```console
$ docker pull crate@sha256:fb84d19b5e9d960ff9a4d93c0ffddc9a371eb448c2cb771ef4e9eacc63cb2306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297920934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404ef386d8d51c8d6289e1981f2b0cc687292b65620ff5cc46e7d9d320dec128`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:28:39 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Sat, 03 Feb 2024 02:28:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:28:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:28:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:28:42 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:28:42 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:28:42 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:28:42 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:28:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:28:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:28:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Sat, 03 Feb 2024 02:28:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:28:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:28:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba6f83beb93e1bb56bb58fe308b7710d62da171305d61c33c146afb8461aa46`  
		Last Modified: Sat, 03 Feb 2024 02:30:32 GMT  
		Size: 227.3 MB (227342918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeaaf1e1f3879d21b279c40814ddac5c546f76ac0b96b9001acff268527837d`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9174c19cc0da2813d937677fe585d937a3838955d687de28c449af49e89c30cb`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292437de10d787d087f888d8b4d74066840de45f1f95df96debddc6075ded52e`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23240c554c5035b9d0ac7caf81e8c74d757a6f67a56f09dc6f523fe86e706870`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2666e272c4599be5cec55c2de101d3cf01038f07775d960c8c22af8f8834fab2`  
		Last Modified: Sat, 03 Feb 2024 02:30:14 GMT  
		Size: 505.0 B  
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
$ docker pull crate@sha256:a3c1b231b8dd4e4ac1b7d902a2bc92dd529a102e2f39843a7454dc938f9326cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:be5f399088802798a8089a71ee43a8cd23fd263c67714c4f6313d75780c71ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300144497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a27bb8d71e6a404ef26ff3c62d1712b6ee7dafcb80eb78a872e0e96dc503417`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:28:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Sat, 03 Feb 2024 02:28:12 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:28:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:28:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:28:13 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:28:13 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:28:13 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:28:13 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:28:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:28:13 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:28:13 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Sat, 03 Feb 2024 02:28:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:28:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:28:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73da7b432215a0756213fbffd324602a98c9c9bb4a16b5e4697954f24d3faed`  
		Last Modified: Sat, 03 Feb 2024 02:30:04 GMT  
		Size: 229.6 MB (229566489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74b5d5ea3d24077707bff5415356e019fd6c4a22271b845a7a1f29a1f32d8c0`  
		Last Modified: Sat, 03 Feb 2024 02:29:47 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cfe9ff83e8ef734eda6d95abb16f142e808c32591c82459eefd188932d259`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf93cbd18c76dc4d70e6fe000c595838bfac3790a97f38c76177352d679d428a`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec9f0cb89c0ca555e00c20115590b29f165bbc507f60c0cd44e4b1328dfe32`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68283646c8d6b4ef3c43767b25630e3418760268b30419ce2f58c2ec2527e0d3`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 504.0 B  
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
$ docker pull crate@sha256:a3c1b231b8dd4e4ac1b7d902a2bc92dd529a102e2f39843a7454dc938f9326cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:be5f399088802798a8089a71ee43a8cd23fd263c67714c4f6313d75780c71ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300144497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a27bb8d71e6a404ef26ff3c62d1712b6ee7dafcb80eb78a872e0e96dc503417`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:28:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Sat, 03 Feb 2024 02:28:12 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:28:12 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:28:12 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:28:13 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:28:13 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:28:13 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:28:13 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:28:13 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:28:13 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:28:13 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Sat, 03 Feb 2024 02:28:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:28:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:28:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73da7b432215a0756213fbffd324602a98c9c9bb4a16b5e4697954f24d3faed`  
		Last Modified: Sat, 03 Feb 2024 02:30:04 GMT  
		Size: 229.6 MB (229566489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74b5d5ea3d24077707bff5415356e019fd6c4a22271b845a7a1f29a1f32d8c0`  
		Last Modified: Sat, 03 Feb 2024 02:29:47 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cfe9ff83e8ef734eda6d95abb16f142e808c32591c82459eefd188932d259`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf93cbd18c76dc4d70e6fe000c595838bfac3790a97f38c76177352d679d428a`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec9f0cb89c0ca555e00c20115590b29f165bbc507f60c0cd44e4b1328dfe32`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68283646c8d6b4ef3c43767b25630e3418760268b30419ce2f58c2ec2527e0d3`  
		Last Modified: Sat, 03 Feb 2024 02:29:46 GMT  
		Size: 504.0 B  
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
$ docker pull crate@sha256:f2150c7a7332ad89b35e39580bb7622498354fc5db0572fb7ec4244b436bae45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:c3758e0e4468bcfe8fbe199edf06ab2e0b050839817da1b4f89e1fdc987f59ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187345532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57161aa417d44981446c022833ba725bd6aac3114b55fbb37a360b8ed94d3be2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:27:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Sat, 03 Feb 2024 02:27:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:27:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:27:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:27:44 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:27:44 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:27:44 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:27:44 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:27:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:27:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:27:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Sat, 03 Feb 2024 02:27:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:27:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f189cf738d426d5b753615eb37881ebe3a9e550b6f416b83b6d41f0eca9ca5c`  
		Last Modified: Sat, 03 Feb 2024 02:29:36 GMT  
		Size: 116.8 MB (116767524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443178ba4cd8a2a453705fdd4484a385922ab5aaa98eece78e19e74c6c5b41f1`  
		Last Modified: Sat, 03 Feb 2024 02:29:26 GMT  
		Size: 1.9 MB (1939613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54526307e6dbda9dd6152af5d44dc552687c50d69c677881d0c9a79e91896f9d`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b9a4d2e06bb6b59c3b99d24bf3033c6fb8356ad9d6b7da377c9f78a0e1f72e`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80a2415c0d634f672374eb0aa8366616d2bbe484192ececd9f21450bca42bee`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d51dead80e32bf58dad931a735a677f3b43520a71391f2da0f192b21ed36ba`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 504.0 B  
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
$ docker pull crate@sha256:f2150c7a7332ad89b35e39580bb7622498354fc5db0572fb7ec4244b436bae45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:c3758e0e4468bcfe8fbe199edf06ab2e0b050839817da1b4f89e1fdc987f59ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187345532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57161aa417d44981446c022833ba725bd6aac3114b55fbb37a360b8ed94d3be2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Sat, 03 Feb 2024 02:27:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Sat, 03 Feb 2024 02:27:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Sat, 03 Feb 2024 02:27:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 Feb 2024 02:27:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Sat, 03 Feb 2024 02:27:44 GMT
RUN mkdir -p /data/data /data/log
# Sat, 03 Feb 2024 02:27:44 GMT
VOLUME [/data]
# Sat, 03 Feb 2024 02:27:44 GMT
WORKDIR /data
# Sat, 03 Feb 2024 02:27:44 GMT
EXPOSE 4200 4300 5432
# Sat, 03 Feb 2024 02:27:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Sat, 03 Feb 2024 02:27:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Sat, 03 Feb 2024 02:27:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Sat, 03 Feb 2024 02:27:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Sat, 03 Feb 2024 02:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 03 Feb 2024 02:27:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f189cf738d426d5b753615eb37881ebe3a9e550b6f416b83b6d41f0eca9ca5c`  
		Last Modified: Sat, 03 Feb 2024 02:29:36 GMT  
		Size: 116.8 MB (116767524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443178ba4cd8a2a453705fdd4484a385922ab5aaa98eece78e19e74c6c5b41f1`  
		Last Modified: Sat, 03 Feb 2024 02:29:26 GMT  
		Size: 1.9 MB (1939613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54526307e6dbda9dd6152af5d44dc552687c50d69c677881d0c9a79e91896f9d`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b9a4d2e06bb6b59c3b99d24bf3033c6fb8356ad9d6b7da377c9f78a0e1f72e`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80a2415c0d634f672374eb0aa8366616d2bbe484192ececd9f21450bca42bee`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d51dead80e32bf58dad931a735a677f3b43520a71391f2da0f192b21ed36ba`  
		Last Modified: Sat, 03 Feb 2024 02:29:25 GMT  
		Size: 504.0 B  
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
$ docker pull crate@sha256:e409cb2f3f66fe521f3fc42b302607b7a4b449a212e97be4ad596f0e70e7a8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:08ad19df2bac48bd858cfbe57dc4dc9e1aa77848dfb1f93c944a0df3ff835ba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189016881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60faa0f9b15b073f4e75fb090fc51c7dba925050cb857a75021c8f942a2463`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 25 Mar 2024 19:59:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.3.tar.gz.asc crate-5.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.3.tar.gz.asc     && tar -xf crate-5.6.3.tar.gz -C /crate --strip-components=1     && rm crate-5.6.3.tar.gz
# Mon, 25 Mar 2024 19:59:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 25 Mar 2024 19:59:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 19:59:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 25 Mar 2024 19:59:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 25 Mar 2024 19:59:43 GMT
VOLUME [/data]
# Mon, 25 Mar 2024 19:59:44 GMT
WORKDIR /data
# Mon, 25 Mar 2024 19:59:44 GMT
EXPOSE 4200 4300 5432
# Mon, 25 Mar 2024 19:59:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 25 Mar 2024 19:59:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 25 Mar 2024 19:59:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-03-22T09:35:11.010811 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.3
# Mon, 25 Mar 2024 19:59:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 25 Mar 2024 19:59:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 25 Mar 2024 19:59:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e3583def04c9296c54190e654366bbae57b748f226114f76a1a4dd5453cfee`  
		Last Modified: Mon, 25 Mar 2024 20:00:20 GMT  
		Size: 118.4 MB (118437816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aaf164b5965e5acc44f3c76877a55f3d82d07fdc71e6dcd37d9d375b9b749`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 1.9 MB (1940672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc8981503ec758cad99956b8427dbf27645dcbff8d2224c5e4e03f8582c25f3`  
		Last Modified: Mon, 25 Mar 2024 20:00:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6282303a4381bf586c4167fb4db39897ac713e6fe3a2c6747aae1b4d4e019`  
		Last Modified: Mon, 25 Mar 2024 20:00:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c9947829f5bd86da4b3865c0e6868bc70eca7eeb89fdbeebe0021d4f751f3a`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976bc68f479ae63481b33b9f9daa5a5b222c587ce2de422c0f2be29f08ac9fbc`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:57c8684779a63e3084f17fe26a3c4b0642dc0f6f21b9f0ac76a5bf6221937fb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187431496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79e04e4aa5a1eefc7a8370ff819a55cda27886df6a03cc50df6ba7f2feafe28`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 25 Mar 2024 20:15:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.3.tar.gz.asc crate-5.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.3.tar.gz.asc     && tar -xf crate-5.6.3.tar.gz -C /crate --strip-components=1     && rm crate-5.6.3.tar.gz
# Mon, 25 Mar 2024 20:15:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 25 Mar 2024 20:15:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 20:15:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 25 Mar 2024 20:15:42 GMT
RUN mkdir -p /data/data /data/log
# Mon, 25 Mar 2024 20:15:42 GMT
VOLUME [/data]
# Mon, 25 Mar 2024 20:15:42 GMT
WORKDIR /data
# Mon, 25 Mar 2024 20:15:42 GMT
EXPOSE 4200 4300 5432
# Mon, 25 Mar 2024 20:15:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 25 Mar 2024 20:15:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 25 Mar 2024 20:15:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-03-22T09:35:11.010811 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.3
# Mon, 25 Mar 2024 20:15:42 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 25 Mar 2024 20:15:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:42 GMT
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
	-	`sha256:d8a99e18b081f16d85ef619f1d9446662e1fe51781dc28d229b9aacf69619097`  
		Last Modified: Mon, 25 Mar 2024 20:16:11 GMT  
		Size: 118.0 MB (117973572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56edf68e692115a8a190a84cde0d28196276c73fbe8b8b31e32af4ec159f94d9`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 1.9 MB (1940652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a9a204fa8f538c63102043301839a0f5ddcc259bebd688540a1179dd07b788`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfedf3a041dfee68642739da5c9b04f2ae8464be436135cf785d7b1ae0f8dd94`  
		Last Modified: Mon, 25 Mar 2024 20:16:00 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81a3532d970df067c05de27c527d9bc1ae43f558c259da049d0055679642c98`  
		Last Modified: Mon, 25 Mar 2024 20:16:00 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f898019761e42a52d28fe9e7002bcb7259e4a1b594caf76eabe9ba4596cfb42`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.4`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:e409cb2f3f66fe521f3fc42b302607b7a4b449a212e97be4ad596f0e70e7a8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:08ad19df2bac48bd858cfbe57dc4dc9e1aa77848dfb1f93c944a0df3ff835ba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189016881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60faa0f9b15b073f4e75fb090fc51c7dba925050cb857a75021c8f942a2463`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 25 Mar 2024 19:59:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.3.tar.gz.asc crate-5.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.3.tar.gz.asc     && tar -xf crate-5.6.3.tar.gz -C /crate --strip-components=1     && rm crate-5.6.3.tar.gz
# Mon, 25 Mar 2024 19:59:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 25 Mar 2024 19:59:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 19:59:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 25 Mar 2024 19:59:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 25 Mar 2024 19:59:43 GMT
VOLUME [/data]
# Mon, 25 Mar 2024 19:59:44 GMT
WORKDIR /data
# Mon, 25 Mar 2024 19:59:44 GMT
EXPOSE 4200 4300 5432
# Mon, 25 Mar 2024 19:59:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 25 Mar 2024 19:59:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 25 Mar 2024 19:59:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-03-22T09:35:11.010811 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.3
# Mon, 25 Mar 2024 19:59:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 25 Mar 2024 19:59:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 25 Mar 2024 19:59:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e3583def04c9296c54190e654366bbae57b748f226114f76a1a4dd5453cfee`  
		Last Modified: Mon, 25 Mar 2024 20:00:20 GMT  
		Size: 118.4 MB (118437816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aaf164b5965e5acc44f3c76877a55f3d82d07fdc71e6dcd37d9d375b9b749`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 1.9 MB (1940672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc8981503ec758cad99956b8427dbf27645dcbff8d2224c5e4e03f8582c25f3`  
		Last Modified: Mon, 25 Mar 2024 20:00:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6282303a4381bf586c4167fb4db39897ac713e6fe3a2c6747aae1b4d4e019`  
		Last Modified: Mon, 25 Mar 2024 20:00:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c9947829f5bd86da4b3865c0e6868bc70eca7eeb89fdbeebe0021d4f751f3a`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976bc68f479ae63481b33b9f9daa5a5b222c587ce2de422c0f2be29f08ac9fbc`  
		Last Modified: Mon, 25 Mar 2024 20:00:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:57c8684779a63e3084f17fe26a3c4b0642dc0f6f21b9f0ac76a5bf6221937fb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187431496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79e04e4aa5a1eefc7a8370ff819a55cda27886df6a03cc50df6ba7f2feafe28`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 25 Mar 2024 20:15:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.3.tar.gz.asc crate-5.6.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.3.tar.gz.asc     && tar -xf crate-5.6.3.tar.gz -C /crate --strip-components=1     && rm crate-5.6.3.tar.gz
# Mon, 25 Mar 2024 20:15:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 25 Mar 2024 20:15:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 20:15:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 25 Mar 2024 20:15:42 GMT
RUN mkdir -p /data/data /data/log
# Mon, 25 Mar 2024 20:15:42 GMT
VOLUME [/data]
# Mon, 25 Mar 2024 20:15:42 GMT
WORKDIR /data
# Mon, 25 Mar 2024 20:15:42 GMT
EXPOSE 4200 4300 5432
# Mon, 25 Mar 2024 20:15:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 25 Mar 2024 20:15:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 25 Mar 2024 20:15:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-03-22T09:35:11.010811 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.3
# Mon, 25 Mar 2024 20:15:42 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 25 Mar 2024 20:15:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:42 GMT
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
	-	`sha256:d8a99e18b081f16d85ef619f1d9446662e1fe51781dc28d229b9aacf69619097`  
		Last Modified: Mon, 25 Mar 2024 20:16:11 GMT  
		Size: 118.0 MB (117973572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56edf68e692115a8a190a84cde0d28196276c73fbe8b8b31e32af4ec159f94d9`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 1.9 MB (1940652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a9a204fa8f538c63102043301839a0f5ddcc259bebd688540a1179dd07b788`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfedf3a041dfee68642739da5c9b04f2ae8464be436135cf785d7b1ae0f8dd94`  
		Last Modified: Mon, 25 Mar 2024 20:16:00 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81a3532d970df067c05de27c527d9bc1ae43f558c259da049d0055679642c98`  
		Last Modified: Mon, 25 Mar 2024 20:16:00 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f898019761e42a52d28fe9e7002bcb7259e4a1b594caf76eabe9ba4596cfb42`  
		Last Modified: Mon, 25 Mar 2024 20:16:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
