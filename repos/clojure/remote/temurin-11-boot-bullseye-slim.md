## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:6a8d2e5f156ce01a9553d82af19decb4f563d8d12668294fe9167b7016beaac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ca7fe1dc83cf80545bfe9c0d64dbc32f4fdae2ecc7ecdfbe683602dcd0a9f47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a24768b21e23a2d84ff4967d4b19f50f25520518682eadb43672e541081c538`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:44 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:59:46 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:59:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:59:46 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:59:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:59:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:59:52 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:00:10 GMT
RUN boot
# Thu, 28 Mar 2024 03:00:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765e80b34419cc4d75a074af22d808e72a16040aef302be6b97f83f87c3cea68`  
		Last Modified: Thu, 28 Mar 2024 03:20:12 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd5998556eee427dc0ce457543ff6eca088bc940cfc3c75591c9e7d93821d4`  
		Last Modified: Thu, 28 Mar 2024 03:20:00 GMT  
		Size: 1.1 MB (1077705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1a40ecb5418168b5c7cc3cf7edeeae7decfe7bc12d3ac7c9a66c9f34b7795c`  
		Last Modified: Thu, 28 Mar 2024 03:20:04 GMT  
		Size: 58.8 MB (58820516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f705cf8feec1492d0b44d0dd6d57dc1448614b0b1d75ef6f35b65a390f080bbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231968097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a6b1062f5e4e9d4c470e04e7fd0485c0069d1a66068d4a69c16d262e7d1d4a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:44:53 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:44:57 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:44:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:44:57 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:45:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:45:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:45:20 GMT
RUN boot
# Wed, 10 Apr 2024 04:45:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9f0cb0cf9f2a91955c0e3d73d286f38239bde001a4ae6b8442625ab39f1197`  
		Last Modified: Wed, 10 Apr 2024 05:02:10 GMT  
		Size: 142.0 MB (142006303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed0d0514e5ab81e67fcbf35cc867cceacacffbe9e831c35778350c44721e341`  
		Last Modified: Wed, 10 Apr 2024 05:02:01 GMT  
		Size: 1.1 MB (1064987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b882d3d22c5bbc456b9d394974cc4d68ffb6a2ce12fbfd390326b703914fe44`  
		Last Modified: Wed, 10 Apr 2024 05:02:04 GMT  
		Size: 58.8 MB (58820501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
