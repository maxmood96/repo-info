## `crate:latest`

```console
$ docker pull crate@sha256:e353f61d3348f46498a61a287bc03360a02986801dbbe0a835f21ec0dadc2ab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e0ec7b6c28207243710bdc07f14c7ca27baf9d122c5e2f8c5345e2f9b93bdb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211446234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562ed476828f869db0ae44363133756644755537f453f8bc6f8a611fc5bd10ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 05:57:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.1.tar.gz.asc crate-5.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.1.tar.gz.asc     && tar -xf crate-5.8.1.tar.gz -C /crate --strip-components=1     && rm crate-5.8.1.tar.gz # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 05:57:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 30 Jul 2024 05:57:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
VOLUME [/data]
# Tue, 30 Jul 2024 05:57:24 GMT
WORKDIR /data
# Tue, 30 Jul 2024 05:57:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 30 Jul 2024 05:57:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-30T05:57:24.295346 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.1
# Tue, 30 Jul 2024 05:57:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 05:57:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:7edcf90c3c130f9638b4525b9a3ffd836d460c724c64b719bdff4aa4c2da1080`  
		Last Modified: Tue, 23 Jul 2024 17:14:54 GMT  
		Size: 68.6 MB (68589259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec472aea49fb6d3763ff469ed53dd8c3f72cf0478c045cec96016002d3e7338`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 11.0 MB (10967379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0447c20799d63af809eb6fd2e8ac99edd171fe2b4e8fd3baf7c6472ad0df1a9a`  
		Last Modified: Mon, 05 Aug 2024 18:57:32 GMT  
		Size: 129.9 MB (129944090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6935c7cdd2a96666409498d4bbdbfd0552b4d68214dff3bebe7fcdeaedfeae4d`  
		Last Modified: Mon, 05 Aug 2024 18:57:30 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8496f41f700609d7cc22eb811a158df80f7de50fca57432f6d38295fd05b7`  
		Last Modified: Mon, 05 Aug 2024 18:57:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6a4cd9a1a00f3d7aeade61379d3dfb9cfbe4168613d2c3f8a642740ee5453`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b602c6141a6057b2921923052bd2b2a00896f56a5f9edea883f3296f5c8357dd`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b97f8d8348fe46a2f4ee08007ee285ac313b84f2317f43cbea2ca89387613ae`  
		Last Modified: Mon, 05 Aug 2024 18:57:32 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:1e5faf2dad0865e67781bd27eb8588c2850a5d879f645a6f209aba5716f53ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5008056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cde06b831b36c0e6a6ab6e9bbbd069451ee17873d61a01aa84108eece90a1c1`

```dockerfile
```

-	Layers:
	-	`sha256:8dac2eabdb2108057b8005fae79257c41e608000365f6d3d0eb8683d26a6dc12`  
		Last Modified: Mon, 05 Aug 2024 18:57:30 GMT  
		Size: 5.0 MB (4984968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ae8c6c40d96ddc91130bfec0c31760d30fc50324dd218b8f756b3a2d0e8f6c`  
		Last Modified: Mon, 05 Aug 2024 18:57:30 GMT  
		Size: 23.1 KB (23088 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:04b9d9829f951c4b2cee22e54063f0ce510e25f0cc22a9e91a4a965c9996e2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198856653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8fdfd313139c123e22568bde41e7be53692e9be8a6930fab76a09b24ce75ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 23 Jul 2024 10:26:38 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Tue, 23 Jul 2024 10:26:38 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 05:57:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.1.tar.gz.asc crate-5.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.1.tar.gz.asc     && tar -xf crate-5.8.1.tar.gz -C /crate --strip-components=1     && rm crate-5.8.1.tar.gz # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 05:57:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 30 Jul 2024 05:57:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
VOLUME [/data]
# Tue, 30 Jul 2024 05:57:24 GMT
WORKDIR /data
# Tue, 30 Jul 2024 05:57:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 30 Jul 2024 05:57:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-07-30T05:57:24.295346 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.1
# Tue, 30 Jul 2024 05:57:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 05:57:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 05:57:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:4743f6afb1d7aec4ef19a35057c609f4576de589137c5535b6818a9e14b096c8`  
		Last Modified: Wed, 24 Jul 2024 02:00:23 GMT  
		Size: 67.5 MB (67503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b65453f3a6d5a9e154e45c80ebf228e6940e0950bcc9202980afe28bd552fc`  
		Last Modified: Wed, 24 Jul 2024 16:32:24 GMT  
		Size: 17.7 KB (17698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614b9aaa9266bc77ad35b4aec37d54269068f358a0c3d29ba001f461ec50720`  
		Last Modified: Mon, 05 Aug 2024 18:57:34 GMT  
		Size: 129.4 MB (129389970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bb145b41efd4ed21ce669823d6bad1a1bbbd15b9403ac4d3a49d4c3873e8fd`  
		Last Modified: Mon, 05 Aug 2024 18:57:32 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace419559fb1243f3a1c37a9dbcf818671d48264d170136f23e37e862faf898e`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5a95c4ba5ee2c28df8000a5aaf07726ab33782c71d85ea037c2107845076fd`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed493c889af4f7c3effc6c081cebb2f7e39ccd84975bcf44e179449584219c3a`  
		Last Modified: Mon, 05 Aug 2024 18:57:32 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6effd59125488b3bb16044886a4a05b682d3a816cadb8c891a644099e0200dee`  
		Last Modified: Mon, 05 Aug 2024 18:57:33 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f1136fe6ea68b4e766140ab98a4c41d3829bd2cd920a6d6a666f99233fa8c048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5006334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c975c889315df72b7caf1cb4a65388566733e430e90e480b6385fc19d2fd6c45`

```dockerfile
```

-	Layers:
	-	`sha256:53b12d7994d462d20e8d4458214b044afb75895c489291b820b771ff88bfab84`  
		Last Modified: Mon, 05 Aug 2024 18:57:32 GMT  
		Size: 5.0 MB (4982897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2428f2add0f6bd766ea36bddfb8bf7191534f443a1784c822b98d03f78fd2b`  
		Last Modified: Mon, 05 Aug 2024 18:57:31 GMT  
		Size: 23.4 KB (23437 bytes)  
		MIME: application/vnd.in-toto+json
