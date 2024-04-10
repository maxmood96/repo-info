## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:d83d666aa0b98bb555062d266b323adfd1b34dd9602db63aa0a90a44a8c33030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ba75d62399ed86abae2b2d6175e05fa2055e23cec0cc39f3923460b6db2b242b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217500018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee88c976a3e2fb7df10fb2904fe4ae6a1f56ef7188f0f65714fc4b294711703`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:16:54 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:16:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:16:55 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:16:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:16:55 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:17:01 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:17:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:17:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:17:22 GMT
RUN boot
# Wed, 10 Apr 2024 06:17:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8414e866d12b4e4b2d1b68c44e322badbd93741b9c94430f6a65b884141a9420`  
		Last Modified: Wed, 10 Apr 2024 06:39:04 GMT  
		Size: 103.6 MB (103591917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16caf5b6fc4cb0d3ea17a7de11f812f7898a4c3d980080461e6aa5e9f998ca9`  
		Last Modified: Wed, 10 Apr 2024 06:38:56 GMT  
		Size: 5.5 MB (5527317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55eb97e46b69f69c06bee19d9ce957b4e69cf3fe033ee9c50a49d27eaba0e18`  
		Last Modified: Wed, 10 Apr 2024 06:38:59 GMT  
		Size: 58.8 MB (58820424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:579a8b19387eb2c2b7a458d32dfe8f41e325a345d1938751cb62235a7dffb544
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216469932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8541ab45fb550c30744d748d479fd320f96443bfd2d02da3cda31ba3b07aa1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:37:54 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:37:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:37:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:37:56 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:38:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:38:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:38:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:38:47 GMT
RUN boot
# Wed, 10 Apr 2024 04:38:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd52f7c6791dfa000d5ac11d0908c05085ecf85295a21261c6c20087e418c71`  
		Last Modified: Wed, 10 Apr 2024 04:57:52 GMT  
		Size: 102.7 MB (102703042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da262b97ee642e262acb86d92cfb9d898ff56b57c3bf695540df58aa62c1beeb`  
		Last Modified: Wed, 10 Apr 2024 04:57:45 GMT  
		Size: 5.3 MB (5349521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbfd118b4631cb6862034779e499485b7229ac689d3d1e308975a6f0632efb`  
		Last Modified: Wed, 10 Apr 2024 04:57:47 GMT  
		Size: 58.8 MB (58821104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
