## `crate:latest`

```console
$ docker pull crate@sha256:cb41c1ed491515417238c48c1fb5d1ad57f1a32bf6524ac1c02e2c46758236c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e7565d09dd1793409875f1a38e086e7a22fb79f97db5f307061a8dc7469d43ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189001890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d9390ea0c9353669cf94f2a91fa3822666ef3639817087de9b94467040330`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:02:58 GMT
ADD file:f9e45b02586d1bbbb5cc973125024a5bac49fefc9988f604a381fcd5c935dc46 in / 
# Fri, 12 Apr 2024 01:02:59 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 01:40:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 01:40:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 01:40:37 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 01:40:37 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 01:40:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 01:40:38 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 01:40:38 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 01:40:38 GMT
WORKDIR /data
# Fri, 12 Apr 2024 01:40:38 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 01:40:38 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 01:40:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 01:40:39 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 01:40:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:40:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3a148d62534a64a4eb34966ff90ee4f5c097d2da3e3560059875fca9d7e9916a`  
		Last Modified: Fri, 12 Apr 2024 01:04:12 GMT  
		Size: 68.2 MB (68197997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066c8404d8aaf65830c088af98faf086cb532177dc76787627d33da23c1934ed`  
		Last Modified: Fri, 12 Apr 2024 01:42:23 GMT  
		Size: 425.7 KB (425661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124713450165b300a5564c7e7f867872efc20dcadcab0da7fefc54e38b26aa8f`  
		Last Modified: Fri, 12 Apr 2024 01:42:32 GMT  
		Size: 118.4 MB (118435699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33edd3abd1664a7ce0a32840f9984b5f7840358dbc7c1511e62420c42761380f`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 1.9 MB (1940654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a5daffa9b99902422d73fce700aa264995b940f35f6f2083de4b2213e54cac`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8081fd96df3d797219535bd2b24584437920b18d3fe62d3d24167cde96f166c`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d03402f6f939c724589ce530ebf44ba1046be714b06c83100fdff412eb565`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204840cd1dee42c195853f6537f7b20ee5881aa86fe55263592c76296dfead3`  
		Last Modified: Fri, 12 Apr 2024 01:42:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:be222d5c95546a9eba0ed2c5aa3553fc53028d1bec4a43d7589b3c6e7207f7af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187424511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388fcbf2fc56dc7d70ac20ee60a958bd4543dede538a3b7c5681e76e754a120e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 12 Apr 2024 01:33:05 GMT
ADD file:e528ba27299971d0ceb9aa91eb76b4dd853355f217c9c9103b7b3e69f7fbcd2c in / 
# Fri, 12 Apr 2024 01:33:06 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 02:12:32 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 12 Apr 2024 02:12:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.4.tar.gz.asc crate-5.6.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.4.tar.gz.asc     && tar -xf crate-5.6.4.tar.gz -C /crate --strip-components=1     && rm crate-5.6.4.tar.gz
# Fri, 12 Apr 2024 02:12:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 12 Apr 2024 02:12:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 02:12:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 12 Apr 2024 02:12:49 GMT
RUN mkdir -p /data/data /data/log
# Fri, 12 Apr 2024 02:12:49 GMT
VOLUME [/data]
# Fri, 12 Apr 2024 02:12:49 GMT
WORKDIR /data
# Fri, 12 Apr 2024 02:12:49 GMT
EXPOSE 4200 4300 5432
# Fri, 12 Apr 2024 02:12:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 12 Apr 2024 02:12:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 12 Apr 2024 02:12:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-04-05T10:12:22.384648 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.4
# Fri, 12 Apr 2024 02:12:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 12 Apr 2024 02:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:12:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c7ef08175a61ad08808e2400cd4b68794b6ca7af77bd8b67c23cdecb32cf08f3`  
		Last Modified: Fri, 12 Apr 2024 01:34:06 GMT  
		Size: 67.1 MB (67083957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c429a3963eef4e0fad17d4ae34d824e9ee153da7e5681b88c99354ae12504`  
		Last Modified: Fri, 12 Apr 2024 02:14:33 GMT  
		Size: 424.6 KB (424600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1686b4bb65d3e8d847fea26425b0c8a7b9f29053a586e39f950013d9e5dde5`  
		Last Modified: Fri, 12 Apr 2024 02:14:40 GMT  
		Size: 118.0 MB (117973419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e844ed34289eda813289d0b228073384424a5d1ab9247d869c7304656a7091`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 1.9 MB (1940656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6574ba80367b745d5cb4a42612babbc0c334a5409046da6ee8953ddb7bc0d`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a756271070466b99015a49a29240cd60e260d271dfcf8e0c8c1629e2bceca6`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb926faadc2da675147b97e4305a15d48d49ce12450072a81dbbdc881debfd27`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3e50353b130bfe837910c7cd483af7a736ab39efa98d4cf16e6386cf97a0e`  
		Last Modified: Fri, 12 Apr 2024 02:14:31 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
