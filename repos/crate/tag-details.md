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
$ docker pull crate@sha256:15dbe672ba95f6163d962e3887d256edd91c1c148ab5cdaa0cb53c289534aff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:4318006a8a5551c9548ed8931bd852f2dbe8fdac9a0ad28695bf25c1c0412d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311045450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615cba64ff79285ad8a6c3d20de1389f1fbcaa05dad380e7201dec51279b55f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb50bfeaca05f02c9953f5228d1afd3960889a904bfb50000c019aaa98ab36`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 11.0 MB (10958339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ffb48f5a745c7c6ebaa174e4c0c04b0576aaf552ad4c4b4204c897463fd86`  
		Last Modified: Thu, 27 Jun 2024 00:59:54 GMT  
		Size: 229.6 MB (229566878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7b7035215846c21fe3768a940beafa66b9b30935173b50bd2ebfb0cc95dc3d`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 1.9 MB (1939588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392fd6231b3a8ec6169f1de6bffee28b5d68a397a9405b802e1d40308726dfe`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efca54f1d849c96299f359942dc816dcc519050ab60511c28e7b4c47fb60987`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b85ea09a9e2b7df77304ffd356840d39bd26ba33e001d3601f98facd3619c98`  
		Last Modified: Thu, 27 Jun 2024 00:59:53 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50f4a9b11412c1c9129ca313ddd87c7d3dcbe96da3a550ee8eb3380ecf53bf5`  
		Last Modified: Thu, 27 Jun 2024 00:59:53 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4` - unknown; unknown

```console
$ docker pull crate@sha256:1821dfe6be8d0dd6da5112d0ae423e00ef26a7c53da7064a80ce1648c848b1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcf5c2d34ee17aebf2ab8b99304c2548099377513c88a7c6ee260fae22d86a5`

```dockerfile
```

-	Layers:
	-	`sha256:e42f30389b3796cc8c9473911373b4cb0dec8c1d6805fe6ab7697b40ceea9366`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 4.9 MB (4906469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae11bffc970fcabd06490623135637ef0977449c8b54ee1c46142bcece282c4`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cf686c122465bffbab824c764546403783ddf2abeb2415e4893932bdf7719858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 MB (308276308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3bf5990a4f16106b6cb4513b270dd001cf8b33233c6310aac0d5e1aca80690`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2094b4384bc2f3c6a5a858933a823c397af8c40896abea32aeb935c6110effc`  
		Last Modified: Thu, 27 Jun 2024 05:53:21 GMT  
		Size: 227.9 MB (227888376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5686987fcd1d547997f19df408513c636ee07c6dac5fb890546bf73b26b63a1`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 1.9 MB (1939591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacec86e5325b9109098ff63732acef9f6fe40595d872f1886adc103dbd6603b`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6262b80d0f1ff8381e9affe49b02f581272648fa855ab0f01874fd677a93e38`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f60147c0c6230e46dc4240832961547757de98607e84bdc56a5c639382b8b7`  
		Last Modified: Thu, 27 Jun 2024 05:53:14 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d31289371dd060d9428fc3b32bc32d671bdc4d2b035691aca03e6345662a8e`  
		Last Modified: Thu, 27 Jun 2024 05:53:14 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4` - unknown; unknown

```console
$ docker pull crate@sha256:eee13ad7edd20f70bba4c9b7332181c3791f6899d8287808f1c31aaaaea53f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f29560f65e4aea9aa9f85f545491f396cf9cff798365815e29bd6d4ccc4e2a4`

```dockerfile
```

-	Layers:
	-	`sha256:18ad1b876a177df512d8adb478ee0dd579c6b8bc549ee47e12a23bfa3821400c`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 4.9 MB (4904386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f764cc849e5117d15e5d65d1d200e2ce4aeec93677fd5a35c0bffb9dd842c9b`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 23.2 KB (23152 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.4.8`

```console
$ docker pull crate@sha256:15dbe672ba95f6163d962e3887d256edd91c1c148ab5cdaa0cb53c289534aff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:4318006a8a5551c9548ed8931bd852f2dbe8fdac9a0ad28695bf25c1c0412d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311045450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615cba64ff79285ad8a6c3d20de1389f1fbcaa05dad380e7201dec51279b55f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb50bfeaca05f02c9953f5228d1afd3960889a904bfb50000c019aaa98ab36`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 11.0 MB (10958339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ffb48f5a745c7c6ebaa174e4c0c04b0576aaf552ad4c4b4204c897463fd86`  
		Last Modified: Thu, 27 Jun 2024 00:59:54 GMT  
		Size: 229.6 MB (229566878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7b7035215846c21fe3768a940beafa66b9b30935173b50bd2ebfb0cc95dc3d`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 1.9 MB (1939588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392fd6231b3a8ec6169f1de6bffee28b5d68a397a9405b802e1d40308726dfe`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efca54f1d849c96299f359942dc816dcc519050ab60511c28e7b4c47fb60987`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b85ea09a9e2b7df77304ffd356840d39bd26ba33e001d3601f98facd3619c98`  
		Last Modified: Thu, 27 Jun 2024 00:59:53 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50f4a9b11412c1c9129ca313ddd87c7d3dcbe96da3a550ee8eb3380ecf53bf5`  
		Last Modified: Thu, 27 Jun 2024 00:59:53 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4.8` - unknown; unknown

```console
$ docker pull crate@sha256:1821dfe6be8d0dd6da5112d0ae423e00ef26a7c53da7064a80ce1648c848b1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcf5c2d34ee17aebf2ab8b99304c2548099377513c88a7c6ee260fae22d86a5`

```dockerfile
```

-	Layers:
	-	`sha256:e42f30389b3796cc8c9473911373b4cb0dec8c1d6805fe6ab7697b40ceea9366`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 4.9 MB (4906469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae11bffc970fcabd06490623135637ef0977449c8b54ee1c46142bcece282c4`  
		Last Modified: Thu, 27 Jun 2024 00:59:52 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cf686c122465bffbab824c764546403783ddf2abeb2415e4893932bdf7719858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 MB (308276308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3bf5990a4f16106b6cb4513b270dd001cf8b33233c6310aac0d5e1aca80690`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2094b4384bc2f3c6a5a858933a823c397af8c40896abea32aeb935c6110effc`  
		Last Modified: Thu, 27 Jun 2024 05:53:21 GMT  
		Size: 227.9 MB (227888376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5686987fcd1d547997f19df408513c636ee07c6dac5fb890546bf73b26b63a1`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 1.9 MB (1939591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacec86e5325b9109098ff63732acef9f6fe40595d872f1886adc103dbd6603b`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6262b80d0f1ff8381e9affe49b02f581272648fa855ab0f01874fd677a93e38`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f60147c0c6230e46dc4240832961547757de98607e84bdc56a5c639382b8b7`  
		Last Modified: Thu, 27 Jun 2024 05:53:14 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d31289371dd060d9428fc3b32bc32d671bdc4d2b035691aca03e6345662a8e`  
		Last Modified: Thu, 27 Jun 2024 05:53:14 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4.8` - unknown; unknown

```console
$ docker pull crate@sha256:eee13ad7edd20f70bba4c9b7332181c3791f6899d8287808f1c31aaaaea53f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f29560f65e4aea9aa9f85f545491f396cf9cff798365815e29bd6d4ccc4e2a4`

```dockerfile
```

-	Layers:
	-	`sha256:18ad1b876a177df512d8adb478ee0dd579c6b8bc549ee47e12a23bfa3821400c`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 4.9 MB (4904386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f764cc849e5117d15e5d65d1d200e2ce4aeec93677fd5a35c0bffb9dd842c9b`  
		Last Modified: Thu, 27 Jun 2024 05:53:13 GMT  
		Size: 23.2 KB (23152 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5`

```console
$ docker pull crate@sha256:99233a0cd865bf54e574236722566fe977970c8474a8bdcd340391eee850a516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:9da020b8355e8ca27d9b9895a2a5a21218aff1f0324f9a64d48f649ccb4d954f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198246504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7b7736f5fc796ef316267825345778e2b15d1170545342f672d9a6e6d299b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ee489e17d361e250f28c518fbc1f7ed8a66e89af6c81af894912a0f3570e27`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 11.0 MB (10958271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80284e7b4ddd4c1e25eff8709db9351bf43501ed4304b8fa4dc00fa8625802`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 116.8 MB (116767999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6bd67d967e470ec50c35a7bdf3794250c57274f885448a757be7d6f5eb20`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 1.9 MB (1939588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392fd6231b3a8ec6169f1de6bffee28b5d68a397a9405b802e1d40308726dfe`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d4338bc579a332e570cab898f642b19b14575acf0312d1851bbb76adf20f1`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22cb4386264a79bbe9443a70e98c83e017a6dffcb01f19c2ed509a3debf5c`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ae233c1a8c37e82735c9647d91f921bdf4e6ff0c46e2e3f80f52f6b3d50ca`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:58c79386b986c580a668cc2b43016bbb58e47a57bfa617fd32db91a6baa13348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965afa057b8390c0cce63957118e47d4a5bea79e52f5b16734d6f4c4ea390d3f`

```dockerfile
```

-	Layers:
	-	`sha256:767bd14b17544037ab404ec1c0c0b871438556aaeffe7b287eb7c7444fda1122`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 4.9 MB (4909949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ac6d56109b00a30a3667ef7fd558485fcc4e8555c076b141f9804b4f1aaeaf`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:008f4c078cd7a6b03adb88c5b3f17439342db8c774ccce069930394fa3d04cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196690371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0265002fed3595757a1a2f825352a1eb66418eda8e00002016781509ac853854`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f11d120d5e42cab8933e852b9a66158aa4ea1e09901c1e75b126b2d5ac7b1`  
		Last Modified: Thu, 27 Jun 2024 05:52:13 GMT  
		Size: 116.3 MB (116302445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165dd6595a1deffaa627dda23730daff70d1de6c2a508f49dc21589915680c65`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e4fb4f2ef0c6fae80e701cc59c920990954bd2bb0625d9407c4f529cbcb46`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7240c215846a48627b0058756091b0991ce6185441e75d6e8fad7fdeb921f7f8`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0ba09f41d34cebec18506db38bd8cdc797b2248212d768ec8ef19296f6576`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b56bb1d94acb74957d0f98fa6a9734bcfb65d8e59fb6535e604ee919d3a8f`  
		Last Modified: Thu, 27 Jun 2024 05:52:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:28d1044adfa132a67e6917c8631d2ba15c93916d2e60ed445fcd09067eac9498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194e11a6c3c16b46b3ac07b72a4538f69a2f8758f6e3430f18b91f4509348907`

```dockerfile
```

-	Layers:
	-	`sha256:4ae27af63a2a3fce9c1e13e18cb00275dc0a95fbb9deded81000d7f2cfcad5db`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 4.9 MB (4907878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fcc3235dfe7a7ad34458a2035d2d38f53e07c07cc9d82006d7276a2eabcfd2`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 23.5 KB (23459 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.4`

```console
$ docker pull crate@sha256:99233a0cd865bf54e574236722566fe977970c8474a8bdcd340391eee850a516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:9da020b8355e8ca27d9b9895a2a5a21218aff1f0324f9a64d48f649ccb4d954f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198246504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7b7736f5fc796ef316267825345778e2b15d1170545342f672d9a6e6d299b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ee489e17d361e250f28c518fbc1f7ed8a66e89af6c81af894912a0f3570e27`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 11.0 MB (10958271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80284e7b4ddd4c1e25eff8709db9351bf43501ed4304b8fa4dc00fa8625802`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 116.8 MB (116767999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6bd67d967e470ec50c35a7bdf3794250c57274f885448a757be7d6f5eb20`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 1.9 MB (1939588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392fd6231b3a8ec6169f1de6bffee28b5d68a397a9405b802e1d40308726dfe`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d4338bc579a332e570cab898f642b19b14575acf0312d1851bbb76adf20f1`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22cb4386264a79bbe9443a70e98c83e017a6dffcb01f19c2ed509a3debf5c`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ae233c1a8c37e82735c9647d91f921bdf4e6ff0c46e2e3f80f52f6b3d50ca`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:58c79386b986c580a668cc2b43016bbb58e47a57bfa617fd32db91a6baa13348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965afa057b8390c0cce63957118e47d4a5bea79e52f5b16734d6f4c4ea390d3f`

```dockerfile
```

-	Layers:
	-	`sha256:767bd14b17544037ab404ec1c0c0b871438556aaeffe7b287eb7c7444fda1122`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 4.9 MB (4909949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ac6d56109b00a30a3667ef7fd558485fcc4e8555c076b141f9804b4f1aaeaf`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:008f4c078cd7a6b03adb88c5b3f17439342db8c774ccce069930394fa3d04cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196690371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0265002fed3595757a1a2f825352a1eb66418eda8e00002016781509ac853854`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f11d120d5e42cab8933e852b9a66158aa4ea1e09901c1e75b126b2d5ac7b1`  
		Last Modified: Thu, 27 Jun 2024 05:52:13 GMT  
		Size: 116.3 MB (116302445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165dd6595a1deffaa627dda23730daff70d1de6c2a508f49dc21589915680c65`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e4fb4f2ef0c6fae80e701cc59c920990954bd2bb0625d9407c4f529cbcb46`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7240c215846a48627b0058756091b0991ce6185441e75d6e8fad7fdeb921f7f8`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0ba09f41d34cebec18506db38bd8cdc797b2248212d768ec8ef19296f6576`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b56bb1d94acb74957d0f98fa6a9734bcfb65d8e59fb6535e604ee919d3a8f`  
		Last Modified: Thu, 27 Jun 2024 05:52:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:28d1044adfa132a67e6917c8631d2ba15c93916d2e60ed445fcd09067eac9498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194e11a6c3c16b46b3ac07b72a4538f69a2f8758f6e3430f18b91f4509348907`

```dockerfile
```

-	Layers:
	-	`sha256:4ae27af63a2a3fce9c1e13e18cb00275dc0a95fbb9deded81000d7f2cfcad5db`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 4.9 MB (4907878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fcc3235dfe7a7ad34458a2035d2d38f53e07c07cc9d82006d7276a2eabcfd2`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 23.5 KB (23459 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.5`

```console
$ docker pull crate@sha256:99233a0cd865bf54e574236722566fe977970c8474a8bdcd340391eee850a516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:9da020b8355e8ca27d9b9895a2a5a21218aff1f0324f9a64d48f649ccb4d954f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198246504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7b7736f5fc796ef316267825345778e2b15d1170545342f672d9a6e6d299b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ee489e17d361e250f28c518fbc1f7ed8a66e89af6c81af894912a0f3570e27`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 11.0 MB (10958271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80284e7b4ddd4c1e25eff8709db9351bf43501ed4304b8fa4dc00fa8625802`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 116.8 MB (116767999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6bd67d967e470ec50c35a7bdf3794250c57274f885448a757be7d6f5eb20`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 1.9 MB (1939588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392fd6231b3a8ec6169f1de6bffee28b5d68a397a9405b802e1d40308726dfe`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d4338bc579a332e570cab898f642b19b14575acf0312d1851bbb76adf20f1`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22cb4386264a79bbe9443a70e98c83e017a6dffcb01f19c2ed509a3debf5c`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ae233c1a8c37e82735c9647d91f921bdf4e6ff0c46e2e3f80f52f6b3d50ca`  
		Last Modified: Thu, 27 Jun 2024 00:59:46 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:58c79386b986c580a668cc2b43016bbb58e47a57bfa617fd32db91a6baa13348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965afa057b8390c0cce63957118e47d4a5bea79e52f5b16734d6f4c4ea390d3f`

```dockerfile
```

-	Layers:
	-	`sha256:767bd14b17544037ab404ec1c0c0b871438556aaeffe7b287eb7c7444fda1122`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 4.9 MB (4909949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ac6d56109b00a30a3667ef7fd558485fcc4e8555c076b141f9804b4f1aaeaf`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:008f4c078cd7a6b03adb88c5b3f17439342db8c774ccce069930394fa3d04cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196690371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0265002fed3595757a1a2f825352a1eb66418eda8e00002016781509ac853854`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f11d120d5e42cab8933e852b9a66158aa4ea1e09901c1e75b126b2d5ac7b1`  
		Last Modified: Thu, 27 Jun 2024 05:52:13 GMT  
		Size: 116.3 MB (116302445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165dd6595a1deffaa627dda23730daff70d1de6c2a508f49dc21589915680c65`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 1.9 MB (1939589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e4fb4f2ef0c6fae80e701cc59c920990954bd2bb0625d9407c4f529cbcb46`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7240c215846a48627b0058756091b0991ce6185441e75d6e8fad7fdeb921f7f8`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0ba09f41d34cebec18506db38bd8cdc797b2248212d768ec8ef19296f6576`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b56bb1d94acb74957d0f98fa6a9734bcfb65d8e59fb6535e604ee919d3a8f`  
		Last Modified: Thu, 27 Jun 2024 05:52:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:28d1044adfa132a67e6917c8631d2ba15c93916d2e60ed445fcd09067eac9498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194e11a6c3c16b46b3ac07b72a4538f69a2f8758f6e3430f18b91f4509348907`

```dockerfile
```

-	Layers:
	-	`sha256:4ae27af63a2a3fce9c1e13e18cb00275dc0a95fbb9deded81000d7f2cfcad5db`  
		Last Modified: Thu, 27 Jun 2024 05:52:10 GMT  
		Size: 4.9 MB (4907878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fcc3235dfe7a7ad34458a2035d2d38f53e07c07cc9d82006d7276a2eabcfd2`  
		Last Modified: Thu, 27 Jun 2024 05:52:09 GMT  
		Size: 23.5 KB (23459 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6`

```console
$ docker pull crate@sha256:27bdd11ce760acf2e252743390bd6ea1cbe0c23943614899d9d78815179bbdd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:a666a914beb925defe02032a43ce1dee5e1182c1576ac19fde8b64c059876a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199395752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e56a116df649c95f558de361e9f34f9f078ae239e0db0cd787c4fb8f687ac1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933dabe625c616e82acc43241671c2f0227e0c5418ae621f2238b8764f3a52d6`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 11.0 MB (10958237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7844e542c809c50549553819201ede7cc7472718f97afc569dee56d274f538`  
		Last Modified: Thu, 27 Jun 2024 01:00:04 GMT  
		Size: 117.9 MB (117916237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2699e5e0ef1d83b3d921d9c1c5430a73a12359d853c700dd51ce8972ed9198f9`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 1.9 MB (1940636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1725ec77e06faeab7c17c7a1baf3057f346b3874e860dd22294b033daa2f48`  
		Last Modified: Thu, 27 Jun 2024 00:59:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831bac3eb3466d7d79e20ed7ab21869a3d35bb869a14bc647d6f88e9f39d4650`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82059bb7cf98f1c218438d814d363a0d1d35cba81d7df19597d3585758eee08`  
		Last Modified: Thu, 27 Jun 2024 01:00:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd962e639f86a45f71b230523fa9853e763ce72e8b4d9559b335d5c0ef7867`  
		Last Modified: Thu, 27 Jun 2024 01:00:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:1eb543b041810b06af55851c10f5671b66e3af89814ba7731eaeca985670bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307de048b4a15800c805da620e6616eb24d926e48e7b7a5641001ca9a993d6db`

```dockerfile
```

-	Layers:
	-	`sha256:398552615b3802e1090ba4caa9237a4730bc0e072474d16846aa6e20b9e0e4b0`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 4.9 MB (4909682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3fd2605520a8da5b6b034ee2d7fc3e55fdc87b991b7e0843aa268051a1eb1d`  
		Last Modified: Thu, 27 Jun 2024 00:59:59 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2f2226f05cd2f5607d7c297bc25635cbfada27c562df968f9d1fbae308d0989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197815608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8933c5e3d65274cdbab7fb19bb9b3dce1498396800af02f28458dc6b23efa73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c147e32867f7ecf704c6d4ea1e98ec0418ec22a5719abba183fbe604e9a5fbc`  
		Last Modified: Thu, 27 Jun 2024 05:51:25 GMT  
		Size: 117.4 MB (117426632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae227b193d9e655491e494172db7f39244948b14fcdd790f3c419fb719b3fa`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6974e9beee1e6b359108ee8adcdc4f31b52b762b3226e63aff37339aa1925`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6729cab256dc7741d2ee1ecb23510335d68da7fe275affd2a81813a72d1fc`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d4582e3b169050999ed4db0a0a01f99ef62a51a564352c7bf7f5660e51afb`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcea5d9dc1273ae352e94632eeea1d3b0cabab2c88eb2e62efde1994ff167e1c`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:6977a21a32ee12ac7b5e36dc647da05451f849596393d8ed616bede821abd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1539afccbf63d331a2dd685b6ac3276994c6b41495664ba79b2eea90186216`

```dockerfile
```

-	Layers:
	-	`sha256:039948e1b38b873f6c28877fcf79806b5cf48249324066c2cf126df6694baa72`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 4.9 MB (4907599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c60cb2021b90a881173a65a90b6f90340430f560262d775c5e6fab338e3d8c4`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6.5`

```console
$ docker pull crate@sha256:27bdd11ce760acf2e252743390bd6ea1cbe0c23943614899d9d78815179bbdd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:a666a914beb925defe02032a43ce1dee5e1182c1576ac19fde8b64c059876a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199395752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e56a116df649c95f558de361e9f34f9f078ae239e0db0cd787c4fb8f687ac1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933dabe625c616e82acc43241671c2f0227e0c5418ae621f2238b8764f3a52d6`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 11.0 MB (10958237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7844e542c809c50549553819201ede7cc7472718f97afc569dee56d274f538`  
		Last Modified: Thu, 27 Jun 2024 01:00:04 GMT  
		Size: 117.9 MB (117916237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2699e5e0ef1d83b3d921d9c1c5430a73a12359d853c700dd51ce8972ed9198f9`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 1.9 MB (1940636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1725ec77e06faeab7c17c7a1baf3057f346b3874e860dd22294b033daa2f48`  
		Last Modified: Thu, 27 Jun 2024 00:59:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831bac3eb3466d7d79e20ed7ab21869a3d35bb869a14bc647d6f88e9f39d4650`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82059bb7cf98f1c218438d814d363a0d1d35cba81d7df19597d3585758eee08`  
		Last Modified: Thu, 27 Jun 2024 01:00:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd962e639f86a45f71b230523fa9853e763ce72e8b4d9559b335d5c0ef7867`  
		Last Modified: Thu, 27 Jun 2024 01:00:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:1eb543b041810b06af55851c10f5671b66e3af89814ba7731eaeca985670bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307de048b4a15800c805da620e6616eb24d926e48e7b7a5641001ca9a993d6db`

```dockerfile
```

-	Layers:
	-	`sha256:398552615b3802e1090ba4caa9237a4730bc0e072474d16846aa6e20b9e0e4b0`  
		Last Modified: Thu, 27 Jun 2024 01:00:00 GMT  
		Size: 4.9 MB (4909682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3fd2605520a8da5b6b034ee2d7fc3e55fdc87b991b7e0843aa268051a1eb1d`  
		Last Modified: Thu, 27 Jun 2024 00:59:59 GMT  
		Size: 22.8 KB (22792 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.6.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2f2226f05cd2f5607d7c297bc25635cbfada27c562df968f9d1fbae308d0989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197815608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8933c5e3d65274cdbab7fb19bb9b3dce1498396800af02f28458dc6b23efa73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c147e32867f7ecf704c6d4ea1e98ec0418ec22a5719abba183fbe604e9a5fbc`  
		Last Modified: Thu, 27 Jun 2024 05:51:25 GMT  
		Size: 117.4 MB (117426632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae227b193d9e655491e494172db7f39244948b14fcdd790f3c419fb719b3fa`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b6974e9beee1e6b359108ee8adcdc4f31b52b762b3226e63aff37339aa1925`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6729cab256dc7741d2ee1ecb23510335d68da7fe275affd2a81813a72d1fc`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d4582e3b169050999ed4db0a0a01f99ef62a51a564352c7bf7f5660e51afb`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcea5d9dc1273ae352e94632eeea1d3b0cabab2c88eb2e62efde1994ff167e1c`  
		Last Modified: Thu, 27 Jun 2024 05:51:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:6977a21a32ee12ac7b5e36dc647da05451f849596393d8ed616bede821abd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1539afccbf63d331a2dd685b6ac3276994c6b41495664ba79b2eea90186216`

```dockerfile
```

-	Layers:
	-	`sha256:039948e1b38b873f6c28877fcf79806b5cf48249324066c2cf126df6694baa72`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 4.9 MB (4907599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c60cb2021b90a881173a65a90b6f90340430f560262d775c5e6fab338e3d8c4`  
		Last Modified: Thu, 27 Jun 2024 05:51:23 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:64c170857e6b74cc5781fce4e5edc5d37a38d1253f0464a1599f15bccb5b15da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:c35840dc6e0600da3b771705295ed4f0d9def7e9424dbc864475d5e19beb84a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209130314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a79bce40a19f826bf75772ad62f81408222c4d901fb8dc78371d47965234bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de1a802a714075efdf9e7ccf32dc2170a772c9e53645c4fabe080e01166d84`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 11.0 MB (10958236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b1500da74848cfb9484722ab12b24cf6a138bd0d98e9aed33c6950b37337bb`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 127.6 MB (127647811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fbd6a88e0b2a411ee1754d4bdb8487afc7b16e24a0a65a27de4ef3347e6b3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0512a922d9745e1980f2fdb1678295bec6b5b7af4cecb69543bee608649585fd`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ef7ba0531035cc4544826099a5800cf6bd00d1d7031537918740fa84db2eda`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c6a5d76b49928c052a25fecd8558cab10a542e98457001ca39547569931fd3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becb98df7d1350ace6d8d85b4b97309233846312bae9cba163dd753844f1efe`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:dfe1cde09a4d5a59cf13deaea4c1cf4d0ff8061e8abc75b4b9b1ec60aa4d7edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bdd7f2751e8e358faf9d6bc66df0b9f30377674aae51c4ed9a860ea13b52`

```dockerfile
```

-	Layers:
	-	`sha256:08c3db401c900d356edf9f601785badda8f6ccb988ac7fe978eb502034eab375`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 4.9 MB (4947813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d912f09ae5dee3635af7e781e3d7cdfd93b4cfe337bd21f83298f2c923f112e`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:759e03685b5c6d39485608214dac43909e0d2734eec17a6490d0fe2ecaa8c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207551737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a08fb49a187c86ed49db8f6eb90275414ced5407d30b1b48207279dbf8de8a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc938a7d17787b324a737e60ca20738e63dc506cf01340dd12025a83e1f73c1`  
		Last Modified: Thu, 27 Jun 2024 05:50:39 GMT  
		Size: 127.2 MB (127159766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d212a44d8faf2e1f263bdd411d9b3af261d08031f02dbc3d9b25b0091cadc9`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576289bf48d3ea49186ec79d6f314d62e0ed0cd3f087001f788d4d45bc0a79f`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44870500fd13f254f73ba1d8ff1c9a77a4c420d3bd9043c71c8c07189be0d09c`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60e2d8212e7cca5bf7b3d11bbe2c971f41398d020cdc4e06b9317c22aa7a2b`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4caec4b03c0f0550583bf3c5762efa8dfee3bd2667a90991d1020c1ca14e6`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:f749aa1ccbcee951e69ba29e526684156a4425e040a1347556c31147b7ad32ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4969203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bc7c2413f9628c04fc234402f35c58bbc65c1f5d86a7f297a15f85b91fdbc9`

```dockerfile
```

-	Layers:
	-	`sha256:500e2592d2cd36b500b2bf1d482969225e14c56824345f6b1793991b67b3020b`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 4.9 MB (4945742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e648297813cfb7e9632c9361d4fd7f5fe6a278381c0d48994a6e63baf0e6d5`  
		Last Modified: Thu, 27 Jun 2024 05:50:35 GMT  
		Size: 23.5 KB (23461 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.2`

```console
$ docker pull crate@sha256:64c170857e6b74cc5781fce4e5edc5d37a38d1253f0464a1599f15bccb5b15da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.2` - linux; amd64

```console
$ docker pull crate@sha256:c35840dc6e0600da3b771705295ed4f0d9def7e9424dbc864475d5e19beb84a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209130314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a79bce40a19f826bf75772ad62f81408222c4d901fb8dc78371d47965234bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de1a802a714075efdf9e7ccf32dc2170a772c9e53645c4fabe080e01166d84`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 11.0 MB (10958236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b1500da74848cfb9484722ab12b24cf6a138bd0d98e9aed33c6950b37337bb`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 127.6 MB (127647811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fbd6a88e0b2a411ee1754d4bdb8487afc7b16e24a0a65a27de4ef3347e6b3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0512a922d9745e1980f2fdb1678295bec6b5b7af4cecb69543bee608649585fd`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ef7ba0531035cc4544826099a5800cf6bd00d1d7031537918740fa84db2eda`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c6a5d76b49928c052a25fecd8558cab10a542e98457001ca39547569931fd3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becb98df7d1350ace6d8d85b4b97309233846312bae9cba163dd753844f1efe`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.2` - unknown; unknown

```console
$ docker pull crate@sha256:dfe1cde09a4d5a59cf13deaea4c1cf4d0ff8061e8abc75b4b9b1ec60aa4d7edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bdd7f2751e8e358faf9d6bc66df0b9f30377674aae51c4ed9a860ea13b52`

```dockerfile
```

-	Layers:
	-	`sha256:08c3db401c900d356edf9f601785badda8f6ccb988ac7fe978eb502034eab375`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 4.9 MB (4947813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d912f09ae5dee3635af7e781e3d7cdfd93b4cfe337bd21f83298f2c923f112e`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:759e03685b5c6d39485608214dac43909e0d2734eec17a6490d0fe2ecaa8c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207551737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a08fb49a187c86ed49db8f6eb90275414ced5407d30b1b48207279dbf8de8a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc938a7d17787b324a737e60ca20738e63dc506cf01340dd12025a83e1f73c1`  
		Last Modified: Thu, 27 Jun 2024 05:50:39 GMT  
		Size: 127.2 MB (127159766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d212a44d8faf2e1f263bdd411d9b3af261d08031f02dbc3d9b25b0091cadc9`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576289bf48d3ea49186ec79d6f314d62e0ed0cd3f087001f788d4d45bc0a79f`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44870500fd13f254f73ba1d8ff1c9a77a4c420d3bd9043c71c8c07189be0d09c`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60e2d8212e7cca5bf7b3d11bbe2c971f41398d020cdc4e06b9317c22aa7a2b`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4caec4b03c0f0550583bf3c5762efa8dfee3bd2667a90991d1020c1ca14e6`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.2` - unknown; unknown

```console
$ docker pull crate@sha256:f749aa1ccbcee951e69ba29e526684156a4425e040a1347556c31147b7ad32ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4969203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bc7c2413f9628c04fc234402f35c58bbc65c1f5d86a7f297a15f85b91fdbc9`

```dockerfile
```

-	Layers:
	-	`sha256:500e2592d2cd36b500b2bf1d482969225e14c56824345f6b1793991b67b3020b`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 4.9 MB (4945742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e648297813cfb7e9632c9361d4fd7f5fe6a278381c0d48994a6e63baf0e6d5`  
		Last Modified: Thu, 27 Jun 2024 05:50:35 GMT  
		Size: 23.5 KB (23461 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:64c170857e6b74cc5781fce4e5edc5d37a38d1253f0464a1599f15bccb5b15da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:c35840dc6e0600da3b771705295ed4f0d9def7e9424dbc864475d5e19beb84a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209130314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a79bce40a19f826bf75772ad62f81408222c4d901fb8dc78371d47965234bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:587e68e1d836d406ed1bbaf40ce890c5e3a654e040152a61037390a552e5a3bd`  
		Last Modified: Fri, 31 May 2024 02:02:51 GMT  
		Size: 68.6 MB (68578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de1a802a714075efdf9e7ccf32dc2170a772c9e53645c4fabe080e01166d84`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 11.0 MB (10958236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b1500da74848cfb9484722ab12b24cf6a138bd0d98e9aed33c6950b37337bb`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 127.6 MB (127647811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fbd6a88e0b2a411ee1754d4bdb8487afc7b16e24a0a65a27de4ef3347e6b3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0512a922d9745e1980f2fdb1678295bec6b5b7af4cecb69543bee608649585fd`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ef7ba0531035cc4544826099a5800cf6bd00d1d7031537918740fa84db2eda`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c6a5d76b49928c052a25fecd8558cab10a542e98457001ca39547569931fd3`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becb98df7d1350ace6d8d85b4b97309233846312bae9cba163dd753844f1efe`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:dfe1cde09a4d5a59cf13deaea4c1cf4d0ff8061e8abc75b4b9b1ec60aa4d7edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bdd7f2751e8e358faf9d6bc66df0b9f30377674aae51c4ed9a860ea13b52`

```dockerfile
```

-	Layers:
	-	`sha256:08c3db401c900d356edf9f601785badda8f6ccb988ac7fe978eb502034eab375`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 4.9 MB (4947813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d912f09ae5dee3635af7e781e3d7cdfd93b4cfe337bd21f83298f2c923f112e`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:759e03685b5c6d39485608214dac43909e0d2734eec17a6490d0fe2ecaa8c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207551737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a08fb49a187c86ed49db8f6eb90275414ced5407d30b1b48207279dbf8de8a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 15:50:21 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Thu, 30 May 2024 15:50:21 GMT
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
	-	`sha256:e4f0aaabb2208daf94c2d9031bb3ff168c55592542281a254653d807cf50cac8`  
		Last Modified: Fri, 31 May 2024 02:02:54 GMT  
		Size: 67.5 MB (67501391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1388d244772e68cc2476909a75ec9d98cd7851b098ae7c3fdbad01ccf39e1`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 10.9 MB (10945071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc938a7d17787b324a737e60ca20738e63dc506cf01340dd12025a83e1f73c1`  
		Last Modified: Thu, 27 Jun 2024 05:50:39 GMT  
		Size: 127.2 MB (127159766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d212a44d8faf2e1f263bdd411d9b3af261d08031f02dbc3d9b25b0091cadc9`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576289bf48d3ea49186ec79d6f314d62e0ed0cd3f087001f788d4d45bc0a79f`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44870500fd13f254f73ba1d8ff1c9a77a4c420d3bd9043c71c8c07189be0d09c`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60e2d8212e7cca5bf7b3d11bbe2c971f41398d020cdc4e06b9317c22aa7a2b`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4caec4b03c0f0550583bf3c5762efa8dfee3bd2667a90991d1020c1ca14e6`  
		Last Modified: Thu, 27 Jun 2024 05:50:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f749aa1ccbcee951e69ba29e526684156a4425e040a1347556c31147b7ad32ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4969203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bc7c2413f9628c04fc234402f35c58bbc65c1f5d86a7f297a15f85b91fdbc9`

```dockerfile
```

-	Layers:
	-	`sha256:500e2592d2cd36b500b2bf1d482969225e14c56824345f6b1793991b67b3020b`  
		Last Modified: Thu, 27 Jun 2024 05:50:36 GMT  
		Size: 4.9 MB (4945742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e648297813cfb7e9632c9361d4fd7f5fe6a278381c0d48994a6e63baf0e6d5`  
		Last Modified: Thu, 27 Jun 2024 05:50:35 GMT  
		Size: 23.5 KB (23461 bytes)  
		MIME: application/vnd.in-toto+json
