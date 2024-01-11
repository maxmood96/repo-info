## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:7d1ffe619ff5f0087d80eb7394cc951966caf284af81141d2a5ba535a9f75d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4ad0854dc57a49801989346daef7eead45a38dd2099e79babf4632ec521038eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195042755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f330ee2d28038afeea7017feffd0ec5f151e1bb6e64469a4b77b9e55f0bd7d43`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:52:51 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:52:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:52:52 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:52:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:52:52 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:52:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:52:58 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:53:19 GMT
RUN boot
# Thu, 11 Jan 2024 04:53:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41492172c513e0c35ae3de357172c14ef468d726ab40d09ad746949a02755019`  
		Last Modified: Thu, 11 Jan 2024 05:14:38 GMT  
		Size: 103.6 MB (103598264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3e4d44dce0b7300f70d52476c436f9975787f7ba3c96d11a47c9e1508c5beb`  
		Last Modified: Thu, 11 Jan 2024 05:14:30 GMT  
		Size: 3.5 MB (3498019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c3d0c8159b9215b8f2962162bd886eb6bf5c72ae85f8ce29d5b50d88f49736`  
		Last Modified: Thu, 11 Jan 2024 05:14:33 GMT  
		Size: 58.8 MB (58820551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a052020c9791e7db0072a4f967d81cfdf47acc2369c529ac305b9ccca57bab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194001401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb7a430b3500bd6f67ea5ae5634bc7e8c649ce627bc9dc247d059e126d34b3e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 07:59:27 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 11 Jan 2024 07:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 07:59:30 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 07:59:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 07:59:30 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 07:59:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 07:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 07:59:35 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 07:59:54 GMT
RUN boot
# Thu, 11 Jan 2024 07:59:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0891c1c0e7c32e5ef639b94142b51a08660a832afa5cb3d34133aead30c39071`  
		Last Modified: Thu, 11 Jan 2024 08:18:15 GMT  
		Size: 102.7 MB (102701520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb64012fd034c659935e0f0ef70829829cf08cd8ef12d5b41f79271a0f830a6`  
		Last Modified: Thu, 11 Jan 2024 08:18:09 GMT  
		Size: 3.3 MB (3321987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e704fcc9020a422c01d7e36e17026f7b5488b6587812c4f646ab940f5c76`  
		Last Modified: Thu, 11 Jan 2024 08:18:11 GMT  
		Size: 58.8 MB (58820559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
