## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:f8159f2759fb3190f36d8330832e647859ec819c282b65acc3c4bb897259f1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1e49ea3a53ef9766f0db4be63ab7352bcca267203032c3857a6015f256ab2a29
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235156954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c3f486b50e7df33fa228a4393f8e60decc6aced93e9d8fca0f74b9e5b9a4be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:34:10 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Tue, 28 May 2024 21:34:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:36:46 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:36:46 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:37:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:37:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:37:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:37:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:37:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870202c9f855ca0e8591b8dd4d90c960431283be1dc917941d8553db3e2d62a8`  
		Last Modified: Tue, 28 May 2024 21:57:47 GMT  
		Size: 145.1 MB (145095164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf3a68a70a872ea783786bcf00676cf9434016f7ca3ecab64c72250aa15868f`  
		Last Modified: Tue, 28 May 2024 21:59:33 GMT  
		Size: 58.6 MB (58626848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e98cba14b37e34795a60d65b44786ac730fe5100ee0ebb4c1bc20d3c3f5b8c`  
		Last Modified: Tue, 28 May 2024 21:59:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46475f5b945a110e1e80ab797ee113f80caa1dd805ba5c74891a067426124431`  
		Last Modified: Tue, 28 May 2024 21:59:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:094035d96fbdfdae0e877fdf7f104289e4422819b5ea36c5be2e4e7c5edd864a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232728118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517076eb983f9ee5f6dfe084fe7ca145ec7de1f98a8220d3564edf9270e07b05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:55:44 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:57:45 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:57:45 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:57:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:57:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:57:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:57:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:57:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf072d6312eeb8d6d05dc50f44eccfa94ca9ae5a08d2b299b845776b87f175a`  
		Last Modified: Tue, 28 May 2024 20:15:28 GMT  
		Size: 143.9 MB (143891870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b948b2b1d5095883ac552af06b8b9b937e1fe64cb5fa4b24477e72320e81c8d8`  
		Last Modified: Tue, 28 May 2024 20:17:11 GMT  
		Size: 58.7 MB (58748326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806f85dd8f866b9df6f6cfd16310786f803f36b46d2e19bc28ad480d4d85a8af`  
		Last Modified: Tue, 28 May 2024 20:17:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be62f08a3ce83443a8f8dc7b92d88231436cb316a8361b3b7d0b399ad04bd7`  
		Last Modified: Tue, 28 May 2024 20:17:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
