## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:6409806b100552dfa13e836b722a62bced1d00b4471e30609a08713748330d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7ef256eab2ebecff11cf8af75ac156368f0257af28b8cfaac4d477595428e856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57ce46e00b7876febfce735d033d480eb3b33e92473b68b451995de8ae0fb5d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:54:06 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:54:07 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 09:54:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:54:07 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:54:15 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 09:54:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:54:15 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 09:54:32 GMT
RUN boot
# Sat, 02 Dec 2023 09:54:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5a177a4408bf01c234a96a773d806e23dea8a68ad9b62f313c86daab19599e`  
		Last Modified: Sat, 02 Dec 2023 10:13:41 GMT  
		Size: 145.3 MB (145266398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851c97cd97b5274efeca3409b47600b25451630664c447d1b1ece018fa00925d`  
		Last Modified: Sat, 02 Dec 2023 10:13:31 GMT  
		Size: 5.5 MB (5530344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23f78ab587f809cfe06337891ab669954c2c90ebc89fa74f3c4243f10969df7`  
		Last Modified: Sat, 02 Dec 2023 10:13:33 GMT  
		Size: 58.8 MB (58820364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2d454c07c8d306c0612ad8a0d45b284058abbfefbb232ae3e49c54317138468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a669c089043090ef890ff163cf34087aae95d8c495eb1a36858f6a0142221ba`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:44:30 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:44:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:44:33 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:44:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:44:34 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:44:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:44:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:44:40 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:44:57 GMT
RUN boot
# Sat, 02 Dec 2023 08:44:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315e261122e4eab35c627bf04f6ca13cb4652c256e98fcc558b03f00b879462f`  
		Last Modified: Sat, 02 Dec 2023 09:03:38 GMT  
		Size: 142.0 MB (142001821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d22cd860770e2bb643fe5d797abf72bf3c74b192dd017c5592871165c9cbb05`  
		Last Modified: Sat, 02 Dec 2023 09:03:29 GMT  
		Size: 5.4 MB (5353236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab7f99c9346a39c0b9209d3ec93a6895efa0c2309ecbb7da5a9191b95a6c88d`  
		Last Modified: Sat, 02 Dec 2023 09:03:32 GMT  
		Size: 58.8 MB (58820534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
