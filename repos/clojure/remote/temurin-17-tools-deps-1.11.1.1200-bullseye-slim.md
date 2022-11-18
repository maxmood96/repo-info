## `clojure:temurin-17-tools-deps-1.11.1.1200-bullseye-slim`

```console
$ docker pull clojure@sha256:d1bcbfb6acb2bdd6053616e34f09a45332e07651fc4fb1f23ddeef2dd484d22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1200-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f7c5b5f0fa8e21f0f939c9e6d6af4905773deac171e8bb12d09ac315a9c9668b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285329351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145fa00d4e3dd35e9a189681e77926e427b1738f38be788bb4513c728713939`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:26:06 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:26:06 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:26:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:26:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:26:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:26:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:26:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe113d7385dc373d3cd6522aaf4d2db250c6a9e6a74413c48a60c1f06a09415`  
		Last Modified: Fri, 18 Nov 2022 22:36:04 GMT  
		Size: 61.5 MB (61484429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dda91e70b7aafb5c31c1060fa9cb19b0ac0a993d3aa8c8cc8fbb5e1a7587feb`  
		Last Modified: Fri, 18 Nov 2022 22:35:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5c18c0ba0690cda945c344450b3d3150f5a15b79e807f11cb6dca42ad1f218`  
		Last Modified: Fri, 18 Nov 2022 22:35:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1200-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4bce583958294ecdc3d401a254b8725e53034513e7e8873fdd7a2c1ce4238da2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282881056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2c73612ae4fbab693a358ce80348e6198b008a35341cd7c335fc41bd01ffe4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:33 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:44:48 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:44:48 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:45:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:45:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:45:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:45:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:45:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032fd948a5495fec37e26e9d086c7c0fa24d0623f43f8ad0471aac3350e5f61`  
		Last Modified: Tue, 15 Nov 2022 06:05:10 GMT  
		Size: 191.2 MB (191215234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f947453f397aa3ed85aed97a6ff5f35d8e8cf2120cc57ae85067d3d2272071e`  
		Last Modified: Fri, 18 Nov 2022 22:52:35 GMT  
		Size: 61.6 MB (61604199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306079e0840d5d69445b37ee474eadbad731c3b1c968f533bc110460f4315ce7`  
		Last Modified: Fri, 18 Nov 2022 22:52:28 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546c2e6d52e15b376f8f23acdaceb554d01b0a7b2e8ecbdaebc269674f09367f`  
		Last Modified: Fri, 18 Nov 2022 22:52:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
