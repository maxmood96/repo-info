## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:55e63938c64b6470f8e66e096db29ce6ca335351fa7a63508cb830b7165c7d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79766f0a55cebefd7217df34fb8c8b8117da56844dab5961399f195738f90649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b24805d1399269a40869551749d64f51b8780d57f5bdf18c5dcaaca0d5dab7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:14:44 GMT
COPY dir:95f5b1bebae6bba6ca961eb10c7982ff1efe410622f69bd5e96558adc723ec83 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:14:45 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:14:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:14:45 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:14:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:14:52 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:15:13 GMT
RUN boot
# Fri, 16 Feb 2024 05:15:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a53aeba54fdd5153fe42a06d8fd3ed13f2567d05193d4f18dcf04eab26cd55`  
		Last Modified: Fri, 16 Feb 2024 05:32:34 GMT  
		Size: 145.3 MB (145270854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3177941390167aca242e14272a7c5235b5ed6d89c724bdea7fca607cf07c2`  
		Last Modified: Fri, 16 Feb 2024 05:32:23 GMT  
		Size: 3.5 MB (3498182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071addbe226f029228a7ff442308df9482b13e1fb4b0404e335382e8f27635b7`  
		Last Modified: Fri, 16 Feb 2024 05:32:26 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a485c8b1297998cb5811ffa786318ff862a3b39d2b5ee95f6df61a856394ddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233305390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da128eb636f7f7fa5ddb15846ad77357039624f101a63b73eb34bda3f5e62741`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:52:27 GMT
COPY dir:0419d7bc8c60addce41546593a3de80cd02ee9001351a641f9cf113402b5fb20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:52:30 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:52:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:52:31 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:52:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:52:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:52:37 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:52:56 GMT
RUN boot
# Fri, 16 Feb 2024 07:52:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a34a9634fccc9a0ab5161b69db53462e2f5dc319edc711c6872c6b1b7e9e5d`  
		Last Modified: Fri, 16 Feb 2024 08:07:50 GMT  
		Size: 142.0 MB (142006423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064e2870bc6f8d2e361a2e4d4aac397b3d4c389159fdcc74e59a7d41ed45bd28`  
		Last Modified: Fri, 16 Feb 2024 08:07:40 GMT  
		Size: 3.3 MB (3322100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c8f4ec45b36a46d8fe95ad4aa737a55d613c0514b8f945fd9716640c8d359d`  
		Last Modified: Fri, 16 Feb 2024 08:07:42 GMT  
		Size: 58.8 MB (58820504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
