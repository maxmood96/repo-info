## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:92b17e4beab76f94a73fd1265786aa9acd8d37bc6e558148fa2b64a457041c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a964b2b39ec692b10c2b4684d38116bfd794f3f474ba357c0e965520dd3790e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9726eb7a9a8f851c358b2a9cddcfcf63214b34858cd8d7c4318f13201cd23270`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:51:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:51:18 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 03:51:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:51:18 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:51:23 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 03:51:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:51:24 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 03:51:50 GMT
RUN boot
# Thu, 06 Oct 2022 03:51:50 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae48098ffe7fd94ae70e214ab303cadbcce413975a6348bcaf92e27c1fc827a`  
		Last Modified: Thu, 06 Oct 2022 04:08:39 GMT  
		Size: 1.1 MB (1077296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e87fa2aa7342eba3eb49d3593c72da4607c37502243bb9a8cc243efc640ac`  
		Last Modified: Thu, 06 Oct 2022 04:08:43 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e26da198d19ea5be6edd80023431750c59f411deaa90fea70d650557cb7b3bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284606183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3103412cc1bd5ded0f813cc24d526038357ac568bb76ecc47b6c3fcd726c401a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:32:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:32:31 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:32:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:32:33 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:32:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:32:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:32:41 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:32:57 GMT
RUN boot
# Thu, 06 Oct 2022 02:32:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da499ec95c69fa2667727ec736189c271e3804b54655a192af5e077d416f187d`  
		Last Modified: Thu, 06 Oct 2022 02:57:17 GMT  
		Size: 859.3 KB (859274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd588306ece944ff691a9d60685d9040c0fcedd15aec58b1894237d9aa4575b6`  
		Last Modified: Thu, 06 Oct 2022 02:57:24 GMT  
		Size: 58.8 MB (58815922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
