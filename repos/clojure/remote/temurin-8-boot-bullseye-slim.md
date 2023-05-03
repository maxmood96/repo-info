## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:48b8c3a2ddac188c2cd3bdfbd60e3535055467597a1b1e30c3dc9713fe4c724c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:675f39591a3b87dca8713d837862c83fe004ee5f593d2138d95085692770b071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145943662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1887ed3192248123f2dbda46e5478cdc4f857da4521d4bb4d933c3d494b2c3df`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:24:44 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Wed, 03 May 2023 20:24:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:24:44 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:24:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:24:44 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:24:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:24:50 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:25:08 GMT
RUN boot
# Wed, 03 May 2023 20:25:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eda8d8deb246b934d051ef2af038ab3fb22f3de2f341e84edf173a887c496ab`  
		Last Modified: Wed, 03 May 2023 20:35:17 GMT  
		Size: 54.6 MB (54642103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba43ffca2c24151502031f77677dcd6464be46db2b2d635a5330f41436337a37`  
		Last Modified: Wed, 03 May 2023 20:35:11 GMT  
		Size: 1.1 MB (1077523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a103e70675e060920fe833f104b39d7480320577d31776adb431f58404e5fe1`  
		Last Modified: Wed, 03 May 2023 20:35:15 GMT  
		Size: 58.8 MB (58820520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c75ef1fb555aa769143f777f7992c5df37617c392eb7a80112e7adc5a0ced134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602ae1b9d9d9948dad723b95933aae2c023c04a6fa200b6e004339520cddc692`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:44:17 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Wed, 03 May 2023 17:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:44:19 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:44:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:44:19 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:44:23 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:44:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:44:24 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:44:41 GMT
RUN boot
# Wed, 03 May 2023 17:44:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45323ce94562764c60b759096664441c4fd32a723ce4c04882e7478c93e9b104`  
		Last Modified: Wed, 03 May 2023 17:53:34 GMT  
		Size: 53.7 MB (53742660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e47ea6893d671d4ce47db33e643de4a2b48cdd7b3e1fdf071fd61fa1b15bf3`  
		Last Modified: Wed, 03 May 2023 17:53:29 GMT  
		Size: 1.1 MB (1064793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33024aadb626500a265c6c38f5daff51752ee6ca7e347e36022764984a1bfce5`  
		Last Modified: Wed, 03 May 2023 17:53:32 GMT  
		Size: 58.8 MB (58820566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
