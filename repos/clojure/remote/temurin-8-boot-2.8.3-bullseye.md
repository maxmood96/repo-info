## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:c929a81faa00905f37406f9d3cb5f5d5c341cabd6f7b0f051b1829e01bf908e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dbe2d249be372e463644f5ba8b3badae9daad991e217b2712d504684a2f9f9ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170863554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7713ec79fafd260befdfc92adf3952d93d98e4b83e90da406d510dd809906ad7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:40:43 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:40:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:40:44 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:40:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:40:44 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:40:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:40:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:41:15 GMT
RUN boot
# Wed, 01 Mar 2023 07:41:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c09a39e83163f7497d4ee9341a8db18267bc11c708c7befcd6e06c90de109bf`  
		Last Modified: Wed, 01 Mar 2023 07:55:03 GMT  
		Size: 54.6 MB (54635557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18783cdbcbe6d8f4ed6b962acff8f4d4d8ae5bf53cc74501eb189a23bc96c3f`  
		Last Modified: Wed, 01 Mar 2023 07:54:57 GMT  
		Size: 2.4 MB (2361576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7689ba28aa4dfe7aac348d9c78ab85df83f6e7187538a6789f3fb28957eea5f9`  
		Last Modified: Wed, 01 Mar 2023 07:55:00 GMT  
		Size: 58.8 MB (58820499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9304542338b8459424bb495cb9ad116fad803d833dd7ee58946e7565c2d3086
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168602811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646bf220b20e25f3cf3a3534ab5c99690975b8576ff945bb5a12834fe834e8dc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:01:16 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:01:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:01:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:01:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:01:17 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:01:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:01:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:01:23 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:01:55 GMT
RUN boot
# Wed, 01 Mar 2023 03:01:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583ae59cedb3d06068194d612b2461bcf03fea5f1f8704c8a9987f693705b0a`  
		Last Modified: Wed, 01 Mar 2023 03:14:07 GMT  
		Size: 53.7 MB (53727940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d45d2418b64eeb2773490dc3776397fc0b7b7a6edd7aee96b720a9d29e4c8e`  
		Last Modified: Wed, 01 Mar 2023 03:14:02 GMT  
		Size: 2.4 MB (2350919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336b623dcf2b05cc69746e8ace440c8fd27ce65367f12dd186e23d2af3f3f14e`  
		Last Modified: Wed, 01 Mar 2023 03:14:04 GMT  
		Size: 58.8 MB (58820737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
