## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:7c6054390050fb9d2e1ba7d2c65ba965729f2b8855b1e278f02fe5b13c6c2288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:30036cd928b0b97d4bce66e5214384364a10d5355c996a25053dc9e09eee22fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236710859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1854aa090ef9c39e9b66c1f757b7dbef2d65bd3752585dc3d1dc12e5c8d7f9f7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:12:44 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:12:46 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:12:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:12:46 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:12:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:12:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:12:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:13:12 GMT
RUN boot
# Wed, 17 Jan 2024 14:13:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e59b0c3a1054d7599b0559304e1fa8dfff032ed3a6c616f721251dfeab2403c`  
		Last Modified: Wed, 17 Jan 2024 14:49:10 GMT  
		Size: 145.3 MB (145266431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c1609049de3c2ca473d9a7bbcacc0dfc42e58e0a2f3d25f7384b57ebc35a`  
		Last Modified: Wed, 17 Jan 2024 14:48:59 GMT  
		Size: 3.5 MB (3498043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829b60a925c6cdc873a9c892d1e5ade0cfbcf089be091830bf4d3028263969a4`  
		Last Modified: Wed, 17 Jan 2024 14:49:02 GMT  
		Size: 58.8 MB (58820464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42a4c15cef20ca92cbfee333bc4b8deea312454853498dc59aadd797fce6d0bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233302062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77ecc6c5f0cad5602dae4dafb34240173e2e21a4d9d01118f6b33ad41525353`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:22:51 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:22:55 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:22:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:22:55 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:23:00 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:23:00 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:23:18 GMT
RUN boot
# Wed, 17 Jan 2024 09:23:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d60c914cfd6ec29bbb66007b64711eda23d84d570031776b4a970869ceec77`  
		Last Modified: Wed, 17 Jan 2024 09:38:34 GMT  
		Size: 142.0 MB (142002109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4588d5db3ef8889c93c6e400e9c9c631854d4cd5dd52f4a84c2d76bc76ac311a`  
		Last Modified: Wed, 17 Jan 2024 09:37:55 GMT  
		Size: 3.3 MB (3322002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252e06534d3e3d9957e039132780335153a19cdca8ef332b7a1a6b440a3dcb3b`  
		Last Modified: Wed, 17 Jan 2024 09:37:58 GMT  
		Size: 58.8 MB (58820616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
