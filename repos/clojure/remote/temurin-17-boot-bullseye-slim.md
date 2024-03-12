## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:1fa339c7f8b97b01209f6c54c3b76a3a52e2f35eda4267aaf14fffd493dddf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

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

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1205115a81397a8edf95fc954e69c0c50eef09c5be622347518dfaa98d6a9bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233678014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d4ce55414bbb5fed19aec9c1acc77c94b6287ceb6cc8b65676b7afbc1f707`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:55:02 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:55:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:55:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:55:05 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:55:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:55:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:55:26 GMT
RUN boot
# Tue, 12 Mar 2024 01:55:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:55:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:55:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59badeb8d34bbf0f51ece5436f47477d1f2cda915511a427b5878125211f50d`  
		Last Modified: Tue, 12 Mar 2024 02:09:36 GMT  
		Size: 143.7 MB (143720928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c2f6ea7eb957b653f3c8bfdc65dfa8da9b05d28c185e10114d363014a8b10b`  
		Last Modified: Tue, 12 Mar 2024 02:09:27 GMT  
		Size: 1.1 MB (1064975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae849a945418af3fd5fa08a6254fe062459db13421b0fd540d77634b964cf5d7`  
		Last Modified: Tue, 12 Mar 2024 02:09:30 GMT  
		Size: 58.8 MB (58820594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73d601f70e3da7e42fc37450f2d5733303ff7baef1829141e10176d68fbe943`  
		Last Modified: Tue, 12 Mar 2024 02:09:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
