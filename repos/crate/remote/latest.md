## `crate:latest`

```console
$ docker pull crate@sha256:c4ac0ca3b9e0e188e43b0028ff0978040c7f749f7d25efc8a769357c852da224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f3984ae4380c47bca4ff7a108b4b3eb5b515686f24dd6e7967b5d6f1175d81a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d2d5d01922ffec79e7b7fe65de79dd3342a65a990827c47d315146a02311f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 07 Aug 2023 19:23:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.1.tar.gz.asc crate-5.4.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.1.tar.gz.asc     && tar -xf crate-5.4.1.tar.gz -C /crate --strip-components=1     && rm crate-5.4.1.tar.gz
# Mon, 07 Aug 2023 19:24:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 07 Aug 2023 19:24:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 19:24:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Aug 2023 19:24:01 GMT
RUN mkdir -p /data/data /data/log
# Mon, 07 Aug 2023 19:24:01 GMT
VOLUME [/data]
# Mon, 07 Aug 2023 19:24:01 GMT
WORKDIR /data
# Mon, 07 Aug 2023 19:24:01 GMT
EXPOSE 4200 4300 5432
# Mon, 07 Aug 2023 19:24:01 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 07 Aug 2023 19:24:02 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 07 Aug 2023 19:24:02 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-08-04T10:56:58.913246 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.1
# Mon, 07 Aug 2023 19:24:02 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 07 Aug 2023 19:24:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:24:02 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:92cbf8f6375271a4008121ff3ad96dbd0c10df3c4bc4a8951ba206dd0ffa17e2`  
		Last Modified: Tue, 18 Jul 2023 19:21:32 GMT  
		Size: 68.2 MB (68212236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d128efc14189e19b8aa9c4f5a0eec8968c3b24e069b006640e98dc8f3169d81`  
		Last Modified: Tue, 18 Jul 2023 19:27:39 GMT  
		Size: 427.7 KB (427659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57e0bffe60a68cec3f95743a49141c583fb9dffacbe30c64f63914388872d4`  
		Last Modified: Mon, 07 Aug 2023 19:25:08 GMT  
		Size: 229.6 MB (229554768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23b38d80cc9c2bf852cf43f2679b14da723d02578ccca7031c23a03c87f5185`  
		Last Modified: Mon, 07 Aug 2023 19:24:49 GMT  
		Size: 1.9 MB (1931734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544bc0deadfd401b7c066ab54971e199211a58585a21f00848e5da3e072be7df`  
		Last Modified: Mon, 07 Aug 2023 19:24:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25c1fec02d1a3f6386927ea0e5b16f42b7c9cfb3ffd183ca0feed441b6b06f0`  
		Last Modified: Mon, 07 Aug 2023 19:24:48 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1c52b6ffaae6e2d7f995e19d7fdea5d1933130525c6372d567a63247c06a98`  
		Last Modified: Mon, 07 Aug 2023 19:24:49 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4f002b9ffe8d272d5d327e65850b01843d0e5670cf79292cb3e2cc4bcb605e`  
		Last Modified: Mon, 07 Aug 2023 19:24:48 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:175bdb2f7fca2f9a99e42731aadca67e464bcdd4acdc7f4a83e7b92612d18b6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297368245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330e7fcdf2bab2edaccaf51edc850ebf16b7314ca35ce27911d60faaa00fa686`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 14 Aug 2023 21:18:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.2.tar.gz.asc crate-5.4.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.2.tar.gz.asc     && tar -xf crate-5.4.2.tar.gz -C /crate --strip-components=1     && rm crate-5.4.2.tar.gz
# Mon, 14 Aug 2023 21:18:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 14 Aug 2023 21:18:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 21:18:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Aug 2023 21:18:45 GMT
RUN mkdir -p /data/data /data/log
# Mon, 14 Aug 2023 21:18:45 GMT
VOLUME [/data]
# Mon, 14 Aug 2023 21:18:46 GMT
WORKDIR /data
# Mon, 14 Aug 2023 21:18:46 GMT
EXPOSE 4200 4300 5432
# Mon, 14 Aug 2023 21:18:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 14 Aug 2023 21:18:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 14 Aug 2023 21:18:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-08-11T11:17:57.318053 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.2
# Mon, 14 Aug 2023 21:18:46 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 14 Aug 2023 21:18:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Aug 2023 21:18:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:835f37e6c17066f8e99a562de9c491c11a1562baae1f6d2476852c9c30f298e2`  
		Last Modified: Tue, 18 Jul 2023 19:40:41 GMT  
		Size: 67.1 MB (67123448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c408286eb8cf39dd4a503a1dcfd5cd1231b678372fbf9ea9ffb1baa10f028`  
		Last Modified: Tue, 18 Jul 2023 19:45:22 GMT  
		Size: 427.0 KB (426966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dfdf2a1582e1e648fa569711e1be1b9306cf7f099372c030efa7bbf7dc7d7a`  
		Last Modified: Mon, 14 Aug 2023 21:19:52 GMT  
		Size: 227.9 MB (227884216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb19a7e2085fb3c326522e131df1cb7f48300d9c895bc32289cb9a41392ddea7`  
		Last Modified: Mon, 14 Aug 2023 21:19:35 GMT  
		Size: 1.9 MB (1931737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f4de16851f248919e37e8dcc23253cab62e7834c170d4aa3e077a2a9471d2`  
		Last Modified: Mon, 14 Aug 2023 21:19:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9519ba755d5d424f021ab0a484e95d4e72dcd41d73fa7b3859fc0b07457b0ed`  
		Last Modified: Mon, 14 Aug 2023 21:19:35 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b152f30d088a594007e6bd2984ed3f13c0578d2d179ce8346dd4ff44277e1b3`  
		Last Modified: Mon, 14 Aug 2023 21:19:35 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fefd2cb51d01ffdf302b09f7baf68155522b3b2de87039cd655ee202cfba8ad`  
		Last Modified: Mon, 14 Aug 2023 21:19:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
