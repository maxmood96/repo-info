## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:1154e5e6d8dd0116242e4f57d5405f86cb86acb721e4c56b695ffd43390df7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c4eb1a8bd15a8e6fc8848f56416b3c2392a95f6f5163086bf2470629e72e4e36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66241684c56ce9f4131b6d909a89a6ea95e5159ed38c282c8a875dfaf49c751`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:52:46 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:52:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:52:48 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:52:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:52:48 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:52:54 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:52:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:52:55 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:53:14 GMT
RUN boot
# Tue, 13 Feb 2024 01:53:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3470e538d4e3cfd65043bfc65a4966ed42ab558a0d02d70086e803479fa66`  
		Last Modified: Tue, 13 Feb 2024 02:12:52 GMT  
		Size: 145.3 MB (145271036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122fb9da8f52172cd51f5fa8b117a4863f588f2836f05cca0e38d2519116ae64`  
		Last Modified: Tue, 13 Feb 2024 02:12:41 GMT  
		Size: 5.5 MB (5527246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0884c7c39e8be4d63555c955db24f432a59f071d4954e2d12f240288044fb56`  
		Last Modified: Tue, 13 Feb 2024 02:12:44 GMT  
		Size: 58.8 MB (58820500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4cf3a3c6641d7131ff7b93536f8dcfe2863586509aa0e9823727b4b7a544159
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255767198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc7625d085752bc7863fda849112feac734313846cece5b7d2e4862540c1d70`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:59:30 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:59:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:59:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:59:34 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:59:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:59:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:59:58 GMT
RUN boot
# Tue, 13 Feb 2024 01:59:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb18bf1feb8a022b56cb764ff4154c937334b989bb90ffde840254ce27e971b`  
		Last Modified: Tue, 13 Feb 2024 02:17:04 GMT  
		Size: 142.0 MB (142006386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea18fcdff867c24d4ccfc5c5e2afb65d04b085cb9f5cc6f55094e8a69c98b72`  
		Last Modified: Tue, 13 Feb 2024 02:16:56 GMT  
		Size: 5.3 MB (5349351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8e4a02a7a1fc605a22a2c11291bcfdf0142f0000c431136dc69bf3a0ea395`  
		Last Modified: Tue, 13 Feb 2024 02:16:58 GMT  
		Size: 58.8 MB (58820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
