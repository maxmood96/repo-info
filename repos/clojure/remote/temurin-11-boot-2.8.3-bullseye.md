## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:3e32f89c68e938912646c04c56f92aef44b82150f68b14da37c0cac08b1b966d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ca912d404d2ede1e7b3e327c5e7815012aaec6e6cc0a400cb129f5c471741eaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856609b824efb8fbcf54967ed067725fe455729ec38c55f519a4fdef6dfd2864`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:12 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:59:13 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:59:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:59:13 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:59:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:59:19 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:59:40 GMT
RUN boot
# Thu, 11 Jan 2024 04:59:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f52cc9014579cafc22fe8590ab39539d23432b192e36ae88e348b78be356b`  
		Last Modified: Thu, 11 Jan 2024 05:18:20 GMT  
		Size: 145.3 MB (145266339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cfb05a37a6f2559cd47cec42cb3e7a91e32147b254f60e169579e2fb24d2d9`  
		Last Modified: Thu, 11 Jan 2024 05:18:09 GMT  
		Size: 2.4 MB (2368668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d50459e8efd943826cba7cd07f93f8b46217069932da143dcdfb8ca3eb44dd`  
		Last Modified: Thu, 11 Jan 2024 05:18:12 GMT  
		Size: 58.8 MB (58820737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

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
