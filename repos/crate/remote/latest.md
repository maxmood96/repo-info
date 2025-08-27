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
