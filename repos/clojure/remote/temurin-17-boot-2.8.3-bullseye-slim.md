## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:e0b6cd75269c59d14134852de9c2161db0f8bae98d3a8549637a822569dc009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51843c8e9e9fb1ce3aadab28ba1b35fb3af4583fe48b91e3ce647fc889924265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236094065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a08c49d2fc491dedb627fdfcfff5913366df3139f4912338462ca2af8f9f78a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:57:49 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:57:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:57:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:57:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:57:51 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:57:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:57:56 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:58:14 GMT
RUN boot
# Wed, 11 Oct 2023 18:58:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:58:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:58:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78747fe143b7fa5e45754d0d844a02627e9122cc66bfd025736a5061056de6`  
		Last Modified: Wed, 11 Oct 2023 19:07:35 GMT  
		Size: 144.8 MB (144775760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c926f6f1af046b37aa468da7d2fd6a970b3c9cce8927b668b4a8b5ffeba23e`  
		Last Modified: Wed, 11 Oct 2023 19:07:23 GMT  
		Size: 1.1 MB (1079451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fed006f8b1bffdf5380b82d7ede0d067fcb184c77993ab0817fd2e95eafb0d`  
		Last Modified: Wed, 11 Oct 2023 19:07:27 GMT  
		Size: 58.8 MB (58820592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a01cc3ee4c40257b51ca75d0035e55773fffe34ec5400a291818b546fc7484`  
		Last Modified: Wed, 11 Oct 2023 19:07:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d138d746dd01670a7286d3ffc6568ba16ec2f214755fb331e3bd44e597620d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233495102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b3e21e647dd6203a0288ff4419e8247af264d633c482f0071c07249d69bf28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:20:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:20:08 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:20:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:20:08 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:20:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:20:13 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:20:30 GMT
RUN boot
# Fri, 13 Oct 2023 10:20:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:20:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:20:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba29605be7387d32f13d0a75a63f10f2144c1ced7c7e502d0cd66a45a5cf34ba`  
		Last Modified: Fri, 13 Oct 2023 10:34:50 GMT  
		Size: 1.1 MB (1066843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741620ee9613407d907cabd18abc6eacdb7330fa0cc47499452163eb05ad4dff`  
		Last Modified: Fri, 13 Oct 2023 10:34:54 GMT  
		Size: 58.8 MB (58820253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c0e0da2f13e593d87148839c614eb6a3a520118b5436c13483d11a0ea6915`  
		Last Modified: Fri, 13 Oct 2023 10:34:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
