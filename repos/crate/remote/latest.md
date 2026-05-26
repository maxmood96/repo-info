## `crate:latest`

```console
$ docker pull crate@sha256:5fa05ec7b3f533f75a9529dd12ad2b6f7b8a13c9f394c044c6945d868a4f3605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:dc8ce9b18d9746387afb8a9e85b3067e5bc0666a5a703fff40d4a843c62b816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ef19c41831b5143d1460d7d3362d7eb8e36d3a3e0feaa96fc6ef09009a870a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:11:57 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:26 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:27 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:27 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bc16abacb35ba25dfec79024653f56d5cb77a1239bdc77a92ec0a93e1fab8de8`  
		Last Modified: Tue, 26 May 2026 19:12:14 GMT  
		Size: 68.6 MB (68562950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c3b6246f20b9a925dc87e934c9cf64c0c44010f77ff19511188cef2b2c0fb`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 18.4 MB (18373082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfba3c79962856a1e54c0451a888bbd72cdc56d39113497c5122a6bacdf5d6`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 139.1 MB (139069153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b23ac2eb4d969f240217e147a30312cad9c3a7c2a2b2d2879d638eea0e0ed0`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 7.8 MB (7763063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be65eec188df7e0de0cc2b3b5bd7c3426e31b5ebee20eede07291da9ecc18238`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684e42778e98a899e4642aa85982a554ff579c919faa689a0ae976e03fcef8d`  
		Last Modified: Tue, 26 May 2026 19:17:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dcbd6619b8f7f19901b4ca519a535fda4ced674fcff6d1561d634bdc4e02f4`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29365e98f1d9c54259e9868bef2078fd5e1d186808a5849fce5142616fff1688`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d11618d4795ebca54f1248ff72a25d44a3c2dd2271774e89b25480689679c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fce6930bdb4ca1a6d109bd30726b7d3c5192a5b236b9bc4df4709c2b0006d45`

```dockerfile
```

-	Layers:
	-	`sha256:27e049d1a72565d90641210798de34acd23fc4fcebbe61a2565986f39096c40b`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 6.6 MB (6606382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b052e0a388755bee67dc90b89240b22fdbc198c98e798c30a70b1bc21473757c`  
		Last Modified: Tue, 26 May 2026 19:17:44 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:53c3dc19d76e2038859d2581497ad614a0f472190c80d951f70e34c2ffb33a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230348745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03adb1f17743c41e0d8fa123e2ff28c04b44b649ace81291f87980ce36533bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 26 May 2026 19:15:06 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 26 May 2026 19:17:34 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.2.tar.gz.asc crate-6.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.2.tar.gz.asc     && tar -xf crate-6.3.2.tar.gz -C /crate --strip-components=1     && rm crate-6.3.2.tar.gz # buildkit
# Tue, 26 May 2026 19:17:37 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 26 May 2026 19:17:37 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 26 May 2026 19:17:37 GMT
VOLUME [/data]
# Tue, 26 May 2026 19:17:37 GMT
WORKDIR /data
# Tue, 26 May 2026 19:17:37 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 26 May 2026 19:17:37 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 26 May 2026 19:17:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-05-13T10:53:03.949869+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.2
# Tue, 26 May 2026 19:17:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 May 2026 19:17:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 May 2026 19:17:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f5e8c3ebd66ecb4894e8e592eb2ab3aab6dba6479752dc4bc0859cbd16395901`  
		Last Modified: Tue, 26 May 2026 19:15:22 GMT  
		Size: 67.1 MB (67134169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ceb39908fa0916b55c1c5fe25d6bcd599da6bfea3b0ff6784403960fede1f`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 18.4 MB (18426634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d685f87a033ed8a0d40ceae6e41e7371f31cb46fee7591a7b0978001f3088`  
		Last Modified: Tue, 26 May 2026 19:17:58 GMT  
		Size: 137.0 MB (137026793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06f03bfaf4751fb824c3110cdf8450ae4ac48f80ad4b2d6b3b7527f785b0907`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 7.8 MB (7759273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d25aad35dc3ad69b8550d33c494253c2fa843098728f64f876a5580709a68`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e780bc235567c7eacd93b2e4de0dd3bd68719be2b1b94568d02b59814ed8a01`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72283ff895861ddf517071d1be26211f55ed97c744a9fc77ea1d71a943589a8b`  
		Last Modified: Tue, 26 May 2026 19:17:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0a0e7416b07e74ca20a4fac603cb172ea2f7031c2ebfc16a39d4ef7e1fd29`  
		Last Modified: Tue, 26 May 2026 19:17:57 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b2dd7888f58360dfb132bbc951711b82224eec40d1778976a460b77f45fdd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b707dc1ed84ad8256cc6ce6a7f51a4a0075f5b986d49d809b342536f2ef70079`

```dockerfile
```

-	Layers:
	-	`sha256:4fb64da8749ab6cb4d64ea706935ff1ffbd1923a6a1fa1b57d269b137fd9bbcc`  
		Last Modified: Tue, 26 May 2026 19:17:55 GMT  
		Size: 6.6 MB (6604306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb513657ce155379bf96b49dceedb36c21d28ed214fa70fb66f1414e7d3e883`  
		Last Modified: Tue, 26 May 2026 19:17:54 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
