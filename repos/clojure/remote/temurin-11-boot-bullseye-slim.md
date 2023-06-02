## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:18f110c738a2bf6ae3e1691427b511506a6789a198c5e217eecbb0c996d4d8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:088ad39843c0fa80fa73c9b4b3d2936c93cc1b91f5339689ef41cdf7f9d45c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289851152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e1f80b7005be173b64b5bdba2c1f33aa5e3b29a74bf3482ed5c784e21e27a4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 08:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:07:45 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:07:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:07:45 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:07:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:07:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:07:51 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:08:09 GMT
RUN boot
# Tue, 23 May 2023 08:08:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201dd3455f2053b9124acb81faba9ffff5b1d3604565d926e1b9b982ad11c01`  
		Last Modified: Tue, 23 May 2023 08:17:02 GMT  
		Size: 1.1 MB (1077533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b5eea3e8f7d77cf5ac945d899b0f9f12b87e59c4ad7156280c6674777b920c`  
		Last Modified: Tue, 23 May 2023 08:17:04 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f96797759ef044f815c0b2385e059d24234c23b577a42732c25312dd647aaef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285262210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80cccc553ef7bb62fbfc895ee45618c4fae7114114b045e2980ea49cbbd6b6b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:15:37 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Jun 2023 01:15:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Jun 2023 01:15:37 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:15:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Jun 2023 01:15:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jun 2023 01:15:42 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Jun 2023 01:16:01 GMT
RUN boot
# Fri, 02 Jun 2023 01:16:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d705060af32e540e3870bf090f116cf7abd76feb0b7bcaec31543d72ffac63d7`  
		Last Modified: Fri, 02 Jun 2023 01:24:48 GMT  
		Size: 1.1 MB (1064803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3b20d45bfc0bf1105dbfcc77c029401abc024c73d693529288b2e07af1d1aa`  
		Last Modified: Fri, 02 Jun 2023 01:24:50 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
