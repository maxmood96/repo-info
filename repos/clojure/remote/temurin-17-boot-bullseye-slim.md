## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:5ce9b67f64fb33ab4c9d9e65469e4ae6762e5cefeb3f691b86752ce1a79119e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f6330356ef071e54b0789afb3707315b38c343d4ad3be365dfd54bba10a094d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283748062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8db16886c2f17b6d521cce3282c9a83a028f5ed210c7a254e8648e9de51319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:39:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:39:26 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 07:39:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 07:39:27 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 07:39:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 07:39:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 07:39:32 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 07:39:50 GMT
RUN boot
# Thu, 16 Mar 2023 07:39:50 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 07:39:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 07:39:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea4011ce2130bbbb1a1ccc97329bab2c80bacfea05fda95f96f60058a86718`  
		Last Modified: Thu, 16 Mar 2023 07:53:44 GMT  
		Size: 1.1 MB (1077400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b5d0fcf5d254f187158fa7c319d82e910f30f716ff16c74b8f18daa66199f`  
		Last Modified: Thu, 16 Mar 2023 07:53:48 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87669f9f60dafc7e6ce956bf63e45daf5841aae8fe4ac3a1744e83289ba4df37`  
		Last Modified: Thu, 16 Mar 2023 07:53:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ae25ac04b70fbabedad5e9b3eb767dec691a02dd5a60c611a734498a4b63394
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3043e645c3bec33aaf9e0ffb0fec33e481588fb42b3a6d67697fabdce1981f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:54:38 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 04:54:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 04:54:38 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:54:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 04:54:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 04:54:43 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 04:54:59 GMT
RUN boot
# Thu, 16 Mar 2023 04:54:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 04:55:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 04:55:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a1b223a22b05354251d3adb4fdc76ca35504d86aae8a4dc6904b807a85549a`  
		Last Modified: Thu, 16 Mar 2023 05:07:58 GMT  
		Size: 1.1 MB (1064638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9f078ec28a0aa51b61b24648a97f635b93cdfb80bca151c1f291a61da089f`  
		Last Modified: Thu, 16 Mar 2023 05:08:00 GMT  
		Size: 58.8 MB (58820363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91aa8b2feab7a0635f471150716775ef24fc17bd099dc52bb5196a3d5c082d82`  
		Last Modified: Thu, 16 Mar 2023 05:07:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
