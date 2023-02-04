## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:173ec10c9e81a7dae8ee952756539cb3c222bd0775187a0bebfdad46a117ca91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:350fa576461903d33320a34bb7cd933b4cbfec5bc39df361b7d70d7c8fd2eeeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283733260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03bbfba99db07889785075b78d63e2eaf4af902bd27ffac0d657ee45c2d7270`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:12:04 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:12:06 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:12:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:12:06 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:12:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:12:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:12:11 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:12:28 GMT
RUN boot
# Sat, 04 Feb 2023 14:12:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:12:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:12:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87fb4ccb46beb33988288373afc1f2c97de5052711ef02009468a1bea691666`  
		Last Modified: Sat, 04 Feb 2023 14:24:01 GMT  
		Size: 192.4 MB (192438215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ac2fedaf80b137c001138c4907957486f3c256afdba4ab3ff5984417ec0d4`  
		Last Modified: Sat, 04 Feb 2023 14:23:46 GMT  
		Size: 1.1 MB (1077362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cbf58807624048dcb79340a5ea74c13ccde92273f1f1c96ab6fda933d40e05`  
		Last Modified: Sat, 04 Feb 2023 14:23:49 GMT  
		Size: 58.8 MB (58820363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f98ad9b750da0a5fd657edbb9b69326f720670143be2466363873754fd9c3e`  
		Last Modified: Sat, 04 Feb 2023 14:23:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1dd9e7016b1abb28ca4cd460e9b44facde305a522a1bed6770ba83655c5b26b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281190677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1137aaeab171e09fadc1a324c927229fb21c169f896a8cec033d1b1d065f172`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 08:44:47 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:08:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:08:19 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:08:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:08:20 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:08:25 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:08:25 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:08:42 GMT
RUN boot
# Sat, 04 Feb 2023 17:08:42 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:08:42 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:08:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3e25b707e39161f4cf1a28cf3bd4a0ec84bd0f2c93f699a34dc6dd1715cd62`  
		Last Modified: Sat, 04 Feb 2023 08:46:51 GMT  
		Size: 191.3 MB (191260441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ed143bada3638286e0822c46b078dbbb39db04031155cfd8e8c4c03a41e1fc`  
		Last Modified: Sat, 04 Feb 2023 17:18:32 GMT  
		Size: 1.1 MB (1064658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d9d1e4093d41b6f094170d1461e71303c75949912e30284592b1c29f56d3dc`  
		Last Modified: Sat, 04 Feb 2023 17:18:35 GMT  
		Size: 58.8 MB (58820386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5db956fb24291a76d586971b30226cff724d608609f3b528020477162de78b1`  
		Last Modified: Sat, 04 Feb 2023 17:18:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
