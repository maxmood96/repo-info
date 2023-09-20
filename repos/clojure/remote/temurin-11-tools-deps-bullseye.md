## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:4d4d8526cec47d9ad183e99cfb4abbf37fe5f5e6acb91e9260fac544a9113b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d3b8b95699311d8de0b7913aa0f5767b972e2889d36002dfc4b688fa981958eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271761131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d47504c1a3d529bea73d1e7ed54be51132886c8f939040ff8a717ac0cec26`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:24:52 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:26:53 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:26:53 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:27:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:27:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:27:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d2593b379fff1802970ddf266f34d6bd5d13fda962a549ac1b0e11020096b1`  
		Last Modified: Wed, 20 Sep 2023 07:35:34 GMT  
		Size: 144.8 MB (144826046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f4e734153c0e58bb7e5d64b716cd1dc7bed7739a944879bb8bb3f3d45fd8a1`  
		Last Modified: Wed, 20 Sep 2023 07:36:35 GMT  
		Size: 71.9 MB (71877756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea72c21a1bb5b4e7478ae772290d4714039bb42b143497a6d5774de339ce0e4`  
		Last Modified: Wed, 20 Sep 2023 07:36:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d1c17c4aed7d02c5af7577de359984b3ccf8463b83ef29e780482c301e338cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267272697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f89233db6cdea26347445b48fa261c959277bebde0faba5212ff6343f7a8a72`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:06:37 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:08:30 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:08:30 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:08:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:08:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:08:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0526516c15ab59c896bde61f8cbcc3d733f5b792e340106528fab44ad40477`  
		Last Modified: Thu, 07 Sep 2023 09:16:03 GMT  
		Size: 141.6 MB (141570385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de02fe321f4ccc4e4ff42b3fb8cd201c94a6f98ddb463d3250d555dbbb445a01`  
		Last Modified: Thu, 07 Sep 2023 09:16:54 GMT  
		Size: 72.0 MB (71996981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42941be49ed7563eb59dd787cd87798c1f48c8365dbd34178c47b421e1b18155`  
		Last Modified: Thu, 07 Sep 2023 09:16:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
