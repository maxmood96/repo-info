## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:de12e6e7d5099e2c0abb56d267621ba8d616bb2761e3d716ed64a443dca4e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b0b6bc21397519d0909394bedc5de428362139ca6e116aa126d947a004d6d456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219845132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81564060d16df56e9fa5c37257ea7167698f88be4680cf986b9deed218f12f8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:53:26 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:53:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:53:26 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:53:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:53:27 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:53:33 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:53:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:53:33 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:53:54 GMT
RUN boot
# Thu, 11 Jan 2024 04:53:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9065c2ddfafbfa61d40470ae40c8be4ed56fd40ce2f79c635ba75bac29eeac1`  
		Last Modified: Thu, 11 Jan 2024 05:14:55 GMT  
		Size: 103.6 MB (103598259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ac7de1e2d8a07803861119921ec5be030ecfd5d7bd29aaae0b8fbad7b4e90`  
		Last Modified: Thu, 11 Jan 2024 05:14:47 GMT  
		Size: 2.4 MB (2368715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710937e4b1309f5c3b48a2d982d3e91e87707e2e504ffc418d0800758fd499b5`  
		Last Modified: Thu, 11 Jan 2024 05:14:50 GMT  
		Size: 58.8 MB (58820435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56bb69c85fa8e5cd127870949af5fa5e164cb050222de9512fd1efae7e103a27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217587535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84fb1bdf7586b68bf2cfb66b36de85407edd6f4a0a2f990aec545d1c59d5695`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:20 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:55:22 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:55:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:55:22 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:55:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:55:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:55:44 GMT
RUN boot
# Tue, 19 Dec 2023 06:55:44 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f246578faf5a2d8e680724996478cd0ec4fc82370e7f6dd3239de87dd1117ee7`  
		Last Modified: Tue, 19 Dec 2023 07:13:15 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e5a56389af4b8dae286978594d48adc44c4831baf7aa22b0733a5b6b651f4`  
		Last Modified: Tue, 19 Dec 2023 07:13:09 GMT  
		Size: 2.4 MB (2357448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e058eb8fdf7677f41b7894c9791175277a470f106a5c6f366edc1cf4dfb0b99a`  
		Last Modified: Tue, 19 Dec 2023 07:13:11 GMT  
		Size: 58.8 MB (58820458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
