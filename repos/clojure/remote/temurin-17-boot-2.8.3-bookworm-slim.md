## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:263c8eb5569306d7ef5fefd98be22d1d777a297e4fd0cb32ec812ce5c3b6a492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f241df9c7e7ecec15185569f6769dd5981cd55f4ce24ac98750a754845cb059a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236343693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6a88d79ddae971bb6967b3fa71477f07e0264c7193893a88e26b3f923f77f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 11:03:24 GMT
COPY dir:634e6dc1071a76d830a1c58e20efb6c42c0d02beb44d214374fc7817b69efa15 in /opt/java/openjdk 
# Tue, 16 Apr 2024 11:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 11:03:25 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 11:03:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 11:03:25 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 11:03:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 11:03:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 11:03:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 11:03:50 GMT
RUN boot
# Tue, 16 Apr 2024 11:03:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 11:03:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 11:03:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171485078ae9e3965efed1e2c5427ae136725fc168bde374dec39e8ee65fccf`  
		Last Modified: Tue, 16 Apr 2024 11:22:14 GMT  
		Size: 144.9 MB (144893099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d13059f95c8186f3168ee363765746de291845a03ebfed207f9d543ede3a5e`  
		Last Modified: Tue, 16 Apr 2024 11:22:03 GMT  
		Size: 3.5 MB (3498215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddbe1541ef03b976230a0d904426cb4c5473c761b761ad434f456256c90b6f2`  
		Last Modified: Tue, 16 Apr 2024 11:22:06 GMT  
		Size: 58.8 MB (58820619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762c41db5fcb2aa52f9bf7341b648e9b0fcd6160cb47f86379c80650db839308`  
		Last Modified: Tue, 16 Apr 2024 11:22:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd275af79ed0094203a26623722cda3cd20c916707876d177b4220dd733961cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820192c5f4c92b4a89657553abedab73495ba6c820e37ca955d4dfc14806b72d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:40:26 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:40:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:40:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:40:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:40:30 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:40:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:40:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:40:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:40:52 GMT
RUN boot
# Tue, 16 Apr 2024 06:40:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:40:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:40:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1524327b5ca19acc0cd54b203239bb4f537664cf1202cda7b226bcd7d428c4e2`  
		Last Modified: Tue, 16 Apr 2024 06:56:52 GMT  
		Size: 143.7 MB (143720949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a04fec57952dc94675ac57ae7974b8859df20db9dddc49245c21a4b497d9e3`  
		Last Modified: Tue, 16 Apr 2024 06:56:43 GMT  
		Size: 3.3 MB (3322220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e050b7e0f454b1657cadd35f5a7cc919070ae6383567a978ce97b7c022948c`  
		Last Modified: Tue, 16 Apr 2024 06:56:45 GMT  
		Size: 58.8 MB (58820414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a817f58459ac16b1ae191137ebf46bce8fa36d28334b446a0133c0a18ac1dd`  
		Last Modified: Tue, 16 Apr 2024 06:56:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
