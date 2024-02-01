## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:152ad81288f14757dcc750d4a60734c404d78068996085903fa05bf35701c252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cd9280db0a15347e36fbaec6ff35841ebd0763d240344f19a7a5d9786494b5c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261517207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60081c8f1cf04197491b3d6d9611e0cd9c3cc9a2535db3fafa28ee08e2120f91`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:49:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:49:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:49:41 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:49:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:49:41 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:49:47 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:49:47 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:50:08 GMT
RUN boot
# Wed, 31 Jan 2024 23:50:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea23dca2c18f20e36988429ad3fd4728d0ec88cdfe95ee9e1b671039deae17d`  
		Last Modified: Thu, 01 Feb 2024 00:09:13 GMT  
		Size: 145.3 MB (145270965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cbf1d78a0b98b2cfda23a01edc29662022ea29f8ed80ff7a82bfc63e28a4ee`  
		Last Modified: Thu, 01 Feb 2024 00:09:02 GMT  
		Size: 2.4 MB (2368701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f46f1027e02f9624bd22df9cb97c5d3b72b31a023cb7ff16ffab4a9eedd244`  
		Last Modified: Thu, 01 Feb 2024 00:09:09 GMT  
		Size: 58.8 MB (58820578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:779eaa67aada80da66e021b52554b064fbecb6a6a0d370d6a9e5483d3880efb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256892802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20959239526c3fe8246206e91a18a8ea057cf42b64900d12e59e9d412ffe47a5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:25:37 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:25:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:25:40 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:25:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:25:40 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:25:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:25:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:25:45 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:26:04 GMT
RUN boot
# Thu, 01 Feb 2024 06:26:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5334aa60b617c8815917a660a8e4e1c07740fd9e60bb51686fab553101763ca9`  
		Last Modified: Thu, 01 Feb 2024 06:42:54 GMT  
		Size: 142.0 MB (142006500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b314e2e7bbc054072cbd598656d3bc2dd6d1dbe154d3909f7c39275089ba93a`  
		Last Modified: Thu, 01 Feb 2024 06:42:45 GMT  
		Size: 2.4 MB (2357408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccd212ad0f71283d1e4db52f11f51a8da4d6b6aea54a53e0b61bb8c164f48dd`  
		Last Modified: Thu, 01 Feb 2024 06:42:47 GMT  
		Size: 58.8 MB (58820627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
