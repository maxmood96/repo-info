## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:c31d4eaaef126f88cd80179d619cce189849a0011ccd2976634788bfc5b0ace0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2626ca93ce8dea52a2e5ce0ace373e77c72f154891e3a03c3a8c9971da13a5ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f80dd7dd69034c423b8d6bb8dafaff6fc009baf2bd2da6a25690a3dbf7cf147`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:09:55 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:09:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:09:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:09:57 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:10:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:10:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:10:04 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:10:24 GMT
RUN boot
# Wed, 06 Mar 2024 14:10:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:10:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:10:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16509130f52dbe6d465329f39db40d29a6c2c14281e633450baff6de75121859`  
		Last Modified: Wed, 06 Mar 2024 14:28:11 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14849b23f9db43fc95aa23f3f0277e5a6374746f72c350bba0da6c21c48abb`  
		Last Modified: Wed, 06 Mar 2024 14:28:00 GMT  
		Size: 5.5 MB (5527203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d83f5107ffae2406a3101cedea5d23e44551d7cbf663455d149b9c4c6fc487`  
		Last Modified: Wed, 06 Mar 2024 14:28:02 GMT  
		Size: 58.8 MB (58820474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd9fa4b06c932a45000534d7e73ecb6b9fc5ddd2d7b27a81e98033d6e6d4597`  
		Last Modified: Wed, 06 Mar 2024 14:27:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f66d3e663f447a7e044d0870fd57b0c28e1ee0599623994a36fbce382a943a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f507b200859c499e240d4e22606b28cb4d6c6d72c0ecad9e0549e290b483a61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:53:22 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:53:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:53:26 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:53:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:53:26 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:53:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:53:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:53:48 GMT
RUN boot
# Tue, 12 Mar 2024 01:53:48 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:53:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:53:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443552151656ad6d5da787f634193a1ca51b30410c526ec21a27bae6141632c0`  
		Last Modified: Tue, 12 Mar 2024 02:08:44 GMT  
		Size: 143.7 MB (143720910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac2b542e43fcf8b62c6a8eb2d54988656a7ca6a2253bb22848271f726595504`  
		Last Modified: Tue, 12 Mar 2024 02:08:36 GMT  
		Size: 5.3 MB (5349353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30cb4a5695278748b7b3e28760e999d5640566e108df88e2aa0f0684decc30`  
		Last Modified: Tue, 12 Mar 2024 02:08:38 GMT  
		Size: 58.8 MB (58820367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e03d561c3cd30cb8d169adca8a1fe718080331b0adc33f42620fda871a3d1dc`  
		Last Modified: Tue, 12 Mar 2024 02:08:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
