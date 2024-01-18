## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:7f2dcbe7af069ef797f8734db8f6f1c511534ac8a0981c7f3316c58088cd4197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:07f22d8b554b9ab8203ab2b880425049376b3f70a831c78d355171f4a82881d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2055c0ee4b044a4448c0c7a8c96225b3941ced94dffc6dcc036dd4c9841d6339`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:20:20 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:20:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:20:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:20:22 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:20:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:20:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:20:45 GMT
RUN boot
# Wed, 17 Jan 2024 14:20:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 14:20:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 14:20:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5b6c19e935fceec282e83861770b734b59de4956764e9c1adfed13faa3893`  
		Last Modified: Wed, 17 Jan 2024 14:57:29 GMT  
		Size: 144.9 MB (144873945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37282bace9a688216c169ee2273e95aba4f60e5e27e83df76ea2030e0c32bfdf`  
		Last Modified: Wed, 17 Jan 2024 14:57:18 GMT  
		Size: 2.4 MB (2368749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ab0136c6e74d8ff27581031e38ac1ab34398b2ac2835d526d5d434088f963c`  
		Last Modified: Wed, 17 Jan 2024 14:57:21 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8412e06cb1501b1d2f8778528e4acf3a001906ea270dfc6a92347429839c9ee1`  
		Last Modified: Wed, 17 Jan 2024 14:57:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99f0d2bc3e87e22532e07f389cd89b08947b8be5e7ec07e31d21e3dd9d1468f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d4f77b95a1cd1b5e13b8da1252ff1cbd2ed0e550e5947b76a3305abce6f1ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:29:07 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:29:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:29:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:29:10 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:29:15 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:29:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:29:32 GMT
RUN boot
# Wed, 17 Jan 2024 09:29:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 09:29:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 09:29:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181c697a313f5492a0ffdbc55abec383164f1aa430b778987b9ebd7cc657d82`  
		Last Modified: Wed, 17 Jan 2024 09:42:28 GMT  
		Size: 143.7 MB (143681767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac410946a2da45268c088892454844815969396104bf974ef5f7c0e561c7ad1`  
		Last Modified: Wed, 17 Jan 2024 09:42:19 GMT  
		Size: 2.4 MB (2357420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7065da13d5db98c4c0096c44aff515c0ec16407eae463025d6bdfbeb5e2054`  
		Last Modified: Wed, 17 Jan 2024 09:42:21 GMT  
		Size: 58.8 MB (58820381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47306096676c9d86250e0a4ea75c88147fbd2a2dd8acdccda77a13cef9d222c`  
		Last Modified: Wed, 17 Jan 2024 09:42:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
