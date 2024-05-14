## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:fc9938dbc6a36ce3d971c4d11ac71c1fb79e731fa668176af67530577b9f954f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:47123dc30f8898d596cdcfa9af1961499cc7f3653e8ca87362c314b239280710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275159848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bbcc5377515759aafcd54b5f73f3b8cea5bdfafc6b818192ef78c375c3281e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:23:13 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Tue, 14 May 2024 02:23:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:25:00 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:25:00 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:25:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:25:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:25:19 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:25:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:25:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba6f7a9e0d7b88608b83c5a6cd461db6a06577d95def4542445eefe821666cc`  
		Last Modified: Tue, 14 May 2024 02:40:50 GMT  
		Size: 145.1 MB (145095140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07dacbcd22a2b3c6ed7d52d59cfc46318d8f2096286cd0c0ef224fc859786f`  
		Last Modified: Tue, 14 May 2024 02:42:18 GMT  
		Size: 80.5 MB (80487301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747dc3cebc49dbccaaec368121e7016b237493b5cff0cd45afa4f16c5d63e697`  
		Last Modified: Tue, 14 May 2024 02:42:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4cca465e934728973fb44e862733cfd152e19c38110b867ee18e53b8f4b669`  
		Last Modified: Tue, 14 May 2024 02:42:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7787668c0f7b1f7ad6c2cf730185aba94d67da45d95346941e6b92a0f1bc95e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273752177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d46e40fa3f3372f1e3ab574f10d194ad2051e9c94473f7ab50aab3337800ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:57:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:04:45 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 14 May 2024 02:04:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:06:25 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:06:25 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:06:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:06:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:06:41 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:06:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:06:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efbb4aebd137be44c8766675abdc90b41807fc2e8621959dbc851c0e3a95dd9`  
		Last Modified: Tue, 14 May 2024 02:20:01 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a682c8ed94ce62dddb7cc0a9b193ccd6aecf959d206dfecb6671da7acedf63`  
		Last Modified: Tue, 14 May 2024 02:21:17 GMT  
		Size: 80.2 MB (80245938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2a26e17b0b9ed67d6d0b85710770b0d7a91e27abdeef46031bf36bafb4363b`  
		Last Modified: Tue, 14 May 2024 02:21:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b783bb13c0ad0527edebb680aafdaff1412bc4abfdf8a01caf8f48d73a591e2c`  
		Last Modified: Tue, 14 May 2024 02:21:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
