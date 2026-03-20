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
$ docker pull crate@sha256:36cb3767c2403ddc7fff864e4a61d296f0168347ee5c985c174b4a1ad9f91249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:a499674bf64b02c81fcf49e9d597e5df328ac416f39b89ba915fde524a060f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233815987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76a9a95054d545c2f98372b6c61f95657ba0216aa42e8c1a2f9eba6e5555d81`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:55 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:55 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:55 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:55 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d42d1df61c8c2adee7880e339bb2e124cd1cbcb11b5ab020fb89bd58bab5eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 13.1 MB (13051148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7173979866676d5e0789bd96c60fddc420e9ed7673ca28ce77d882e4fbf43d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:16 GMT  
		Size: 151.3 MB (151299527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81ca6896638763ef003121d60922fc11d7c1e7ae1d7fbcadfcf003b0c499ac1`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60ab311bbce78472dc2f56e1d8ad2a2278449323e25c41eefccd7cad74e71d`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3e66a9903d0b0fbdf320cdb9b769177b59050874bc052bd72a525050532d9`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d33be94b10eba090d1e942b9daf0ebc34b33558395eec9cdff3722d32ff1d6a`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccb71e1d4e87b54ba418ad25b2cd92fc2d8a7f24a5645511ae500d9a0c348d3`  
		Last Modified: Fri, 06 Mar 2026 18:17:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:a03aa2c04e05136b7329c25aea398509fb38e488f4ecd4fa89fe040c25ffe9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d70993efa875744a8d6594da736dd5122a87786cdc82499784005a4a0387c3b`

```dockerfile
```

-	Layers:
	-	`sha256:4d61d67630d9fefe9f84d591581129f1e15ab4c59c2676895559e16fd11860a2`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 5.2 MB (5156500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af05c066a22fa5cd225786881484865ec2531bb64e138c160997166cbf3b512f`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:09960e34d2389e3b4647796b37ac2e27c5ac76f1e92d0ed6073d78a732c30f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230419274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82521b5f7aad1a3028dcad2a2468a2726cb70c876b02ccd1e2d1f3f68bb05221`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:47 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb9966dd80a3c898b0ab4dfdf34be280f5e8f2797e33791b371a24ad52e1673`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 13.1 MB (13104611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa64a45453b88dd2dfbce5e53084242d601bfaaec48593efc67cc3761f5b21d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:09 GMT  
		Size: 149.3 MB (149269172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77638d5af0c1c9c9b26f5ff46cd1fd8d1aa2d96a4cf850770943183966a463d`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9b6226a425c7b05f2722d7fffb61971d74036000d49566cafd5b793c92d3e2`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd466f939c44100b794f11ec968e922144a624039be67f43ce20edce1aeb79`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb5261e92a29a5a3f4631919be5c9d3cae4e08fac50bf6c800caa10f33837d6`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c19ec6771d12a701007f67fefd01143bdf2369ee39ed697f2bd9dda68ae235`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:6f85ca3a9ae8b6d3c087cf44808bc8541ffa1472a6f6503c76c2c5358d8a6bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8e8c27058f8de779676de200459c45dfeda64bb61d03238a0c28ba2b076134`

```dockerfile
```

-	Layers:
	-	`sha256:83daa76baf0914e0cd92f6026b8a04d477a1045eb33c18ff55b8f14e4bf6cedc`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 5.2 MB (5154419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4824ec79e890e47441646d72de5b24ac5ead97d18f186a28ce35f3c057390eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.3`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:36cb3767c2403ddc7fff864e4a61d296f0168347ee5c985c174b4a1ad9f91249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:a499674bf64b02c81fcf49e9d597e5df328ac416f39b89ba915fde524a060f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233815987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76a9a95054d545c2f98372b6c61f95657ba0216aa42e8c1a2f9eba6e5555d81`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:55 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:55 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:55 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:55 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d42d1df61c8c2adee7880e339bb2e124cd1cbcb11b5ab020fb89bd58bab5eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 13.1 MB (13051148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7173979866676d5e0789bd96c60fddc420e9ed7673ca28ce77d882e4fbf43d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:16 GMT  
		Size: 151.3 MB (151299527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81ca6896638763ef003121d60922fc11d7c1e7ae1d7fbcadfcf003b0c499ac1`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60ab311bbce78472dc2f56e1d8ad2a2278449323e25c41eefccd7cad74e71d`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3e66a9903d0b0fbdf320cdb9b769177b59050874bc052bd72a525050532d9`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d33be94b10eba090d1e942b9daf0ebc34b33558395eec9cdff3722d32ff1d6a`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccb71e1d4e87b54ba418ad25b2cd92fc2d8a7f24a5645511ae500d9a0c348d3`  
		Last Modified: Fri, 06 Mar 2026 18:17:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:a03aa2c04e05136b7329c25aea398509fb38e488f4ecd4fa89fe040c25ffe9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d70993efa875744a8d6594da736dd5122a87786cdc82499784005a4a0387c3b`

```dockerfile
```

-	Layers:
	-	`sha256:4d61d67630d9fefe9f84d591581129f1e15ab4c59c2676895559e16fd11860a2`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 5.2 MB (5156500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af05c066a22fa5cd225786881484865ec2531bb64e138c160997166cbf3b512f`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:09960e34d2389e3b4647796b37ac2e27c5ac76f1e92d0ed6073d78a732c30f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230419274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82521b5f7aad1a3028dcad2a2468a2726cb70c876b02ccd1e2d1f3f68bb05221`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:47 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb9966dd80a3c898b0ab4dfdf34be280f5e8f2797e33791b371a24ad52e1673`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 13.1 MB (13104611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa64a45453b88dd2dfbce5e53084242d601bfaaec48593efc67cc3761f5b21d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:09 GMT  
		Size: 149.3 MB (149269172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77638d5af0c1c9c9b26f5ff46cd1fd8d1aa2d96a4cf850770943183966a463d`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9b6226a425c7b05f2722d7fffb61971d74036000d49566cafd5b793c92d3e2`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd466f939c44100b794f11ec968e922144a624039be67f43ce20edce1aeb79`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb5261e92a29a5a3f4631919be5c9d3cae4e08fac50bf6c800caa10f33837d6`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c19ec6771d12a701007f67fefd01143bdf2369ee39ed697f2bd9dda68ae235`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:6f85ca3a9ae8b6d3c087cf44808bc8541ffa1472a6f6503c76c2c5358d8a6bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8e8c27058f8de779676de200459c45dfeda64bb61d03238a0c28ba2b076134`

```dockerfile
```

-	Layers:
	-	`sha256:83daa76baf0914e0cd92f6026b8a04d477a1045eb33c18ff55b8f14e4bf6cedc`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 5.2 MB (5154419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4824ec79e890e47441646d72de5b24ac5ead97d18f186a28ce35f3c057390eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
