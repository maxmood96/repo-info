## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:8758afe79b6b161816b2b3635f8df21fd614224cf3467bf6322a1de880ec5ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a285551c6d04756378bbc95fe13d1904113e0d898f6b5a6417c6ca2e5b98ca2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed805b9149618bec78722ecf1da2fd9268d02505437c8a8e4e5c872c43176010`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:15:53 GMT
COPY dir:95f5b1bebae6bba6ca961eb10c7982ff1efe410622f69bd5e96558adc723ec83 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:15:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:15:54 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:15:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:15:54 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:16:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:16:01 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:16:21 GMT
RUN boot
# Fri, 16 Feb 2024 05:16:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cb3bc6e5d615589c9a5580c68f6da3b1dd0b87bb430e1db31a35d9ed769d25`  
		Last Modified: Fri, 16 Feb 2024 05:33:18 GMT  
		Size: 145.3 MB (145270844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27429a16d63be4f0730790256d3fe90d55ff9122c5d1d5efff4d142183a7aede`  
		Last Modified: Fri, 16 Feb 2024 05:33:07 GMT  
		Size: 1.1 MB (1077683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b120f5a844658ba7de4d0e28d7310c5aa6a34d54508b47f49bedcf0f321334b0`  
		Last Modified: Fri, 16 Feb 2024 05:33:10 GMT  
		Size: 58.8 MB (58820620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c7d9f0ca7a40d45b3d49b147ef097718ac47558e71e9cb965feeed33fa25b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231962998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e32694fe6b899a9976559f958d8a71b141e8e4cfd464383d13ccc30b544816`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:53:34 GMT
COPY dir:0419d7bc8c60addce41546593a3de80cd02ee9001351a641f9cf113402b5fb20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:53:38 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:53:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:53:38 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:53:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:53:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:53:43 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:54:02 GMT
RUN boot
# Fri, 16 Feb 2024 07:54:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d9cdd9da40b4d7a8153b1476d37576a3e0ed4b006be09f0d43e22e4886175d`  
		Last Modified: Fri, 16 Feb 2024 08:08:25 GMT  
		Size: 142.0 MB (142006403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f46edfa14fde2a9586d618b69ab3594156391279c8d53996bbbe60b2d065bc`  
		Last Modified: Fri, 16 Feb 2024 08:08:16 GMT  
		Size: 1.1 MB (1065001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135ee3815d7231e261813fb4f26f3f0c24a2630e7fb8365cc1845abe714e18bc`  
		Last Modified: Fri, 16 Feb 2024 08:08:19 GMT  
		Size: 58.8 MB (58820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
