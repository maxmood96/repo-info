## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:b1b449acd8518c8db07b0a0e2811316e50e06b3d4fff81357fd417889d7c5caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8c299c8c1624b4d1699221f1cf59f86651cd0104e19bd14794f5350536df5328
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308811882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c58741764a53feece954451e8ecfb7521ce501c2d11c436d0fe0d8bb90804b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:09:51 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:09:53 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:09:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:09:53 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:09:59 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:09:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:09:59 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:10:16 GMT
RUN boot
# Tue, 23 May 2023 08:10:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:10:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:10:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62e3a1941399287928e0b128fbf9c001cd1f164f2cd9d5b0f242162cb22481`  
		Last Modified: Tue, 23 May 2023 08:18:28 GMT  
		Size: 192.6 MB (192580373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84feaddbceda3af591163538831493ff2a82a2c307928e286aeba710c1800f5`  
		Last Modified: Tue, 23 May 2023 08:18:15 GMT  
		Size: 2.4 MB (2361679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d58c4b4ffd2e7bd6b020aeb49b2ff42c4503d13a53cfb10d4012ca94c15ceb`  
		Last Modified: Tue, 23 May 2023 08:18:18 GMT  
		Size: 58.8 MB (58820406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51d40e31b47c9fd21e8c7d76d19a1650fed10cab44ad987d92e012a90f8482`  
		Last Modified: Tue, 23 May 2023 08:18:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a3b09617bde44c8049f2235cc7b5f205ec460fcd33f956e9841aabbeb049824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306252643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba74915c90128cc79dbabd157bed3e13b2dc6d3b6650cc48cc93668f05386ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:18:37 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:18:41 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Jun 2023 01:18:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Jun 2023 01:18:41 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:18:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Jun 2023 01:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jun 2023 01:18:46 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Jun 2023 01:19:04 GMT
RUN boot
# Fri, 02 Jun 2023 01:19:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Jun 2023 01:19:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Jun 2023 01:19:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f84bb66698dfd6516ae40960a9ff86d5acdff3a75decc6e793b695113145916`  
		Last Modified: Fri, 02 Jun 2023 01:26:57 GMT  
		Size: 191.4 MB (191387660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a346e9d0307735dd0753e673da3b13f84a007f01d12041eb11872d8b7e60adb`  
		Last Modified: Fri, 02 Jun 2023 01:26:47 GMT  
		Size: 2.4 MB (2351394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11984f1f16ad9a9c05b317374595e5a14b1d8a14ac17a5ca11b2531f7f07fd2`  
		Last Modified: Fri, 02 Jun 2023 01:26:49 GMT  
		Size: 58.8 MB (58820577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd129f11bbf48aeffecbeeeee2e8269bb2584efa4ef0eff7d4bd83f2a0df55`  
		Last Modified: Fri, 02 Jun 2023 01:26:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
