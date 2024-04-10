## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:be9ff53a95160d6b661ed6f8c01c6b0e34e0faacf4632fa00e14e92ecd667b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f64543d161d4867fc8f5792c9a811ebce9eb6f94f71490fbe21494ea13ac9791
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236597358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47df8bf9760576299fc9250edd3ce2ad5089b103736a4dffb1948082dca71efe`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:24:24 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:24:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:24:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:24:25 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:24:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:24:31 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:24:51 GMT
RUN boot
# Wed, 10 Apr 2024 06:24:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c9a5d9034646068efcee2e089ff8f21c4e19e7eb8efdc59ac64d220c0f8fd`  
		Last Modified: Wed, 10 Apr 2024 06:43:23 GMT  
		Size: 145.3 MB (145271242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f8765b84d80d44dbe1d424a317b093484c58b022774fdb92f3fa0af165ee75`  
		Last Modified: Wed, 10 Apr 2024 06:43:12 GMT  
		Size: 1.1 MB (1077743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393f736d66210f9ef718864e8b60d3c5b72b30864970f4802182a3716fe1ecbb`  
		Last Modified: Wed, 10 Apr 2024 06:43:15 GMT  
		Size: 58.8 MB (58820635 bytes)  
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
