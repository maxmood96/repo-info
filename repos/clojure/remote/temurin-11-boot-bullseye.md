## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:5ec44170179070ffba1c3cb328df5884280895115b99d6ff822e329ff4ff1a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e49ab3e64582d7ed0bbefd58a22b40a8ebd001cdb04521378633b20d6404b310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaeb9b41cec6960eb46472f3aeeeb10969cdf8c538f7c1635b1b21b2181a8d6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:44:00 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:44:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:44:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:44:01 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:44:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:44:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:44:07 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:44:26 GMT
RUN boot
# Tue, 31 Oct 2023 00:44:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8783e157202ff66c1d853d56e97fa10361d4b4bc746c69f6cf3062eb255816`  
		Last Modified: Tue, 31 Oct 2023 01:07:27 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1be71d4c27a189899a1d1371182821aeb7a7fb3c8985e574faa71e8896058c`  
		Last Modified: Tue, 31 Oct 2023 01:07:16 GMT  
		Size: 2.4 MB (2368767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858a81ed44faa00f3e0d4bcc69a65bdb52b06f88ce350460574662e62d1af0ea`  
		Last Modified: Tue, 31 Oct 2023 01:07:20 GMT  
		Size: 58.8 MB (58820512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89cf19b860790d52616b176edde9d21c8238f5aee74e81dd7122632804135e38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17f8c40be5eddef6fc43fd157222453f8d9a29b9900ce4b18a8bd63fa83174`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:57:56 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:57:59 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:57:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:57:59 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:58:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:58:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:58:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:58:22 GMT
RUN boot
# Tue, 31 Oct 2023 00:58:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314cc05ddbde5072f40f29d8bb5b7ee277835c4cdd222b0e3cb1fc866cd351c`  
		Last Modified: Tue, 31 Oct 2023 01:17:58 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e509e41aca71233b843df12cd3dce57bfacc0633598762d9b8c26f2f76fc60`  
		Last Modified: Tue, 31 Oct 2023 01:17:49 GMT  
		Size: 2.4 MB (2357450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b83d19e864f8f82d3bef9d5f4a2f91b3eb89fcc42da63edf2f3b218ee25d1a0`  
		Last Modified: Tue, 31 Oct 2023 01:17:52 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
