## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:6e96663ab3b88fd465073a47f3dd713cae03c08815ced2a5d8f624ba7c63837c
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
$ docker pull clojure@sha256:d118bece6826b4b8b383339f4f4ef8298f11b9a88edc1c0205eff0f88b9b4197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194001186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6fc14d0d4648890ba442a43e14220fbcb53408b20d674dfb36259b32b31f0f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:52 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:54:54 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:54:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:54:54 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:54:59 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:54:59 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:55:16 GMT
RUN boot
# Tue, 19 Dec 2023 06:55:17 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1a5fc697b6e1327948a1ba0fb49b56508bfc165490af939f46435eec9d53d`  
		Last Modified: Tue, 19 Dec 2023 07:13:00 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdd9593457fc95a041802dcc8be3b19424f38628c6186efc5d1f5b14eec1d73`  
		Last Modified: Tue, 19 Dec 2023 07:12:54 GMT  
		Size: 3.3 MB (3321945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dc8d76219237c5b197a75b1182f9f0355fd6f3c9d6617a6e170118b65adf40`  
		Last Modified: Tue, 19 Dec 2023 07:12:56 GMT  
		Size: 58.8 MB (58820434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
