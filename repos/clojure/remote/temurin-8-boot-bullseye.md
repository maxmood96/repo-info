## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:2c9a15170974cc9b3b58c448be1fb9f879694f41256d8dcb5766dbee85d44688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2c4a0772ccc5e65155f1cd07a366b9bdc717f7b297fc03faf166373f08b7dd24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170880770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422e8e19e8b745e18a9a9516456cd364d692d310ed2cbbec2b4abfea4c0e56fe`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:13:49 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:13:50 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:13:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:13:50 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:13:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:13:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:13:55 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:14:35 GMT
RUN boot
# Fri, 28 Jul 2023 03:14:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f2467027ab6a97b20105e61541ccde22023beb67dd246cdb940a2f15187d3c`  
		Last Modified: Fri, 28 Jul 2023 03:27:57 GMT  
		Size: 54.6 MB (54642111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f10820eb5b432c11ace8794aa4e3cf37e4618046c51600ed5e9634c752e0c0`  
		Last Modified: Fri, 28 Jul 2023 03:27:52 GMT  
		Size: 2.4 MB (2362133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca31f68a562aec5285fe072cfed1f94e6ca95c14cbaca698bda4f22901df7a2`  
		Last Modified: Fri, 28 Jul 2023 03:27:55 GMT  
		Size: 58.8 MB (58820955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69a8943b71ea45b52fccc2f65438224c807de6d91371d9a8d18f326a2e5b8d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168619870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2add60f97d99cd6c499764d896c004768700c9595adda5af8969e30c58cff38`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:29:56 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:29:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:29:57 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 14:29:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 14:29:58 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:30:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 14:30:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 14:30:03 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 14:30:35 GMT
RUN boot
# Fri, 28 Jul 2023 14:30:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc74632d4a0922fbad114070648e7c127eeb09926f5eafadaa39881a3da4e323`  
		Last Modified: Fri, 28 Jul 2023 14:40:06 GMT  
		Size: 53.7 MB (53742683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032eeccfed61ded01105df62fc759cb641ac4c937ef9cb73d32f6988f3cf8980`  
		Last Modified: Fri, 28 Jul 2023 14:40:00 GMT  
		Size: 2.4 MB (2351429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a7c91a7f9e2a315b2698eae328c2567d89954eee22c5411ffffe041d2cc5c4`  
		Last Modified: Fri, 28 Jul 2023 14:40:05 GMT  
		Size: 58.8 MB (58820968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
