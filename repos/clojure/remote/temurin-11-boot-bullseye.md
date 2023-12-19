## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:2bc7879cf1f05735a312d180ddd5257aba9ff4aa2cc2db6f45c7bc45546c8e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:733189c6af92e66e2caf2d65e9171a82a24bdbe2c2440e7c32839e272111f48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3572cc4a6a5a5b188e3424e3c68fad183ec109c84bd04e7545f90d620da71`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:39 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:59:40 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:59:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:59:40 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:59:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:59:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:59:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:00:04 GMT
RUN boot
# Tue, 19 Dec 2023 07:00:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb854c5d99526cd57c3e6a9ea2e5f9f57043350200a89c9b279c0ebf18d225`  
		Last Modified: Tue, 19 Dec 2023 07:18:52 GMT  
		Size: 145.3 MB (145266384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1b45044b3412ff3a643fa25f5179efcef5d9da83f8976a7d17ab6ded4ea381`  
		Last Modified: Tue, 19 Dec 2023 07:18:40 GMT  
		Size: 2.4 MB (2368743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b57320a331299c866f89f7fa269a8c16e6eb277a530357c195638ce02fb22`  
		Last Modified: Tue, 19 Dec 2023 07:18:43 GMT  
		Size: 58.8 MB (58820557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18c6f6130b39529948e8e42e70cbb8b9cf9c98a3c54b85f720e6063f97387e27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33311404cdd51ec9f95d94318b6bedda1adbdf7531c7551f668f36424d38ac7f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:59 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:00:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:00:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:00:03 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:00:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:00:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:00:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:00:24 GMT
RUN boot
# Tue, 19 Dec 2023 07:00:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3697c4b45425ca398154987d262efe41d68ea04eec970b5480ea6c59afc915c2`  
		Last Modified: Tue, 19 Dec 2023 07:16:22 GMT  
		Size: 142.0 MB (142001858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc3e07564f520a59993934bd1adc01055a9b150bb0c87a3bacdc81de8e5ebe8`  
		Last Modified: Tue, 19 Dec 2023 07:16:13 GMT  
		Size: 2.4 MB (2357471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81cbf6f4664663ef6f0b71c694761561f5ebe69df5d3442cf24d3e9a83847`  
		Last Modified: Tue, 19 Dec 2023 07:16:16 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
