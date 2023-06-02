## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:d07f494e50039ac679443ccf92d3e8dc50718f9b200cf5481fede6c8dd00a717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c11758c045c9845638e4562b36458a12a407fcf55626bcc6264fe3bc87a3ccce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283882459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a813a2419a1be8a8f7ed72d50fed76e552ea6b30bc47e9896196a40f226d89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:10:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:10:23 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:10:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:10:23 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:10:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:10:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:10:29 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:10:46 GMT
RUN boot
# Tue, 23 May 2023 08:10:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:10:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:10:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432f099456cdedc7ddcd307e305c6b0fac23b7a57290e296b721fc518e6154f2`  
		Last Modified: Tue, 23 May 2023 08:18:37 GMT  
		Size: 1.1 MB (1077537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8dd2eb442bbe5a033c4ad126b2f856ae534600895a064f3eed374d099e5c24`  
		Last Modified: Tue, 23 May 2023 08:18:40 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84221829bb0c20f84f0b2b0fb6d1b08f1a4c438f8992bd4186ac7182aeb27bd2`  
		Last Modified: Tue, 23 May 2023 08:18:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:daed4844928184a9f03fd33c2b2980a2d97e1ca3966126197fe635ce77fa7c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281325943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d049fcf743fac4f737596e12b3ea2fd3b3ed53440d5c7dcd0833b39215bb6fff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:19:13 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Jun 2023 01:19:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Jun 2023 01:19:13 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:19:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Jun 2023 01:19:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jun 2023 01:19:18 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Jun 2023 01:19:35 GMT
RUN boot
# Fri, 02 Jun 2023 01:19:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Jun 2023 01:19:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Jun 2023 01:19:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad6eba380acd4e5e6454cd68c63258689f2717351e03f8a683b4593d6843f3`  
		Last Modified: Fri, 02 Jun 2023 01:27:06 GMT  
		Size: 1.1 MB (1064783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3798179d8b35ed9eb86c235ea91b8b4195691b19d32c1a0009fe6aa7adfa9`  
		Last Modified: Fri, 02 Jun 2023 01:27:08 GMT  
		Size: 58.8 MB (58820358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dc010d193bf7d5855aecacdddc3be6289167232e901ffc3ef581a13aa0378b`  
		Last Modified: Fri, 02 Jun 2023 01:27:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
