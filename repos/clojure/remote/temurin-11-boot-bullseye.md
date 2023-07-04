## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:124bf695926f0d0f64930d85b690b69cbb261937d30daa6835a6e8a8bde9ea72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1fe00aec137b5f8b6871aae1ecc75742387991c35528d1d304e5b60017f2abc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314787074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268e40203262e40d2556934ebbf1fea57951b32efdb16057d8c409c6417d2a3d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:03:00 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:03:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:03:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:03:02 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:03:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:03:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:03:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:03:26 GMT
RUN boot
# Tue, 04 Jul 2023 04:03:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b5fb32c7c13fc3044e1370f05931aae1497f5be699a0ec5bf4c0e665c4881`  
		Last Modified: Tue, 04 Jul 2023 04:13:22 GMT  
		Size: 198.5 MB (198549439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3def4527e47ef333285ccaa3b9cbbe86fe95f3dbf96acf1f91a257015dba13`  
		Last Modified: Tue, 04 Jul 2023 04:13:09 GMT  
		Size: 2.4 MB (2361935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b97c71b5d05d701a169e501fe9ae9e90ba8fab91e7e8f16d079d9ab7a68bf9`  
		Last Modified: Tue, 04 Jul 2023 04:13:11 GMT  
		Size: 58.8 MB (58820400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d04067274042e13cc6c1486418d4dbf6492195e58289eab714146db12bf08744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310200225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92afdfe414f409f8b5172cbf2ed330ccd2f75829c027f25356b35b4eb0eede`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:41:42 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:41:46 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:41:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:41:47 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:41:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:41:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:41:56 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:42:14 GMT
RUN boot
# Fri, 16 Jun 2023 04:42:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b429dc913a313200e2709dc18ae8c848cf538439e00d089ddee5b4541385cd44`  
		Last Modified: Fri, 16 Jun 2023 04:54:03 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf71a08da7f244340b9830b1ca93d79f63ac4fa070dc7c70c3abeefa93dcf31`  
		Last Modified: Fri, 16 Jun 2023 04:53:52 GMT  
		Size: 2.4 MB (2351346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84315f8cf675e5ebc8e532fa123e6a35f24c1eb9a5c3d9a0b512bb8294e4ade9`  
		Last Modified: Fri, 16 Jun 2023 04:53:55 GMT  
		Size: 58.8 MB (58820555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
