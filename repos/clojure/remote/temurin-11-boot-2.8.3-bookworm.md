## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:52c4a34e8fdcc254c672b4348b72a01965f61912f32c3bc7b5ce656fa8d7c755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

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

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:511afab36bc9f7dc8007cc8f116ec00add99dd3de26af034923bddf1300bf1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255763912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8a6b6eefd863f0f2dda5cbd77078ff157ebad59fc46937ab33f0ee4524607a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 08:03:55 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:03:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:03:59 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:03:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:03:59 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:04:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:04:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:04:04 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:04:24 GMT
RUN boot
# Thu, 11 Jan 2024 08:04:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a89131881d8be83ab54ed31e484435f358a2e757e082baa72f336ff8dbbacb`  
		Last Modified: Thu, 11 Jan 2024 08:20:55 GMT  
		Size: 142.0 MB (142001888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c598ef7765da42f5b4fed15b68dcfec3380a1f7d91fd63a6b0300edc2f7575be`  
		Last Modified: Thu, 11 Jan 2024 08:20:47 GMT  
		Size: 5.3 MB (5349231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e147342e5965eb80ec0b3a99ff3d66e34c5f21003fd9539d9ca6176afd3467d9`  
		Last Modified: Thu, 11 Jan 2024 08:20:49 GMT  
		Size: 58.8 MB (58820546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
