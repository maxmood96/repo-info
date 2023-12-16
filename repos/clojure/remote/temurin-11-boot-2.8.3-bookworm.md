## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:57ece80292aa1b309f3aba29eaab07cd28919ea5c60c380bd2414988ff654776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4b2107c50610584d52bd4892036d1c16f47035f6a6fa853244c56c07780b8df7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07606d52e6849c06051188539421866703833b430014aeb43369e60f1e7cd05a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:24:39 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:24:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:24:41 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:24:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:24:41 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:24:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:24:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:24:49 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:25:05 GMT
RUN boot
# Sat, 16 Dec 2023 15:25:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a771d9b6c5f4bde297158365f39ffd096a67247a2c15605592e73738745d1`  
		Last Modified: Sat, 16 Dec 2023 15:44:15 GMT  
		Size: 145.3 MB (145266405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00f8c00148d60e685c81336d3874afc18d6bcfd4ef80b3a2afea71b8eae21b4`  
		Last Modified: Sat, 16 Dec 2023 15:44:05 GMT  
		Size: 5.5 MB (5530250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512a7901086c1c90b8af32732eef629e231629cbbe583917150fb5638dda7f4b`  
		Last Modified: Sat, 16 Dec 2023 15:44:07 GMT  
		Size: 58.8 MB (58820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8da5b27b06945d5b1cd4f33b365618c596939bdcf9a7eaea22bbdc37d96329b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a1990629276d85b158a78a7e1f97ce8da60ddcab251884406f580e31011a1b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:02:26 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:02:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:02:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 13:02:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 13:02:29 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:02:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 13:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 13:02:36 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 13:02:52 GMT
RUN boot
# Sat, 16 Dec 2023 13:02:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d125f1849f90f4e047bb3ef55b198f35368f7a1ad3522a435d47de1c8e908`  
		Last Modified: Sat, 16 Dec 2023 13:15:32 GMT  
		Size: 142.0 MB (142001834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c7d5efc6a889c9bfd72e17ed01aefa6b6d8a40bd49816b48bcb02906ae8d74`  
		Last Modified: Sat, 16 Dec 2023 13:15:24 GMT  
		Size: 5.4 MB (5353251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd91632a0069ba6dece294b2bfbf368f36368ca8035b54eb400c4b89e45ea4`  
		Last Modified: Sat, 16 Dec 2023 13:15:26 GMT  
		Size: 58.8 MB (58820497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
