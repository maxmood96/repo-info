## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:88405d721ca5bd09f8438fd6b546fa8e947690b1b502c4456b614224d177aa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1007220e1f2b2c285b393382e7925e93ac189593ee8b7439f6ab67333d25830b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261012413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732557d86af2bb2d999d3b466e5394af9738fa52858ac3b02a262bad419bcf48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:19:44 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:19:46 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:19:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:19:46 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:19:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:19:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:19:51 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:20:10 GMT
RUN boot
# Fri, 28 Jul 2023 03:20:10 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 03:20:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 03:20:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc877887922ff2413aab64a1fb8e4d446b9669ade73fd06cd4ed11c9c851d9`  
		Last Modified: Fri, 28 Jul 2023 03:31:21 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fd2a608f2627452452a87750820cd8c212bfed999de34df4bc0fbcf5635af`  
		Last Modified: Fri, 28 Jul 2023 03:31:09 GMT  
		Size: 2.4 MB (2362092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791a8b71dde20c55e0987bb7b292cda1843aa3f261a4305559efa5a6160bb555`  
		Last Modified: Fri, 28 Jul 2023 03:31:13 GMT  
		Size: 58.8 MB (58820603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bb70e2834122e061ab5864910417094f11b27c313c9eb8680494f98f44c3f4`  
		Last Modified: Fri, 28 Jul 2023 03:31:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8149c13250870e77e2964ce3ffe7222227e1a04134f661bc4fce0413ff5aba20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258415376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d5b3c3b22c259e7bd515f63aa2c78fe20c9df5bd9ff7d3110123d0022d65f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:35:02 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:35:06 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 14:35:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 14:35:06 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:35:11 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 14:35:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 14:35:11 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 14:35:30 GMT
RUN boot
# Fri, 28 Jul 2023 14:35:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 14:35:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 14:35:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d0f61795693efb86b2bc273c0ea30def7d3c4e57a24be4dac110415235a921`  
		Last Modified: Fri, 28 Jul 2023 14:43:11 GMT  
		Size: 143.5 MB (143538050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3310b9d380f122338aa57bc4b8cc9a19b14803ce0d57ec0d8da83fbd2e7f87`  
		Last Modified: Fri, 28 Jul 2023 14:43:02 GMT  
		Size: 2.4 MB (2351486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ba02943b43ba70cec21196d202a963b0cd27cb4f0bff24e51d1b5e95e4c0f`  
		Last Modified: Fri, 28 Jul 2023 14:43:07 GMT  
		Size: 58.8 MB (58820651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4567a0bf9975caa9a8b730b6bbf21fbb7c64d230edf1b5a9ef901e3b72a234`  
		Last Modified: Fri, 28 Jul 2023 14:43:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
