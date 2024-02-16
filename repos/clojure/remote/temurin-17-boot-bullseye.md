## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:b29a34e8731fa5081e204ef0063140c12a86cc8db7d9891e3a10b15beaa6f02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7b93d97ed67c3f14f0bf4e0d3c87a1dcba989566a34ed48280f4bac3c2ad0731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261165663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7865c0dc2027970187513afd2e1a34aa193d3e19c2c71384a75231950d2c8f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:22:28 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:22:29 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:22:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:22:29 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:22:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:22:36 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:22:55 GMT
RUN boot
# Fri, 16 Feb 2024 05:22:55 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:22:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:22:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868da7564e4b1e4da0fe7d569a33bd39a03d781e42fcb9924379b0ad8881c350`  
		Last Modified: Fri, 16 Feb 2024 05:37:07 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51059bbc226f3d94e5fd8433da63ef6a3da8a96da292123e959ca31028093e17`  
		Last Modified: Fri, 16 Feb 2024 05:36:55 GMT  
		Size: 2.4 MB (2367233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae224663539660f70a2c49a849637afc7d7805f4b4df735efc98e6617cdb08a`  
		Last Modified: Fri, 16 Feb 2024 05:36:59 GMT  
		Size: 58.8 MB (58820631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fe22d433d77300e41a9463cf5965b1f7cf1c8f6f11310de848325727bc2fc9`  
		Last Modified: Fri, 16 Feb 2024 05:36:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53563b0e6d02b564ebe23156d6d3ed44bd4d8608b055ef3fc8701675d48bd5a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258618982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8cc1def97537936bf13ef29927029c5e8fd39d802063379a7774f61e31c61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:36 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:05:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:05:40 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:05:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:05:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:06:01 GMT
RUN boot
# Tue, 13 Feb 2024 02:06:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:06:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:06:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b93abada80d7a4cca39f20b2fb149ebf7e2868c862d216131fb6c28cc287e7`  
		Last Modified: Tue, 13 Feb 2024 02:21:10 GMT  
		Size: 143.7 MB (143720884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2ec2c2c63d8048964bfaedae65b44bf02ce09599184abc894ec53294fc8ac0`  
		Last Modified: Tue, 13 Feb 2024 02:21:01 GMT  
		Size: 2.4 MB (2355782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d50f41954c30ba61b08c94e980cac35f4538d8f3f8b8834f23bd5b71bb4c203`  
		Last Modified: Tue, 13 Feb 2024 02:21:04 GMT  
		Size: 58.8 MB (58820431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9954c933941db6bedd1a25b0c09a2d718adc581178d971abb564e840344a57`  
		Last Modified: Tue, 13 Feb 2024 02:21:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
