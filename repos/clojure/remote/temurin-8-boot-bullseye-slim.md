## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:00e895bc16a5c55180e9d85b2f46c69ea321f6a1de6678068ad1a06051a646ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfcf70ae7bea27d34c1cabeb7ad9e0934a9afdb3f39dc882e1d67044f6b8e0ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194902705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3ef2757688444239216719c09dd1af61faf733e4a5581b770324b9e54fad9`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:52:00 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:52:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:52:01 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:52:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:52:01 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:52:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:52:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:52:07 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:52:25 GMT
RUN boot
# Wed, 11 Oct 2023 18:52:25 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3e4eff0060ac1af3402a6f29c395f2ef52fc165d154de228b912c193fc9f45`  
		Last Modified: Wed, 11 Oct 2023 19:03:44 GMT  
		Size: 103.6 MB (103585038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd35d087cf90d45afe133b344f0b1dd2ce7c7e2b4f5e7e86740a9dac46f36b28`  
		Last Modified: Wed, 11 Oct 2023 19:03:35 GMT  
		Size: 1.1 MB (1079474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221816ec453629d671258cd3f9845659930a30637c626bb2a68524c02e558c8`  
		Last Modified: Wed, 11 Oct 2023 19:03:38 GMT  
		Size: 58.8 MB (58820331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:caa24f89c85dd82c4d97f8383b9c459f5e4b80fdc7862357b969e4c78ae8dd1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a552a51d8dbdb185671fc247628ac0f542c01ae43d61fa544fe85511694022`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:46:09 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:46:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:46:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:46:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:46:12 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:46:16 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:46:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:46:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:46:34 GMT
RUN boot
# Wed, 11 Oct 2023 18:46:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865ba808396777a6b8ccd88f4ace2c7e93ce0815719cc60a7da9ffb2bdb63662`  
		Last Modified: Wed, 11 Oct 2023 18:56:27 GMT  
		Size: 102.7 MB (102690512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63de560d7e7ee0a91861d7ef41397222bf1c7ad7e17b3680e4fde824d86a02a`  
		Last Modified: Wed, 11 Oct 2023 18:56:20 GMT  
		Size: 1.1 MB (1066851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1288a05683bd8f948d2f3f6729fc61655ec8a1d4beb85b9f762c46bcb95ce73`  
		Last Modified: Wed, 11 Oct 2023 18:56:25 GMT  
		Size: 58.8 MB (58820582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
