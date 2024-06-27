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
