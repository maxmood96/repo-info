## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:466964aa61f5bf2c2a4a1f450e38aeb8a7db1da08a445ed163859a40e9e1cb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4e56041cb7848f901ee8a212c3d8c5ac74ebb8bbd90229bd018d6c1b9369efc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261067780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8625a1ce294031278e7da08e4229b2d4b484f20c81c71602562da3720551ec`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:17:02 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:17:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:17:03 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:17:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:17:03 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:17:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:17:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:17:09 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:17:27 GMT
RUN boot
# Fri, 28 Jul 2023 03:17:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df166fc4715d337f554c5b6904774af766db5e850d3500e12eeafae147f25b5`  
		Last Modified: Fri, 28 Jul 2023 03:29:39 GMT  
		Size: 144.8 MB (144829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782dd0817ff7e751ac7cd7df09cc33a27a370534e24fee77783e54db7141dc6`  
		Last Modified: Fri, 28 Jul 2023 03:29:28 GMT  
		Size: 2.4 MB (2362154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e460839bb1b401df6827b07db7e0ed6f07eabe288406ea41a9d077b1bb1b73ee`  
		Last Modified: Fri, 28 Jul 2023 03:29:31 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2aac5971e1a1dae8d74bde0c9e2681de8977b235179e65b6fe0f9d9fd73b237b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256442107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318139d36143cb69444bc598d3aec1a8d1a7688642000b76652aa02effaa5503`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:32:41 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:32:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:32:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 14:32:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 14:32:44 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:32:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 14:32:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 14:32:49 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 14:33:09 GMT
RUN boot
# Fri, 28 Jul 2023 14:33:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c090d6125b47746cd211b7c7a3115e5035be71f75f3c71fa40f7596d4be055`  
		Last Modified: Fri, 28 Jul 2023 14:41:36 GMT  
		Size: 141.6 MB (141565337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1d5bbb3e7510c871fc96bcf9832345f10b7202f7f3d48d3dfdb458d23271d6`  
		Last Modified: Fri, 28 Jul 2023 14:41:28 GMT  
		Size: 2.4 MB (2351416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5df275f05f6e207259b4f631c56a2509e5d742571b60d49b41e8138dea64b`  
		Last Modified: Fri, 28 Jul 2023 14:41:31 GMT  
		Size: 58.8 MB (58820564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
