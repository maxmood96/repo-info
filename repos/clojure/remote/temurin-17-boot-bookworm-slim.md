## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:78d3fa341169c3bd0ba530854f8afc13da9cf4c5fa8f12ce8313397fc0173257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d497aba40c1e57dfcba627cc0628f3ba3a2b3d5eea12b195871846aad267c334
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236336181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28037d787db24f5523ba1caa208aaf1a10eb43488206e16f6dfa19520824700a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:10:35 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:10:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:10:36 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:10:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:10:36 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:10:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:10:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:10:43 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:11:02 GMT
RUN boot
# Wed, 06 Mar 2024 14:11:02 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:11:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:11:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44496d713a839fdd0b47c7b0973155ed9bb317b54231c21b7337e12eb724bb83`  
		Last Modified: Wed, 06 Mar 2024 14:28:32 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba68b864bdd09b38ee41fc74f8e608f5a75391a3e05520fee514e6d48cff58b`  
		Last Modified: Wed, 06 Mar 2024 14:28:21 GMT  
		Size: 3.5 MB (3498227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af078512ae21e2c0b75a6ba8ac8a4fbbb6d7ba93a53d5f265cb7e2a7c355a8`  
		Last Modified: Wed, 06 Mar 2024 14:28:24 GMT  
		Size: 58.8 MB (58820359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0159d8784e4c5b5c49a898875b5a7b9170886f5c16ea0986252b0ace722beb6c`  
		Last Modified: Wed, 06 Mar 2024 14:28:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:609db4795898a81584570227410ca8a9b248547c37f3d49a1e50504ca8df7093
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4554058dda5dad05f98ea0901fac4b9b49b810f2ed65f95f54455c3443004ecc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:53:54 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:53:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:53:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:53:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:53:58 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:54:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:54:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:54:20 GMT
RUN boot
# Tue, 12 Mar 2024 01:54:21 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:54:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:54:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc56412027ee59e7ee15cd13a8ab482381595108513644a75ffc9f30cd96cf7`  
		Last Modified: Tue, 12 Mar 2024 02:09:01 GMT  
		Size: 143.7 MB (143720928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0842ba81f9e69a761ad47903886e7ac56ab3068441e0a83fad72b2222c21b7a2`  
		Last Modified: Tue, 12 Mar 2024 02:08:52 GMT  
		Size: 3.3 MB (3322111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504ab80642f8b9212b8452dedbcf0737d5204542737c631e138852d53c6a4d8`  
		Last Modified: Tue, 12 Mar 2024 02:08:54 GMT  
		Size: 58.8 MB (58820580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6378f5b1c21efaea889f2e9252865654472c312fe1896d46083bf7400e4f1f`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
