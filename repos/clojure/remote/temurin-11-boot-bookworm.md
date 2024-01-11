## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:71a5c814732757a44efe2d64991c76cd1870ef8026ce44cbe8125cc8d05f9988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de584417369c3b31dda05f7ab5e4611d0624748700c508494c40e81de86d681b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259175346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c99b6d3fcab19d2846d4de358b2c58ad140b1e29da5d63f1aa108af822c3fa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:58:04 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:58:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:58:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:58:06 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:58:12 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:58:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:58:13 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:58:33 GMT
RUN boot
# Thu, 11 Jan 2024 04:58:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4828ea3928dab776906e18f4cf1d64b338cf2fb9966f9414f22c0c6cda899dae`  
		Last Modified: Thu, 11 Jan 2024 05:17:34 GMT  
		Size: 145.3 MB (145266366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75aadaeb8d52d028b878ba91c6798463ce0187b2cc4de961437e8755a5a13b49`  
		Last Modified: Thu, 11 Jan 2024 05:17:23 GMT  
		Size: 5.5 MB (5527024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0bf93eeb6ada5543def7c26b9f5813cdc76a7a85d3dd57904f9ed770c96e13`  
		Last Modified: Thu, 11 Jan 2024 05:17:25 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bd429c0b567e94b045c153695656cbc83daf0eaf3e3e671e1e5940333554ca2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255763869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12686166c0251c01009a2e0f84e8c24bf7303591cff25351d9a309c37f5d29`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:58:59 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:59:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:59:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:59:03 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:59:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:59:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:59:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:59:24 GMT
RUN boot
# Tue, 19 Dec 2023 06:59:25 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593f42435501ab6968f6cf2d6070608060a249b959ac3906a8d5dee7d8736304`  
		Last Modified: Tue, 19 Dec 2023 07:15:45 GMT  
		Size: 142.0 MB (142001822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d90881b523d7bf494d1e30f89b9c14c2365bef69dd42d39c5ba11b18ce9a514`  
		Last Modified: Tue, 19 Dec 2023 07:15:37 GMT  
		Size: 5.3 MB (5349332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9239a44a0b08e3a199c007a397a91473014e69b3f652cbbcaaf8c51b1233f6`  
		Last Modified: Tue, 19 Dec 2023 07:15:39 GMT  
		Size: 58.8 MB (58820456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
