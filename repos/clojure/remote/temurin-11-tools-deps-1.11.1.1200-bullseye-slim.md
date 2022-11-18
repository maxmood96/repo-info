## `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye-slim`

```console
$ docker pull clojure@sha256:b3cdde090700db6e27fae951c9263c9ce528cef830b1e4db2ea4bf5ade7084e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1efbf887c605865a22197a09f883335255a9a0002bfa55d1ad09c438b1b782d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291353638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803fa6ae3782608480bea9891c8a6d361b073865bb33f40fd3c2fcbd357bc929`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:24:07 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:24:08 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:24:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:24:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:24:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75552aa9b1dac0e78cda1a0d179b618b53990e028eba75314a120596a7b0fec6`  
		Last Modified: Fri, 18 Nov 2022 22:34:15 GMT  
		Size: 61.5 MB (61484578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655978057e5c293f82131db36b59ca3edfef17d3fee0a62f80e704a62092fa37`  
		Last Modified: Fri, 18 Nov 2022 22:34:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16810b0338313542eef9e31247ff4314e6145804e93451cb2d49dfbd3efeeedc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286866689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97b92685828e2dc502e192fcfbca88024850a9bb8b73cc21adab04dbcf74040`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:59 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:43:23 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:43:23 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:43:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:43:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:43:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cde71cdd6ac565f043bc4ec8903ab809981c13bc3c9e55dd5b7290a1bb0801`  
		Last Modified: Tue, 15 Nov 2022 06:03:30 GMT  
		Size: 195.2 MB (195201143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc65bd4c6763427247c29c7918bbb6ab6f4fad7f235340cc7a611611e17864f`  
		Last Modified: Fri, 18 Nov 2022 22:51:14 GMT  
		Size: 61.6 MB (61604325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab39eefc5d751aeb7cff32ec041759f5cd10c273095e23bb9099819fe06d348`  
		Last Modified: Fri, 18 Nov 2022 22:51:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
