## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:55ab98858f4e930a30b42320c0ff5ef5a2339ebea7fb9248e67f836e97dde4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:391bdba6ec0f53b0a407f5df906b9f0bb694f3f2209d73f1e03e4ea194124b59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236743615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab0bb129b805322c7ad7336daf2561c015bf3f78969e0bff78491e4c14b5583`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:10:34 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:10:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:10:36 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:10:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:10:36 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:10:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:10:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:10:42 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:11:02 GMT
RUN boot
# Fri, 02 Feb 2024 17:11:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575fad5380f55c159ccfbe24fb0dca8cc435788398d5e90f186fbe5108ff4842`  
		Last Modified: Fri, 02 Feb 2024 17:31:23 GMT  
		Size: 145.3 MB (145271007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264cc7610130b11cf45d7ecce29b044cb05a21186143b824ed47d58b53b0050b`  
		Last Modified: Fri, 02 Feb 2024 17:31:12 GMT  
		Size: 3.5 MB (3501697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53d685f90f7a5a9ce47b0ba01052dbbb147e4fef979e8af7ac716c4ea515796`  
		Last Modified: Fri, 02 Feb 2024 17:31:15 GMT  
		Size: 58.8 MB (58820446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1939f2bfaa830d01d36b03ef1db05261cbafa1c3848b60665edfb1e49f367d8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233332644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4330d8c9d6976572d3e40fdb7ddc01079630da00ce29fb682cca3fab10e239`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:20:17 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:20:21 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:20:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:20:21 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:20:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:20:27 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:20:45 GMT
RUN boot
# Fri, 02 Feb 2024 08:20:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00498bb373c7ab039d3c50e9ee01de46ff61000a6e4866749566b453c520b9fc`  
		Last Modified: Fri, 02 Feb 2024 08:38:25 GMT  
		Size: 142.0 MB (142006400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73e7076b7d676d139af65423abe12b95a266f5aa9e61655448347858d9f6853`  
		Last Modified: Fri, 02 Feb 2024 08:38:17 GMT  
		Size: 3.3 MB (3324937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0878c1d19106151108b8a6db9441a4b8ccd79abea0b20a5f93cbe784f7efcf56`  
		Last Modified: Fri, 02 Feb 2024 08:38:19 GMT  
		Size: 58.8 MB (58820475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
