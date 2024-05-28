## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e2194048f72b3bc92cbb1c443676b1d978847ac1bb583563af9503c1b6502dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97cafcad2116e7c880fde28396ca58a0d8d0b10263499b4492d10b297fc8a9f3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273753351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f28b56d21dc7e5fe8120f46f4d284c26ca6f0b8afd82361953af7ce95a440ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:54:30 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:54:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:56:47 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:56:48 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:57:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:57:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:57:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:57:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:57:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0a7ab35eca8753def28d2c15916fa2d25792099a1b4427f44564e27bdb212`  
		Last Modified: Tue, 28 May 2024 20:14:35 GMT  
		Size: 143.9 MB (143891866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9683128fd02f5d32ab27d33dccd705277456de89e559b6804f8b02f6f89e555`  
		Last Modified: Tue, 28 May 2024 20:16:18 GMT  
		Size: 80.2 MB (80247080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5656f37827640522ac90636fd1019147b2d1b6273a1f85a70267d1db7f4c7e74`  
		Last Modified: Tue, 28 May 2024 20:16:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5125e907ddffb967cc07fe181d5373334de0f16a43c28d38dfd4c5e73262fb5`  
		Last Modified: Tue, 28 May 2024 20:16:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
