## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:f90996e24bd05dd348c10d0e4cf4db815ec4f3a9b3aaac4a58e8834ec7f8c58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:adffb98c73dd88a7fffff0a837852333ed6a747671cb930abcc1a1da8c3071df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5096587c56dda0b4a595696e8db6646e694f658783ce8ed69e65fafbe2201`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:02:05 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:02:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:02:07 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:02:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:02:07 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:02:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:02:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:02:33 GMT
RUN boot
# Wed, 06 Mar 2024 14:02:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d001d8a2900abfa74e3eea1ab01d3a896c3ba25736082483c2e900b34e2ad16`  
		Last Modified: Wed, 06 Mar 2024 14:23:15 GMT  
		Size: 145.3 MB (145271156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ab27a4ba672f08246e529dec5f73e6007a79e790a9b7520c1f02d04be3de8d`  
		Last Modified: Wed, 06 Mar 2024 14:23:04 GMT  
		Size: 3.5 MB (3498213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d799e0b5074df0c794b82894437b152f641eb167b0656a7bf473943b7d7527`  
		Last Modified: Wed, 06 Mar 2024 14:23:07 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:639319686506266322470c596491d545f5bb124f1d2bc5e9b80e5269cf837d8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233307613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94255611d3d4fe154bb823d062dbac232c510649e1cdd916759755d96ada293`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:48:58 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:49:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:49:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:49:01 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:49:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:49:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:49:06 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:49:24 GMT
RUN boot
# Tue, 12 Mar 2024 01:49:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6040bd46f1e6585005f3d535c4dbe9fde45d2da23e3e11b657cf2ced2543d6c`  
		Last Modified: Tue, 12 Mar 2024 02:05:59 GMT  
		Size: 142.0 MB (142008486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c080d25ffba1dd2859f2cd4673498e6fed1e78d4e341454d57a91b643ca8f`  
		Last Modified: Tue, 12 Mar 2024 02:05:51 GMT  
		Size: 3.3 MB (3322120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebc84a00bf12e70e69082c82a103fd4a4eb509af3a556f04dfe822b9197e1d1`  
		Last Modified: Tue, 12 Mar 2024 02:05:54 GMT  
		Size: 58.8 MB (58820573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
