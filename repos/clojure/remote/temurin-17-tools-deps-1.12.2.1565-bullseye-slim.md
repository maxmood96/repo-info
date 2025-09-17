## `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:f44217e97fcc82ec854ad1cf15e1b75c406e23c8805d2c7165a5058127dfbb36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70828062643b8ea43a567647b08594a967d0bd3b14566733b9fd2d1fb3ed813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234101520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8892cc20b62b5cab8cf368ff28706fa562e08a87c6524582360ecdf2ff7296`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ae41f8a4ea2f7c7894dedb0b712bbfa2af55273b96e85ac9418271f56a138`  
		Last Modified: Wed, 17 Sep 2025 13:03:07 GMT  
		Size: 144.7 MB (144693570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f06a8097ca4fcca45737b8c8b2bcbf4dfa330bf2c25833f61eefb68fe02633`  
		Last Modified: Mon, 15 Sep 2025 23:27:03 GMT  
		Size: 59.2 MB (59150843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09a3fd21a305e84b383ee9f8d065d728e794ba948d1a9be074f3813fc4efa3`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d85805ff4a6d56f717f7cdb8d961d8f6f95e255b1e5f36ae408845927ab80`  
		Last Modified: Mon, 15 Sep 2025 23:26:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:277d8dbc0305995e679ae139f5e88fada6dcbd7a65836cd3fd0182c9850a1061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eb996eec214fdcbd714c89b0ce43643e2269cda64507e805b92d8df5bec7f8`

```dockerfile
```

-	Layers:
	-	`sha256:2037c5bd1e22e8742ba614b65572d7f4bdc00f9eb44d3915e31243fbfa066800`  
		Last Modified: Tue, 16 Sep 2025 00:38:58 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a0310a4c58777a3bad7a0e05d0e48fa58f81539f8479a000e3a1d05d3805fd0`  
		Last Modified: Tue, 16 Sep 2025 00:38:59 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6332dc0711bb5e0601be196e1f6a9be8983144f4e45faa7450f84ecd146caa0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88d9619e1af417bd1f1569bbd91e7f06e6e7da6e3f8035de6a625ce967e8cf8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89708372ba05c03374d5c7e3269b8f9d5faa23749a8d1f29117f68473155706a`  
		Last Modified: Mon, 15 Sep 2025 23:26:55 GMT  
		Size: 143.5 MB (143542121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ec3dbd9b3ebab5260644103cc92922765cd9ea28f36142469f8c210b5b5415`  
		Last Modified: Mon, 15 Sep 2025 23:27:13 GMT  
		Size: 59.3 MB (59282754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798185b8b9287da6df80095c21223cbcf54eb4ee5f347d1e79cda6ad95f49a2`  
		Last Modified: Mon, 15 Sep 2025 23:27:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172cb97dd485115d50f29c40b48b6584eace17a1441730477f1b6a7bd009c26`  
		Last Modified: Mon, 15 Sep 2025 23:27:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d1df24059517ca64d42e603ce6c8144a7f80e273861b7a273d4a74e99d03a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d817ae2fb77e84df06e0c8400b987722054374975a05c1e12cefd7241dadb99`

```dockerfile
```

-	Layers:
	-	`sha256:dd57ce4d75462c782e5e96c272ddb92a844c9803fc38a37ae4f6ffeb027618ec`  
		Last Modified: Tue, 16 Sep 2025 00:39:04 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ae8a4ef64183389ba687a17b5eb6599741e4c66ec5a1a2469762d0d19c3195`  
		Last Modified: Tue, 16 Sep 2025 00:39:05 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
