## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:b8784b62fe2b33249ce10c85f4341c2485c8b7da2da5e9f08b1d66038c77450a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:306f65108331727ee364e07cdb60ec1edff74e3fefb8ae114308633383e9385d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f169d13e3bb9ff105f54568447066ebf73c6f605efb8f0715d4f8bcbbc83d07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:11:09 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:11:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:11:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:11:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:11:11 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:11:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:11:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:11:35 GMT
RUN boot
# Wed, 06 Mar 2024 14:11:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:11:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:11:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6eab155a0ed2d9028ca2f4a82935d930aace1dae36184ea7a85b71e3543e8f`  
		Last Modified: Wed, 06 Mar 2024 14:28:52 GMT  
		Size: 144.9 MB (144893105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8fc433683d2051e8d4896382c908412ded028a0e83c26260700b61792f54c`  
		Last Modified: Wed, 06 Mar 2024 14:28:40 GMT  
		Size: 2.4 MB (2367298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e59e237c46dea8faa1767b39c2a3ac9934a8309fbf88908214b473a609a030`  
		Last Modified: Wed, 06 Mar 2024 14:28:43 GMT  
		Size: 58.8 MB (58820362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975918d2199300033840caa38a50df8019ffdd3952c7430c82be7748e0ae338b`  
		Last Modified: Wed, 06 Mar 2024 14:28:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3de021688ce3a06e76dd3e2ca6b1b00e7be6846ae7de45129eef6639aca2aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258618967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccf008c4b26fd922f2adf178be97f7bcc55e3f5a51cbf821574e46d0f6529d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:23:54 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:23:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:23:57 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:23:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:23:57 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:24:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:24:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:24:03 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:24:19 GMT
RUN boot
# Wed, 06 Mar 2024 13:24:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:24:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:24:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6455a65bd6ad4d9673722258d4cd56d6bf8df5927f8fc237ec05a3773a3bfd50`  
		Last Modified: Wed, 06 Mar 2024 13:38:33 GMT  
		Size: 143.7 MB (143720835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f01078cf1dba5893e33e3981cb3b8dcd7ecee4035830591dd12c3e4f987496`  
		Last Modified: Wed, 06 Mar 2024 13:38:23 GMT  
		Size: 2.4 MB (2355821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e086b819a688c2f3c37a7dc4df1bae111eb189f8835ebf8bbc332601a9cdd98`  
		Last Modified: Wed, 06 Mar 2024 13:38:26 GMT  
		Size: 58.8 MB (58820424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8dba64e29497927b847e2a07c6a0cca59b6a6e7afb80c4246f5b51a465f8b9`  
		Last Modified: Wed, 06 Mar 2024 13:38:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
