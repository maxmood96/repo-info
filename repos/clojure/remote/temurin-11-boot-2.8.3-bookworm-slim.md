## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:9f3f2eeba83c8ace17b5a5b0d95c3107f529890035d9a1f36becddcd421e726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03f061bcf10f1970602584e570fa23f865a26a47c8a349d7ee4e5b4aa9260681
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79a233abc4228bedfac519feff95d949e9a5c8f73c901d2a7da10713c686956`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:43:25 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:43:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:43:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:43:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:43:27 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:43:33 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:43:33 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:43:50 GMT
RUN boot
# Tue, 31 Oct 2023 00:43:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd4cc1352ba8bc75177e70d6c392b13eac93f6a6b0e4f8886cab8c4b6bd5a8a`  
		Last Modified: Tue, 31 Oct 2023 01:07:06 GMT  
		Size: 145.3 MB (145266684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7531ca942997b35655b3666a3b66868f6a6a22ef7666600f8735ac1911b3e8f6`  
		Last Modified: Tue, 31 Oct 2023 01:06:52 GMT  
		Size: 3.5 MB (3501704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca1b11832908bd26e9cbe2118dec7d610044519990d8bfa3dcde0c4635dbe85`  
		Last Modified: Tue, 31 Oct 2023 01:06:55 GMT  
		Size: 58.8 MB (58820582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fe28bfd7a1fbc880f4894a8c36229d40627431a80c77e4fce2f38ec1e6f4da3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b8d22d7775e3458227edc0866b5fbe98d860b7dc516ab403e3dd3d420a14c0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:57:22 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:57:26 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:57:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:57:26 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:57:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:57:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:57:48 GMT
RUN boot
# Tue, 31 Oct 2023 00:57:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eb29d768a9f4bddddbb15bd2381be6f475f0d817d5b776808080bd9b3d984e`  
		Last Modified: Tue, 31 Oct 2023 01:17:39 GMT  
		Size: 142.0 MB (142001972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca92f8e96d06f9ecb11e17d3c16e4936e07786b6a5964f90dabb81da6b2a399`  
		Last Modified: Tue, 31 Oct 2023 01:17:30 GMT  
		Size: 3.3 MB (3324901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f75a7842e1d793e6ba3dacac901df17a6f414a675f0a102c94f2b52b549137`  
		Last Modified: Tue, 31 Oct 2023 01:17:33 GMT  
		Size: 58.8 MB (58820374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
