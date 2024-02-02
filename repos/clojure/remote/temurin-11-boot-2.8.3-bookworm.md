## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:7e8e5f809eb6a3f0c92b0b360c95e772da3ef926a2f14fdb064d0f654044d520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4c463b34daae109edf8bcd16d31f1dee4d83ca64d7af44d2cbb2a4214727055d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259205532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103f5e4a2dd54d3108baf205bd965d5487a340a865772e30487c6895e8e1fa88`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:48:31 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:48:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:48:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:48:33 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:48:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:48:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:48:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:48:59 GMT
RUN boot
# Wed, 31 Jan 2024 23:48:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afe2d1272b0c5e9161314942fa02036caab8b5f924665169595a113d2b85488`  
		Last Modified: Thu, 01 Feb 2024 00:08:30 GMT  
		Size: 145.3 MB (145271031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06516abc7cedd1772433acc1186717b1c65de9feb08814e74de4dc688422b558`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 5.5 MB (5530344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f9199f244d834f5d5ad824babad588313db21ca4925a730ff652821a339d27`  
		Last Modified: Thu, 01 Feb 2024 00:08:22 GMT  
		Size: 58.8 MB (58820403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3d54ff93e1facdf74fd751be84ad6c515656999cb4507561f2c7ccaaeeeb329
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255795509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47ada72289ff2da00bc66542795d3680029b9b5252a4fa19869f0015bf91283`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:19:38 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:19:42 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:19:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:19:42 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:19:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:19:49 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:20:08 GMT
RUN boot
# Fri, 02 Feb 2024 08:20:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300b593857f6a07a4266828dbbe1e03ed64d43a6bf503b48194d30675f3a069`  
		Last Modified: Fri, 02 Feb 2024 08:38:08 GMT  
		Size: 142.0 MB (142006417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ed9593f0535e54919c08a07c1d86c1d3ccaee794edd394ff7f94cbc74ea7c4`  
		Last Modified: Fri, 02 Feb 2024 08:37:59 GMT  
		Size: 5.4 MB (5353269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ebc19eb1faf9537495d12cae0982dfae8b7807631b160439b3ec8ac5fcbdbb`  
		Last Modified: Fri, 02 Feb 2024 08:38:01 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
