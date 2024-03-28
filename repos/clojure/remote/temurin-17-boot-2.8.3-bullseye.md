## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:660d23d23c995451ce0ef15cb15507d1a6aea45026285a49afd62b6499a279e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f69ab445c548844ce51d89e909be54e43c85364bb33f35c864382d07b74abd44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3527570b8afcf45cbc55d2dec0c172a724348fd03e74b0e555e15ec0d09cfe9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:07:20 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:07:21 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:07:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:07:21 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:07:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:07:27 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:07:44 GMT
RUN boot
# Thu, 28 Mar 2024 03:07:44 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:07:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:07:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bcd404f330742d08e449c864937a0247411adf1e0630d702b0d270a8c84eae`  
		Last Modified: Thu, 28 Mar 2024 03:24:58 GMT  
		Size: 144.9 MB (144893082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9decfce24eede648bd63be5c7b15fc6535a164fdf5fa89966110bc04239289`  
		Last Modified: Thu, 28 Mar 2024 03:24:47 GMT  
		Size: 2.4 MB (2367343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408cad15645ddc894e32ca3732e76d0f015e5447071d8a3f8d6c2e39b1e31bfa`  
		Last Modified: Thu, 28 Mar 2024 03:24:50 GMT  
		Size: 58.8 MB (58820384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574389fb16552f0c8a2ece16841f81c19ded6ee831473bec0128a9dd7227c8a9`  
		Last Modified: Thu, 28 Mar 2024 03:24:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0fff1c2d017c6ec6ce353013b7b2e4cb907ed1df57d34268e4cecd10b41d9f07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258619611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7571c8421ca196be5051c64f8090a64e1e360016097993435be49fc1393de419`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:59 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:40:02 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:40:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:40:03 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:40:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:40:08 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:40:23 GMT
RUN boot
# Thu, 28 Mar 2024 02:40:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:40:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fcbeb5850480786ffe08e1502f043ad8bc5d2f3b44ca90dbf17efaa841dacb`  
		Last Modified: Thu, 28 Mar 2024 02:54:18 GMT  
		Size: 143.7 MB (143720923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454020489f7256bfc6faa582ba534813aa003dcec54ebbf721aa481078e4ff75`  
		Last Modified: Thu, 28 Mar 2024 02:54:09 GMT  
		Size: 2.4 MB (2355854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710a9b3d1aec8738d650ca2c8860514eca0b87e99b06224fa9c2379d2a526e73`  
		Last Modified: Thu, 28 Mar 2024 02:54:12 GMT  
		Size: 58.8 MB (58820334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29f7079631e1f5ab74e2eadfc0185cea41ebe3eb59709f27f0502465d05016e`  
		Last Modified: Thu, 28 Mar 2024 02:54:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
