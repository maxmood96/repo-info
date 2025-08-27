<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.11`](#crate51011)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:67bc203cbe8807ff37fb7433080462d6d0978d7fd7c3a34afe7dee465bc58c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:95958f45c69310d050d19809b23193f6c35d21247fcdca3d569eb65faf365c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dff6807121cff1144eb2f77068bbec45f729b9cf9e2a84803f068b626839d7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8cf720232028b764dea94e13423657e5bd528d4122f5e40debee5779f9e45e83`  
		Last Modified: Wed, 27 Aug 2025 16:55:53 GMT  
		Size: 67.0 MB (67041415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b203a03fca50ddc2cb82b731236232f25e95938f7d0621c2d17bb16c3db41c96`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 14.6 MB (14574579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cfca241620ff4b6f46a49c5c23710f1558e324f9b00639e5cdb45485bceaa2`  
		Last Modified: Wed, 27 Aug 2025 17:37:12 GMT  
		Size: 149.7 MB (149668906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0072fcf63fbb7fa674e54180b1c8d98f8f45ec5ac731949e80940ee59caf9`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb5f950bffd24fe4425fcf51e4681ab7e6233420dd2efef5cf06603c8ec18f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7157b7c13867781f16e5163ccafefbc5b20b0229fb50af87455381933765468`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b470985774ed2afdb2e4a3a5c7413f595e53322aa7d9ec9c637a737e06d7c5`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fd85fc8cd7f5a498587a5b5364b9f8dbea065eb6518444e58b6e482ba502f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:ecbb52e76db9f2873030250c9e5a9bf2b45fd23e3d0fa41d76645362baa4a2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25425d9de66f7b17849680ab2e1cd590d776def3fc46ef10c50a3fa89782650`

```dockerfile
```

-	Layers:
	-	`sha256:87480ccea139f22a8b4d859c156523e2c68c7d902c31fe3a0e815431036c3eee`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 5.2 MB (5185728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa2c2a6f4ecf23e0431a26d4fe319c792628d5b42fab0ff35c58bbf38e57b77`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:50849bafe7174643d746beb07e5a33ce2470e2a48e3dd38c2358892b38e08681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232457624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a1525a4802bccd10ea26d4dcc8e54f42edcac24e8abc29a29115dbc715cfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3784e0c144ba9ce263ec17b39e5222cc8c2846ef547a5160e2e9019ee96cba4`  
		Last Modified: Wed, 27 Aug 2025 17:28:53 GMT  
		Size: 65.5 MB (65534994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41c8e1f468fe2d079821e096a6636d695f37e969c3d41c54eeafc8bed260c03`  
		Last Modified: Wed, 27 Aug 2025 17:36:02 GMT  
		Size: 14.6 MB (14631636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cf830059522640e54bf2436dd06a50ae46bb2fa35169649d965d3a7625979c`  
		Last Modified: Wed, 27 Aug 2025 17:36:21 GMT  
		Size: 150.3 MB (150345491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab781920c3f9fd5195a6132bbe9c1b54418a2e33ff36b74a9d480ea7703ac5c0`  
		Last Modified: Wed, 27 Aug 2025 17:36:23 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35284442bd079f67990210eea0b3586dca838a412707c6c1a02afcf629dbb021`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5a7677f0a91fa0ed880ea2353a825d5f2e18e4cb1234b2203b99e94797e73`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623a620071f48f17cf2f5deabf35784eda9045845ec99f89d25d6fdb9d8b92c4`  
		Last Modified: Wed, 27 Aug 2025 17:36:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43dc92a26926b2583acf7360f8a5f954d74549b59c6134a0cc11a6e8a3c7ff3`  
		Last Modified: Wed, 27 Aug 2025 17:36:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:37193e8f94f182ad80e9cf8056dd2a2150c89a6ff5b3ce24ae8b3ca69b6bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25d7c85614280feb484d3d3a21e1b5954172433e416b622d6ae7baf06cd40d3`

```dockerfile
```

-	Layers:
	-	`sha256:dc57dfff1f7043a7d090ec6835da4d1874ea69557e667e442046e902fc1db332`  
		Last Modified: Wed, 27 Aug 2025 17:38:31 GMT  
		Size: 5.2 MB (5183036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b260e035835951806c10b833386583289136bc7107c52d4592791c2c420685`  
		Last Modified: Wed, 27 Aug 2025 17:38:32 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.11`

```console
$ docker pull crate@sha256:67bc203cbe8807ff37fb7433080462d6d0978d7fd7c3a34afe7dee465bc58c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.11` - linux; amd64

```console
$ docker pull crate@sha256:95958f45c69310d050d19809b23193f6c35d21247fcdca3d569eb65faf365c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dff6807121cff1144eb2f77068bbec45f729b9cf9e2a84803f068b626839d7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8cf720232028b764dea94e13423657e5bd528d4122f5e40debee5779f9e45e83`  
		Last Modified: Wed, 27 Aug 2025 16:55:53 GMT  
		Size: 67.0 MB (67041415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b203a03fca50ddc2cb82b731236232f25e95938f7d0621c2d17bb16c3db41c96`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 14.6 MB (14574579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cfca241620ff4b6f46a49c5c23710f1558e324f9b00639e5cdb45485bceaa2`  
		Last Modified: Wed, 27 Aug 2025 17:37:12 GMT  
		Size: 149.7 MB (149668906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0072fcf63fbb7fa674e54180b1c8d98f8f45ec5ac731949e80940ee59caf9`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb5f950bffd24fe4425fcf51e4681ab7e6233420dd2efef5cf06603c8ec18f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7157b7c13867781f16e5163ccafefbc5b20b0229fb50af87455381933765468`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b470985774ed2afdb2e4a3a5c7413f595e53322aa7d9ec9c637a737e06d7c5`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fd85fc8cd7f5a498587a5b5364b9f8dbea065eb6518444e58b6e482ba502f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:ecbb52e76db9f2873030250c9e5a9bf2b45fd23e3d0fa41d76645362baa4a2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25425d9de66f7b17849680ab2e1cd590d776def3fc46ef10c50a3fa89782650`

```dockerfile
```

-	Layers:
	-	`sha256:87480ccea139f22a8b4d859c156523e2c68c7d902c31fe3a0e815431036c3eee`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 5.2 MB (5185728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa2c2a6f4ecf23e0431a26d4fe319c792628d5b42fab0ff35c58bbf38e57b77`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.11` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:50849bafe7174643d746beb07e5a33ce2470e2a48e3dd38c2358892b38e08681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232457624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a1525a4802bccd10ea26d4dcc8e54f42edcac24e8abc29a29115dbc715cfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3784e0c144ba9ce263ec17b39e5222cc8c2846ef547a5160e2e9019ee96cba4`  
		Last Modified: Wed, 27 Aug 2025 17:28:53 GMT  
		Size: 65.5 MB (65534994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41c8e1f468fe2d079821e096a6636d695f37e969c3d41c54eeafc8bed260c03`  
		Last Modified: Wed, 27 Aug 2025 17:36:02 GMT  
		Size: 14.6 MB (14631636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cf830059522640e54bf2436dd06a50ae46bb2fa35169649d965d3a7625979c`  
		Last Modified: Wed, 27 Aug 2025 17:36:21 GMT  
		Size: 150.3 MB (150345491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab781920c3f9fd5195a6132bbe9c1b54418a2e33ff36b74a9d480ea7703ac5c0`  
		Last Modified: Wed, 27 Aug 2025 17:36:23 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35284442bd079f67990210eea0b3586dca838a412707c6c1a02afcf629dbb021`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5a7677f0a91fa0ed880ea2353a825d5f2e18e4cb1234b2203b99e94797e73`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623a620071f48f17cf2f5deabf35784eda9045845ec99f89d25d6fdb9d8b92c4`  
		Last Modified: Wed, 27 Aug 2025 17:36:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43dc92a26926b2583acf7360f8a5f954d74549b59c6134a0cc11a6e8a3c7ff3`  
		Last Modified: Wed, 27 Aug 2025 17:36:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:37193e8f94f182ad80e9cf8056dd2a2150c89a6ff5b3ce24ae8b3ca69b6bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25d7c85614280feb484d3d3a21e1b5954172433e416b622d6ae7baf06cd40d3`

```dockerfile
```

-	Layers:
	-	`sha256:dc57dfff1f7043a7d090ec6835da4d1874ea69557e667e442046e902fc1db332`  
		Last Modified: Wed, 27 Aug 2025 17:38:31 GMT  
		Size: 5.2 MB (5183036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b260e035835951806c10b833386583289136bc7107c52d4592791c2c420685`  
		Last Modified: Wed, 27 Aug 2025 17:38:32 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:e6a9632eff66618747183fabbe7d49ebe534264ec6ffd2dd2f85b2f529251f6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:f67ff45527b2733c5e40a5dbfb439194da5b1bedc9a6b843d8a06548f1dc8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232571255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9bf9e988a9fbb73ef51a48e57c313beb1fc65f7d9b272485c789b9b2eef9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8cf720232028b764dea94e13423657e5bd528d4122f5e40debee5779f9e45e83`  
		Last Modified: Wed, 27 Aug 2025 16:55:53 GMT  
		Size: 67.0 MB (67041415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73470e27fca28215e06bf3ddaad3002a69adb921a118b475b220263bfa6dae`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 14.6 MB (14574651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef44efdffe4c215221e2f6a2d6982c4ddeaa0b1138c306aa990cf0b2274784c8`  
		Last Modified: Wed, 27 Aug 2025 21:39:28 GMT  
		Size: 149.0 MB (149009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d24423b866cf7039c6ce23f69cb4d5cf4b05c3e3128d4021d6596ddccb138ab`  
		Last Modified: Wed, 27 Aug 2025 17:00:13 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8b9d235aaebe04aad3bd16b6e3f61eed1c29745b4501ea659eab30febe11a9`  
		Last Modified: Wed, 27 Aug 2025 17:00:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdce120692f36e2354d5b7963e28b2d79ee41ac93697871ea9635dab813e42b`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467c2ce5dd4da3ccf4c1766bedf0867f7de7a5e7bf5a2b596c19b9b9ba9a7ad`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d393f283beb290aeb3579dab1972e4f645a9d47f1000ae1a22f10952f514110d`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:dd939d20653864df8a5873f10e3f01e8475b7908dd718dbaf76665276bc2cfcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015f223ec7ae83a680610bb76f5818276f35e72a85fbdefa0fb7acde900116e3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb08855423150dbbb26787fe62a2cf2121585f86610f3c2050f705112f8ee62`  
		Last Modified: Wed, 27 Aug 2025 17:38:33 GMT  
		Size: 5.2 MB (5183793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f361e6813abc995b015b92d6761cfffc0c030b4777cad5381db7500856521b24`  
		Last Modified: Wed, 27 Aug 2025 17:38:34 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c60f1b07389aee1c5f274fe426aaaa35e8f47f6cbd98a2b357d030aaba9ab047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231820637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f2dbf6b01403191675136699d347b8e6dd126dfb3776a34d7d7cc91b187d6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3784e0c144ba9ce263ec17b39e5222cc8c2846ef547a5160e2e9019ee96cba4`  
		Last Modified: Wed, 27 Aug 2025 17:28:53 GMT  
		Size: 65.5 MB (65534994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41c8e1f468fe2d079821e096a6636d695f37e969c3d41c54eeafc8bed260c03`  
		Last Modified: Wed, 27 Aug 2025 17:36:02 GMT  
		Size: 14.6 MB (14631636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4dfef53897f955b52c308584474d225262e23927209519283f9616ffb3c437`  
		Last Modified: Wed, 27 Aug 2025 21:40:09 GMT  
		Size: 149.7 MB (149708497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a54ea7018cfe7c81c5d150781e4ef7473cd8c22299a0dba3aa4e57f2520c319`  
		Last Modified: Wed, 27 Aug 2025 17:06:01 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dc50f4ceb96f2603f0fccdda694a6516af43d8289ffef87d7fc64197a4f85`  
		Last Modified: Wed, 27 Aug 2025 17:06:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945643a367d188559124ba8441d853d30f5dfdc3bea2aa24d9b133287366a683`  
		Last Modified: Wed, 27 Aug 2025 17:06:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bb1abec9a7bf215c2c1465a936c53af59e7b0414f2b0d091b67870edbb0cc`  
		Last Modified: Wed, 27 Aug 2025 17:06:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7449eea5322cabd3f5ed3de06fbcab52e683c76f81cb1ddd339439a66f534f6`  
		Last Modified: Wed, 27 Aug 2025 17:06:15 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:fa6b21c827b0adacd2e03daaf41e961a84f34651b940cfda6f6bd2e1627f623d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c3bb8849162c8611796cd152846cae08ab939201ae9305756375aed0d5ca95`

```dockerfile
```

-	Layers:
	-	`sha256:4104c7c6727e71a511d523a83e456e5ae783b58c1942e29655cd27d39ea11498`  
		Last Modified: Wed, 27 Aug 2025 17:38:39 GMT  
		Size: 5.2 MB (5181089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1a4c40cb77d8f2e951e51c943b106970fa081f19e699d6096bc0b833fca5e7`  
		Last Modified: Wed, 27 Aug 2025 17:38:39 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:e6a9632eff66618747183fabbe7d49ebe534264ec6ffd2dd2f85b2f529251f6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:f67ff45527b2733c5e40a5dbfb439194da5b1bedc9a6b843d8a06548f1dc8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232571255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9bf9e988a9fbb73ef51a48e57c313beb1fc65f7d9b272485c789b9b2eef9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8cf720232028b764dea94e13423657e5bd528d4122f5e40debee5779f9e45e83`  
		Last Modified: Wed, 27 Aug 2025 16:55:53 GMT  
		Size: 67.0 MB (67041415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73470e27fca28215e06bf3ddaad3002a69adb921a118b475b220263bfa6dae`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 14.6 MB (14574651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef44efdffe4c215221e2f6a2d6982c4ddeaa0b1138c306aa990cf0b2274784c8`  
		Last Modified: Wed, 27 Aug 2025 21:39:28 GMT  
		Size: 149.0 MB (149009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d24423b866cf7039c6ce23f69cb4d5cf4b05c3e3128d4021d6596ddccb138ab`  
		Last Modified: Wed, 27 Aug 2025 17:00:13 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8b9d235aaebe04aad3bd16b6e3f61eed1c29745b4501ea659eab30febe11a9`  
		Last Modified: Wed, 27 Aug 2025 17:00:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdce120692f36e2354d5b7963e28b2d79ee41ac93697871ea9635dab813e42b`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467c2ce5dd4da3ccf4c1766bedf0867f7de7a5e7bf5a2b596c19b9b9ba9a7ad`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d393f283beb290aeb3579dab1972e4f645a9d47f1000ae1a22f10952f514110d`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:dd939d20653864df8a5873f10e3f01e8475b7908dd718dbaf76665276bc2cfcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015f223ec7ae83a680610bb76f5818276f35e72a85fbdefa0fb7acde900116e3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb08855423150dbbb26787fe62a2cf2121585f86610f3c2050f705112f8ee62`  
		Last Modified: Wed, 27 Aug 2025 17:38:33 GMT  
		Size: 5.2 MB (5183793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f361e6813abc995b015b92d6761cfffc0c030b4777cad5381db7500856521b24`  
		Last Modified: Wed, 27 Aug 2025 17:38:34 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c60f1b07389aee1c5f274fe426aaaa35e8f47f6cbd98a2b357d030aaba9ab047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231820637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f2dbf6b01403191675136699d347b8e6dd126dfb3776a34d7d7cc91b187d6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3784e0c144ba9ce263ec17b39e5222cc8c2846ef547a5160e2e9019ee96cba4`  
		Last Modified: Wed, 27 Aug 2025 17:28:53 GMT  
		Size: 65.5 MB (65534994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41c8e1f468fe2d079821e096a6636d695f37e969c3d41c54eeafc8bed260c03`  
		Last Modified: Wed, 27 Aug 2025 17:36:02 GMT  
		Size: 14.6 MB (14631636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4dfef53897f955b52c308584474d225262e23927209519283f9616ffb3c437`  
		Last Modified: Wed, 27 Aug 2025 21:40:09 GMT  
		Size: 149.7 MB (149708497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a54ea7018cfe7c81c5d150781e4ef7473cd8c22299a0dba3aa4e57f2520c319`  
		Last Modified: Wed, 27 Aug 2025 17:06:01 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dc50f4ceb96f2603f0fccdda694a6516af43d8289ffef87d7fc64197a4f85`  
		Last Modified: Wed, 27 Aug 2025 17:06:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945643a367d188559124ba8441d853d30f5dfdc3bea2aa24d9b133287366a683`  
		Last Modified: Wed, 27 Aug 2025 17:06:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bb1abec9a7bf215c2c1465a936c53af59e7b0414f2b0d091b67870edbb0cc`  
		Last Modified: Wed, 27 Aug 2025 17:06:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7449eea5322cabd3f5ed3de06fbcab52e683c76f81cb1ddd339439a66f534f6`  
		Last Modified: Wed, 27 Aug 2025 17:06:15 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:fa6b21c827b0adacd2e03daaf41e961a84f34651b940cfda6f6bd2e1627f623d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c3bb8849162c8611796cd152846cae08ab939201ae9305756375aed0d5ca95`

```dockerfile
```

-	Layers:
	-	`sha256:4104c7c6727e71a511d523a83e456e5ae783b58c1942e29655cd27d39ea11498`  
		Last Modified: Wed, 27 Aug 2025 17:38:39 GMT  
		Size: 5.2 MB (5181089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1a4c40cb77d8f2e951e51c943b106970fa081f19e699d6096bc0b833fca5e7`  
		Last Modified: Wed, 27 Aug 2025 17:38:39 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:67bc203cbe8807ff37fb7433080462d6d0978d7fd7c3a34afe7dee465bc58c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:95958f45c69310d050d19809b23193f6c35d21247fcdca3d569eb65faf365c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233230407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dff6807121cff1144eb2f77068bbec45f729b9cf9e2a84803f068b626839d7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8cf720232028b764dea94e13423657e5bd528d4122f5e40debee5779f9e45e83`  
		Last Modified: Wed, 27 Aug 2025 16:55:53 GMT  
		Size: 67.0 MB (67041415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b203a03fca50ddc2cb82b731236232f25e95938f7d0621c2d17bb16c3db41c96`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 14.6 MB (14574579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cfca241620ff4b6f46a49c5c23710f1558e324f9b00639e5cdb45485bceaa2`  
		Last Modified: Wed, 27 Aug 2025 17:37:12 GMT  
		Size: 149.7 MB (149668906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0072fcf63fbb7fa674e54180b1c8d98f8f45ec5ac731949e80940ee59caf9`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb5f950bffd24fe4425fcf51e4681ab7e6233420dd2efef5cf06603c8ec18f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7157b7c13867781f16e5163ccafefbc5b20b0229fb50af87455381933765468`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b470985774ed2afdb2e4a3a5c7413f595e53322aa7d9ec9c637a737e06d7c5`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fd85fc8cd7f5a498587a5b5364b9f8dbea065eb6518444e58b6e482ba502f`  
		Last Modified: Wed, 27 Aug 2025 17:00:09 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:ecbb52e76db9f2873030250c9e5a9bf2b45fd23e3d0fa41d76645362baa4a2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25425d9de66f7b17849680ab2e1cd590d776def3fc46ef10c50a3fa89782650`

```dockerfile
```

-	Layers:
	-	`sha256:87480ccea139f22a8b4d859c156523e2c68c7d902c31fe3a0e815431036c3eee`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 5.2 MB (5185728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa2c2a6f4ecf23e0431a26d4fe319c792628d5b42fab0ff35c58bbf38e57b77`  
		Last Modified: Wed, 27 Aug 2025 17:38:25 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:50849bafe7174643d746beb07e5a33ce2470e2a48e3dd38c2358892b38e08681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232457624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a1525a4802bccd10ea26d4dcc8e54f42edcac24e8abc29a29115dbc715cfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3784e0c144ba9ce263ec17b39e5222cc8c2846ef547a5160e2e9019ee96cba4`  
		Last Modified: Wed, 27 Aug 2025 17:28:53 GMT  
		Size: 65.5 MB (65534994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41c8e1f468fe2d079821e096a6636d695f37e969c3d41c54eeafc8bed260c03`  
		Last Modified: Wed, 27 Aug 2025 17:36:02 GMT  
		Size: 14.6 MB (14631636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cf830059522640e54bf2436dd06a50ae46bb2fa35169649d965d3a7625979c`  
		Last Modified: Wed, 27 Aug 2025 17:36:21 GMT  
		Size: 150.3 MB (150345491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab781920c3f9fd5195a6132bbe9c1b54418a2e33ff36b74a9d480ea7703ac5c0`  
		Last Modified: Wed, 27 Aug 2025 17:36:23 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35284442bd079f67990210eea0b3586dca838a412707c6c1a02afcf629dbb021`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5a7677f0a91fa0ed880ea2353a825d5f2e18e4cb1234b2203b99e94797e73`  
		Last Modified: Wed, 27 Aug 2025 17:36:24 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623a620071f48f17cf2f5deabf35784eda9045845ec99f89d25d6fdb9d8b92c4`  
		Last Modified: Wed, 27 Aug 2025 17:36:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43dc92a26926b2583acf7360f8a5f954d74549b59c6134a0cc11a6e8a3c7ff3`  
		Last Modified: Wed, 27 Aug 2025 17:36:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:37193e8f94f182ad80e9cf8056dd2a2150c89a6ff5b3ce24ae8b3ca69b6bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25d7c85614280feb484d3d3a21e1b5954172433e416b622d6ae7baf06cd40d3`

```dockerfile
```

-	Layers:
	-	`sha256:dc57dfff1f7043a7d090ec6835da4d1874ea69557e667e442046e902fc1db332`  
		Last Modified: Wed, 27 Aug 2025 17:38:31 GMT  
		Size: 5.2 MB (5183036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b260e035835951806c10b833386583289136bc7107c52d4592791c2c420685`  
		Last Modified: Wed, 27 Aug 2025 17:38:32 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json
