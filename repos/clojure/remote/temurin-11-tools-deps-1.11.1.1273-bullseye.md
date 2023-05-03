## `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye`

```console
$ docker pull clojure@sha256:b90e3d5273c4f53b32ecd7030f5d6e7a6803aa3a2fced96461ca54d179b22b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e4e1b1f31c85dacc3bd5a13c514e54cb3317428bb646041c6e02a396eddfe806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325479325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7275718c9a7d1f644617c0df184c724e8e968ad2b854c030e27715f4b452c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:26:50 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 03 May 2023 20:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:28:48 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:28:48 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:29:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:29:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:29:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127538ce586198e269e9a4ff9f0268aed32fd316a7287fcdb85700312b200f6e`  
		Last Modified: Wed, 03 May 2023 20:36:35 GMT  
		Size: 198.5 MB (198549535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde4265af1c9ef6a51cd739653e0b5cd4b90da3817cebafcee4afd60a2f104e`  
		Last Modified: Wed, 03 May 2023 20:37:33 GMT  
		Size: 71.9 MB (71880106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbde4bd405e33106857ec299076983ebf93148ea6bc4370de80ba9279574e89`  
		Last Modified: Wed, 03 May 2023 20:37:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c87900e2fbae4571d4cf631fd160e7b7f74313fad1c2048acd6fda753946be8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321014288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7931f1775829ade53fcc30d4a914628a3913bf0bb8bf27954de8d240972a0e74`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:46:17 GMT
COPY dir:8d5d0106b2c3fe64c4905be44080473b7828ffb48e0e107739a7ba7a3cb627cf in /opt/java/openjdk 
# Wed, 03 May 2023 17:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:47:58 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:47:58 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:48:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:48:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:48:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4d5e76f4319fe5a3ea2caf1641913a58d75b0a1015af977eb92876edf0d64e`  
		Last Modified: Wed, 03 May 2023 17:54:48 GMT  
		Size: 195.3 MB (195324181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dcab43b0e50e50c13c4231a858e0b1d9d304a09f6a31c5eb59a3356ecb3c0c`  
		Last Modified: Wed, 03 May 2023 17:55:43 GMT  
		Size: 72.0 MB (71996787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3188fa36d9f6f49f5c047366d2b4db2d6a0027813134d971bc47f7c12eba1866`  
		Last Modified: Wed, 03 May 2023 17:55:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
