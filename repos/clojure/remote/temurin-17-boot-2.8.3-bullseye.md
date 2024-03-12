## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:514f5cf95dcb3f8daa0b787d98e1fc8661117af01e386d95838e8f581822c18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4f0e4fdf9b902ebb101670763fa9248645baf028871444be37ede142f80065a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acab1f83f9f8850bd0129d62062aed8940079207cbf147d7a919a4cfef09988`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:23:40 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:23:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:23:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:23:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:23:42 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:23:47 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:23:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:23:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:24:05 GMT
RUN boot
# Tue, 12 Mar 2024 06:24:05 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:24:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:24:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0a6dff1d086a6e22a033f3e8e82ecebda2cf307ef106d9c945377612642e65`  
		Last Modified: Tue, 12 Mar 2024 06:41:11 GMT  
		Size: 144.9 MB (144893135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749c08c7440727ae62c3b2d0dbec9a1a6b7cf00c8dc664dd3e603f2fc1c7ecda`  
		Last Modified: Tue, 12 Mar 2024 06:40:59 GMT  
		Size: 2.4 MB (2367238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a838ac9124cfcb3e1ae1437f5fe73672b6777b0f2c9d5ad7a1e45c87e6d9a4c`  
		Last Modified: Tue, 12 Mar 2024 06:41:03 GMT  
		Size: 58.8 MB (58820627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af95e85e50425e1e1bb938f018f166897e2eb51eae5b56dc778bfb29a07c42ea`  
		Last Modified: Tue, 12 Mar 2024 06:40:59 GMT  
		Size: 400.0 B  
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
