## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:d215019010009f91ca923a103601b235f05681bc918e87f2948a869b3a8174b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f9382f7af25e6092c7636460cd3e5e34be6c3dd7937446c8209942a8aaa17a4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314703401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d7cf8d73e9ee28ef0373f35c7bbb2496d7359e2a1a0775a27eb6808872f27`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:04 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 08:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 08:55:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Mar 2023 08:55:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Mar 2023 08:55:06 GMT
WORKDIR /tmp
# Thu, 02 Mar 2023 08:55:14 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2023 08:55:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Mar 2023 08:55:14 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Mar 2023 08:55:31 GMT
RUN boot
# Thu, 02 Mar 2023 08:55:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5820d2bbbd2970cc90facbdcbef131608a5ed716d56ff1bba2614ecda317ebb4`  
		Last Modified: Thu, 02 Mar 2023 09:12:31 GMT  
		Size: 198.5 MB (198475399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563be3ca349543601b9f6743b79a669939587105d7d79aae78ec04789c64ef8`  
		Last Modified: Thu, 02 Mar 2023 09:12:17 GMT  
		Size: 2.4 MB (2361682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f447674d3b3a75db94688d467ee1a5500ef0dd49cccb1fe94d9bc8facec972`  
		Last Modified: Thu, 02 Mar 2023 09:12:21 GMT  
		Size: 58.8 MB (58820398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c011b8389eebec068d6e96fbcc08f898aefc33ca509f32a3ce3a127b14e2455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310117314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c9ae61770e154b8f59437bbd3f908ac422044ae2a2874fabde921f80c9317`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:49:40 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:49:45 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 04:49:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 04:49:45 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:49:52 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 04:49:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 04:49:52 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 04:50:09 GMT
RUN boot
# Thu, 16 Mar 2023 04:50:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78a05cee032288c91b44a6ea7c2e0389feb35b08ef573e2bd5677647987ef0b`  
		Last Modified: Thu, 16 Mar 2023 05:04:28 GMT  
		Size: 195.2 MB (195242536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe53f2c0fe569dd72bf3104330e84ac791fdc3f1d3957ef8ee632b92e9f0ed3`  
		Last Modified: Thu, 16 Mar 2023 05:04:17 GMT  
		Size: 2.4 MB (2351050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7b0d5873950b10c6f99fc4044958e0fe77a4db7c39e8af41130a9cf11a46a4`  
		Last Modified: Thu, 16 Mar 2023 05:04:20 GMT  
		Size: 58.8 MB (58820513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
