## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:1a6a4ad35dea937acf31e5f51068a712a3eaa0b63ca8640fb73a81999ca2ed57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b80901af08777e31257fd8e42d35f3b14c4ccc029bf71e8a5898e3c3029d9c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236346494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1439d9738d325cfd223e804ed420b94ea056c2bc83c93d0c2fcbcaad5f86b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:52:38 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:52:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:52:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:52:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:52:39 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:52:45 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:52:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:52:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:53:03 GMT
RUN boot
# Tue, 31 Oct 2023 00:53:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 00:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 00:53:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29aa87389f888844609a24a907ba194da7cfe360007dd36c50173a872e3072`  
		Last Modified: Tue, 31 Oct 2023 01:12:31 GMT  
		Size: 144.9 MB (144873895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04b1dce274d8765e4f98a74315707e3637dfe40c9c1293a0f6f3bb5b654d86`  
		Last Modified: Tue, 31 Oct 2023 01:12:21 GMT  
		Size: 3.5 MB (3501729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4977c71087dd321ed103e05f3a94dba50da2ca382cb145177278180c17886b`  
		Last Modified: Tue, 31 Oct 2023 01:12:23 GMT  
		Size: 58.8 MB (58820597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83463be8ea42b6041614cf2d413d873ad68020dc73c415b66c649dc8e08c0bc6`  
		Last Modified: Tue, 31 Oct 2023 01:12:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87bfd5be44c74b6fc0d24ff87b69d154d9e3a3d831e101c48a4880b9ecced71d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235006663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49cbb43149ca509c0b6f80a890b08ca39acfd4ae1f77e6ed3d3a9d01b5448de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:05:28 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:05:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:05:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:05:32 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:05:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:05:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:05:37 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:05:54 GMT
RUN boot
# Tue, 31 Oct 2023 01:05:54 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:05:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:05:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed13091dc8653df4bb00fe6e6584527ee55d9420cf9bf1d72fd4e280fb96c81a`  
		Last Modified: Tue, 31 Oct 2023 01:22:39 GMT  
		Size: 143.7 MB (143681739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35accde96f2828bb96fecdc7ecb136bc3f45bbf3ff939d186a38cdbe60b5fb6b`  
		Last Modified: Tue, 31 Oct 2023 01:22:30 GMT  
		Size: 3.3 MB (3324883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd790d3e63b7ae8cd44a1a71e47845501ef6a4c6e3cb8e1269193d9ee40c570`  
		Last Modified: Tue, 31 Oct 2023 01:22:33 GMT  
		Size: 58.8 MB (58820358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919548864db59df75fefb78af1cd480998dde196f60294b62d05fa19ec5c57f9`  
		Last Modified: Tue, 31 Oct 2023 01:22:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
