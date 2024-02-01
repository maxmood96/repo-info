## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:8915494f18bc1657078c2190f25aa2e22523fbcab81b5bb379adb50d6338c164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4072809103cc0e17b733a50eef8abd5fba19df67ddf5bc07f511009b5309f844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217527097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2982666182d7c470f5ebc56c5854070815193daf26f53849c7a325f41521888`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:42:17 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:42:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:42:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:42:18 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:42:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:42:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:43:12 GMT
RUN boot
# Wed, 31 Jan 2024 23:43:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638eb245e4649122c3cde175020b7b674960d80dc7cec3f2975ba51d86bc7a4d`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 103.6 MB (103591896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247569ce3765ac5a207b33bf6619b9e0eff651091aecb584637c81c310934ce7`  
		Last Modified: Thu, 01 Feb 2024 00:05:03 GMT  
		Size: 5.5 MB (5530435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bcc08d66368a8d8536c47d65b13634e7988e0d2a4987b8c8874c6308fac1ce`  
		Last Modified: Thu, 01 Feb 2024 00:05:05 GMT  
		Size: 58.8 MB (58821012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d243f9ca41dca64befdb9d87b906ad700efbd7abee712382fc01b675289252e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216492801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a52dd6e0146a4e959a0f1d7a2b4132d8ff53980bb7c1df339e437993e38f7c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:19:09 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:19:12 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:19:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:19:12 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:19:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:19:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:19:18 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:19:59 GMT
RUN boot
# Thu, 01 Feb 2024 06:19:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b427f51620767e3cfcd5376d7a199da31d4e087e65e7c8baa20d06efb81dd05d`  
		Last Modified: Thu, 01 Feb 2024 06:39:02 GMT  
		Size: 102.7 MB (102703057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c6786d12f51d916f1cf9742935e2ae2162aa56f394e847e452d32fa4496396`  
		Last Modified: Thu, 01 Feb 2024 06:38:56 GMT  
		Size: 5.4 MB (5353230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31ca25a62413be2a90b1c680888c55ff222ab059c139d8adc59ead3845b4b97`  
		Last Modified: Thu, 01 Feb 2024 06:38:59 GMT  
		Size: 58.8 MB (58821218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
