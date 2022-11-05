## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ba996074b1e401d73b93e41cc5cf146fe466b21d2a39c82cc5c5f575ea2de8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eabc26356ffed9e1abefc6f4e58bef14cc413194c71a9bff1c4552e4fc87eadf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289775379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f30022bc588fc9f257fa8af301151da054a857d05a1f61d2555553fa5c1a6e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:12:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:12:15 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:12:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:12:15 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:12:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:12:21 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:12:39 GMT
RUN boot
# Sat, 05 Nov 2022 01:12:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a21464f5b990fbe757683a1df3aba4ce54599f4217a365b7323347a647e028`  
		Last Modified: Sat, 05 Nov 2022 01:26:08 GMT  
		Size: 1.1 MB (1078963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de134961dd269e1e4671256cafc08f4cc13f3333e035a8078073650b38bd002`  
		Last Modified: Sat, 05 Nov 2022 01:26:11 GMT  
		Size: 58.8 MB (58820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b49843ec23caa7af99691b0868414ebdcbedf08e317553b4cfc2ec7061e64fd4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285151780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58c1a02c0798d06a6512790703fef4ebc4652bf1e462403da7b54170dbb9141`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:12:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:12:53 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Nov 2022 23:12:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Nov 2022 23:12:53 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:12:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:12:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Nov 2022 23:12:58 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Nov 2022 23:13:15 GMT
RUN boot
# Fri, 04 Nov 2022 23:13:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fa156b4c13e0f25bced9f528ade179440b7a8b977a9f98d88412436e544435`  
		Last Modified: Fri, 04 Nov 2022 23:23:24 GMT  
		Size: 1.1 MB (1066302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348fb91b9ac4916d86d1b523d412a9527f301113c201f527a06a9533c9c440ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:26 GMT  
		Size: 58.8 MB (58820479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
