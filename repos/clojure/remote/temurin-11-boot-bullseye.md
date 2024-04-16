## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:747090d18e734f14fa05de2d7c6792cd3e5ed0620f4d60794374aed9b8d8cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:410af06fd3663d7a4710c51d187318817b3a59627466ebeea056b1dbd458bb84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261549262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210362b5d94f99c2e179a7c4dd4140aa69f86a9681a42c864a0745a334878189`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:23:49 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:23:50 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:23:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:23:51 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:23:57 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:23:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:23:57 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:24:16 GMT
RUN boot
# Wed, 10 Apr 2024 06:24:17 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c507d9904bfeb82b742f3c4fa084d1261c4ed6c24cac8b9671dce60380a20c`  
		Last Modified: Wed, 10 Apr 2024 06:43:04 GMT  
		Size: 145.3 MB (145271259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6325d34a2deeec6e53a0d672742b597cc06a17ad049e235910dcc4486e577ccc`  
		Last Modified: Wed, 10 Apr 2024 06:42:48 GMT  
		Size: 2.4 MB (2367270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffc9ba2807172a0dcfb315a564a266f4bab6fb7c9fb9eba96e8342bd61a963`  
		Last Modified: Wed, 10 Apr 2024 06:42:50 GMT  
		Size: 58.8 MB (58820469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75c9c4a48e319fc0d3be70a690b50b85d16aa79293d4f097c8e812e0a36dad98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256911943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b8c1122e4837f45db5b8c106932832038fd89a96010df74563db60ce720b4b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:33:45 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:33:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:33:48 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:33:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:33:49 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:33:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:33:55 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:34:13 GMT
RUN boot
# Tue, 16 Apr 2024 06:34:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c70dc33680c6cbcc872c11af38e2d83af8622a965f0d2d3c904c999ffaa3062`  
		Last Modified: Tue, 16 Apr 2024 06:52:48 GMT  
		Size: 142.0 MB (142006343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ceba4a38681dd3855cf4462f26642eed61dac7af4a22cb02d0739ab1df1907`  
		Last Modified: Tue, 16 Apr 2024 06:52:39 GMT  
		Size: 2.4 MB (2355823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878c182fcf970f1335ae60ece1bf8c75bc8a6e992574469f8cd6b3361dba4c6a`  
		Last Modified: Tue, 16 Apr 2024 06:52:41 GMT  
		Size: 58.8 MB (58820601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
