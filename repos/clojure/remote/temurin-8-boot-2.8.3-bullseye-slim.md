## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:89331ddc0e264d13ab1bb3fd3dacba3a8d82badd86b1ede2ab99a4624e94be43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b0444e99d18d2625a97e2aa5fb677d13c78ad03dd144637a0e398627ed1b66e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194900886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e093cd3a69d5df47c8a1cee16e99272e1d18ec336ed2fa3946b8c336e29c7ff`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:22:28 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:22:29 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:22:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:22:29 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:22:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:22:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:22:35 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:22:54 GMT
RUN boot
# Wed, 20 Sep 2023 07:22:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d904e0e0acb14ab36621cdb61a83d87d553b53cafbe8016f9cc443e19e4ff9`  
		Last Modified: Wed, 20 Sep 2023 07:34:08 GMT  
		Size: 103.6 MB (103585017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cf35b44da32661093b4ddd9add983354404c7a45f367c4ec3c3d26758427f7`  
		Last Modified: Wed, 20 Sep 2023 07:33:59 GMT  
		Size: 1.1 MB (1077545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7598c6f5715661f815ee95340cc6a5108ec1514462c74b0c2b5b8d6ab9c2ae`  
		Last Modified: Wed, 20 Sep 2023 07:34:02 GMT  
		Size: 58.8 MB (58820613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b23d14aeb7274b50175b2ac7bae3c97402d7a87c60e035a5e8a7c19908ef211
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192638451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d5a602fc1c3b6037fdbaef828bea2dd2e077a87305c551db76d19d0b3b85b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:04:32 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:04:34 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:04:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:04:34 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:04:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:04:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:04:40 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:04:59 GMT
RUN boot
# Thu, 07 Sep 2023 09:04:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256b28be577c49d6f216cda63c69699c76582076b787ffcf77067af08f7f0490`  
		Last Modified: Thu, 07 Sep 2023 09:14:43 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d3fce16ad3a2ff224c1775775cc4dd675ceb7f04d63ddfc3bdddeff78427a0`  
		Last Modified: Thu, 07 Sep 2023 09:14:36 GMT  
		Size: 1.1 MB (1064790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018c45e58b39621d1ee1b2c7978343570ba43ffcba167dff9d9f85f6436ba279`  
		Last Modified: Thu, 07 Sep 2023 09:14:40 GMT  
		Size: 58.8 MB (58820300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
