## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:04c7baef8179306a883fc2013a7d16d71354929bc9791ed57a9aff862fc4d4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:537df2c17f6c13b61d5a635a5f8a55bee0cb89bc3a15e33b50d5e5d35a8a0005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50bd3a9d50f5c9d118ce082612be8f369cb4a50eb4af0d15dda1cd6a25ce82a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:09 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:55:10 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:55:16 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:55:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:55:35 GMT
RUN boot
# Wed, 31 Jan 2024 23:55:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:55:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:55:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56f94c4ac8cf1517e75f20daa59713855b2a987cde3f5a473b73b8fca109c`  
		Last Modified: Thu, 01 Feb 2024 00:12:50 GMT  
		Size: 144.9 MB (144892488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f4c3ff8947ca24726a619dac2b2aecc3370a14051399e92ddc42713524794`  
		Last Modified: Thu, 01 Feb 2024 00:12:39 GMT  
		Size: 2.4 MB (2368750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a794919da05b7033fdb34852494594c7bb3686cc938954ebdb2fb2aadb6b90c3`  
		Last Modified: Thu, 01 Feb 2024 00:12:41 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f11a7810235ef2bc7a1b438a7b1f5416edef7bcecba3ed91f9e250518a6f44`  
		Last Modified: Thu, 01 Feb 2024 00:12:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c31d04da0103425695e37003aa4d30075f801c550dc120251faab0d0bf3b797d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258607610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3587e0951c5d6ae0989246faae761644b86807f677a382eb07d37e032a2429f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:28:07 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:28:11 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:28:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:28:11 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:28:16 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:28:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:28:16 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:28:34 GMT
RUN boot
# Fri, 02 Feb 2024 08:28:34 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:28:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:28:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523444442ef38521daa043679e098a4bc371abf52c97c5b3cc69543c2795e1f4`  
		Last Modified: Fri, 02 Feb 2024 08:44:13 GMT  
		Size: 143.7 MB (143720935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cca7edd385c7b4ceb86405c9f06cee6e67d53c050cb581ce2bf10966082dc7`  
		Last Modified: Fri, 02 Feb 2024 08:44:03 GMT  
		Size: 2.4 MB (2357483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073331134cc196d2eaa50d3a7a92c0803e4de4db0683dc6954bb77e7e001b44`  
		Last Modified: Fri, 02 Feb 2024 08:44:06 GMT  
		Size: 58.8 MB (58820525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c812a69759c597c43b0886e29050cc60a2d53f411d7f0076bc28a0ff715e467`  
		Last Modified: Fri, 02 Feb 2024 08:44:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
