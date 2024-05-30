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
$ docker pull crate@sha256:b3dc47a1b2da2d05dce7b22c9296053806f312f4ed4c8937fb40f227be74e6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:f73eb135374ed00d4cc65f33dbe3f7cb5b021560e977dbd91c1bfe38414b3c9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300510759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b332dc646ac6936844a803dd69cd19764d5c4a64bf11b5e80de9086ca9c5604e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:36:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:36:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:36:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:36:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:36:35 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:36:35 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:36:35 GMT
WORKDIR /data
# Thu, 30 May 2024 20:36:35 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:36:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:36:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:36:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:36:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:36:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edd129766265acb54d38946bc0b994f79c572d4f0b592351061b937c359bb5`  
		Last Modified: Thu, 30 May 2024 20:38:14 GMT  
		Size: 229.6 MB (229566559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da3d04b9eaa9aedc9ffc8c254465ccfca16900e3b7b24fc14b0b008a7f64d30`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d273ecb72b9928285b630e24b281b84294c4d6f5bbd0e83cccd4858af30c83`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c539fa440538b58f2f4e4e29f8b1cd9448aafa63c771efa1828eb404e1876ab`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db63bcc6b3a1f7ba2a4ed9f7dfd05139dd6dfeb2dda30860b21a32c9e13b6ce8`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a7ceabeef131e8ca7e5e6786c1c73edfd051d87edfc5019171de94cbaf6c8e`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:35031e812994186924463c9e959e2fbf806e507453d6e0ee36fd3f1a19a324f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297752208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5cae1c023b51573ef5d0e93d93208c3e0e83a6a0de1dec1f96f138eb10f8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:49:53 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:53 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:53 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:53 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:53 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:53 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:53 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:49:54 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf636b5c8162cd8fd6b069dac68f24b7d61292ac58898180f0077cf7f7fddb`  
		Last Modified: Thu, 30 May 2024 20:51:25 GMT  
		Size: 227.9 MB (227888420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ecc3ac145619784c69d92d47a988fc8f49e365e9e9e79a92ab337e87bbbb43`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 1.9 MB (1939612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081a3f2a8dfe4289368272ad96fa21a491e719600aead0c0c20867efc1fc938`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46329c8169bfa356ac1be46c6e376349c5f70f7203c85ba6ea5d76cf0177323`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85daad9bfee4be0793638b05eae7bd3ea6e2afb1a92118f81c48ef01b788de49`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe53944723f0059ac353184ef1c887e6c4175134d96b7b375ec64b17c6c012`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:b3dc47a1b2da2d05dce7b22c9296053806f312f4ed4c8937fb40f227be74e6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:f73eb135374ed00d4cc65f33dbe3f7cb5b021560e977dbd91c1bfe38414b3c9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300510759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b332dc646ac6936844a803dd69cd19764d5c4a64bf11b5e80de9086ca9c5604e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:36:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:36:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:36:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:36:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:36:35 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:36:35 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:36:35 GMT
WORKDIR /data
# Thu, 30 May 2024 20:36:35 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:36:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:36:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:36:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:36:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:36:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edd129766265acb54d38946bc0b994f79c572d4f0b592351061b937c359bb5`  
		Last Modified: Thu, 30 May 2024 20:38:14 GMT  
		Size: 229.6 MB (229566559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da3d04b9eaa9aedc9ffc8c254465ccfca16900e3b7b24fc14b0b008a7f64d30`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d273ecb72b9928285b630e24b281b84294c4d6f5bbd0e83cccd4858af30c83`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c539fa440538b58f2f4e4e29f8b1cd9448aafa63c771efa1828eb404e1876ab`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db63bcc6b3a1f7ba2a4ed9f7dfd05139dd6dfeb2dda30860b21a32c9e13b6ce8`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a7ceabeef131e8ca7e5e6786c1c73edfd051d87edfc5019171de94cbaf6c8e`  
		Last Modified: Thu, 30 May 2024 20:37:56 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:35031e812994186924463c9e959e2fbf806e507453d6e0ee36fd3f1a19a324f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297752208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d5cae1c023b51573ef5d0e93d93208c3e0e83a6a0de1dec1f96f138eb10f8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:49 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Thu, 30 May 2024 20:49:53 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:53 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:53 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:53 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:53 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:53 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:53 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:54 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Thu, 30 May 2024 20:49:54 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf636b5c8162cd8fd6b069dac68f24b7d61292ac58898180f0077cf7f7fddb`  
		Last Modified: Thu, 30 May 2024 20:51:25 GMT  
		Size: 227.9 MB (227888420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ecc3ac145619784c69d92d47a988fc8f49e365e9e9e79a92ab337e87bbbb43`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 1.9 MB (1939612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081a3f2a8dfe4289368272ad96fa21a491e719600aead0c0c20867efc1fc938`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46329c8169bfa356ac1be46c6e376349c5f70f7203c85ba6ea5d76cf0177323`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85daad9bfee4be0793638b05eae7bd3ea6e2afb1a92118f81c48ef01b788de49`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe53944723f0059ac353184ef1c887e6c4175134d96b7b375ec64b17c6c012`  
		Last Modified: Thu, 30 May 2024 20:51:10 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:93fc9d3f8a72ae5ac6dff994242cac6ae0d1018c2cf1286f481ed2a94bcb359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:c5e133b7611c03c3eec7c61ec767161a2a672f0433ae30df160b770ce1034fa7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187711644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533850e81cc913ee63b29eba1efd81b38996327fcbc1807f2aa8f942d7fb8b2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:36:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:36:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:36:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:36:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:36:03 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:36:03 GMT
WORKDIR /data
# Thu, 30 May 2024 20:36:03 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:36:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:36:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:36:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:36:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:36:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:36:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b30332f0ad7828d617b427d42fa116a3fd11de6859ef0906956b0898989a722`  
		Last Modified: Thu, 30 May 2024 20:37:43 GMT  
		Size: 116.8 MB (116767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773045a0e3d3a98d9592caa350f24112b5422b34f95eb014c6b71574c20f5aa`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f7651abfbd7320e00bbad3aa197ed57ad93a18586cd95c62dba7582c50f249`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c03f00c23ae1d6a8313d743357c4f36ac2e0adffb6f0780779e17a9604b2d`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4400f79c578f5c7f452f48881d31f8fd87e132f5eefe2a1e7fab8d6ea21b5525`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401cfa6019d135477f0e91ed7760a55f50926f8aa60ce81fe688f8bde1dbcd11`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.4`

```console
$ docker pull crate@sha256:93fc9d3f8a72ae5ac6dff994242cac6ae0d1018c2cf1286f481ed2a94bcb359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:c5e133b7611c03c3eec7c61ec767161a2a672f0433ae30df160b770ce1034fa7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187711644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533850e81cc913ee63b29eba1efd81b38996327fcbc1807f2aa8f942d7fb8b2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:36:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:36:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:36:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:36:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:36:03 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:36:03 GMT
WORKDIR /data
# Thu, 30 May 2024 20:36:03 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:36:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:36:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:36:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:36:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:36:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:36:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b30332f0ad7828d617b427d42fa116a3fd11de6859ef0906956b0898989a722`  
		Last Modified: Thu, 30 May 2024 20:37:43 GMT  
		Size: 116.8 MB (116767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773045a0e3d3a98d9592caa350f24112b5422b34f95eb014c6b71574c20f5aa`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f7651abfbd7320e00bbad3aa197ed57ad93a18586cd95c62dba7582c50f249`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c03f00c23ae1d6a8313d743357c4f36ac2e0adffb6f0780779e17a9604b2d`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4400f79c578f5c7f452f48881d31f8fd87e132f5eefe2a1e7fab8d6ea21b5525`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401cfa6019d135477f0e91ed7760a55f50926f8aa60ce81fe688f8bde1dbcd11`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:93fc9d3f8a72ae5ac6dff994242cac6ae0d1018c2cf1286f481ed2a94bcb359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:c5e133b7611c03c3eec7c61ec767161a2a672f0433ae30df160b770ce1034fa7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187711644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533850e81cc913ee63b29eba1efd81b38996327fcbc1807f2aa8f942d7fb8b2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:36:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:36:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:36:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:36:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:36:03 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:36:03 GMT
WORKDIR /data
# Thu, 30 May 2024 20:36:03 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:36:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:36:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:36:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:36:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:36:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:36:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b30332f0ad7828d617b427d42fa116a3fd11de6859ef0906956b0898989a722`  
		Last Modified: Thu, 30 May 2024 20:37:43 GMT  
		Size: 116.8 MB (116767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773045a0e3d3a98d9592caa350f24112b5422b34f95eb014c6b71574c20f5aa`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f7651abfbd7320e00bbad3aa197ed57ad93a18586cd95c62dba7582c50f249`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c03f00c23ae1d6a8313d743357c4f36ac2e0adffb6f0780779e17a9604b2d`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4400f79c578f5c7f452f48881d31f8fd87e132f5eefe2a1e7fab8d6ea21b5525`  
		Last Modified: Thu, 30 May 2024 20:37:33 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401cfa6019d135477f0e91ed7760a55f50926f8aa60ce81fe688f8bde1dbcd11`  
		Last Modified: Thu, 30 May 2024 20:37:32 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:73fa42825f76aaf8131b370c7d344a0d7b7e5515a78fcb3fbe4b3b5b91da19e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186166012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f59c9be22fe396155468c21be5ef09648a2829b1b5722e370713cb866b75dc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Thu, 30 May 2024 20:49:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:22 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:23 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:23 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:23 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:23 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Thu, 30 May 2024 20:49:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cde1420cf9ea258023b25797a18cfe559a9edff8f7b867f8bfd98913c17d`  
		Last Modified: Thu, 30 May 2024 20:50:59 GMT  
		Size: 116.3 MB (116302222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8692789ff6ff8a20becd2b6364ab283cc60ce288ffaf10a8e2e342a04a63ff72`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32543754a48f04fd03754f61c59a44e98d3b97b397ff9fdbcaaa4d527503bfb4`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88b9cc8441148e61b76413393848ee0eef3ab1c64a5ee1889793c0b8679de`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178ec6dd3fb2e28e551a618c9d0d3821de2d8ab060b7a5a7fcd7a6097ba307be`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e92324bc936bef7f2b7067233e9da31665ce891477211d956e8f14ebc41b47`  
		Last Modified: Thu, 30 May 2024 20:50:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:6acf34134148cdb5cb01615516ec6cab72b8ecafd3eeb615fef030a06dc5a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:087663c7bb8d1db286a7d02967e0dc77446e7120b51f138603099e9fe38c046b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188862235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528ba3407ed5f8f6916bc193c79cac692a570c380d3cb28a6a2b7035910d927`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:35:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:36 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:37 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:37 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:37 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:35:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5286e3a5fc8c3b043a9e3955aacd6a52af6cd029cf440f1674a80d3a50ee2e`  
		Last Modified: Thu, 30 May 2024 20:37:23 GMT  
		Size: 117.9 MB (117916994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a7935bd223a6b01c413aad38ab7dcdce31a5238a5a70dc6402fa82d9abda0a`  
		Last Modified: Thu, 30 May 2024 20:37:13 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70957b1e857f250ba1c68c6ae7d9598a7d7d7ba0057bd4ef3c5da3dec90ac1a`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c14b357b8c3e46c9d78418b90661e38032aa0bdf410aeec189260876d9f9f1`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a414ae4a6cc5a461a2dd6e668262f87114c712a65995bdf3280ed6e7ee62824`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb341d943ae3c5a90f0d8b632f0d6f854be20ad90f6f83c820d623f745631465`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6a27f74dfc318043ccf8b02390511a884f6a6902f6bb84b3ae0d4db06b5a17e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187291851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059addbbe35ba3a6d4573c5b45c22262a5d1dc40acbac0720e04fa1a76c4a021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:01 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:49:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:04 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:04 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:04 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:04 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:49:05 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c499c532cbb6ff39a98b87d56d1d02b62c24b51a4be7d41440f680706a378f`  
		Last Modified: Thu, 30 May 2024 20:50:41 GMT  
		Size: 117.4 MB (117427024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666298ed1cdec8c65865b36765d1c5972876c94f9c09b84955d3ee0413c0ea3e`  
		Last Modified: Thu, 30 May 2024 20:50:32 GMT  
		Size: 1.9 MB (1940644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e2649e57debc1e956c9b4ac0dc744e19f2ae8844ac94f4d87221f7b4924d5`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2e644ce4d5a8be47aac40902d62b049fde4b4de32d153a24d29f5b97da75f4`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2c11b626940e12fee215ef74940a4545917633e8c7ed40ee5352afba8dc69a`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b0bc1cab79db268163c990f48396f90222d15cf81c5f2ad84a59bd2d17dc49`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.5`

```console
$ docker pull crate@sha256:6acf34134148cdb5cb01615516ec6cab72b8ecafd3eeb615fef030a06dc5a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:087663c7bb8d1db286a7d02967e0dc77446e7120b51f138603099e9fe38c046b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188862235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528ba3407ed5f8f6916bc193c79cac692a570c380d3cb28a6a2b7035910d927`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:35:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:36 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:37 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:37 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:37 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:35:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:38 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5286e3a5fc8c3b043a9e3955aacd6a52af6cd029cf440f1674a80d3a50ee2e`  
		Last Modified: Thu, 30 May 2024 20:37:23 GMT  
		Size: 117.9 MB (117916994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a7935bd223a6b01c413aad38ab7dcdce31a5238a5a70dc6402fa82d9abda0a`  
		Last Modified: Thu, 30 May 2024 20:37:13 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70957b1e857f250ba1c68c6ae7d9598a7d7d7ba0057bd4ef3c5da3dec90ac1a`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c14b357b8c3e46c9d78418b90661e38032aa0bdf410aeec189260876d9f9f1`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a414ae4a6cc5a461a2dd6e668262f87114c712a65995bdf3280ed6e7ee62824`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb341d943ae3c5a90f0d8b632f0d6f854be20ad90f6f83c820d623f745631465`  
		Last Modified: Thu, 30 May 2024 20:37:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6a27f74dfc318043ccf8b02390511a884f6a6902f6bb84b3ae0d4db06b5a17e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187291851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059addbbe35ba3a6d4573c5b45c22262a5d1dc40acbac0720e04fa1a76c4a021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:49:01 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Thu, 30 May 2024 20:49:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:49:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:49:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:49:04 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:49:04 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:49:04 GMT
WORKDIR /data
# Thu, 30 May 2024 20:49:04 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:49:05 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:49:05 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Thu, 30 May 2024 20:49:05 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:49:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:49:05 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c499c532cbb6ff39a98b87d56d1d02b62c24b51a4be7d41440f680706a378f`  
		Last Modified: Thu, 30 May 2024 20:50:41 GMT  
		Size: 117.4 MB (117427024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666298ed1cdec8c65865b36765d1c5972876c94f9c09b84955d3ee0413c0ea3e`  
		Last Modified: Thu, 30 May 2024 20:50:32 GMT  
		Size: 1.9 MB (1940644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e2649e57debc1e956c9b4ac0dc744e19f2ae8844ac94f4d87221f7b4924d5`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2e644ce4d5a8be47aac40902d62b049fde4b4de32d153a24d29f5b97da75f4`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2c11b626940e12fee215ef74940a4545917633e8c7ed40ee5352afba8dc69a`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b0bc1cab79db268163c990f48396f90222d15cf81c5f2ad84a59bd2d17dc49`  
		Last Modified: Thu, 30 May 2024 20:50:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7`

```console
$ docker pull crate@sha256:6c773239683d52aa6afdabc46d6d3587a99d6ca2866fbe0dfa1f1d57d3a669a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:f102522a7c1cbcde795e87fb4ce5ace234f9d522ca2301fd227990d02bca5d69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198583951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd2d72e8b1af3e7c607ef1a3edd6bc03bc9f6ed1bbadb7d9f2b80e8d7b70afd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:35:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:12 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:12 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:12 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:12 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:35:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:13 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777b9d136d07781af2e1c328496e3d744cd628712063953f1b537cf616fd0b5`  
		Last Modified: Thu, 30 May 2024 20:37:02 GMT  
		Size: 127.6 MB (127638719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebe7fb06631d4e6e173b631e8392cc91f21245e8e5c730da93a295b7aa25026`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 1.9 MB (1940648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be2b39b73ddc110624aee6c44c9907e8deca77e12af50d0e70d57b21a10dda`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac73a3d073b3944966e33f7502c769aeafad521d66f762c46340cfa2a6f95ed`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b296e5312310c9c03e6481c9775945ae48bbb5239c03eba8ffc6284e4ed5bac1`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa16674af1872afd51b63ac0cf3c3cde2cd3e3452f22e8e30b1948c4b17659a`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:baa09b3f8e9907d4a46b2efca21385f1fad66285acfa4c72cd647ab1f5da84fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197015007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121024ee810b16ad5641246032d1bbc089f915f6a4c0af24b7dfd53766c97254`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:48:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:48:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:48:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:48:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:48:42 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:48:42 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:48:42 GMT
WORKDIR /data
# Thu, 30 May 2024 20:48:42 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:48:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:48:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:48:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:48:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1cc4c6bf1087c8c8d1cfbeb622742b1a8c0d642772684a4e43f4868064a23`  
		Last Modified: Thu, 30 May 2024 20:50:20 GMT  
		Size: 127.2 MB (127150172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddb0706b704f087d004f781f3edc3b28ee0366060bb6a60bb3e25bd4e3a945`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddd8cac97fe9d05b6fd59dc7e2a91ec99ae6fb1b0f3bc55e6fe5aeee71f129a`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75345bad7e502e81e171377de774903d7a0f4c02c59339eec0cc01cd25ba4106`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6e807eecfa87edaf6d9dab165764072012366d77cdd18b92d63b31a58addc`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b28701486bbe025e0c77aefc4dc9f06feba8cf4d884c5ac5bafbdec472daa`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7.1`

```console
$ docker pull crate@sha256:6c773239683d52aa6afdabc46d6d3587a99d6ca2866fbe0dfa1f1d57d3a669a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.7.1` - linux; amd64

```console
$ docker pull crate@sha256:f102522a7c1cbcde795e87fb4ce5ace234f9d522ca2301fd227990d02bca5d69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198583951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd2d72e8b1af3e7c607ef1a3edd6bc03bc9f6ed1bbadb7d9f2b80e8d7b70afd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:35:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:12 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:12 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:12 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:12 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:35:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:13 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777b9d136d07781af2e1c328496e3d744cd628712063953f1b537cf616fd0b5`  
		Last Modified: Thu, 30 May 2024 20:37:02 GMT  
		Size: 127.6 MB (127638719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebe7fb06631d4e6e173b631e8392cc91f21245e8e5c730da93a295b7aa25026`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 1.9 MB (1940648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be2b39b73ddc110624aee6c44c9907e8deca77e12af50d0e70d57b21a10dda`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac73a3d073b3944966e33f7502c769aeafad521d66f762c46340cfa2a6f95ed`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b296e5312310c9c03e6481c9775945ae48bbb5239c03eba8ffc6284e4ed5bac1`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa16674af1872afd51b63ac0cf3c3cde2cd3e3452f22e8e30b1948c4b17659a`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.7.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:baa09b3f8e9907d4a46b2efca21385f1fad66285acfa4c72cd647ab1f5da84fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197015007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121024ee810b16ad5641246032d1bbc089f915f6a4c0af24b7dfd53766c97254`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:48:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:48:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:48:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:48:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:48:42 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:48:42 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:48:42 GMT
WORKDIR /data
# Thu, 30 May 2024 20:48:42 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:48:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:48:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:48:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:48:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1cc4c6bf1087c8c8d1cfbeb622742b1a8c0d642772684a4e43f4868064a23`  
		Last Modified: Thu, 30 May 2024 20:50:20 GMT  
		Size: 127.2 MB (127150172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddb0706b704f087d004f781f3edc3b28ee0366060bb6a60bb3e25bd4e3a945`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddd8cac97fe9d05b6fd59dc7e2a91ec99ae6fb1b0f3bc55e6fe5aeee71f129a`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75345bad7e502e81e171377de774903d7a0f4c02c59339eec0cc01cd25ba4106`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6e807eecfa87edaf6d9dab165764072012366d77cdd18b92d63b31a58addc`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b28701486bbe025e0c77aefc4dc9f06feba8cf4d884c5ac5bafbdec472daa`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:6c773239683d52aa6afdabc46d6d3587a99d6ca2866fbe0dfa1f1d57d3a669a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f102522a7c1cbcde795e87fb4ce5ace234f9d522ca2301fd227990d02bca5d69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198583951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd2d72e8b1af3e7c607ef1a3edd6bc03bc9f6ed1bbadb7d9f2b80e8d7b70afd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:35:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:12 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:12 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:12 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:12 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:35:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:13 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777b9d136d07781af2e1c328496e3d744cd628712063953f1b537cf616fd0b5`  
		Last Modified: Thu, 30 May 2024 20:37:02 GMT  
		Size: 127.6 MB (127638719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebe7fb06631d4e6e173b631e8392cc91f21245e8e5c730da93a295b7aa25026`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 1.9 MB (1940648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be2b39b73ddc110624aee6c44c9907e8deca77e12af50d0e70d57b21a10dda`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac73a3d073b3944966e33f7502c769aeafad521d66f762c46340cfa2a6f95ed`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b296e5312310c9c03e6481c9775945ae48bbb5239c03eba8ffc6284e4ed5bac1`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa16674af1872afd51b63ac0cf3c3cde2cd3e3452f22e8e30b1948c4b17659a`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:baa09b3f8e9907d4a46b2efca21385f1fad66285acfa4c72cd647ab1f5da84fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197015007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121024ee810b16ad5641246032d1bbc089f915f6a4c0af24b7dfd53766c97254`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:48:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:48:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:48:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:48:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:48:42 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:48:42 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:48:42 GMT
WORKDIR /data
# Thu, 30 May 2024 20:48:42 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:48:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:48:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:48:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:48:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1cc4c6bf1087c8c8d1cfbeb622742b1a8c0d642772684a4e43f4868064a23`  
		Last Modified: Thu, 30 May 2024 20:50:20 GMT  
		Size: 127.2 MB (127150172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddb0706b704f087d004f781f3edc3b28ee0366060bb6a60bb3e25bd4e3a945`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddd8cac97fe9d05b6fd59dc7e2a91ec99ae6fb1b0f3bc55e6fe5aeee71f129a`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75345bad7e502e81e171377de774903d7a0f4c02c59339eec0cc01cd25ba4106`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6e807eecfa87edaf6d9dab165764072012366d77cdd18b92d63b31a58addc`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b28701486bbe025e0c77aefc4dc9f06feba8cf4d884c5ac5bafbdec472daa`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
