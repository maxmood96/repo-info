## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:e41d713a5b95cc5152ddb593f39c89b5bfc1ec1645af165c186e06d07ee2f2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0f8232421550244a97028f97b70072ab42ab3f73f88c4eb28f3d6740d4d64654
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236584285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9994d9b62ea52c959aeccc16ec7b544ce1a82b2abb1efec3245910a99f99d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:13:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:13:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:13:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:13:52 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:13:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:13:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:13:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:14:17 GMT
RUN boot
# Wed, 17 Jan 2024 14:14:17 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c490024f647e1f5426afd18bcea5b83305c1dcde2948ccad2babc1faba786a5`  
		Last Modified: Wed, 17 Jan 2024 14:50:02 GMT  
		Size: 1.1 MB (1079464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e37e05506b25cca1a60e44c83844ae5153a08b1b82941f9b61535522f0d689`  
		Last Modified: Wed, 17 Jan 2024 14:50:05 GMT  
		Size: 58.8 MB (58820434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2964d7961ba97bfd4733c110b9b76e4e747399eed85d6efa2edceab6fbbb6b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231953511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84fac49aaf49740a67e5a8ecaf69643accca948f48edd4a1488fca704960161`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:23:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:23:58 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:23:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:23:58 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:24:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:24:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:24:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:24:19 GMT
RUN boot
# Wed, 17 Jan 2024 09:24:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599b6594ad68158d2003bca5a0c08b3a48ab8592ba25a41180291ebcb79d1308`  
		Last Modified: Wed, 17 Jan 2024 09:39:00 GMT  
		Size: 1.1 MB (1066814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a9375d5bdd628c9b0a960ab73f48c4cabebd80ff07f2550fe47cd25bd0430`  
		Last Modified: Wed, 17 Jan 2024 09:39:02 GMT  
		Size: 58.8 MB (58820631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
