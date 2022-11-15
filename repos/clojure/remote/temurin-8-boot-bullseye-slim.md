## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:941512b69da8abb85f4305c130feb70a7135db779c20ff587b744d902225d89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f72bcadde0a875b9d52b1c58813aafd8d42d1bf39a4dce1acaee77c67a3618ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194850190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea51d8c52e5c03d48bb23199ee643d8e4e6cf22618b30e8fa501ff56d03a87f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:06:16 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:06:17 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:06:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:06:17 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:06:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:06:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:06:23 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:06:42 GMT
RUN boot
# Sat, 05 Nov 2022 01:06:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44770319b57989fffd145e48755d83843c0b9ca57cc5daa5ce8fd5ff705e3972`  
		Last Modified: Sat, 05 Nov 2022 01:22:08 GMT  
		Size: 103.5 MB (103530625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30eade7249c1bd2c0d55793f605a28c71bea51fdcb11574df6d838c31363da`  
		Last Modified: Sat, 05 Nov 2022 01:21:59 GMT  
		Size: 1.1 MB (1078958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc7586f2f6004940e3b87db110ed97734f8ad196a778a836822f8a407271850`  
		Last Modified: Sat, 05 Nov 2022 01:22:02 GMT  
		Size: 58.8 MB (58820569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

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
