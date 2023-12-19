## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:4d237e5e82b4e59f27bfa96d452f9e8320083f3e95525a4c689f3470ee6bf9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:283e8b556f579cc9dc90598b6a5d379f84947201a291cb7e13d9ea403ca05e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236710916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20954fafc0bc75fb87cc41f0a5124ffb443c4b468105fa38d115f16cf54351c8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:05 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:59:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:59:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:59:06 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:59:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:59:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:59:31 GMT
RUN boot
# Tue, 19 Dec 2023 06:59:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f381a6c442e4c567d840bbe8d23ac05753126b0641011e48b804c55c4b6c27`  
		Last Modified: Tue, 19 Dec 2023 07:18:32 GMT  
		Size: 145.3 MB (145266436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e32a5efd3222685fd05b6a78b1671440ff164da8cae866b560b032ffea5bd6`  
		Last Modified: Tue, 19 Dec 2023 07:18:21 GMT  
		Size: 3.5 MB (3497966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba161d2ebe3666b90bb5deba32dd5bb7cf54c9daa0794301eddc927fb76b2402`  
		Last Modified: Tue, 19 Dec 2023 07:18:23 GMT  
		Size: 58.8 MB (58820551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c020f2206c7b0e32a97fd9d0132acbf3fc372affad33f377530dce6b8baba55e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233301520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f550692f103a8962e323a3d9275763a338be6bbabca24398db6880fd915525`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:31 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:59:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:59:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:59:35 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:59:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:59:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:59:56 GMT
RUN boot
# Tue, 19 Dec 2023 06:59:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3caa98fe64b6e771f2487121c32bd24ed3c1efe0b70cd6eba73ff5a9db11b6`  
		Last Modified: Tue, 19 Dec 2023 07:16:03 GMT  
		Size: 142.0 MB (142001823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd17915340db71b8388a9b788f875fcff51ae38204fa64804f1dbef7814d57`  
		Last Modified: Tue, 19 Dec 2023 07:15:54 GMT  
		Size: 3.3 MB (3321991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5d7c6012bf97911da4a9a0a64993365bd66dd367871051dd133ac982907fa2`  
		Last Modified: Tue, 19 Dec 2023 07:15:57 GMT  
		Size: 58.8 MB (58820437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
