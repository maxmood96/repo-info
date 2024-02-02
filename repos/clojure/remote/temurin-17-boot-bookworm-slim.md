## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:2cf276cd3db427da4c07c7a032905a84dbecaa7af2096e53761fe906ae3c7e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0d71f2b4d7d3e991f6c3ab2bc9240474516217db68d98bff0939ee7afe2bb28d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236366340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b04b70716e053f32f5cc257a754eb1ba3674fffe714851844090dc5804f93ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:40 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:18:42 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:18:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:18:42 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:18:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:18:49 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:19:09 GMT
RUN boot
# Fri, 02 Feb 2024 17:19:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:19:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7efeba6e82ed6b263a3a20620e986ed4521adda8da2894ddc213ef6994c1f`  
		Last Modified: Fri, 02 Feb 2024 17:36:17 GMT  
		Size: 144.9 MB (144893201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ac12725c0bcf261b694ca849ff0f7e6fd1084811e9b78a81a90cd460726f62`  
		Last Modified: Fri, 02 Feb 2024 17:36:06 GMT  
		Size: 3.5 MB (3501748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62dc987f067fb4a1d3a06020bfd2f61ca37be47a43fc94d61120504c5483081`  
		Last Modified: Fri, 02 Feb 2024 17:36:08 GMT  
		Size: 58.8 MB (58820523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe45e5538e6c544d4d59a6d12da49dad3bcb0947410b37c3801383839ef103`  
		Last Modified: Fri, 02 Feb 2024 17:36:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e29934c78329798934ac844e76244ee7e7cf212bb861b5888682b2763a4bc19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235047672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc35f4ba1fcae012bc5358659bbb488a7f2d2dbb35a7f1522761bfb55eb0a732`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:34 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:27:37 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:27:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:27:37 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:27:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:27:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:27:43 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:28:01 GMT
RUN boot
# Fri, 02 Feb 2024 08:28:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:28:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:28:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a2971378842cba2355c934edd4fe1c223f5b855eb23918cd0885b86957c0ae`  
		Last Modified: Fri, 02 Feb 2024 08:43:54 GMT  
		Size: 143.7 MB (143720893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73026963e0d4ef0a95acd2517a0fe68d241390db19d8bfe59d7012ac73e41f`  
		Last Modified: Fri, 02 Feb 2024 08:43:37 GMT  
		Size: 3.3 MB (3324958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f454e86f746a15990e13af7766938010be92ac88414d561c977242fdc2c9223`  
		Last Modified: Fri, 02 Feb 2024 08:43:40 GMT  
		Size: 58.8 MB (58820588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2b58d30a1733543380974e75b7407738d90348ab819bab4b341cd6a73192fe`  
		Last Modified: Fri, 02 Feb 2024 08:43:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
