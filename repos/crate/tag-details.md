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
$ docker pull crate@sha256:2c7d730f4c4ec94916bd07b3ba99780cf62647065973b694dc9b0d8638e8d102
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
$ docker pull crate@sha256:6c9b7895617d0424415799dcb50f9c99acfd121bd751a9fba791381986641fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297346447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653536eab918527beb4cd5d94519a9acc6268edafc327b87a2e2e88f6ae5086f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6197b7d94066d9434963e5d862459d95fc96e465759d5974476e628bb6784f96`  
		Last Modified: Fri, 21 Jun 2024 07:15:53 GMT  
		Size: 227.9 MB (227888369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebdd398c5f62408e07fd1b4503e918957aae716fdf3c012f97bab1a67d253c`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 1.9 MB (1939586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d6e6d954fc425734a6a7e5ade0d7ea05cff9ea2480bcde86dd24ed5ab51ec`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5b7f8a5e79d509effe21136be1608abb8e06dca996870c58903464f73a1e1`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3c6240b70ba1e90b760be6f0aba3b7470870ffee6f68c58481a0ad09a952ff`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fc2cd5c71d584d12610118e8bee099663cf206c003eefdbf9b3a63b661341`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4` - unknown; unknown

```console
$ docker pull crate@sha256:9deaf5ce0827b672c6d8cb1c7cb1368c5e67f88b6593bb5f979137bab4a4222c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d6c2a3654a7de137e89190a343cf8d6ead2f519c7ec4f9c0dc6d398e95cf3`

```dockerfile
```

-	Layers:
	-	`sha256:43bcb2cb5ee6980e0d9b1aa1842a62ce75fcebf8ebebea818c5ab9e606dd4978`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 4.9 MB (4904362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3c68611bcffdfc437084ad5b0ac94a373b6718806feda36b63e14f371078f8`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.4.8`

```console
$ docker pull crate@sha256:2c7d730f4c4ec94916bd07b3ba99780cf62647065973b694dc9b0d8638e8d102
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
$ docker pull crate@sha256:6c9b7895617d0424415799dcb50f9c99acfd121bd751a9fba791381986641fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297346447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653536eab918527beb4cd5d94519a9acc6268edafc327b87a2e2e88f6ae5086f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 17:48:09 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6197b7d94066d9434963e5d862459d95fc96e465759d5974476e628bb6784f96`  
		Last Modified: Fri, 21 Jun 2024 07:15:53 GMT  
		Size: 227.9 MB (227888369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebdd398c5f62408e07fd1b4503e918957aae716fdf3c012f97bab1a67d253c`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 1.9 MB (1939586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d6e6d954fc425734a6a7e5ade0d7ea05cff9ea2480bcde86dd24ed5ab51ec`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5b7f8a5e79d509effe21136be1608abb8e06dca996870c58903464f73a1e1`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3c6240b70ba1e90b760be6f0aba3b7470870ffee6f68c58481a0ad09a952ff`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fc2cd5c71d584d12610118e8bee099663cf206c003eefdbf9b3a63b661341`  
		Last Modified: Fri, 21 Jun 2024 07:15:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.4.8` - unknown; unknown

```console
$ docker pull crate@sha256:9deaf5ce0827b672c6d8cb1c7cb1368c5e67f88b6593bb5f979137bab4a4222c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d6c2a3654a7de137e89190a343cf8d6ead2f519c7ec4f9c0dc6d398e95cf3`

```dockerfile
```

-	Layers:
	-	`sha256:43bcb2cb5ee6980e0d9b1aa1842a62ce75fcebf8ebebea818c5ab9e606dd4978`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 4.9 MB (4904362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3c68611bcffdfc437084ad5b0ac94a373b6718806feda36b63e14f371078f8`  
		Last Modified: Fri, 21 Jun 2024 07:15:49 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5`

```console
$ docker pull crate@sha256:612bb4a1998be4b1ece5eb688566c148b21cb8ea41bcd270c0214477eac41dae
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
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.4`

```console
$ docker pull crate@sha256:612bb4a1998be4b1ece5eb688566c148b21cb8ea41bcd270c0214477eac41dae
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
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.4` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.5.5`

```console
$ docker pull crate@sha256:612bb4a1998be4b1ece5eb688566c148b21cb8ea41bcd270c0214477eac41dae
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
$ docker pull crate@sha256:4390b4c5d01e422e6883ebc9487e32eaa1d75bb2aab5525a0c59204979117a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185760429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668fd7dfceefc6d142d36a85b7e13504d3558f79cdd883051ee5b7186393ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 29 Jan 2024 18:39:32 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc8190b30a2a8331316ec6a481ba66a7c2b66f4eede1097ed5df06ecd7856e6`  
		Last Modified: Fri, 21 Jun 2024 07:14:49 GMT  
		Size: 116.3 MB (116302353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3f48995b67f294391e385c312267a7ae21782aebb970f898872ecdb97ed34`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 1.9 MB (1939587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd265207878d1d35ff113e65105e7ec559844b7faa27cbe683dd466ec8b86ba`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae429234ff1c70c9b66b5a63ff6792cf9cd37def7dfe81721c3abb0db921a26c`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365a075602298f5a213c52aff0b113bf9f254d3895de871aeba9d0c31f31d50`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65918ca1e4e868f824aa08a89d62490e582326c10c140bc6d55de6914a0ab19`  
		Last Modified: Fri, 21 Jun 2024 07:14:47 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.5.5` - unknown; unknown

```console
$ docker pull crate@sha256:38319c6243853e35172ee0092b494b978ac356c7c28903aebe68408b2b7e0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a249b8743ce40056fdc9cf5139645d5df9999dd6ddc3b8b890c937981b16e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9740ecd3a0364fc0b6f9fe1ecb1ae44212189592624bdef1a7cc673ddb2031`  
		Last Modified: Fri, 21 Jun 2024 07:14:46 GMT  
		Size: 4.9 MB (4907854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d950fc5b12019d49031b9e83171886b792183ca7d88e60921427d503719d67c`  
		Last Modified: Fri, 21 Jun 2024 07:14:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6`

```console
$ docker pull crate@sha256:78677bd7c330648ad83115ad9777992bd33b22db50a3a336a1194c067b70addb
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
$ docker pull crate@sha256:ca7b0adc7a9ae7675625ebb5157bd9f6a932777586586ffd1907d0a8d0690629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186885776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b306af9b11b2a4ca8d8d5ae70fa01314022fc4e83fde59eea6aeabbb2278bbb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497854d6ecf796d164cfd72f6ab25d5b8b87510a455668c71a02ef8fd3a5cfe7`  
		Last Modified: Fri, 21 Jun 2024 07:13:58 GMT  
		Size: 117.4 MB (117426650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54deb0e70b569452bdb4ca1236e0941d6ca005271583d14634acafca167f0f`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebf456af4786a8ba19e6bc2963d4901233960c2ddd0e2c46735adf326a8e69`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64152a91245b85b9f7b92f8f0198b673c8ebcba1dfd5cd69b8676f01044d026`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73300b322cf7777ec0ddac485e316de893cbf556dce957035a653e252769c93c`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff357aeb7705f9e10a6a29e1b040f766f73c3674011ce52037c045efa1d7bc94`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6` - unknown; unknown

```console
$ docker pull crate@sha256:000c64b9eb1b47b9b6e252db978882e14302329ff4dfbb368ed36e2c785841d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c19ae11b4e13629837b9ad93fbd716e851f669aa597bf40f4db463ad16da40`

```dockerfile
```

-	Layers:
	-	`sha256:a3914984236a06cc63c6b2936b14b462c4e11f145d69045eadd3d767fbe0f6ec`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826c98aa6ee51897a4efb972d746fa82c9847539c5e99220c199429bc8e4caf1`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.6.5`

```console
$ docker pull crate@sha256:78677bd7c330648ad83115ad9777992bd33b22db50a3a336a1194c067b70addb
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
$ docker pull crate@sha256:ca7b0adc7a9ae7675625ebb5157bd9f6a932777586586ffd1907d0a8d0690629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186885776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b306af9b11b2a4ca8d8d5ae70fa01314022fc4e83fde59eea6aeabbb2278bbb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 02 May 2024 12:27:16 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497854d6ecf796d164cfd72f6ab25d5b8b87510a455668c71a02ef8fd3a5cfe7`  
		Last Modified: Fri, 21 Jun 2024 07:13:58 GMT  
		Size: 117.4 MB (117426650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54deb0e70b569452bdb4ca1236e0941d6ca005271583d14634acafca167f0f`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 1.9 MB (1940637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebf456af4786a8ba19e6bc2963d4901233960c2ddd0e2c46735adf326a8e69`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64152a91245b85b9f7b92f8f0198b673c8ebcba1dfd5cd69b8676f01044d026`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73300b322cf7777ec0ddac485e316de893cbf556dce957035a653e252769c93c`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff357aeb7705f9e10a6a29e1b040f766f73c3674011ce52037c045efa1d7bc94`  
		Last Modified: Fri, 21 Jun 2024 07:13:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.6.5` - unknown; unknown

```console
$ docker pull crate@sha256:000c64b9eb1b47b9b6e252db978882e14302329ff4dfbb368ed36e2c785841d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c19ae11b4e13629837b9ad93fbd716e851f669aa597bf40f4db463ad16da40`

```dockerfile
```

-	Layers:
	-	`sha256:a3914984236a06cc63c6b2936b14b462c4e11f145d69045eadd3d767fbe0f6ec`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826c98aa6ee51897a4efb972d746fa82c9847539c5e99220c199429bc8e4caf1`  
		Last Modified: Fri, 21 Jun 2024 07:13:55 GMT  
		Size: 22.9 KB (22875 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:e8cb3d422e56da9f57ac19ee58590bb280ec3319487f61ec7153712863c99c99
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
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.2`

```console
$ docker pull crate@sha256:e8cb3d422e56da9f57ac19ee58590bb280ec3319487f61ec7153712863c99c99
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
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.2` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:e8cb3d422e56da9f57ac19ee58590bb280ec3319487f61ec7153712863c99c99
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
$ docker pull crate@sha256:923f8ba39ff9b833a0098492a9ef541fffbdecfc27c9b26e67b537a8b763ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196621836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d223ba82a70fab3f4ad6dfef9ea85b51aeb91f3817702b5cf1df9457eb58e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
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
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b38b0fb608e402bc27b57241ae5790993fbe0382b7c704ff5065125e4d126`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 17.6 KB (17609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe29766f4309c741ef9760505facfc060f2354025b2002d05e609817bbd334a`  
		Last Modified: Fri, 21 Jun 2024 07:13:10 GMT  
		Size: 127.2 MB (127159721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4d5e59e5db2e293c1eb22f2afb00c2b723fe0cb60254e81ca44bc3bb4d237`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421fd4374e45f978724b378517d9cccf563e858bb1bcc069c4042fd98179af3`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0002738e59c223b72d22cd0a67116c4654c2fd54358e3ea05f3a18623c6ba`  
		Last Modified: Fri, 21 Jun 2024 07:13:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90afa3b6f3f7c13c7c6126f95b8a31cf1b36b09977b47a3b6e5f8c9bb10b95`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7a16692f5a2d03f05cc79f86d312019838a34788fb3d96249139de6b32b4d`  
		Last Modified: Fri, 21 Jun 2024 07:13:09 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:bde67d83ea51d721d26b70d9037380584b754f01503829f3018da0bc6df725d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4968901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720e27d234553d16994b6bcaacaf8914c620e3c878d83be3d6cfc4195be2851`

```dockerfile
```

-	Layers:
	-	`sha256:a6f3254c2caf8b2bdcdc7d7bf78a41c56a7bae04702ce701b16c075561602f2e`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 4.9 MB (4945718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a6a1ea8ddd57aed0d61e517fc9e43d0a5fbe7b59024fa46a5449a7b5b630ce`  
		Last Modified: Fri, 21 Jun 2024 07:13:07 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json
