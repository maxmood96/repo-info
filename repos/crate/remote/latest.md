## `crate:latest`

```console
$ docker pull crate@sha256:96e2cca206020daa2330521db9996b810e31484604f28a1bfe7398b223e2989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:5c17cb810f81f15c3d06703381623d518960b0ae38932b3950da0bd01b1652e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300130277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee6d23d686d4799ef0b30414b515f051b477a0ace6db062d8651b53f008fd05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:20:21 GMT
ADD file:f1f574c0238642ba50927632ce79b8686be2da6793b9aa968b9556f567dc3437 in / 
# Tue, 18 Jul 2023 19:20:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:26:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 17 Oct 2023 01:19:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.4.tar.gz.asc crate-5.4.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.4.tar.gz.asc     && tar -xf crate-5.4.4.tar.gz -C /crate --strip-components=1     && rm crate-5.4.4.tar.gz
# Tue, 17 Oct 2023 01:19:59 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 17 Oct 2023 01:20:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 01:20:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 17 Oct 2023 01:20:00 GMT
RUN mkdir -p /data/data /data/log
# Tue, 17 Oct 2023 01:20:00 GMT
VOLUME [/data]
# Tue, 17 Oct 2023 01:20:00 GMT
WORKDIR /data
# Tue, 17 Oct 2023 01:20:00 GMT
EXPOSE 4200 4300 5432
# Tue, 17 Oct 2023 01:20:01 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 17 Oct 2023 01:20:01 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 17 Oct 2023 01:20:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-13T08:53:58.719371 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.4
# Tue, 17 Oct 2023 01:20:01 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 17 Oct 2023 01:20:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Oct 2023 01:20:01 GMT
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
	-	`sha256:7d3a01fd0465685c57cbc6604dc3beca48933cfc00b5d32d8f55caf68eaa6cbb`  
		Last Modified: Tue, 17 Oct 2023 01:21:43 GMT  
		Size: 229.6 MB (229556765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7138ed5ab8d8a1a4f726cbc41276355c2768e34c8bac0ce55128586103ec06`  
		Last Modified: Tue, 17 Oct 2023 01:21:24 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e132492e2cdf9fadc8290fa9e893b48ded22a69c83cdc42993a24e6824b2f6`  
		Last Modified: Tue, 17 Oct 2023 01:21:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53259d7877f25a33734c64733d139b5e27a254505eb48fe7bd46f71a92a60d8c`  
		Last Modified: Tue, 17 Oct 2023 01:21:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66904c3ec5ef0e8c3b25a662b483c2d0569da96b8caa3546738e3dc1dfc0cd11`  
		Last Modified: Tue, 17 Oct 2023 01:21:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e97ce2b0a04a27669ace0612113c5c2ccced6385b6891380f17344b12221a8`  
		Last Modified: Tue, 17 Oct 2023 01:21:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a979f77f7008a9fd0df6fee1758b24e4f82af53019eab3061b5b74acb94e10f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297372693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e79fa7034cf09c899971637d2639f5ac9a313f88f09ee2a3b7b83c965b2299`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 18 Jul 2023 19:39:39 GMT
ADD file:40800ee585298348133157273f601922b26aea5ea4e21cd03223a28d6bb24c71 in / 
# Tue, 18 Jul 2023 19:39:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 19:44:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 17 Oct 2023 00:40:52 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.4.tar.gz.asc crate-5.4.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.4.tar.gz.asc     && tar -xf crate-5.4.4.tar.gz -C /crate --strip-components=1     && rm crate-5.4.4.tar.gz
# Tue, 17 Oct 2023 00:40:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 17 Oct 2023 00:40:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 00:40:58 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 17 Oct 2023 00:40:59 GMT
RUN mkdir -p /data/data /data/log
# Tue, 17 Oct 2023 00:40:59 GMT
VOLUME [/data]
# Tue, 17 Oct 2023 00:40:59 GMT
WORKDIR /data
# Tue, 17 Oct 2023 00:40:59 GMT
EXPOSE 4200 4300 5432
# Tue, 17 Oct 2023 00:40:59 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 17 Oct 2023 00:40:59 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 17 Oct 2023 00:40:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-13T08:53:58.719371 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.4
# Tue, 17 Oct 2023 00:41:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 17 Oct 2023 00:41:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Oct 2023 00:41:00 GMT
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
	-	`sha256:5d65297b280fa0c81493a9f91c653303ee5b43e21452c4087cf498205eb012f4`  
		Last Modified: Tue, 17 Oct 2023 00:42:40 GMT  
		Size: 227.9 MB (227888664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b5319ad45c699e5debe91b94e1b9a6e4a9e085baed53f8a5800e73fef886b`  
		Last Modified: Tue, 17 Oct 2023 00:42:24 GMT  
		Size: 1.9 MB (1931735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c9f6a40b1dccd0463f9b61f49ee8c7ce097108aede8f99590da252f118950b`  
		Last Modified: Tue, 17 Oct 2023 00:42:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10deb4236c62f1dc160154f201bdae103d9b06769f346768aaa8b0bf33f6e60a`  
		Last Modified: Tue, 17 Oct 2023 00:42:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4c631d5e2bb699926129527bb21ca5a78b81f26b68fe9672e09640a75515d9`  
		Last Modified: Tue, 17 Oct 2023 00:42:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047fc4f5df34d1865dffa51cf9f44a1c77d16d2f738bba1644f0253bdfa6688`  
		Last Modified: Tue, 17 Oct 2023 00:42:23 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
