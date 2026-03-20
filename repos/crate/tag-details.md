<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.1`](#crate61)
-	[`crate:6.1.3`](#crate613)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.3`](#crate623)
-	[`crate:latest`](#cratelatest)

## `crate:6.1`

```console
$ docker pull crate@sha256:b5ad862d8ffc9ec706cf26e96b5fbf9741d697c023f6e020f2c1a907758aa7d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:033274b8ef218540c51650f6c86e6ead08661bd290014dd303c550303cb2c3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231668836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4d2bcd19666b91ff11f65e891d655f74f02487dc5259a634146ebee2377d0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:12:50 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:13:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:13:03 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:13:03 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:13:03 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:13:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Fri, 27 Feb 2026 23:13:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:13:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec6487de6519d8a3c1bd8d0090102c9dd6e020c1a5bef7d7ab7101da8409a1e`  
		Last Modified: Fri, 27 Feb 2026 23:13:21 GMT  
		Size: 13.1 MB (13051195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2e8db4c5e94155301a9e067440e98d1bd6662a7a710a6442febe9fa8921c33`  
		Last Modified: Fri, 27 Feb 2026 23:13:25 GMT  
		Size: 149.2 MB (149152342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5364712af880ab8946126b440cb16425c8563be3ce531393cf53b00e25298f`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db333b1ce761efa43df629af5f337cadc187b81099ff27f2cb74ec48160d89e4`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9f33186a31c625d5e5903f6a149d0a63eabe0e042fd6d24b2f495c9c1719d`  
		Last Modified: Fri, 27 Feb 2026 23:13:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7784afc39d2af6bec07fa0d516a4031f5baeeaae2472611c3c38b8b27cab4eb`  
		Last Modified: Fri, 27 Feb 2026 23:13:22 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52be4b8f6141ed0b178c6d0a77b3a92c0fa99743eee057d2bb9d807f06a27a`  
		Last Modified: Fri, 27 Feb 2026 23:13:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:a9fa343af935423b18fbfba37bdd9780c210695f0cf31834804b7c09691d8bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdc1c17f98603db358e235f77169c084cd857d164bfff1901578698f521ca06`

```dockerfile
```

-	Layers:
	-	`sha256:11cd7c93b7a68fbfd7a714f3a00a655cd36158727ef36f7c403c723e6448e4af`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 5.2 MB (5150676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538eab3050f00e2e79ead97bd4796f95dd56265406f6911bc2e75b453c31ff42`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:14916928b4d0b2a699033171911f24c226c3c66a4d9c33a0cdd6dda93f903f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230991250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736f78cbafa72e61a134062a0adbe13bdd8a15eed31f0a53089ec190795c0df3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:12:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:12:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:12:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:12:48 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:12:48 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:12:48 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:12:48 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Fri, 27 Feb 2026 23:12:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:12:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55f22c718823d2fb4483154449db25a753a46067ec4ad2df1607568e6f4eef0`  
		Last Modified: Fri, 27 Feb 2026 23:13:06 GMT  
		Size: 13.1 MB (13104605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4a68011d1f4b2b0e30855c024d0ea394026fd7c3912c58e16979ed93b8f19c`  
		Last Modified: Fri, 27 Feb 2026 23:13:08 GMT  
		Size: 149.8 MB (149841152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b8970ab9821d4e69841431a131fb354a7334a96d912ca39acfdf6bec214169`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b325af4c8090d2d071b25a072007b205a702ea3f6ff80921dae29b54a7d62d`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2a878e37f1c8a83ee47ba983ff9df7ee73ede3dadda33e6a5da7338563eb6a`  
		Last Modified: Fri, 27 Feb 2026 23:13:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1b836b24fddbfd8e357de546499abbdfc4a769263bc8222131f9438ccb7081`  
		Last Modified: Fri, 27 Feb 2026 23:13:07 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ce8c6bbe8159bd4e3ae2d7ad0a6f7dfbe28b45ca55ab0f42a0b4d6ec918b4`  
		Last Modified: Fri, 27 Feb 2026 23:13:07 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:15b66bf5fe655e8b18df083cf4437f0cde92e6d725c12f750e3e469feccd6f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a09c625d9bda17d9131616457a477a2abf122602df22a0a42f9e29bd0e725f`

```dockerfile
```

-	Layers:
	-	`sha256:a10feeef5c9be7c8ecca2083a954ac56f7cb2cc71fecf071730ac4227b02d6c2`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 5.1 MB (5148583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910e5efaffc326a503ca9c0c514ff22221573f92bb60567ba4fb10b1b3d8be61`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.3`

```console
$ docker pull crate@sha256:b5ad862d8ffc9ec706cf26e96b5fbf9741d697c023f6e020f2c1a907758aa7d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.3` - linux; amd64

```console
$ docker pull crate@sha256:033274b8ef218540c51650f6c86e6ead08661bd290014dd303c550303cb2c3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231668836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4d2bcd19666b91ff11f65e891d655f74f02487dc5259a634146ebee2377d0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:12:50 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:13:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:13:03 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:13:03 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:13:03 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:13:03 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:13:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Fri, 27 Feb 2026 23:13:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:13:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:13:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec6487de6519d8a3c1bd8d0090102c9dd6e020c1a5bef7d7ab7101da8409a1e`  
		Last Modified: Fri, 27 Feb 2026 23:13:21 GMT  
		Size: 13.1 MB (13051195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2e8db4c5e94155301a9e067440e98d1bd6662a7a710a6442febe9fa8921c33`  
		Last Modified: Fri, 27 Feb 2026 23:13:25 GMT  
		Size: 149.2 MB (149152342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5364712af880ab8946126b440cb16425c8563be3ce531393cf53b00e25298f`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db333b1ce761efa43df629af5f337cadc187b81099ff27f2cb74ec48160d89e4`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9f33186a31c625d5e5903f6a149d0a63eabe0e042fd6d24b2f495c9c1719d`  
		Last Modified: Fri, 27 Feb 2026 23:13:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7784afc39d2af6bec07fa0d516a4031f5baeeaae2472611c3c38b8b27cab4eb`  
		Last Modified: Fri, 27 Feb 2026 23:13:22 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52be4b8f6141ed0b178c6d0a77b3a92c0fa99743eee057d2bb9d807f06a27a`  
		Last Modified: Fri, 27 Feb 2026 23:13:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.3` - unknown; unknown

```console
$ docker pull crate@sha256:a9fa343af935423b18fbfba37bdd9780c210695f0cf31834804b7c09691d8bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdc1c17f98603db358e235f77169c084cd857d164bfff1901578698f521ca06`

```dockerfile
```

-	Layers:
	-	`sha256:11cd7c93b7a68fbfd7a714f3a00a655cd36158727ef36f7c403c723e6448e4af`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 5.2 MB (5150676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538eab3050f00e2e79ead97bd4796f95dd56265406f6911bc2e75b453c31ff42`  
		Last Modified: Fri, 27 Feb 2026 23:13:20 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:14916928b4d0b2a699033171911f24c226c3c66a4d9c33a0cdd6dda93f903f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230991250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736f78cbafa72e61a134062a0adbe13bdd8a15eed31f0a53089ec190795c0df3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:12:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:12:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.3.tar.gz.asc crate-6.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.3.tar.gz.asc     && tar -xf crate-6.1.3.tar.gz -C /crate --strip-components=1     && rm crate-6.1.3.tar.gz # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:12:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:12:48 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:12:48 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:12:48 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:12:48 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T10:25:22.180622 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.3
# Fri, 27 Feb 2026 23:12:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:12:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:12:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55f22c718823d2fb4483154449db25a753a46067ec4ad2df1607568e6f4eef0`  
		Last Modified: Fri, 27 Feb 2026 23:13:06 GMT  
		Size: 13.1 MB (13104605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4a68011d1f4b2b0e30855c024d0ea394026fd7c3912c58e16979ed93b8f19c`  
		Last Modified: Fri, 27 Feb 2026 23:13:08 GMT  
		Size: 149.8 MB (149841152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b8970ab9821d4e69841431a131fb354a7334a96d912ca39acfdf6bec214169`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b325af4c8090d2d071b25a072007b205a702ea3f6ff80921dae29b54a7d62d`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2a878e37f1c8a83ee47ba983ff9df7ee73ede3dadda33e6a5da7338563eb6a`  
		Last Modified: Fri, 27 Feb 2026 23:13:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1b836b24fddbfd8e357de546499abbdfc4a769263bc8222131f9438ccb7081`  
		Last Modified: Fri, 27 Feb 2026 23:13:07 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ce8c6bbe8159bd4e3ae2d7ad0a6f7dfbe28b45ca55ab0f42a0b4d6ec918b4`  
		Last Modified: Fri, 27 Feb 2026 23:13:07 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.3` - unknown; unknown

```console
$ docker pull crate@sha256:15b66bf5fe655e8b18df083cf4437f0cde92e6d725c12f750e3e469feccd6f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a09c625d9bda17d9131616457a477a2abf122602df22a0a42f9e29bd0e725f`

```dockerfile
```

-	Layers:
	-	`sha256:a10feeef5c9be7c8ecca2083a954ac56f7cb2cc71fecf071730ac4227b02d6c2`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 5.1 MB (5148583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910e5efaffc326a503ca9c0c514ff22221573f92bb60567ba4fb10b1b3d8be61`  
		Last Modified: Fri, 27 Feb 2026 23:13:05 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:d5e86343358492a986feae4789e48cdf822230533b18d54ca17bd0787483ca11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:59ed3713fca1b45d541123d9c2faa81fab0d757b2ef554a66fe413889ef190e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246335537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a888f30eaa42a519a10ec413f84317bb301741ca66f41444088510d29b11f7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:26 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:42 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d4a2f522ee17404b58349e2e9b80e78a9228a0b75805bb5dc937bae4d80d4`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 19.8 MB (19843050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9105668fa79e60b76edc182535ea5999ea9416c27995379545d03efcd4e5d31`  
		Last Modified: Fri, 20 Mar 2026 17:39:04 GMT  
		Size: 151.3 MB (151298417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a6cf1619628c149b3acc6f58dd0c7055b9b2079b339a4880efcf65a474f69`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 7.7 MB (7672387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8191653307aa050f560f612051d03674a07e211f2513d981783acbd44c3b9ee`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500628ef4d316d19457f980998f395f4117a65cfd14a88de20757f3cd6de503e`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad209fe4bba1f9c144bca7917af50d53ef0e81c1e750c9ebf973b40fe46f9029`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb260b3a4c4083630e6895fe424dd7b3e52e5422c09c27c5a6f9fcb3d8d5a3`  
		Last Modified: Fri, 20 Mar 2026 17:39:03 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:26e110b2a7a8c00c56e197fd2c0f26de66d26e717b02ae2c9673dbaca0a9c85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ca2cee829a990a0c234223ac73a995dc4da00fbad1eb4e3744ef7b20512a23`

```dockerfile
```

-	Layers:
	-	`sha256:7b0fe1b293b5fdded81e1fb4912cce9600fa22035dc80c611aeba357f93fae1e`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 6.5 MB (6462601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbdb920ed71d4ed0f3e031df4b37d6737469641f203b8326639678ee44bb4a6`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:25cfdb8b29e22bdbf112a4e6d029ac917868f9988256f7e7d22e8b70b0dc76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242918168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb8be037a74c18a403633ef3dc0eab626563964f321d988d587dbaf9a8393a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:56 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a337b4f954f7fcf1b22f8dc069c4f5504d5a200e7174eda296ae236c02b320`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 19.9 MB (19886912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a866e2afd101ad67942eabfabc06b8f9e8691e59bff21ae3c6849c9323787fa7`  
		Last Modified: Fri, 20 Mar 2026 17:39:19 GMT  
		Size: 149.3 MB (149270162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aef35f43e61cd69dbe33bad393583b4de63adeb3ceddaaff66d3b3b2f9602c`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 7.7 MB (7659235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be18d61fb05b761ba6f7273074ed2d793a3416b9e4ef7aa34f421c4b6c7073`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b5bcb4667b940fa2189d3bce876719dc90d7c4e84e44cbb664f2642a886e5`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee57940efa37bdbc779411e61741b3005e1a878a5bd2c635ac94a485345e07d1`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df8725c273f283d425c87bb804ddf29c401b660d70bb5b8ddc1ddbaa9e52d86`  
		Last Modified: Fri, 20 Mar 2026 17:39:18 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:d8d6f087513adfc9b6850be805c2b23c44a080dbe659e6c4cc2280d4d0182196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4cb7d490022acd121e1f53be88f66aa986ae5db148899dd20a55a87249ae6d`

```dockerfile
```

-	Layers:
	-	`sha256:9112ed5ade70d2955262023d912dc27eb588c94af779edaa157e11d8bbbec245`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 6.5 MB (6460520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb2cd8e50df39d78f7ca8034dd82029d4cb9b68ae1844d3f4b1c66a46f211e7`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.3`

```console
$ docker pull crate@sha256:d5e86343358492a986feae4789e48cdf822230533b18d54ca17bd0787483ca11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.3` - linux; amd64

```console
$ docker pull crate@sha256:59ed3713fca1b45d541123d9c2faa81fab0d757b2ef554a66fe413889ef190e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246335537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a888f30eaa42a519a10ec413f84317bb301741ca66f41444088510d29b11f7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:26 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:42 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d4a2f522ee17404b58349e2e9b80e78a9228a0b75805bb5dc937bae4d80d4`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 19.8 MB (19843050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9105668fa79e60b76edc182535ea5999ea9416c27995379545d03efcd4e5d31`  
		Last Modified: Fri, 20 Mar 2026 17:39:04 GMT  
		Size: 151.3 MB (151298417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a6cf1619628c149b3acc6f58dd0c7055b9b2079b339a4880efcf65a474f69`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 7.7 MB (7672387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8191653307aa050f560f612051d03674a07e211f2513d981783acbd44c3b9ee`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500628ef4d316d19457f980998f395f4117a65cfd14a88de20757f3cd6de503e`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad209fe4bba1f9c144bca7917af50d53ef0e81c1e750c9ebf973b40fe46f9029`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb260b3a4c4083630e6895fe424dd7b3e52e5422c09c27c5a6f9fcb3d8d5a3`  
		Last Modified: Fri, 20 Mar 2026 17:39:03 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.3` - unknown; unknown

```console
$ docker pull crate@sha256:26e110b2a7a8c00c56e197fd2c0f26de66d26e717b02ae2c9673dbaca0a9c85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ca2cee829a990a0c234223ac73a995dc4da00fbad1eb4e3744ef7b20512a23`

```dockerfile
```

-	Layers:
	-	`sha256:7b0fe1b293b5fdded81e1fb4912cce9600fa22035dc80c611aeba357f93fae1e`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 6.5 MB (6462601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbdb920ed71d4ed0f3e031df4b37d6737469641f203b8326639678ee44bb4a6`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:25cfdb8b29e22bdbf112a4e6d029ac917868f9988256f7e7d22e8b70b0dc76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242918168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb8be037a74c18a403633ef3dc0eab626563964f321d988d587dbaf9a8393a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:56 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a337b4f954f7fcf1b22f8dc069c4f5504d5a200e7174eda296ae236c02b320`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 19.9 MB (19886912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a866e2afd101ad67942eabfabc06b8f9e8691e59bff21ae3c6849c9323787fa7`  
		Last Modified: Fri, 20 Mar 2026 17:39:19 GMT  
		Size: 149.3 MB (149270162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aef35f43e61cd69dbe33bad393583b4de63adeb3ceddaaff66d3b3b2f9602c`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 7.7 MB (7659235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be18d61fb05b761ba6f7273074ed2d793a3416b9e4ef7aa34f421c4b6c7073`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b5bcb4667b940fa2189d3bce876719dc90d7c4e84e44cbb664f2642a886e5`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee57940efa37bdbc779411e61741b3005e1a878a5bd2c635ac94a485345e07d1`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df8725c273f283d425c87bb804ddf29c401b660d70bb5b8ddc1ddbaa9e52d86`  
		Last Modified: Fri, 20 Mar 2026 17:39:18 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.3` - unknown; unknown

```console
$ docker pull crate@sha256:d8d6f087513adfc9b6850be805c2b23c44a080dbe659e6c4cc2280d4d0182196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4cb7d490022acd121e1f53be88f66aa986ae5db148899dd20a55a87249ae6d`

```dockerfile
```

-	Layers:
	-	`sha256:9112ed5ade70d2955262023d912dc27eb588c94af779edaa157e11d8bbbec245`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 6.5 MB (6460520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb2cd8e50df39d78f7ca8034dd82029d4cb9b68ae1844d3f4b1c66a46f211e7`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:d5e86343358492a986feae4789e48cdf822230533b18d54ca17bd0787483ca11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:59ed3713fca1b45d541123d9c2faa81fab0d757b2ef554a66fe413889ef190e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246335537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a888f30eaa42a519a10ec413f84317bb301741ca66f41444088510d29b11f7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:26 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:42 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d4a2f522ee17404b58349e2e9b80e78a9228a0b75805bb5dc937bae4d80d4`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 19.8 MB (19843050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9105668fa79e60b76edc182535ea5999ea9416c27995379545d03efcd4e5d31`  
		Last Modified: Fri, 20 Mar 2026 17:39:04 GMT  
		Size: 151.3 MB (151298417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a6cf1619628c149b3acc6f58dd0c7055b9b2079b339a4880efcf65a474f69`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 7.7 MB (7672387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8191653307aa050f560f612051d03674a07e211f2513d981783acbd44c3b9ee`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500628ef4d316d19457f980998f395f4117a65cfd14a88de20757f3cd6de503e`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad209fe4bba1f9c144bca7917af50d53ef0e81c1e750c9ebf973b40fe46f9029`  
		Last Modified: Fri, 20 Mar 2026 17:39:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb260b3a4c4083630e6895fe424dd7b3e52e5422c09c27c5a6f9fcb3d8d5a3`  
		Last Modified: Fri, 20 Mar 2026 17:39:03 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:26e110b2a7a8c00c56e197fd2c0f26de66d26e717b02ae2c9673dbaca0a9c85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ca2cee829a990a0c234223ac73a995dc4da00fbad1eb4e3744ef7b20512a23`

```dockerfile
```

-	Layers:
	-	`sha256:7b0fe1b293b5fdded81e1fb4912cce9600fa22035dc80c611aeba357f93fae1e`  
		Last Modified: Fri, 20 Mar 2026 17:39:01 GMT  
		Size: 6.5 MB (6462601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbdb920ed71d4ed0f3e031df4b37d6737469641f203b8326639678ee44bb4a6`  
		Last Modified: Fri, 20 Mar 2026 17:39:00 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:25cfdb8b29e22bdbf112a4e6d029ac917868f9988256f7e7d22e8b70b0dc76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242918168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb8be037a74c18a403633ef3dc0eab626563964f321d988d587dbaf9a8393a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:38:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 20 Mar 2026 17:38:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.3.tar.gz.asc crate-6.2.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.3.tar.gz.asc     && tar -xf crate-6.2.3.tar.gz -C /crate --strip-components=1     && rm crate-6.2.3.tar.gz # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:38:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 20 Mar 2026 17:38:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
VOLUME [/data]
# Fri, 20 Mar 2026 17:38:56 GMT
WORKDIR /data
# Fri, 20 Mar 2026 17:38:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-17T08:20:31.212028+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.3
# Fri, 20 Mar 2026 17:38:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 17:38:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:38:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a337b4f954f7fcf1b22f8dc069c4f5504d5a200e7174eda296ae236c02b320`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 19.9 MB (19886912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a866e2afd101ad67942eabfabc06b8f9e8691e59bff21ae3c6849c9323787fa7`  
		Last Modified: Fri, 20 Mar 2026 17:39:19 GMT  
		Size: 149.3 MB (149270162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aef35f43e61cd69dbe33bad393583b4de63adeb3ceddaaff66d3b3b2f9602c`  
		Last Modified: Fri, 20 Mar 2026 17:39:16 GMT  
		Size: 7.7 MB (7659235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be18d61fb05b761ba6f7273074ed2d793a3416b9e4ef7aa34f421c4b6c7073`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b5bcb4667b940fa2189d3bce876719dc90d7c4e84e44cbb664f2642a886e5`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee57940efa37bdbc779411e61741b3005e1a878a5bd2c635ac94a485345e07d1`  
		Last Modified: Fri, 20 Mar 2026 17:39:17 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df8725c273f283d425c87bb804ddf29c401b660d70bb5b8ddc1ddbaa9e52d86`  
		Last Modified: Fri, 20 Mar 2026 17:39:18 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d8d6f087513adfc9b6850be805c2b23c44a080dbe659e6c4cc2280d4d0182196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4cb7d490022acd121e1f53be88f66aa986ae5db148899dd20a55a87249ae6d`

```dockerfile
```

-	Layers:
	-	`sha256:9112ed5ade70d2955262023d912dc27eb588c94af779edaa157e11d8bbbec245`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 6.5 MB (6460520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb2cd8e50df39d78f7ca8034dd82029d4cb9b68ae1844d3f4b1c66a46f211e7`  
		Last Modified: Fri, 20 Mar 2026 17:39:15 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
