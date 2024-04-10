## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:bdb73336e310e3f8263ee62ae7fb9db99204a764e5d2ee857ac783b6ab2189c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1552567c9339c48bdfb22f75d2c6977af222b4fc08575749a74a08c9c60954c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259179486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424ef4122341b5d64237b45af008598fbbd52362c077adda225d76fea236c9a7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:22:41 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:22:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:22:42 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:22:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:22:43 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:22:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:22:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:22:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:23:09 GMT
RUN boot
# Wed, 10 Apr 2024 06:23:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a514947677172b8fc44890310625cf6cc5b905b6756bd6f81147c12bf9d8653f`  
		Last Modified: Wed, 10 Apr 2024 06:42:18 GMT  
		Size: 145.3 MB (145271226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e9115f4b702bf5b963e83e3c9e05a48f1ae97031e63ea9af3ee11bcb43d744`  
		Last Modified: Wed, 10 Apr 2024 06:42:07 GMT  
		Size: 5.5 MB (5527332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88ab3e23c592305487c615cca0c4c10b1bc42d100dffca01f09140a8cb14bf`  
		Last Modified: Wed, 10 Apr 2024 06:42:10 GMT  
		Size: 58.8 MB (58820568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:474e0572a02f3fdf06b68b7c669e15290b6dde0f914e40e4a56cba3bd6e650a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255772734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbe556e8aedca40280cfd0076a06c1b1286129bc9c0add53169200bdb386b60`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:43:13 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:43:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:43:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:43:16 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:43:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:43:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:43:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:43:41 GMT
RUN boot
# Wed, 10 Apr 2024 04:43:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9bdda611d99cfbb82c7d1a5c1aec0235837c8fadc922cd581de255634dfb66`  
		Last Modified: Wed, 10 Apr 2024 05:01:17 GMT  
		Size: 142.0 MB (142006303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf1bfa1ff3d69fc359eb0a94cf8fc48fa92c8626213048efda35fca44cd597c`  
		Last Modified: Wed, 10 Apr 2024 05:01:10 GMT  
		Size: 5.3 MB (5349558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a444f980789f0c11db4deccdd98c2aed38c701c067083b7f45015b7075af18cf`  
		Last Modified: Wed, 10 Apr 2024 05:01:11 GMT  
		Size: 58.8 MB (58820608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
