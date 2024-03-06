## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:0750eb714b3367b2d67551bdc7edbf55fea577e8b356206dc481ee4077bd2cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:15cb61733634cef1fed363e984e10482c85458497502432a0428dcc9bb57d0d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236213979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d0cddbdb4c7ab96fa42fef2f742dd870277f42245314e2758175a7b18d86e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:11:44 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:11:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:11:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:11:46 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:11:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:11:52 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:12:10 GMT
RUN boot
# Wed, 06 Mar 2024 14:12:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:12:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:12:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d972ea79502e7e2f800aa3c0a6f461338ca6315edfd2710e566531c30a8da3d1`  
		Last Modified: Wed, 06 Mar 2024 14:29:14 GMT  
		Size: 144.9 MB (144893135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758c7fa5526e3bb33f0151c4f592c63f5bcdf01d27d3c0b7b8d338d91f02bf0a`  
		Last Modified: Wed, 06 Mar 2024 14:29:02 GMT  
		Size: 1.1 MB (1077668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fae94acaf69ca4a8188c18c0c2be910af1169c83849155cc30cbf605623b01`  
		Last Modified: Wed, 06 Mar 2024 14:29:05 GMT  
		Size: 58.8 MB (58820351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404d47ba43c3b416888e15e457073ff5d85a9156a157453538cb2f7ba14c2d1a`  
		Last Modified: Wed, 06 Mar 2024 14:29:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:742e83f6527ca1af0deeac6baeef5de9c2563184c14263cf405adbc707df2eec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233677809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b081c3510bb31579e76dd291cf05b16027bc7a390178f5ee435720815151dedc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:24:27 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:24:31 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:24:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:24:31 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:24:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:24:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:24:36 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:24:52 GMT
RUN boot
# Wed, 06 Mar 2024 13:24:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:24:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:24:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf35eb2bf4fc602ed30acd3561a79fab4f053e204653890e517eb9ffbcbb39`  
		Last Modified: Wed, 06 Mar 2024 13:38:51 GMT  
		Size: 143.7 MB (143720928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34704a7c980262bf14e05bc85b4ad9a92949dcb2bf97d6c7779250f88c11b05e`  
		Last Modified: Wed, 06 Mar 2024 13:38:41 GMT  
		Size: 1.1 MB (1065002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6cf62c6268154e31a57e04616000c6e9894fde70473c43af7a033f22f9d687`  
		Last Modified: Wed, 06 Mar 2024 13:38:44 GMT  
		Size: 58.8 MB (58820402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6f3ab6fa482ce5b64588916777f9e411adf973a81e13f83f1ac2a68e13ca34`  
		Last Modified: Wed, 06 Mar 2024 13:38:41 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
