## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:36d641a5475c20cf206161d0ab2407e3f7c3fe341e1958a69ef4c8eda6856c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7b29ce31ad5d81d91cb125f195ee961e100f27d8af22f48b0e8a9f2f64dde72e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314703841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0c9a7073da83be5e4fe910d6aeaeb126bfa4a0bec96266ba4d94da8506a8ab`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:33:47 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:33:49 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 07:33:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 07:33:49 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 07:33:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 07:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 07:33:56 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 07:34:14 GMT
RUN boot
# Thu, 16 Mar 2023 07:34:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2dcd1e2bf77431590203ffdf654085ce8aca2e30f82f7499367035ec790dab`  
		Last Modified: Thu, 16 Mar 2023 07:50:28 GMT  
		Size: 198.5 MB (198476007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a496f73bfd74f45074b488b9fa3b25a5ba9bbb8a63bee2ca63728146d5bef58`  
		Last Modified: Thu, 16 Mar 2023 07:50:14 GMT  
		Size: 2.4 MB (2361576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76287cce63c32c69cce1d42a2e88c018ea91bf2a86ea4a7ebec82f93ae8c7b1`  
		Last Modified: Thu, 16 Mar 2023 07:50:17 GMT  
		Size: 58.8 MB (58820336 bytes)  
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
