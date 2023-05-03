## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:0b34aaf6a33e381b39a155ee612f9e24a2febaacd320faa2972a45adc6582544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:83096f2e619b9b233627e1bf4c8ce17e2116cb9f6f4756690c999589c6b1db45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145958136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c49de0a9dc91a88342cd973a6510a25185e3477142a0d4c69856d74687697e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 19:58:51 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Wed, 26 Apr 2023 19:58:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 19:58:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 19:58:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 19:58:52 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 19:58:57 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 19:58:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 19:58:57 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 19:59:15 GMT
RUN boot
# Wed, 26 Apr 2023 19:59:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7773126247f89efdc56db7f90c92282e6c501ad8da6e738413eb8294ca8f168d`  
		Last Modified: Wed, 26 Apr 2023 20:17:34 GMT  
		Size: 54.6 MB (54642132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767d43556fb1915c3295794a4aeab3b5fd5642dbbbc0657159bbfdc80e120205`  
		Last Modified: Wed, 26 Apr 2023 20:17:28 GMT  
		Size: 1.1 MB (1077511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941cab73c0cb601fe020e20f894f1924c7cf0f26b5596773531bd8db1580e27c`  
		Last Modified: Wed, 26 Apr 2023 20:17:31 GMT  
		Size: 58.8 MB (58820265 bytes)  
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
