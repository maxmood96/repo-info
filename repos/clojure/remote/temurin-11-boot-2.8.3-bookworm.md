## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:21ef217bab52512a9d6cbbbef513892db44e7880777570b5f9a9cdcb51598cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9d3f0512f15e46c0338e4a8144fb1974bf64bc010e78559d03968f9bd5bbf51b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259171058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcfcb1d852de1a680f1e4be6c0fcbb2f6d8d75a1775f257489a0f57028f2efd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:14:04 GMT
COPY dir:95f5b1bebae6bba6ca961eb10c7982ff1efe410622f69bd5e96558adc723ec83 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:14:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:14:06 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:14:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:14:06 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:14:14 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:14:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:14:15 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:14:35 GMT
RUN boot
# Fri, 16 Feb 2024 05:14:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab73dfaeb8efe8e61bb2e2183ff6055868cfdd75b609e2a918178a08b7e341f2`  
		Last Modified: Fri, 16 Feb 2024 05:32:14 GMT  
		Size: 145.3 MB (145270882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f246ca3c70d0b38a923fb89551ae4c1429c21b5e1074d555a46286c5896398`  
		Last Modified: Fri, 16 Feb 2024 05:32:03 GMT  
		Size: 5.5 MB (5527118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93598a27835519056e38236b3f7458bfb7c696eebace5ab0bbcf4783b135fd2`  
		Last Modified: Fri, 16 Feb 2024 05:32:05 GMT  
		Size: 58.8 MB (58820453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa0b37292e06857234d25637a438b80103e87b41ba2070aef055024abe405357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255767271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1c5d3c1ab8379873b628b1110f1158b8768d09ddf9121e4a367bfb91637be8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:51:48 GMT
COPY dir:0419d7bc8c60addce41546593a3de80cd02ee9001351a641f9cf113402b5fb20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:51:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:51:52 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:51:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:51:52 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:51:59 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:51:59 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:52:19 GMT
RUN boot
# Fri, 16 Feb 2024 07:52:19 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91414dc7277237ee0166b6b51ae31fc8134626648f3b346e684414e3e91c8865`  
		Last Modified: Fri, 16 Feb 2024 08:07:32 GMT  
		Size: 142.0 MB (142006397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1545b6d8a06e2fdf7ff26fd9cfdb6a99357f7025ebd2df16874e14cc5028f7`  
		Last Modified: Fri, 16 Feb 2024 08:07:24 GMT  
		Size: 5.3 MB (5349467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be796c3caba57aea36557a45c3dfd66b2e2eceb5edd4d0d4c29b7330a4ed863`  
		Last Modified: Fri, 16 Feb 2024 08:07:26 GMT  
		Size: 58.8 MB (58820442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
