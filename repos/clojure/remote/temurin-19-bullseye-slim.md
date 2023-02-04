## `clojure:temurin-19-bullseye-slim`

```console
$ docker pull clojure@sha256:72fcc2a71e169706433b1192ec9ff57e8e1d914bfd00c1abe2346e3bae7debcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fecba0883c16afc0555ae405f1bd281364d916aa5c9833282a9dec499be7893a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293993877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eed16247bf9390fef6bb21c317396e345e4db3b418efc7922b41b811b3ce01f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:15:02 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:16:59 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:16:59 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:17:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:17:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:17:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:17:16 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:17:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300431c7a62af0031d946dcb4bce1afaa7937b894471d1bac4795c1091262f26`  
		Last Modified: Sat, 04 Feb 2023 14:26:05 GMT  
		Size: 201.1 MB (201112956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99e0cf58969078bde80af38bfd3d8f04e256f471f0fa05503f91c7f4b05c5a7`  
		Last Modified: Sat, 04 Feb 2023 14:27:06 GMT  
		Size: 61.5 MB (61482986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e13d54ed048fd849113e8f8123c9d911b123114d2d52bc2cb06e26e222aeb6`  
		Last Modified: Sat, 04 Feb 2023 14:26:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bffc1ad04603eb3dba2d161da4439718dd74acf4068234aee68d805b3eaa`  
		Last Modified: Sat, 04 Feb 2023 14:26:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a1c7d328d551db77a38a687835590923219e0fc879f0dfc5d97b0c4b749bad68
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291498177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778c2db48125f85fee98a614220543980bfcc793d6758c5a839b9dc77ef69fa9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:10:54 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:10:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:12:33 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:12:33 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:12:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:12:48 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:12:48 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:12:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:12:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd6a2c95889ff1bf974c1d3aa8d9648da50dd043fb5c120824cf6fb0944985e`  
		Last Modified: Sat, 04 Feb 2023 17:20:30 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e005d6810fea62a41cda2dc169d96ffedddef1442dea4b07df295d1cf3a305`  
		Last Modified: Sat, 04 Feb 2023 17:21:26 GMT  
		Size: 61.6 MB (61597169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb39627ede9c9f38bdbe6a82b439a9d227d7c08fa2abf5e78a6fb1921058d9b`  
		Last Modified: Sat, 04 Feb 2023 17:21:20 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5986d2da4ee66f0532c39dacc31d588ac9614cab4d88cfb2c37ea85eea0cba3`  
		Last Modified: Sat, 04 Feb 2023 17:21:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
