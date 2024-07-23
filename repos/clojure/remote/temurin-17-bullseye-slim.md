## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:f6c2ee0ebd600ed969417ff824bc90d4082089e3318e19530fdfd0fadc118671
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:37ac08a8b4e548ac2d32c6302be50149f66c8eb2439a20a2991c6d0f8a43e90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235214201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85930d0be61830aa5d52a7ccaf2e1b3a956736df90c8f0cb0c98edecd5916ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb2e9e578a52d2aa3b300b12a0154a4342eee3b57f3f7a4db2e0050a32b72b`  
		Last Modified: Tue, 23 Jul 2024 02:01:20 GMT  
		Size: 145.2 MB (145166532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dcea6c49e064cfe2ae9824c0a06b8ec324a4c190c19593278420832bcfef07`  
		Last Modified: Tue, 23 Jul 2024 02:01:18 GMT  
		Size: 58.6 MB (58624345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e48604fbf89ae55d6c85bf9d7be4e837b666f6a43c7280942b2c42d3dc7d7b8`  
		Last Modified: Tue, 23 Jul 2024 02:01:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b75933a87e1106ce5f22d25d9d22b96d915d282ab7571d0eef79b345857ee8`  
		Last Modified: Tue, 23 Jul 2024 02:01:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a72e5d7da7e2d5b68e90f79ce34105447072c0a1d6ece5e397d9a2ec6549f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6292a4f4b97a21f3aa80178c4c6dd6034db95a32f978e8cb2fe8ea37a92269`

```dockerfile
```

-	Layers:
	-	`sha256:0432780a8cf1ec1cc2c99d21c25777f2da65d1084205342787a2b05e3d614bac`  
		Last Modified: Tue, 23 Jul 2024 02:01:16 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a81a654af4b606d78f6fe24c30c0c32d187dffb7f4987894b92025f81e1be`  
		Last Modified: Tue, 23 Jul 2024 02:01:16 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ea6b7e7e877e583e42faa4246636e5011fae5b1174701667d5770b852160ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232707502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f50fd2617d09ea714592cf5646e3660fb44fd3d0ec3e9e6be183f5a40d5879`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343d2af50bf52fcbb3bfdbf2cbe68f34c183905bca6495e7adb48e9aadb23f0c`  
		Last Modified: Tue, 02 Jul 2024 09:30:27 GMT  
		Size: 143.9 MB (143892776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf6f0e889bd789d934d40e1f655c7d7f6fb48974672ce85937bb93155d1868`  
		Last Modified: Tue, 02 Jul 2024 09:34:36 GMT  
		Size: 58.7 MB (58744069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99108935d6073fd1db90935b5726735745bd898b22cfd9f79dc1b1eb07222db9`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436927d4d62cca035cf8ba26dd609ed12ed014da006cf70fd134e0ed994c8883`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d48e87d2375f3a96aba2d51e63cade52d4015b38e87520496b88259ddd9519b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2aaf1fd353e8ad4f12c897a6b16eb21f8eec1548d4b2225ddfcce965c45743`

```dockerfile
```

-	Layers:
	-	`sha256:df0b9b75e71bf8611f4cdb416e86e18c9a43998580fcb88b58c9af346958bc8d`  
		Last Modified: Tue, 02 Jul 2024 09:34:35 GMT  
		Size: 4.9 MB (4915628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fa21c3d08430f222653b4e0be9fca93fef52d627487f6e8a68e25dfc845d9b`  
		Last Modified: Tue, 02 Jul 2024 09:34:34 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
