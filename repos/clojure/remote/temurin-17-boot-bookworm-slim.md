## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:602906184bf7aaa1727081ca2bae28c77a6a62291d3f2cc1b84e5031174e6227
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
$ docker pull clojure@sha256:6b9cf850687017acc2f806d73c7501a20c16b941cf5b5c7b655b916e61a76a1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a87a842835600f6f83e83e3bf29b158115cfa6331356efcb578605e0f443e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:23:20 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:23:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:23:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:23:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:23:24 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:23:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:23:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:23:29 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:23:46 GMT
RUN boot
# Wed, 06 Mar 2024 13:23:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:23:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:23:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8baf922fb4d908d3a3587a0482690306454d53960171f76f1db75d33164d944b`  
		Last Modified: Wed, 06 Mar 2024 13:38:15 GMT  
		Size: 143.7 MB (143720843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5984f85d78bac381ea261df1f4a96fb72cfc3b1ea873a94238b90b092e2f22a5`  
		Last Modified: Wed, 06 Mar 2024 13:38:06 GMT  
		Size: 3.3 MB (3322114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262e03ddcabf7fe29dc5b471a1c23b7ae3982a2da85f332b043fdbbe4a31dc7d`  
		Last Modified: Wed, 06 Mar 2024 13:38:09 GMT  
		Size: 58.8 MB (58820363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e2dc560a5cc5b487a9b75e01ae1b3c3254a54c8d2f3f9ebc050ac954f2db42`  
		Last Modified: Wed, 06 Mar 2024 13:38:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
