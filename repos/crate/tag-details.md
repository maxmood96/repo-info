<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.1`](#crate61)
-	[`crate:6.1.3`](#crate613)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.2`](#crate622)
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
$ docker pull crate@sha256:5d5244b69541944f4d87d29f543de127b6d08d235fc984279e3566003b4673cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:9b8c1478d4625c681be60756599fb2a002b2f0ba69043941acdeaadda56d2845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233843735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b5646d240d3f3c6a6b7bb0b651f132534ec4d56e6d41965be83014712b13f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:11:48 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:11:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Fri, 27 Feb 2026 23:11:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:11:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:11:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:11:56 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:11:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:11:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Fri, 27 Feb 2026 23:11:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:11:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7791282da6f42a044dbc8e189f84e6b4972c196241a8e4080849334b44b47b9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 13.1 MB (13051013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04abc80bb772d566d39cd3297f0f3e2be27778f23ac9120b59689c1c168fe3`  
		Last Modified: Fri, 27 Feb 2026 23:12:17 GMT  
		Size: 151.3 MB (151327419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7f57d87e55beab075170094adbeca915063ff2a187dd06685be65243c08e53`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef8090f44150a112f9ad86ee1ff05072bd6fa997a4f8ec7484beeffe74967a`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47cdcbe5587335a6c8c674b56c1e8c626e42f1a439a0363c63a1ba7da5e2a9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa34fdcbd5d57c40a327150b7ce99cfb24e2eae137221e26fdd35044e71e0b`  
		Last Modified: Fri, 27 Feb 2026 23:12:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef61df7eae0da6dcb55dbabfb3094d73bb7167a9d1c7ccde8e45a8315305cf`  
		Last Modified: Fri, 27 Feb 2026 23:12:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:9628cb98c842156335a63d3c680b833fe1bd7d73086e95966cdb118f3e4187b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae395c93f66aea7792baf4263f61b22f8d5b738cb45f46cfeb23a2668ba647b`

```dockerfile
```

-	Layers:
	-	`sha256:e51db1a267b3da9c37e9fe73b414a53890e7dac70dfe6aaa108dafb578eea0e9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 5.2 MB (5156451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98a2a796dc2a311d7b102cc7b2ab553d70bda03812c05940d8446728bc1bd31`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:fb32260cdc30e3f8c1bace70f4c95511ae587e328bca38662a954acca8373050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230449740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c127fdb52412e46e67c6fa908ca947cc0941332c2e2d69961b6f307eeef132`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:11:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:12:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:12:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:12:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:12:11 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:12:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:12:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Fri, 27 Feb 2026 23:12:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:12:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78282673ebf00c196545a69e0d1c5c2f4331da09c945a29296fe96ac47cf0634`  
		Last Modified: Fri, 27 Feb 2026 23:12:29 GMT  
		Size: 13.1 MB (13104609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86107e01bdcc66bacd5da83d3064732d6597da686ac936325fd0d7060be20535`  
		Last Modified: Fri, 27 Feb 2026 23:12:32 GMT  
		Size: 149.3 MB (149299644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e9f865b06b0e7de35d3d65b2fbdfff49b3e2fc4fd33a976a36eea88cc05887`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe0784cf2e95ef508e80ad7ee6e60600d0509350dea2f75643019945849f4a`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2109279352d3886755378fe52037e7e4362a7642ba940266b0eed254a287e50`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a73cfb9bbbbad1a0617fc3f6f3efee87ca503558e1d4b78ed84f029638b0c8`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45546e703f7ef3e6183e5456c9b6d43719e68bcc7b94b5cf72c83568f4a28`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:6db5dfca2bab46772d9d45378b800ff0ed142ba66b03975c82c7084563af682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc936990baf0601b3701bd29262b03876cf77782161c24bfa20019ff76e4b38`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f7e911bf6c374cae51d5d6589e0b25a9035a4daa2328b34ef336f51eea254`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 5.2 MB (5154370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f0228d0a23156f5b58474a886076f9eb9bc38a8ce07deb1257a2ebaf49d364`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 23.3 KB (23276 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.2`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:5d5244b69541944f4d87d29f543de127b6d08d235fc984279e3566003b4673cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9b8c1478d4625c681be60756599fb2a002b2f0ba69043941acdeaadda56d2845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233843735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b5646d240d3f3c6a6b7bb0b651f132534ec4d56e6d41965be83014712b13f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:11:48 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:11:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Fri, 27 Feb 2026 23:11:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:11:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:11:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:11:56 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:11:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:11:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Fri, 27 Feb 2026 23:11:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:11:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:11:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7791282da6f42a044dbc8e189f84e6b4972c196241a8e4080849334b44b47b9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 13.1 MB (13051013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04abc80bb772d566d39cd3297f0f3e2be27778f23ac9120b59689c1c168fe3`  
		Last Modified: Fri, 27 Feb 2026 23:12:17 GMT  
		Size: 151.3 MB (151327419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7f57d87e55beab075170094adbeca915063ff2a187dd06685be65243c08e53`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef8090f44150a112f9ad86ee1ff05072bd6fa997a4f8ec7484beeffe74967a`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47cdcbe5587335a6c8c674b56c1e8c626e42f1a439a0363c63a1ba7da5e2a9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa34fdcbd5d57c40a327150b7ce99cfb24e2eae137221e26fdd35044e71e0b`  
		Last Modified: Fri, 27 Feb 2026 23:12:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef61df7eae0da6dcb55dbabfb3094d73bb7167a9d1c7ccde8e45a8315305cf`  
		Last Modified: Fri, 27 Feb 2026 23:12:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:9628cb98c842156335a63d3c680b833fe1bd7d73086e95966cdb118f3e4187b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae395c93f66aea7792baf4263f61b22f8d5b738cb45f46cfeb23a2668ba647b`

```dockerfile
```

-	Layers:
	-	`sha256:e51db1a267b3da9c37e9fe73b414a53890e7dac70dfe6aaa108dafb578eea0e9`  
		Last Modified: Fri, 27 Feb 2026 23:12:14 GMT  
		Size: 5.2 MB (5156451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98a2a796dc2a311d7b102cc7b2ab553d70bda03812c05940d8446728bc1bd31`  
		Last Modified: Fri, 27 Feb 2026 23:12:13 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:fb32260cdc30e3f8c1bace70f4c95511ae587e328bca38662a954acca8373050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230449740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c127fdb52412e46e67c6fa908ca947cc0941332c2e2d69961b6f307eeef132`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 23:11:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 27 Feb 2026 23:12:10 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.1.tar.gz.asc crate-6.2.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.1.tar.gz.asc     && tar -xf crate-6.2.1.tar.gz -C /crate --strip-components=1     && rm crate-6.2.1.tar.gz # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 23:12:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 27 Feb 2026 23:12:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
VOLUME [/data]
# Fri, 27 Feb 2026 23:12:11 GMT
WORKDIR /data
# Fri, 27 Feb 2026 23:12:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 27 Feb 2026 23:12:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-02-03T11:14:19.799212 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.1
# Fri, 27 Feb 2026 23:12:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Feb 2026 23:12:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Feb 2026 23:12:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78282673ebf00c196545a69e0d1c5c2f4331da09c945a29296fe96ac47cf0634`  
		Last Modified: Fri, 27 Feb 2026 23:12:29 GMT  
		Size: 13.1 MB (13104609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86107e01bdcc66bacd5da83d3064732d6597da686ac936325fd0d7060be20535`  
		Last Modified: Fri, 27 Feb 2026 23:12:32 GMT  
		Size: 149.3 MB (149299644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e9f865b06b0e7de35d3d65b2fbdfff49b3e2fc4fd33a976a36eea88cc05887`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe0784cf2e95ef508e80ad7ee6e60600d0509350dea2f75643019945849f4a`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2109279352d3886755378fe52037e7e4362a7642ba940266b0eed254a287e50`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a73cfb9bbbbad1a0617fc3f6f3efee87ca503558e1d4b78ed84f029638b0c8`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45546e703f7ef3e6183e5456c9b6d43719e68bcc7b94b5cf72c83568f4a28`  
		Last Modified: Fri, 27 Feb 2026 23:12:30 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:6db5dfca2bab46772d9d45378b800ff0ed142ba66b03975c82c7084563af682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc936990baf0601b3701bd29262b03876cf77782161c24bfa20019ff76e4b38`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f7e911bf6c374cae51d5d6589e0b25a9035a4daa2328b34ef336f51eea254`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 5.2 MB (5154370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f0228d0a23156f5b58474a886076f9eb9bc38a8ce07deb1257a2ebaf49d364`  
		Last Modified: Fri, 27 Feb 2026 23:12:28 GMT  
		Size: 23.3 KB (23276 bytes)  
		MIME: application/vnd.in-toto+json
