## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:6c6741aa68bf8d4f3798195bfc2337f67e9fff1e742551690ddd0a46a7f59e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:50af96d877c2029ec0232f28f59df1539583cc0272a838a5512dc2d42ce509c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314784410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d59d6628604a91a4c94227e054e4b5f3c6300c183b4ed86c7fe6e51f56b389b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:03:36 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:03:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:03:38 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 20:03:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 20:03:38 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:03:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 20:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 20:03:44 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 20:04:02 GMT
RUN boot
# Wed, 26 Apr 2023 20:04:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef585044f2e536739897cb58b63d90fd8259705b2ea701d530f9eb0462baf4`  
		Last Modified: Wed, 26 Apr 2023 20:20:37 GMT  
		Size: 198.5 MB (198549498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af3ed88188e63333beff482312d43769425ca6f7723003c14db03ea758b10d3`  
		Last Modified: Wed, 26 Apr 2023 20:20:24 GMT  
		Size: 2.4 MB (2361805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dc4d1bc4082c9b8171cc805c58b9d3fb4d02d437362dee12ca9af488b725e2`  
		Last Modified: Wed, 26 Apr 2023 20:20:27 GMT  
		Size: 58.8 MB (58820371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12c5a179f770148a486adf03749b53d873f632ed2fab268fa1b48eb7c5eba3fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310188426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de748cbeab78c7a9054164760285461ca9d36903afeded9f41e5095b8cda43`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:46:17 GMT
COPY dir:8d5d0106b2c3fe64c4905be44080473b7828ffb48e0e107739a7ba7a3cb627cf in /opt/java/openjdk 
# Wed, 03 May 2023 17:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:46:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:46:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:46:21 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:46:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:46:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:46:43 GMT
RUN boot
# Wed, 03 May 2023 17:46:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4d5e76f4319fe5a3ea2caf1641913a58d75b0a1015af977eb92876edf0d64e`  
		Last Modified: Wed, 03 May 2023 17:54:48 GMT  
		Size: 195.3 MB (195324181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b925673b92e09ac3d3b1f2be7ffede6f6d107c00a52bdc26a7d89bf6bf48b2`  
		Last Modified: Wed, 03 May 2023 17:54:38 GMT  
		Size: 2.4 MB (2351092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e62482e0799843f9f6fef3f5e0902aa90ccaf093ed10ceee7eeeb90ce24692f`  
		Last Modified: Wed, 03 May 2023 17:54:40 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
