## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:4c23e67f25bdf1b292e24dd93baf2100e6d934d7ecb9ce157e8e8cc115b2207a
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
$ docker pull clojure@sha256:8c1033f9c56ee1f6bf3c386fabca9c0aa62025f6f373d4ebc20c87e67a11be5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258619622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b84ff11b52ef2f8d1f49b4e561cd0a7cf1745ea40f8a8b2611ce42c4596206`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:54:28 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:54:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:54:32 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:54:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:54:32 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:54:37 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:54:37 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:54:54 GMT
RUN boot
# Tue, 12 Mar 2024 01:54:54 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:54:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:54:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e020525753822bd630f3ffa4ae69003bc79371ec735416706e7a5bade6ab4ec`  
		Last Modified: Tue, 12 Mar 2024 02:09:19 GMT  
		Size: 143.7 MB (143720910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2da22c7c1253430b9e6d0bb612e74468a577bf8c7c407b5d8556a58b9b323`  
		Last Modified: Tue, 12 Mar 2024 02:09:10 GMT  
		Size: 2.4 MB (2355770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2df5d6ef20ede5804d89f65fc7912dcec0b934d1ba024a927de973c8b42845`  
		Last Modified: Tue, 12 Mar 2024 02:09:12 GMT  
		Size: 58.8 MB (58820444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2c5f94d0cdcba6781692849a76f466a534e72fcae10c31173129b062ac2d5b`  
		Last Modified: Tue, 12 Mar 2024 02:09:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
