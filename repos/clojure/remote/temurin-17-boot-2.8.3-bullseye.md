## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:283f8142112d7dea01235b739564d563b4369e7ad2a6bac6ef64bba2bbf8e7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1309681f4de0185b5d9b607565df7d1462dac98f8e32da6bd5263d62b473346b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261171398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aece99fa02b8198e5811b30c7fe22f7b7145eafb2803bfd17d203844d2cbab9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 11:03:58 GMT
COPY dir:634e6dc1071a76d830a1c58e20efb6c42c0d02beb44d214374fc7817b69efa15 in /opt/java/openjdk 
# Tue, 16 Apr 2024 11:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 11:04:00 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 11:04:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 11:04:00 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 11:04:06 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 11:04:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 11:04:06 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 11:04:24 GMT
RUN boot
# Tue, 16 Apr 2024 11:04:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 11:04:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 11:04:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16199a1d15aa77000652c9bf81de1324ecf36eb5aad0f612c186f29d6b572226`  
		Last Modified: Tue, 16 Apr 2024 11:22:34 GMT  
		Size: 144.9 MB (144893099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce8fe0a8eb80671e06122a4d04931baa96a7fe07c17b72cd26fe78be027fadb`  
		Last Modified: Tue, 16 Apr 2024 11:22:23 GMT  
		Size: 2.4 MB (2367305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5019bedfbff5f1f475b0e4c961afc758529bd304ba1b4431cf9dc342ee15f6`  
		Last Modified: Tue, 16 Apr 2024 11:22:26 GMT  
		Size: 58.8 MB (58820331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e14cb492ed37812d8b3f221cabc3b6ea821915d41f377dfc98928a195c57be`  
		Last Modified: Tue, 16 Apr 2024 11:22:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d213be22969d7e70338ce07e712caa3fd9a9931eb21fe68f88e67c5a4185b0e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258626835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07cd7b97ebddb6fd1ee4dadab5f5602902737e1e7cfca3c968872f2586d5b5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:41:00 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:41:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:41:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:41:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:41:03 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:41:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:41:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:41:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:41:25 GMT
RUN boot
# Tue, 16 Apr 2024 06:41:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:41:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:41:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c21b09d53fed41b7bd3ec1a4b9e920db379f3c64904afb6272b7efd4be7ad`  
		Last Modified: Tue, 16 Apr 2024 06:57:09 GMT  
		Size: 143.7 MB (143720948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55b41418faecec6a291850752037d35cbda6872d7b59c4b608d2f78bd7f309a`  
		Last Modified: Tue, 16 Apr 2024 06:57:00 GMT  
		Size: 2.4 MB (2355803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb407eb11be28e79ad362e530d569f7e79118049c11ae2e38825a99c588ac32`  
		Last Modified: Tue, 16 Apr 2024 06:57:03 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94697b86ad7e57083a16dd6a3b6864d59ebb51ad4d3009200931c1d435617c5`  
		Last Modified: Tue, 16 Apr 2024 06:57:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
