## `crate:latest`

```console
$ docker pull crate@sha256:4a64b31b6840341aa39399b88741ae925c341582f11ecd73eacc33cddc87ef2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:226c51f49ecc6a69b77a453192966374b1ef555540753377963bfbe33e6ee628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242388761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d93cf3c690755ef1c2dbc4d500930dde85368f706f2a3b84ac2fbc22495bf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 09:51:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.6.tar.gz.asc crate-5.9.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.6.tar.gz.asc     && tar -xf crate-5.9.6.tar.gz -C /crate --strip-components=1     && rm crate-5.9.6.tar.gz # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jan 2025 09:51:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 09 Jan 2025 09:51:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
VOLUME [/data]
# Thu, 09 Jan 2025 09:51:54 GMT
WORKDIR /data
# Thu, 09 Jan 2025 09:51:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-09T09:51:54.945195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.6
# Thu, 09 Jan 2025 09:51:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 09 Jan 2025 09:51:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Jan 2025 09:51:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Fri, 13 Dec 2024 15:55:44 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3dd3c1b43a094a57c82f7c759e85dfd0f0d11c22757bf9d66f39b8e6473324`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 14.1 MB (14148844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482f67ddb8a7b3d7a84e40719de1c9e941390bd028ff957fdddbc23451f3bb20`  
		Last Modified: Tue, 14 Jan 2025 21:38:39 GMT  
		Size: 147.2 MB (147215424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3fc86289e6e8ebb83dfd994802ca96d5e3d914683cb5911159985438ae6da`  
		Last Modified: Tue, 14 Jan 2025 21:38:54 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cdbfc93a57c32d59db0a675ba6d988a3f50b7018b56323528567fdd0dd95e`  
		Last Modified: Tue, 14 Jan 2025 21:38:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04ce584b69bb42ca4276462807c5e3ed21605e7393a8c572474c440bcc792a`  
		Last Modified: Tue, 14 Jan 2025 21:38:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e295e350f57f4e6b0bb10f153233b44e5ca75c3e4469f88f5fbeb2fc7e9d2`  
		Last Modified: Tue, 14 Jan 2025 19:28:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74c1dfcca3b21a5e74e91a095b205f966a45c6ca09954e11e301451fc1a8bd0`  
		Last Modified: Tue, 14 Jan 2025 21:38:55 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:79eb120af451887579bf6515acc29cf2ec35881d82f5afc41db98410df827d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9600d8173123bbbbca9b93d2801f835653fb2e7c82af77edb202ab21df0439`

```dockerfile
```

-	Layers:
	-	`sha256:7534b7fd988c1da09755b678a4fcbbc4f69641cff79dceccac1576090e37ad39`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 6.3 MB (6316984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947cef4af6a5e3e0836cce96333e75a58c26087374980cba36905aa26fb5758a`  
		Last Modified: Tue, 14 Jan 2025 19:28:20 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:631edf26dbc222e38eadea02a51fd7f45637812c5da2b03f3989a50c5a0b8553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2e63d1c9955a1f63d0a5e77654904553ee260bfd92dec147b9e0931b9f3cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Tue, 10 Dec 2024 16:21:56 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.5.tar.gz.asc crate-5.9.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.5.tar.gz.asc     && tar -xf crate-5.9.5.tar.gz -C /crate --strip-components=1     && rm crate-5.9.5.tar.gz # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Dec 2024 16:21:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 10 Dec 2024 16:21:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
VOLUME [/data]
# Tue, 10 Dec 2024 16:21:56 GMT
WORKDIR /data
# Tue, 10 Dec 2024 16:21:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-12-10T16:21:56.023234 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.5
# Tue, 10 Dec 2024 16:21:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Dec 2024 16:21:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Dec 2024 16:21:56 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eeccda12ed247fc86af9756eed85b9493924d0e5654243889a076103dba020`  
		Last Modified: Sat, 14 Dec 2024 18:11:31 GMT  
		Size: 13.5 MB (13537879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1e6977d7c6274d2809b4c27d1e41a2b9519f487a53b741263dd04bca7dac8b`  
		Last Modified: Sat, 14 Dec 2024 18:11:38 GMT  
		Size: 148.4 MB (148375948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298f0d0860c7d87c45abc13dd98458d6f6aaaffc41f61973f23de9e7da30493`  
		Last Modified: Fri, 13 Dec 2024 20:28:13 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5390f2f5edde014145aa39036356876d9045e93796c8af41f4de3f71dfd9f`  
		Last Modified: Fri, 13 Dec 2024 20:28:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fdf3527e264dc2003068e61b266a4b9ee395d3d153a57a7058014ac80ddbd6`  
		Last Modified: Fri, 13 Dec 2024 20:28:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf88d03d210975a6da59c0047af95728c1f90f1608754b2a2d81fee08f48f104`  
		Last Modified: Fri, 13 Dec 2024 20:28:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ae2da509d2a624303fe3b492d1fc6f1f49114065d73181123b41c3f3a6c9ff`  
		Last Modified: Mon, 16 Dec 2024 12:05:00 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:51c6206ce4d37e8fa7f927139e42061f862ec183a8590194a033e7f08dc5697a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9291f3cb2fa49d1ee7ba0bcea78940880bfafcb9cd823e7f0656f5df7eb99cb3`

```dockerfile
```

-	Layers:
	-	`sha256:9a37744ec313b2f7e8f033eaa064ba70ae9340eac85a59af74ac84ed1bb4598a`  
		Last Modified: Mon, 16 Dec 2024 19:09:09 GMT  
		Size: 6.3 MB (6327739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a505c2a4fac5bac8830a37aedf1b0540c2fa6604c6499f774f7bdfabe7910dfb`  
		Last Modified: Fri, 13 Dec 2024 20:28:13 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json
