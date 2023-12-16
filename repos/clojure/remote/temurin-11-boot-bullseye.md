## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:6a79386dfbefc7813c270f5533673ac42e2ee7affe9f1e01e5e424c20305d888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:df9473f1c8cb0b37b44e192b64157d555c73ab400493ff9c5a4eb532e644de7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87f6954d94f3a516f4cd02947027a0b93aeadef948abfe9f249638612ee080`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:55:14 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:55:16 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 09:55:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:55:16 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:55:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 09:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:55:22 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 09:55:39 GMT
RUN boot
# Sat, 02 Dec 2023 09:55:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100270be7c7a032e8711a8951a07234acf8e56368673f84b3d9df6b333e239f7`  
		Last Modified: Sat, 02 Dec 2023 10:14:22 GMT  
		Size: 145.3 MB (145266419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286ff7c42896e17f1e4d033ec20bbaffae9da5a0fcdd9d976bdcc78df50f5bfd`  
		Last Modified: Sat, 02 Dec 2023 10:14:11 GMT  
		Size: 2.4 MB (2368745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdddfb94c4f5be025956d673408d143b43ce42e5401751333089e6115bbcdeb`  
		Last Modified: Sat, 02 Dec 2023 10:14:14 GMT  
		Size: 58.8 MB (58820409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05c7643bff7067b96d06aec2a994cb0215373935e3a14de2e91aae05a878d04f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2d831da05f451415951af440d786f3760b0f84f952a7f98b4329a33a775cb8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:03:25 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:03:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 13:03:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 13:03:29 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:03:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 13:03:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 13:03:35 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 13:03:50 GMT
RUN boot
# Sat, 16 Dec 2023 13:03:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af54c8e663dc85f64ce40fefa66d7c03c32ea39f2b5b91b849f62df8782494b`  
		Last Modified: Sat, 16 Dec 2023 13:16:08 GMT  
		Size: 142.0 MB (142001837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c909865373725638abcbc9e7aeca13f7ad07b1308aaeb0c3e21dae47dbdf6c`  
		Last Modified: Sat, 16 Dec 2023 13:15:59 GMT  
		Size: 2.4 MB (2357479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1e89c840201441d33215bf22ddcd4ba92cda12a0e1e75e27b21277f14b3c6`  
		Last Modified: Sat, 16 Dec 2023 13:16:02 GMT  
		Size: 58.8 MB (58820407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
