## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:c23d5bd8dab303531f463bc2db9c750ec6da74bdd997cbbfe0eeea7445a682f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:63cd762b617b3ddc66af58ebf3f4f777696b9d6d0ce1b6792a91ba6e202a8faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259171043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b181171aa2391337ee7c60f1bbe11cd175cc2e13d0fcde07940d6996f2dd8442`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:16:57 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:16:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:16:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:16:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:16:58 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:17:05 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:17:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:17:24 GMT
RUN boot
# Tue, 12 Mar 2024 06:17:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b85a9fcbbf5a0a052848635659c63d396693d85528a35da1c265afa9132de20`  
		Last Modified: Tue, 12 Mar 2024 06:37:22 GMT  
		Size: 145.3 MB (145271167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b919f1aa1c5fff387acb422ab94d65d87b7bce78d23d669c1e38ed6a82104c`  
		Last Modified: Tue, 12 Mar 2024 06:37:11 GMT  
		Size: 5.5 MB (5527024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df3ac102ba8843d0074cc4208f7e75aa9b38a21ee8324114ae4e5e868a129f`  
		Last Modified: Tue, 12 Mar 2024 06:37:13 GMT  
		Size: 58.8 MB (58820656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de37179bb7d92a2563b9b2f2bdb95d740f5add4456bb9cbc5495e4f7cd70ae60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255769173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b6a934e459e254edc69d267bbb7888f8a29bba0f02e3117d224f53311f0aa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:48:26 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:48:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:48:29 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:48:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:48:29 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:48:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:48:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:48:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:48:52 GMT
RUN boot
# Tue, 12 Mar 2024 01:48:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efe74819c45ca24d4fb4cc6018bb42a3ff6ee6fc375497131a8630dd1800dbb`  
		Last Modified: Tue, 12 Mar 2024 02:05:41 GMT  
		Size: 142.0 MB (142008468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddedf702d9a9d86f31cddc2e2a634f3eb354d3b8794cf36813ec5c829e800a0`  
		Last Modified: Tue, 12 Mar 2024 02:05:33 GMT  
		Size: 5.3 MB (5349361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e3f58cf45d0d3449fd3b0fde13f079884d2c89cd95866d8940468b126e9d2`  
		Last Modified: Tue, 12 Mar 2024 02:05:35 GMT  
		Size: 58.8 MB (58820360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
