## `clojure:temurin-20-tools-deps-1.11.1.1347-bullseye`

```console
$ docker pull clojure@sha256:358f32987e7410937c91323410f0d3c68423f4612ad2cabee8ef57daa7db76bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-1.11.1.1347-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6888772ad938db8ffbe1e85fd2199a9f8197200604afcad36c148475db3beb77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280730489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390920c2d575f1edc98160641bb3d49a7952e55cdfb9defc29726be37a8eec4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 00:35:48 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Tue, 25 Jul 2023 00:35:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 00:39:20 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 25 Jul 2023 00:39:20 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 00:39:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Jul 2023 00:39:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Jul 2023 00:39:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 00:39:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 00:39:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa78c342db56746dd84f2fd6f98dfdcc0e5dfbdae249b1e1ac19359012fa2653`  
		Last Modified: Tue, 25 Jul 2023 00:43:00 GMT  
		Size: 153.8 MB (153791697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0ad942a4d4d765c55d9b1051bd9b6e226854edf066ba2af578ac6cb4e488d`  
		Last Modified: Tue, 25 Jul 2023 00:44:02 GMT  
		Size: 71.9 MB (71882476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d62d721f4a96b6a9f6a88ba8de53fd70be1c43fa9810f9eeeccac93d5fc622`  
		Last Modified: Tue, 25 Jul 2023 00:43:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06fb479615f4baf49d32784b02cf19bc5f2949a169393d8d09a72d469ca60`  
		Last Modified: Tue, 25 Jul 2023 00:43:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-1.11.1.1347-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76f1a99ab4669fdafbb1c8eba6dec39ef8d01b732e93a57c71a100ad7c0481c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277826322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dd5737687ce9e8d9c2fdb8554b4a8da871f1783cee5335e26dfa586c3e5242`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 00:45:26 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Tue, 25 Jul 2023 00:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 00:46:49 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 25 Jul 2023 00:46:49 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 00:47:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Jul 2023 00:47:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Jul 2023 00:47:06 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 00:47:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 00:47:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1177b7fdf5d2c9a1102d1fdec93f218e522f33ccea84bf9d6de3d6146895e033`  
		Last Modified: Tue, 25 Jul 2023 00:49:49 GMT  
		Size: 152.1 MB (152120121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23114d31257fc7986ade3e7eafd65f44d35444313d1805dfb4f87c9a69118100`  
		Last Modified: Tue, 25 Jul 2023 00:50:36 GMT  
		Size: 72.0 MB (72001206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb48db6af6342b0572971ae718b2f877c4355b0d2660ea3c4c49027f1a91e3dd`  
		Last Modified: Tue, 25 Jul 2023 00:50:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb29e0819f487374c31d53728a35a671b057e790e57381ba9919475260e431`  
		Last Modified: Tue, 25 Jul 2023 00:50:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
