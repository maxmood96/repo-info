## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:6dcb8377b14b5a59aba411fcda0ff7142886e07fa8d8b5a63fe94f19248d83bd
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
$ docker pull clojure@sha256:14f89f44920b4f11a60b8ff87df13b458b9a522358a5a213fda03b59870fe0ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255768352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18099949cdee374b007018522b1d8099d179d4674b6019b0c6f672ba1369d616`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:14:18 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:14:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:14:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:14:21 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:14:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:14:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:14:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:14:42 GMT
RUN boot
# Wed, 24 Jan 2024 22:14:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec5047588aad160e7dc5c6e44a35baeeed650fc3f5e788618cd10cc64259a62`  
		Last Modified: Wed, 24 Jan 2024 22:36:40 GMT  
		Size: 142.0 MB (142006514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484f8265c768de70032a64bc12dea3030d49709863c6e910fedd85ad55d66277`  
		Last Modified: Wed, 24 Jan 2024 22:36:32 GMT  
		Size: 5.3 MB (5349334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d921ad00a3380a6974ecbd3c901d26682b6bc629becd970c90a2392cc333d`  
		Last Modified: Wed, 24 Jan 2024 22:36:34 GMT  
		Size: 58.8 MB (58820257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
