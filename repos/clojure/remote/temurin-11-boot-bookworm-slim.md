## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:ed4bdd8b324871603feba555ed0085524f68a9546810e9e476f5df15b3a68e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6815ce4f4b35de175d827543f9567abe42403ec8c8f5d8b3cb00851e0cb33675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18792b2541db0b1bd4155336b5bb0790af1fc75bf28087268f21fbffb0936ee7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:53:20 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:53:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:53:21 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:53:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:53:21 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:53:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:53:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:53:28 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:53:48 GMT
RUN boot
# Tue, 13 Feb 2024 01:53:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23518d57bf40c348bd9c1e85b43b7e3f4452d4943541bd697c10200fd700cdee`  
		Last Modified: Tue, 13 Feb 2024 02:13:12 GMT  
		Size: 145.3 MB (145271038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9530c6da0401939af8e9e86f0bcc84b7c7f876e564d497ba439051cb456b4b`  
		Last Modified: Tue, 13 Feb 2024 02:13:01 GMT  
		Size: 3.5 MB (3498147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199eab73029e363e7b5e7f6dc5d83c73fde7788637884cc1c72db68e776ab4cb`  
		Last Modified: Tue, 13 Feb 2024 02:13:04 GMT  
		Size: 58.8 MB (58820549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80b1fd0ad9c6d1e2dcfff50682342a5f35b353214511b9e2bb4cf9d609369e92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233305371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575e25348fb9afa7964ed7f08d26509da75829716db3b10aac4f9337c954b9e1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:00:02 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:00:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:00:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:00:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:00:06 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:00:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:00:11 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:00:29 GMT
RUN boot
# Tue, 13 Feb 2024 02:00:29 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eed5a2d468c6ef35857ba2b647fa12e7a17a3753b2e34c9d347ef5423087e82`  
		Last Modified: Tue, 13 Feb 2024 02:17:28 GMT  
		Size: 142.0 MB (142006403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ad3cca02814a689d754f4b1d29a3c4b25b0b9665194f9e7b7daa51bcc18acf`  
		Last Modified: Tue, 13 Feb 2024 02:17:20 GMT  
		Size: 3.3 MB (3322109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950e7bdb5bd64502a1d54b1446398a9a38076b25311bc96a94afc132025f507e`  
		Last Modified: Tue, 13 Feb 2024 02:17:22 GMT  
		Size: 58.8 MB (58820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
