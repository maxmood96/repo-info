## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:02fc5852dad1c3681ec64bbd3113f0c1a8ca1767802435f0a099ed22f68f30c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ca912d404d2ede1e7b3e327c5e7815012aaec6e6cc0a400cb129f5c471741eaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856609b824efb8fbcf54967ed067725fe455729ec38c55f519a4fdef6dfd2864`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:12 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:59:13 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:59:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:59:13 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:59:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:59:19 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:59:40 GMT
RUN boot
# Thu, 11 Jan 2024 04:59:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f52cc9014579cafc22fe8590ab39539d23432b192e36ae88e348b78be356b`  
		Last Modified: Thu, 11 Jan 2024 05:18:20 GMT  
		Size: 145.3 MB (145266339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cfb05a37a6f2559cd47cec42cb3e7a91e32147b254f60e169579e2fb24d2d9`  
		Last Modified: Thu, 11 Jan 2024 05:18:09 GMT  
		Size: 2.4 MB (2368668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d50459e8efd943826cba7cd07f93f8b46217069932da143dcdfb8ca3eb44dd`  
		Last Modified: Thu, 11 Jan 2024 05:18:12 GMT  
		Size: 58.8 MB (58820737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05b4e16ce43abbe176c7ac750a1f58f8db69fbf9d8f3c9c8ebbf7ea953e91760
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f524f0d270da622573c471bc0bc05c2446ec107c3a75a0e454852a5d7ec5ced0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 08:05:01 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:05:04 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:05:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:05:04 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:05:09 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:05:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:05:09 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:05:27 GMT
RUN boot
# Thu, 11 Jan 2024 08:05:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba11ae3a10b8853b170f41cbd5cd5fc8190585468f9d264c1390459d38f55f90`  
		Last Modified: Thu, 11 Jan 2024 08:21:30 GMT  
		Size: 142.0 MB (142001834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12113e73576496aa6edc112a2295cb1ba96bb8c4862be71d3cb8a8f6416e36c`  
		Last Modified: Thu, 11 Jan 2024 08:21:21 GMT  
		Size: 2.4 MB (2357357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04aa570184a0c55cebf36e6a891c20f1bf6e547166087fa983208df189f885`  
		Last Modified: Thu, 11 Jan 2024 08:21:24 GMT  
		Size: 58.8 MB (58820598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
