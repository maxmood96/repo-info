## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:5e8184bebe933d1e66ebb43a7f98b262179f6fe145fa6e02e1ef67bad01e14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b10d4b3a73297aec1fb9cf496efc9e4f109462c1f907f16fd90a66dbcf2025d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289770310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df862acbeac2f71a7884e16c84b6c08f1fece56aec8755424045274b41e5cd68`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:09:02 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:09:03 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:09:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:09:04 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:09:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:09:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:09:09 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:09:27 GMT
RUN boot
# Sat, 04 Feb 2023 14:09:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e30efc225d57cd9e62995f1d0420aa7db3d1ee71af748e8f579251b162ca44`  
		Last Modified: Sat, 04 Feb 2023 14:22:08 GMT  
		Size: 198.5 MB (198475569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7db36cf7ce1f67a6b2beb439b7448ee3c7a32e970c4a84f830237cc755a86a4`  
		Last Modified: Sat, 04 Feb 2023 14:21:54 GMT  
		Size: 1.1 MB (1077373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92592624f2357f9d605c9d51606969e5088db6667265ef0d1270bb51e321d92`  
		Last Modified: Sat, 04 Feb 2023 14:21:57 GMT  
		Size: 58.8 MB (58820449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7838f5189c3abc036f946723470e5b607e4bd35aa9de148183327db0a88ad3a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285170226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355b7ae0337ad1edac951b563c4fd1ad4ba5ce03ba645b4ee3920250874fc00c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 08:45:37 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:05:46 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:05:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:05:46 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:05:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:05:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:05:51 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:06:09 GMT
RUN boot
# Sat, 04 Feb 2023 17:06:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6cab391fa4078e01d740a8b8f1dd48285df4066fdd71923d0588beb66395ce`  
		Last Modified: Sat, 04 Feb 2023 08:47:42 GMT  
		Size: 195.2 MB (195240323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9949e8c7efd1adb49a65d4d9d8114833670db72e7cc261e96fab8761ae058d39`  
		Last Modified: Sat, 04 Feb 2023 17:17:00 GMT  
		Size: 1.1 MB (1064643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eea79a9d603cba9a2db2fed7303351c0fb65ff7acd1b01685979aa01b20440`  
		Last Modified: Sat, 04 Feb 2023 17:17:03 GMT  
		Size: 58.8 MB (58820468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
