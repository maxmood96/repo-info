## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:73172df3136b28d9fe782db73474b74c74bb33f2cac401b222da52212b0e42b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:201ff80fe80e40048f019b1c75e1756fcd1a32f03186ef52065491526d831e04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258783470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6e94f6288b057756606ad1da72dd490d84adc0290598cab87ed8e8dfa88bd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:03:43 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:03:44 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:03:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:03:45 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:03:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:03:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:03:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:04:10 GMT
RUN boot
# Thu, 11 Jan 2024 05:04:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:04:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:04:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108338e55df135d6bc601717541883bf916e61c490583967476dc73e4809007f`  
		Last Modified: Thu, 11 Jan 2024 05:21:08 GMT  
		Size: 144.9 MB (144873964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e4081d92940e3fca5b00e0f1d7256174ddaadf12eef4e9949796bcd4675781`  
		Last Modified: Thu, 11 Jan 2024 05:20:56 GMT  
		Size: 5.5 MB (5527004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065baa300952c92770403cdbd7fd43766f2d5b2a8fa05c21f20c656a2bb8c774`  
		Last Modified: Thu, 11 Jan 2024 05:20:59 GMT  
		Size: 58.8 MB (58820612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe61f6f48cc86dc0405fa9770602e882e7769cbb2b280e9e8ec9b3e0bad8a8d6`  
		Last Modified: Thu, 11 Jan 2024 05:20:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3ab0a72563be74cd86ad1b70d39f8760b5c72456bd95a070dc4a2eb31051284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257443944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2fdd4f4deea2a290f5e2f0cb957d4cc393d0d7af1fc3f260e97968cfa272d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:03:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:03:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:03:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:03:39 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:03:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:03:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:04:00 GMT
RUN boot
# Tue, 19 Dec 2023 07:04:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:04:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:04:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c921ebaa0e3aa9234b54378bc303467ff63a194e02c492c4836def5239e7f3`  
		Last Modified: Tue, 19 Dec 2023 07:18:48 GMT  
		Size: 143.7 MB (143681701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9962100de87eb14ef7d23fdf549d3ccab8cba3bfb115ef84a168c84a74f96b`  
		Last Modified: Tue, 19 Dec 2023 07:18:39 GMT  
		Size: 5.3 MB (5349306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05677dbe403a6241d072327d491e1c703e109e4b080630655f98d1ea6a07f5c8`  
		Last Modified: Tue, 19 Dec 2023 07:18:41 GMT  
		Size: 58.8 MB (58820278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddf1407d793a8556f027f0c12e1ba8e09dc9c5558d333c3d2e9eda0e41bb8c4`  
		Last Modified: Tue, 19 Dec 2023 07:18:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
