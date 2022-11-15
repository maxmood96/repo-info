## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:0c2b12c11daaba37f0f78628239c4552d75428190aaa00e9cc895cd5ecfa44c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5686a5541043da1eab304852425528a713c80b01cc53ee7a9c7a4d7034ac9250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194842733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d8917217d094fa55f88b8369de26494f0b0c254aa83d26153fbd7a31d89c53`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:51:10 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:51:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:51:11 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:51:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:51:12 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:51:17 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:51:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:51:18 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:51:37 GMT
RUN boot
# Tue, 15 Nov 2022 17:51:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05516bbc03e0cd1f73865c9a4a41f11df1cc12062f6b425c2b18212f6025faf6`  
		Last Modified: Tue, 15 Nov 2022 18:06:48 GMT  
		Size: 103.5 MB (103530607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc494fa2e667caf7061684f5789337447d57fe0f5f5b4ab5f909f24bb312cfb`  
		Last Modified: Tue, 15 Nov 2022 18:06:39 GMT  
		Size: 1.1 MB (1078970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40640266ac2fd39b65d63f002f633c07dff80588ab17e1755e8effe03414726`  
		Last Modified: Tue, 15 Nov 2022 18:06:43 GMT  
		Size: 58.8 MB (58820526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ed0a0e78d5816d30001bb47374495a9669d92777139161fa24fcbdd05c7d5a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192573923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5650327126b8df8fc797d27b90f905e97c5c71fd9c9a7f9951c563cef9a817`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:49:25 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:49:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:49:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:49:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:49:27 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:49:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:49:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:49:51 GMT
RUN boot
# Tue, 15 Nov 2022 05:49:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801358ff5f2e42bc914ccad34f344c2f79c73c7246811cecac0e1e3502c74b1e`  
		Last Modified: Tue, 15 Nov 2022 06:01:53 GMT  
		Size: 102.6 MB (102626554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a53f0d495109885a3ea1b1748defefcb52711c89000f36cb08dde9b8a1a2c`  
		Last Modified: Tue, 15 Nov 2022 06:01:45 GMT  
		Size: 1.1 MB (1066322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86838aaa4314692e5b65ecbd12b83cdaf9792a69dbebca546cca259169d89f41`  
		Last Modified: Tue, 15 Nov 2022 06:01:49 GMT  
		Size: 58.8 MB (58820442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
