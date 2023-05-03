## `clojure:temurin-20-bullseye-slim`

```console
$ docker pull clojure@sha256:774c57dced12b749755d6103cc99ff6214a216e313b194abc35321b94c1827cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a89dc9d8d557dfb90ced76c99f9ca6290a7fbb44c442ed3d46da8153c49b9f89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295713950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640c07c9c6a3d246cbcc231a1daa08d9f299d91c4f45f6d3f59957a08c68bc4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:32:51 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Wed, 03 May 2023 20:32:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:33:36 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:33:36 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:33:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:33:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:33:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:33:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02720e2873c980e5fcc584b01ace091e5d4d05cd22a426e5b195f3d93f338875`  
		Last Modified: Wed, 03 May 2023 20:40:25 GMT  
		Size: 202.8 MB (202813964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23619be5edae573d52cfa9463b5bccc5b0bde1851eeb9bbc63a3e56205277034`  
		Last Modified: Wed, 03 May 2023 20:40:59 GMT  
		Size: 61.5 MB (61495460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b0e5d340c11722d3dd730e6f978fefae83839f6f6e62da85bc99615c255141`  
		Last Modified: Wed, 03 May 2023 20:40:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5627626a5475ef71e750ced0d55d3ba49dd8115885babc42395f99da563e33`  
		Last Modified: Wed, 03 May 2023 20:40:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38eabcc172fa42c424e6d080adf3eeed37f680429cb7556f69ef89e5a2d0d49c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292822504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce92585ffcab4081acd10f6fbfb62a060846fd180bd787671638b4cb1e8eb6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:51:22 GMT
COPY dir:f555428af67a610819205eec573e23f479077e0999818ee9dc0f3375599d21db in /opt/java/openjdk 
# Wed, 03 May 2023 17:51:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:52:09 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:52:09 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:52:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:52:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:52:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:52:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:52:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428345b4e9aa28cfa10998d30caebabc2e8cc0a23cb3c5e1642b394643a3de24`  
		Last Modified: Wed, 03 May 2023 17:58:23 GMT  
		Size: 201.2 MB (201158010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417c7a64ae3e1de9f512338f755f60948915fababd0fd2dbb6b6490f9f3279c6`  
		Last Modified: Wed, 03 May 2023 17:58:54 GMT  
		Size: 61.6 MB (61610748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622f515e353c736e9c6513f1974fecbc5d39579bbd4304128dfca1aa31f13847`  
		Last Modified: Wed, 03 May 2023 17:58:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579adddc825965271dc1a4dfefdfae60530387086570c732b7dbc7c58e25b025`  
		Last Modified: Wed, 03 May 2023 17:58:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
