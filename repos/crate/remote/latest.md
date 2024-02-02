## `crate:latest`

```console
$ docker pull crate@sha256:a8b677e16638e3e253400fb398d54fcc073bff8319589e1279b0376680bc95be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9f958a830953682f4ccd11af8ea934fb792629b6be73e8d3a41ddc5f820a5a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186870503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86ee3cb3413e75940da34eb557c55868f9d3ff2053a981782b9694ec91b821`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 22 Jan 2024 19:38:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.3.tar.gz.asc crate-5.5.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.3.tar.gz.asc     && tar -xf crate-5.5.3.tar.gz -C /crate --strip-components=1     && rm crate-5.5.3.tar.gz
# Mon, 22 Jan 2024 19:38:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 22 Jan 2024 19:38:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:38:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 22 Jan 2024 19:38:35 GMT
RUN mkdir -p /data/data /data/log
# Mon, 22 Jan 2024 19:38:35 GMT
VOLUME [/data]
# Mon, 22 Jan 2024 19:38:35 GMT
WORKDIR /data
# Mon, 22 Jan 2024 19:38:36 GMT
EXPOSE 4200 4300 5432
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 22 Jan 2024 19:38:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-17T13:51:08.432216 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.3
# Mon, 22 Jan 2024 19:38:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 22 Jan 2024 19:38:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:38:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f91ae4aa845d750268f9dab72264048a18c127e675954cc679ddcda1687a74`  
		Last Modified: Mon, 22 Jan 2024 19:39:11 GMT  
		Size: 116.3 MB (116277645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85a2368f5ae7b63abaccaa819c7f69cb3f68493079e438552c01fcecc82505`  
		Last Modified: Mon, 22 Jan 2024 19:39:00 GMT  
		Size: 2.0 MB (1954466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b33fda5199736a83b1af39bb08eb6e5e9ec4b9be4ae967e9b0dfb1d937c4a4`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba12b4c41f7801f96610e4e9730bcd4ff7a36a7585c1d3288ad37cb18d33bab5`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72532fc3f5543c472e129c401709aeac24a359be79725784bba85fc0f67e530b`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6251c14959303ad5d41eb604b503f6ec87894ab0b408e4f8a7080ae3a02a570`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:29af014af4ca44990ea7b866e12fa40f135532b860c542f8beac284a5b067472
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187428841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbd6f9428c194610e1bb0aa05436eceacab9dee4702a1be20001849ac332b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:39:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.1.tar.gz.asc crate-5.6.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.1.tar.gz.asc     && tar -xf crate-5.6.1.tar.gz -C /crate --strip-components=1     && rm crate-5.6.1.tar.gz
# Fri, 02 Feb 2024 19:39:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:39:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:39:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:39:50 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:39:50 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:39:50 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:39:50 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:39:50 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T19:27:30.643907 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.1
# Fri, 02 Feb 2024 19:39:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:39:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:39:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eefb87b90b01bb7659ee9f8421262e383dd80d805ddd24b0048c7bd33b28a8`  
		Last Modified: Fri, 02 Feb 2024 19:41:45 GMT  
		Size: 118.0 MB (117971945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1aabf07a32e19976f9af402d61787aefc03490e353e8003d91755255ae8c2`  
		Last Modified: Fri, 02 Feb 2024 19:41:36 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e16f4908665795d2bab19ee0de7cca1b7c9a4a880cc362edaa65f105716d6ea`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3d3e9154228d29d2170185c8d44a4c6219edf7866169d803f06129d6d3d53`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3991c9b483f493e1ddc8e0f095a245ee3bd9f092108729d9668ac30af13f55d`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d664d1250e308308a65a76b90bc2c661ac145bd64dee9b3caf0d3c097276f`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
