## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:214478aefd3c1a5b6951c89834c2d26d41e0af04909dfb76b7a8dea6f646aadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2eb1518d7d3c1fc81d821c0b0bab415a5b0a35803df7f61fddd6f5ac9d5f3206
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192577311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f285cfddf36ad73ff67e2188d0edfd3e64371803b1a592264bc4b0e7b813c523`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:07:51 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:07:54 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Nov 2022 23:07:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Nov 2022 23:07:54 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:07:59 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:07:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Nov 2022 23:07:59 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Nov 2022 23:08:16 GMT
RUN boot
# Fri, 04 Nov 2022 23:08:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f441f545c19bf4b3a8cf835cc8fa7a9a80b78c85b47e4cfa93821a1095caf`  
		Last Modified: Fri, 04 Nov 2022 23:20:16 GMT  
		Size: 102.6 MB (102626601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39b05f1a1aed4bedad29df1714be3445ed529ff312344d864e81bec1a3df6b9`  
		Last Modified: Fri, 04 Nov 2022 23:20:09 GMT  
		Size: 1.1 MB (1066367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3e2c35197842adb1db3a8a35a4db87f90c2f4a79c35d61d9d45ade0b0b3ca8`  
		Last Modified: Fri, 04 Nov 2022 23:20:12 GMT  
		Size: 58.8 MB (58820433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
