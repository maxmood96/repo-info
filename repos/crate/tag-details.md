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
$ docker pull crate@sha256:1eae60eef4ac477ff6c641943009a64e00c60b795348655100518c4abb5277c8
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
$ docker pull crate@sha256:791182a03c364a84530d1217f8187cdec89e71c82af381e4a3d3123b82abd68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97998e3aa541ad927f31f1994d3e9448630192ccf2c9a4035ef5fdd3cbf31b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:14:11 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 12 Apr 2024 02:14:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:14:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:14:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:14:16 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:14:16 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:14:16 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:14:16 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:14:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:14:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:14:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 12 Apr 2024 02:14:17 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:14:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:14:17 GMT
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
	-	`sha256:0e0e73cf74b011abb998fc27d0a1aee34a247fd901aea4d8716a8d1201606fa0`  
		Last Modified: Fri, 12 Apr 2024 02:15:52 GMT  
		Size: 226.1 MB (226079684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2c046cd2c7200d3fa1a9037dcaf86c36e712489f2ed367e1dac1077afa63ca`  
		Last Modified: Fri, 12 Apr 2024 02:15:37 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d5ae2ec8fa9369607b2da569cd177c2de553c4ab6c850e407d541aac1ab176`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15599cd4a1cba7d087dc4b157f5f4160fb408b91e793e011ee3c90feec7a5726`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6661bfa70baea5b7cb9659304aa4095a4999c91702bab470ee15de9a0a2ed2bb`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44a5c65bb3915bbc87faedd71e9f67a6c64cf6af13a5ebde453e125291ae567`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.9`

```console
$ docker pull crate@sha256:1eae60eef4ac477ff6c641943009a64e00c60b795348655100518c4abb5277c8
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
$ docker pull crate@sha256:791182a03c364a84530d1217f8187cdec89e71c82af381e4a3d3123b82abd68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97998e3aa541ad927f31f1994d3e9448630192ccf2c9a4035ef5fdd3cbf31b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:14:11 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 12 Apr 2024 02:14:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:14:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:14:16 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:14:16 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:14:16 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:14:16 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:14:16 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:14:16 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:14:16 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:14:16 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 12 Apr 2024 02:14:17 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:14:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:14:17 GMT
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
	-	`sha256:0e0e73cf74b011abb998fc27d0a1aee34a247fd901aea4d8716a8d1201606fa0`  
		Last Modified: Fri, 12 Apr 2024 02:15:52 GMT  
		Size: 226.1 MB (226079684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2c046cd2c7200d3fa1a9037dcaf86c36e712489f2ed367e1dac1077afa63ca`  
		Last Modified: Fri, 12 Apr 2024 02:15:37 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d5ae2ec8fa9369607b2da569cd177c2de553c4ab6c850e407d541aac1ab176`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15599cd4a1cba7d087dc4b157f5f4160fb408b91e793e011ee3c90feec7a5726`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6661bfa70baea5b7cb9659304aa4095a4999c91702bab470ee15de9a0a2ed2bb`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44a5c65bb3915bbc87faedd71e9f67a6c64cf6af13a5ebde453e125291ae567`  
		Last Modified: Fri, 12 Apr 2024 02:15:36 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:8f3f338b7fe742b59e4e50f409de51cb999960ceb7c5c4b534afe8239f66a5a0
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
$ docker pull crate@sha256:8f3f338b7fe742b59e4e50f409de51cb999960ceb7c5c4b534afe8239f66a5a0
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
$ docker pull crate@sha256:a4803340544113c0bb3c6a6d2f6bf3ecca7a975fb51fd0aef51f9ac62231f72c
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
$ docker pull crate@sha256:a4803340544113c0bb3c6a6d2f6bf3ecca7a975fb51fd0aef51f9ac62231f72c
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
$ docker pull crate@sha256:cb41c1ed491515417238c48c1fb5d1ad57f1a32bf6524ac1c02e2c46758236c4
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

## `crate:5.6.4`

```console
$ docker pull crate@sha256:cb41c1ed491515417238c48c1fb5d1ad57f1a32bf6524ac1c02e2c46758236c4
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

## `crate:latest`

```console
$ docker pull crate@sha256:cb41c1ed491515417238c48c1fb5d1ad57f1a32bf6524ac1c02e2c46758236c4
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
