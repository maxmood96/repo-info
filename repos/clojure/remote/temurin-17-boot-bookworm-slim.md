## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:4f72baa60cee331385c703cb1be10f317aac3f6cb3b348bd915f5b9300cf156e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:369608d470e0f2c06b469bf3147ad495c17d4a66266e0c9d33a0976a4b64e3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236335770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2272ea0651a2c0d311783e111791d6964543727d2c1d14f64a64e5a6d0e1b5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:21:53 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:21:55 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:21:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:21:55 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:22:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:22:02 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:22:22 GMT
RUN boot
# Fri, 16 Feb 2024 05:22:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:22:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954503457635d4984fa02d42e6a7fe96adb6ed04ec63bd42b5805de30d4f95ba`  
		Last Modified: Fri, 16 Feb 2024 05:36:46 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449ebc0c6a76c29d7255738fd71818f5f3dea4c48d505fc9303b6fddd74f39b1`  
		Last Modified: Fri, 16 Feb 2024 05:36:34 GMT  
		Size: 3.5 MB (3498232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af79193a04b622c6fdf9c9e31a22defc359174195b1515744657cc2632887630`  
		Last Modified: Fri, 16 Feb 2024 05:36:37 GMT  
		Size: 58.8 MB (58820485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e9461e98f139041fd674e57f6098a514ad2a8b355de775b6da74cbb5e6b63`  
		Last Modified: Fri, 16 Feb 2024 05:36:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24ff16e94c73c81ea2f6d5e8b8bff2cb3192b512babb5c633b89f6004f1dc9e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eda16a01b0249e3d3c333768a72461a8f404852bbf0e8b704ef7beab4b0736`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:02 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:05:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:05:06 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:05:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:05:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:05:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:05:28 GMT
RUN boot
# Tue, 13 Feb 2024 02:05:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:05:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:05:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fb8e9ed56ae2fc55656e8fa8952cbea195e103052380154edd3fd24c87552b`  
		Last Modified: Tue, 13 Feb 2024 02:20:52 GMT  
		Size: 143.7 MB (143720877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915046820c956ec16e620cf3aad3b235ede280c8f8a834b3e5e0440ae21d410`  
		Last Modified: Tue, 13 Feb 2024 02:20:43 GMT  
		Size: 3.3 MB (3322132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251cdd945d8ec8e48d339b6cd081e10ab0c4d2ddea57043643a12ff5d70b257f`  
		Last Modified: Tue, 13 Feb 2024 02:20:45 GMT  
		Size: 58.8 MB (58820319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253098e4053b024f291630f6d17dc066e77a7abd17fd245d623cd279e00505e6`  
		Last Modified: Tue, 13 Feb 2024 02:20:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
