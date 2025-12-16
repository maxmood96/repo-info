## `crate:latest`

```console
$ docker pull crate@sha256:68d1430b4f7edf386dcaeb01d52b18d92d595da2a3012cb5a80b2e56579b1b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:03755e49eb92ae8eb1d7acc49092a05b6502092caedb5339174b22f67f35709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5242d7e52462d870dd44bc64aa0d685a59bfe7c86e5145e0e634dd198a5aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:57 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6acbee9d5348079cb85dae713b115ba05302b41e9b227cbfe3b2dae9cb290`  
		Last Modified: Mon, 15 Dec 2025 19:29:37 GMT  
		Size: 14.5 MB (14512829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ced334c44f4de2a971bd22e1992bd6b0c842659e52fc9e255fd46337df525`  
		Last Modified: Mon, 15 Dec 2025 21:39:33 GMT  
		Size: 149.1 MB (149133517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7111a74856498548b678c9cb798ca45fbec416115cb9472774d5cb902a1cd1`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666a64ebf108b2bbfd8f845c7510d51aa7b19993cd83bcf5d3c7288ad3982d5`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d862f94a754e253e94e266b073be3fe868359c5fb4e3671943799233a67d11`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c1baaaba5c1a5127f7301c826ffb775362c6a3b3f9b611dda2fad16ed28ec`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150126d40904960df7e55865dc704e4f7ab9b1435a671f51840b9a8373e9748c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:acbb49761e5d8ba0a18936d9b890cab96742b70ef486ac924cfe2eb50163923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056c1346f8a30d4061ef1f68698acfe20196c9a24ab4903c071318a960a9d07`

```dockerfile
```

-	Layers:
	-	`sha256:839de76bcc0825cd1a263ccae664ae2da6cc19324fd5bb0909f66319014847fe`  
		Last Modified: Mon, 15 Dec 2025 21:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e89c8b5fd1284ead2b63564ba79b930853662954d8dc82bfe01da7e1989113f`  
		Last Modified: Mon, 15 Dec 2025 21:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e49af2c974ad83ad55b4b44edbceb941a8356738af0c661bf44ec20b3f68c4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232278226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386e1b9355b4ee549be27edab692905aba2e5643739a3962fe5541973efd8b92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 19:28:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 15 Dec 2025 19:28:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 19:28:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 15 Dec 2025 19:28:56 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 15 Dec 2025 19:28:56 GMT
VOLUME [/data]
# Mon, 15 Dec 2025 19:28:56 GMT
WORKDIR /data
# Mon, 15 Dec 2025 19:28:56 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 15 Dec 2025 19:28:56 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 15 Dec 2025 19:28:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 19:28:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 19:28:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf824064357212c0db8f7ac35a1d7742479613edf2e9473b965e75c0e6d439`  
		Last Modified: Mon, 15 Dec 2025 19:29:40 GMT  
		Size: 14.6 MB (14567746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263b2b1d6e00611a009470a5e6c157ed0f005dead6fdc5343d40c17a5c89989a`  
		Last Modified: Mon, 15 Dec 2025 19:29:47 GMT  
		Size: 149.8 MB (149821981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82ce11b8ab22af2550cfd8dd0bda0535a9b282c189088e2b53ef8ae91d7e35`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ac1a82b7183428d26f4c85130380e6f813ad98d42c649345b6012616bbd0a`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e193941b5b441906dc3bc62458716e36d7e2d87656b0f221499cab4acccf00`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327eef58bc79a5f8ef34349f4a48f02bf17d3de10b2ebfc9fc7c580eea1c89`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a563353501f74fb1e5911728c89d06ce1cf70169b156bddcd288278092ea66c`  
		Last Modified: Mon, 15 Dec 2025 19:29:36 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:8dd3f419410d61586f8040128d81cac4c4e5bea6416df22b2db77cad724f8213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e8f0df4aed567043ecef4c2f04a3927975d93f92aec3d006333ce3de04e0d5`

```dockerfile
```

-	Layers:
	-	`sha256:b627ca132cfd98bd44a00d1c7f926fe11c029a623b007adc63cba8c2def09cb4`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaea1d0720139b2b23b37c4dad6ef4b068aa322a0f5171aa266b7a37422c92a`  
		Last Modified: Mon, 15 Dec 2025 21:38:53 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
